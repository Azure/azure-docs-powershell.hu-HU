---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 107441c07e958099d330859a5003a2dafcd64bf9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844473"
---
# New-AzVM

## Áttekintés
Virtuális gépet hoz létre.

## SZINTAXISA

### SimpleParameterSet (alapértelmezett)
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DefaultParameterSet
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DiskFileParameterSet
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzVM** parancsmag létrehoz egy virtuális gépet az Azure-ban.
Ez a parancsmag a virtuális gép objektumát bemenetként veszi át.
A New-AzVMConfig parancsmag segítségével hozzon létre egy virtuálisgép-objektumot.
Más parancsmagok segítségével konfigurálhatja a virtuális gépet, például set-AzVMOperatingSystem, set-AzVMSourceImage, add-AzVMNetworkInterface és set-AzVMOSDisk.

A `SimpleParameterSet` VM létrehozásának kényelmes módja, ha a virtuális VM-létrehozási argumentumokat nem kötelező megadni.

## Példák

### Példa 1: virtuális gép létrehozása
```
PS C:\> New-AzVM -Name MyVm
```

Ebben a példában a parancsfájl bemutatja, hogy miként hozhat létre virtuális gépet.
Ez a parancsfájl számos más parancsmagot használ.

### 2. példa: virtuális gép létrehozása egyéni felhasználói képből
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force 
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account. 
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance. 
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3" 
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword); 

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

Ez a példa egy meglévő sys-prepped, általános egyéni operációs rendszer lemezképet hoz létre, és egy adatlemezt csatol hozzá, kiépít egy új hálózatot, telepíti a virtuális merevlemezt, és futtatja azt.

Ez a parancsfájl automatikusan használható a kikészítéshez, mert a helyi virtuális gép rendszergazdai hitelesítő adatait használja a felhasználói interakciót igénylő " **Get-hitelesítőadat** " helyett.

Ez a parancsfájl feltételezi, hogy már bejelentkezett az Azure-fiókjába.
Bejelentkezési állapotát a **Get-AzureSubscription** parancsmag használatával ellenőrizheti.

## PARAMÉTEREK

### -AddressPrefix
A virtuális hálózathoz tartozó cím előtagja, amelyet a VM rendszerhez hoz létre.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllocationMethod
A VM rendszerhez létrehozott nyilvános IP-cím IP-kiosztási módja.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailabilitySetName
Az elérhetőségi halmaz nevét adja meg.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hitelesítő adatok
A VM rendszergazdai hitelesítő adatai.

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableBginfoExtension
Jelzi, hogy ez a parancsmag nem telepíti a **BG információs** bővítményt a virtuális gépre.

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskFile
A virtuális merevlemez-fájl helyi elérési útja, amelyet fel kell tölteni a felhőbe, és létre kell hoznia a VM-et, és az utótagnak ". vhd"-nek kell lennie.

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNameLabel
A VM teljes tartománynevét (FQDN) tartalmazó aldomain címkéje.  Ez az űrlapon fog szerepelni `{domainNameLabel}.{location}.cloudapp.azure.com` .

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
Az a felhasználóbarát kép neve, amelyen a VM épül.  Ezek a következők: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-LEAP, RHEL, SLES.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
A licenc típusát adja meg, amely azt jelzi, hogy a virtuális gép képe vagy lemeze engedélyezett a helyszíni verzióban.
Ezt az értéket csak a Windows Server operációs rendszert tartalmazó képek esetén használja a rendszer.
A paraméter elfogadható értékei a következők:

- Windows_Client 
- Windows_Server

Ez az érték nem módosítható.
Ha ezt a paramétert a frissítéshez adja meg, az értéknek meg kell egyeznie a virtuális gép kezdeti értékével.

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Azt jelzi, hogy a lemezmeghajtó a Linux VM-re van-e megadva, ha meg van adva; vagy Windows, ha alapértelmezés szerint nincs megadva.

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A virtuális gép helyét adja meg.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A VM-erőforrás neve.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OpenPorts
A létrehozott VM-es hálózati biztonsági csoport (NSG) azon portjainak listája, amelyeket meg szeretne nyitni.  Az alapértelmezett érték a választott kép típusától függ (azaz Windows: 3389, 5985 és Linux: 22).

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
A létrehozott VM új (vagy meglévő) nyilvános IP-címének neve.  Ha nem adja meg, akkor létrejön egy név.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityGroupName
A létrehozott VM új (vagy meglévő) hálózati biztonsági csoportja (NSG) neve.  Ha nem adja meg, akkor létrejön egy név.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Méret
A virtuális gép mérete.  Az alapértelmezett érték a következő: Standard_DS1_v2.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
Annak az alhálózatnak a cím előtagja, amelyet a VM-hez fog létrehozni.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
A létrehozott VM új (vagy meglévő) alhálózatának neve.  Ha nem adja meg, akkor létrejön egy név.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Címke
Itt adhatja meg, hogy az erőforrások és az erőforráscsoportok a name-Value pairek halmazával legyenek címkézve.
Ha címkéket ad az erőforrásokhoz, az erőforrásokat csoportosíthatja az erőforráscsoportok között, és saját nézeteket hozhat létre.
Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkét tartalmazhat.

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkName
A létrehozott VM új (vagy meglévő) virtuális hálózatának neve.  Ha nem adja meg, akkor létrejön egy név.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
A létrehozandó helyi virtuális gépet adja meg.
A virtuálisgép-objektum beolvasásához használja az New-AzVMConfig parancsmagot.
Más parancsmagok segítségével konfigurálhatja a virtuális gépet, például set-AzVMOperatingSystem, set-AzVMSourceImage és add-AzVMNetworkInterface.

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Zone (zóna)
A virtuális gép zóna listáját adja meg.

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.

A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSVirtualMachine
A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Remove-AzVM](./Remove-AzVM.md)

[Újraindítás – AzVM](./Restart-AzVM.md)

[Start-AzVM](./Start-AzVM.md)

[Stop-AzVM](./Stop-AzVM.md)

[Update-AzVM](./Update-AzVM.md)

[Add-AzVMDataDisk](./Add-AzVMDataDisk.md)

[Add-AzVMNetworkInterface](./Add-AzVMNetworkInterface.md)

[Új – AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[Set-AzVMSourceImage](./Set-AzVMSourceImage.md)

[Set-AzVMOSDisk](./Set-AzVMOSDisk.md)


