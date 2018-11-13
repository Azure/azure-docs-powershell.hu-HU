---
title: Az Azure PowerShell használatának első lépései | Microsoft Docs
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 7eb5e3fad31b5a92be1cfb36aefdaa7b920bae5f
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/08/2018
ms.locfileid: "51273973"
---
# <a name="getting-started-with-azure-powershell"></a>Ismerkedés az Azure PowerShell-lel

Az Azure PowerShell az Azure-erőforrások parancssori kezelésére és adminisztrálására, valamint az Azure Resource Manageren futtatható automatizálási szkriptek létrehozására készült. Használhatja a böngészőjében az [Azure Cloud Shell-lel](/azure/cloud-shell/overview), vagy telepítheti a helyi gépen, és használhatja bármely PowerShell-munkamenetben. A cikk segítséget nyújt a használatának megkezdésében, és ismerteti az alapvető fogalmakat.

## <a name="connect"></a>Kapcsolódás

Első lépésként a legegyszerűbb módszer, ha [elindítja a Cloud Shellt](/azure/cloud-shell/quickstart).

1. Indítsa el a Cloud Shellt az Azure Portal felső navigációs szakaszából.

   ![Shell ikon](~/media/get-started-azureps/shell-icon.png)

2. Válassza ki a használni kívánt előfizetést, és hozzon létre egy tárfiókot.

   ![Tárfiók létrehozása](~/media/get-started-azureps/storage-prompt.png)

A tároló létrehozása után a Cloud Shell megnyit egy PowerShell-munkamenetet a böngészőben.

![Cloud Shell a PowerShellhez](~/media/get-started-azureps/cloud-powershell.png)

Telepítheti az Azure PowerShellt, és helyileg is használhatja PowerShell-munkamenetben.

## <a name="install-azure-powershell"></a>Az Azure PowerShell telepítése

Első lépésként győződjön meg róla, hogy az Azure PowerShell legújabb verziója van telepítve. A legújabb kiadással kapcsolatos információkért lásd a [kibocsátási megjegyzéseket](./release-notes-azureps.md).

1. [Telepítse az Azure PowerShellt](install-azurerm-ps.md).

2. A telepítés sikerességének ellenőrzéséhez futtassa a `Get-Module AzureRM -ListAvailable` parancsot a parancssorról.

## <a name="sign-in-to-azure"></a>Bejelentkezés az Azure-ba

Interaktív bejelentkezés:

1. Gépelje be: `Login-AzureRmAccount`. Egy párbeszédpanel jelenik meg, amelyen meg kell adnia Azure-beli hitelesítő adatait. Az -EnvironmentName kapcsoló lehetővé teszi az Azure China vagy az Azure Germany szolgáltatással való hitelesítést.

   például: Login-AzureRmAccount -EnvironmentName AzureChinaCloud

2. Írja be a fiókjához tartozó e-mail-címet és jelszót. Az Azure hitelesíti és menti a hitelesítő adatokat, majd bezárja az ablakot.

Miután bejelentkezett egy Azure-fiókba, az Azure PowerShell parancsmagjaival elérheti és kezelheti az előfizetésben lévő erőforrásokat.

## <a name="create-a-resource-group"></a>Hozzon létre egy erőforráscsoportot

Most, hogy mindent beállítottunk, hozzunk létre erőforrásokat az Azure-ban az Azure PowerShell használatával.

Először is hozzon létre egy erőforráscsoportot. Az Azure erőforráscsoportjaiban együtt kezelhet több olyan erőforrást, amelyeket logikailag egy csoportba kíván foglalni. Például létrehozhat egy erőforráscsoportot egy alkalmazáshoz vagy projekthez, majd hozzáadhat egy virtuális gépet, egy adatbázist és egy CDN-szolgáltatást.

Hozzunk létre egy erőforráscsoportot „MyResourceGroup” néven az Azure westeurope (Nyugat--Európa) régiójában. Ehhez írja be a következő parancsot:

```powershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a>Windows rendszerű virtuális gép létrehozása

Most, hogy létrehoztuk az erőforráscsoportot, hozzunk létre benne egy windowsos virtuális gépet. Az új virtuális gép létrehozásához előbb létre kell hoznunk a többi szükséges erőforrást, és egy konfigurációt kell hozzájuk rendelnünk. Ezután ezzel a konfigurációval létrehozhatjuk a virtuális gépet.

### <a name="create-the-required-network-resources"></a>A szükséges hálózati erőforrások létrehozása

Először létre kell hoznunk egy alhálózati konfigurációt a virtuális hálózat létrehozásához. Létrehozunk egy nyilvános IP-címet is, hogy csatlakozhassunk a virtuális géphez. Létrehozunk egy hálózati biztonsági csoportot, hogy biztonságossá tehessük a nyilvános cím elérését. Végül létrehozzuk a virtuális NIC-t az összes előbbi erőforrás használatával.

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>A virtuális gép létrehozása

Először is szükségünk lesz az operációs rendszerhez tartozó hitelesítő adatok egy készletére.

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

Most, hogy rendelkezünk a szükséges erőforrásokkal, létrehozhatjuk a virtuális gépet. Ehhez a lépéshez létrehozunk egy VM-konfigurációs objektumot, majd ezzel a konfigurációval létrehozzuk a virtuális gépet.

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

A `New-AzureRmVM` parancs kimeneti eredményei akkor érhetők el, amikor a virtuális gép létrejött és használatra kész.

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

Most jelentkezzen be az újonnan létrehozott, Windows Server-alapú virtuális gépre a Távoli asztal szolgáltatással és a virtuális gép nyilvános IP-címével. A következő parancs az előző szkriptben létrehozott nyilvános IP-címet jeleníti meg.

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

Windows-alapú rendszer használata esetén ezt a parancssorból az mstsc parancs használatával teheti meg:

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

A bejelentkezéshez ugyanazt a felhasználónév–jelszó kombinációt adja meg, amelyet a virtuális gép létrehozása során használt.

## <a name="create-a-linux-virtual-machine"></a>Linux rendszerű virtuális gép létrehozása

Az új linuxos virtuális gép létrehozásához előbb létre kell hoznunk a többi szükséges erőforrást, és egy konfigurációt kell hozzájuk rendelnünk. Ezután ezzel a konfigurációval létrehozhatjuk a virtuális gépet. Mindez feltételezi, hogy már létrehozta az erőforráscsoportot az előzőekben ismertetettek szerint. Emellett szüksége lesz egy `id_rsa.pub` nevű nyilvános SSH-kulcsra a felhasználói profilja .ssh könyvtárában.

### <a name="create-the-required-network-resources"></a>A szükséges hálózati erőforrások létrehozása

Először létre kell hoznunk egy alhálózati konfigurációt a virtuális hálózat létrehozásához. Létrehozunk egy nyilvános IP-címet is, hogy csatlakozhassunk a virtuális géphez. Létrehozunk egy hálózati biztonsági csoportot, hogy biztonságossá tehessük a nyilvános cím elérését. Végül létrehozzuk a virtuális NIC-t az összes előbbi erőforrás használatával.

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>A virtuális gép létrehozása

Most, hogy rendelkezünk a szükséges erőforrásokkal, létrehozhatjuk a virtuális gépet. Ehhez a lépéshez létrehozunk egy VM-konfigurációs objektumot, majd ezzel a konfigurációval létrehozzuk a virtuális gépet.

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Most, hogy a virtuális gép létrejött, bejelentkezhet az új Linux rendszerű virtuális gépre SSH használatával a létrehozott virtuális gép nyilvános IP-címével:

```bash
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a>Egyéb erőforrások létrehozása az Azure-ban

Bemutattuk, hogyan hozhat létre erőforráscsoportot, valamint Linux és Windows Server rendszerű virtuális gépet. Számos más típusú Azure-erőforrást is létrehozhat.

Például a következő parancs használatával létrehozhat egy Azure-beli hálózati terheléselosztót, amelyet aztán társíthat az újonnan létrehozott virtuális gépekkel:

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Vagy létrehozhat egy új privát virtuális hálózatot (vagy az Azure-ban gyakran használt nevén „VNetet”) az infrastruktúránkhoz a következő paranccsal:

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Az Azure és az Azure PowerShell attól igazán sokoldalúak, hogy nemcsak a felhőalapú infrastruktúrához használhatók, hanem felügyelt platformszolgáltatások kialakításához is. A felügyelt platformszolgáltatásokat az infrastruktúrával kombinálva még nagyobb teljesítményű megoldások építhetők ki.

Például az Azure PowerShell használatával létrehozhat egy Azure AppService-t. Az Azure AppService egy felügyelt platformszolgáltatás, amely nagyszerű megoldás a webappok üzemeltetésére anélkül, hogy aggódnia kellene az infrastruktúra miatt. Az Azure AppService létrehozása után két új Azure webappot hozhat létre az AppService-ben a következő parancsokkal:

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Üzembe helyezett erőforrások listázása

A `Get-AzureRmResource` parancsmag használatával listázhatja az Azure-ban futó erőforrásokat. Az alábbi példa az új erőforráscsoportban létrehozott erőforrásokat mutatja be.

```powershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a>Erőforrások törlése

Az Azure-fiók tisztítása érdekében érdemes lehet törölnie a példában létrehozott erőforrásokat. A `Remove-AzureRm*` parancsmagokkal törölheti a már nem szükséges erőforrásokat. A létrehozott Windows rendszerű virtuális gép eltávolításához futtassa az alábbi parancsot:

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

A rendszer rákérdez az erőforrás törlésének jóváhagyására.

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Egyszerre több erőforrást is törölhet. A következő parancs például törli a teljes „MyResourceGroup” erőforráscsoportot, amelyet ebben a bevezető oktatóanyagban az összes mintához használtunk. Törli az erőforráscsoportot, és minden benne lévő erőforrást is.

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Ez több percig is eltarthat.

## <a name="get-samples"></a>Minták letöltése

Az Azure PowerShell használatával kapcsolatos további tudnivalókért tekintse át a [Linux rendszerű virtuális gépek](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), a [Windows rendszerű virtuális gépek](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), a [Web Apps-alkalmazások](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) és az [SQL Database-adatbázisok](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) leggyakoribb szkriptjeit.

## <a name="next-steps"></a>További lépések

* [Bejelentkezés az Azure PowerShell-lel](authenticate-azureps.md)
* [Azure-előfizetések kezelése az Azure PowerShell-lel](manage-subscriptions-azureps.md)
* [Szolgáltatásnevek létrehozása az Azure PowerShell használatával](create-azure-service-principal-azureps.md)
* A régi kiadásokról való áttéréssel kapcsolatban olvassa át a kibocsátási megjegyzéseket: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Segítség kérése a közösségtől:
  * [Azure-fórum az MSDN-en](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
