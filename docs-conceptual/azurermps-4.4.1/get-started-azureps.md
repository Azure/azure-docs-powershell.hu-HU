---
title: Az Azure PowerShell használatának első lépései | Microsoft Docs
description: 'További információ: az Azure PowerShell első lépései'
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 78f8217bf9fefba37dc1f9d11d9331ac3a7170d9
ms.sourcegitcommit: 3715500acad08bcc482b0465edddaafb7b95cb9e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/19/2021
ms.locfileid: "98566069"
---
# <a name="getting-started-with-azure-powershell"></a><span data-ttu-id="7ea58-103">Ismerkedés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="7ea58-103">Getting started with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="7ea58-104">Az Azure PowerShell az Azure-erőforrások parancssori kezelésére és adminisztrálására, valamint az Azure Resource Manageren futtatható automatizálási szkriptek létrehozására készült.</span><span class="sxs-lookup"><span data-stu-id="7ea58-104">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="7ea58-105">Használhatja a böngészőjében az [Azure Cloud Shell-lel](/azure/cloud-shell/overview), vagy telepítheti a helyi gépen, és használhatja bármely PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="7ea58-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span> <span data-ttu-id="7ea58-106">A cikk segítséget nyújt a használatának megkezdésében, és ismerteti az alapvető fogalmakat.</span><span class="sxs-lookup"><span data-stu-id="7ea58-106">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

## <a name="connect"></a><span data-ttu-id="7ea58-107">Kapcsolódás</span><span class="sxs-lookup"><span data-stu-id="7ea58-107">Connect</span></span>

<span data-ttu-id="7ea58-108">Első lépésként a legegyszerűbb módszer, ha [elindítja a Cloud Shellt](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="7ea58-108">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="7ea58-109">Indítsa el a Cloud Shellt az Azure Portal felső navigációs szakaszából.</span><span class="sxs-lookup"><span data-stu-id="7ea58-109">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell ikon](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="7ea58-111">Válassza ki a használni kívánt előfizetést, és hozzon létre egy tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="7ea58-111">Choose the subscription you want to use and create a storage account.</span></span>

   ![Tárfiók létrehozása](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="7ea58-113">A tároló létrehozása után a Cloud Shell megnyit egy PowerShell-munkamenetet a böngészőben.</span><span class="sxs-lookup"><span data-stu-id="7ea58-113">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell a PowerShellhez](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="7ea58-115">Telepítheti az Azure PowerShellt, és helyileg is használhatja PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="7ea58-115">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="7ea58-116">Az Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="7ea58-116">Install Azure PowerShell</span></span>

<span data-ttu-id="7ea58-117">Első lépésként győződjön meg róla, hogy az Azure PowerShell legújabb verziója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="7ea58-117">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="7ea58-118">A legújabb kiadással kapcsolatos információkért lásd a [kibocsátási megjegyzéseket](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="7ea58-118">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="7ea58-119">[Telepítse az Azure PowerShellt](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="7ea58-119">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="7ea58-120">A telepítés sikerességének ellenőrzéséhez futtassa a `Get-InstalledModule AzureRM -AllVersions` parancsot a parancssorról.</span><span class="sxs-lookup"><span data-stu-id="7ea58-120">To verify the installation was successful, run `Get-InstalledModule AzureRM -AllVersions` from your command line.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="7ea58-121">Bejelentkezés az Azure-ba</span><span class="sxs-lookup"><span data-stu-id="7ea58-121">Sign in to Azure</span></span>

<span data-ttu-id="7ea58-122">Interaktív bejelentkezés:</span><span class="sxs-lookup"><span data-stu-id="7ea58-122">Sign on interactively:</span></span>

1. <span data-ttu-id="7ea58-123">Gépelje be: `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="7ea58-123">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="7ea58-124">Egy párbeszédpanel jelenik meg, amelyen meg kell adnia Azure-beli hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="7ea58-124">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="7ea58-125">Az -EnvironmentName kapcsoló lehetővé teszi az Azure China vagy az Azure Germany szolgáltatással való hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="7ea58-125">Option '-EnvironmentName' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="7ea58-126">például: Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="7ea58-126">e.g. Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span></span>

2. <span data-ttu-id="7ea58-127">Írja be a fiókjához tartozó e-mail-címet és jelszót.</span><span class="sxs-lookup"><span data-stu-id="7ea58-127">Type the email address and password associated with your account.</span></span> <span data-ttu-id="7ea58-128">Az Azure hitelesíti és menti a hitelesítő adatokat, majd bezárja az ablakot.</span><span class="sxs-lookup"><span data-stu-id="7ea58-128">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="7ea58-129">Miután bejelentkezett egy Azure-fiókba, az Azure PowerShell parancsmagjaival elérheti és kezelheti az előfizetésben lévő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="7ea58-129">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="7ea58-130">Hozzon létre egy erőforráscsoportot</span><span class="sxs-lookup"><span data-stu-id="7ea58-130">Create a resource group</span></span>

<span data-ttu-id="7ea58-131">Most, hogy mindent beállítottunk, hozzunk létre erőforrásokat az Azure-ban az Azure PowerShell használatával.</span><span class="sxs-lookup"><span data-stu-id="7ea58-131">Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.</span></span>

<span data-ttu-id="7ea58-132">Először is hozzon létre egy erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="7ea58-132">First, create a Resource Group.</span></span> <span data-ttu-id="7ea58-133">Az Azure erőforráscsoportjaiban együtt kezelhet több olyan erőforrást, amelyeket logikailag egy csoportba kíván foglalni.</span><span class="sxs-lookup"><span data-stu-id="7ea58-133">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="7ea58-134">Például létrehozhat egy erőforráscsoportot egy alkalmazáshoz vagy projekthez, majd hozzáadhat egy virtuális gépet, egy adatbázist és egy CDN-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="7ea58-134">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="7ea58-135">Hozzunk létre egy erőforráscsoportot „MyResourceGroup” néven az Azure westeurope (Nyugat--Európa) régiójában.</span><span class="sxs-lookup"><span data-stu-id="7ea58-135">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="7ea58-136">Ehhez írja be a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="7ea58-136">To do so type the following command:</span></span>

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

## <a name="create-a-windows-virtual-machine"></a><span data-ttu-id="7ea58-137">Windows rendszerű virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="7ea58-137">Create a Windows Virtual Machine</span></span>

<span data-ttu-id="7ea58-138">Most, hogy létrehoztuk az erőforráscsoportot, hozzunk létre benne egy windowsos virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7ea58-138">Now that we have our resource group, let's create a Windows VM within it.</span></span> <span data-ttu-id="7ea58-139">Az új virtuális gép létrehozásához előbb létre kell hoznunk a többi szükséges erőforrást, és egy konfigurációt kell hozzájuk rendelnünk.</span><span class="sxs-lookup"><span data-stu-id="7ea58-139">To create a new VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="7ea58-140">Ezután ezzel a konfigurációval létrehozhatjuk a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7ea58-140">Then we can use that configuration to create the VM.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="7ea58-141">A szükséges hálózati erőforrások létrehozása</span><span class="sxs-lookup"><span data-stu-id="7ea58-141">Create the required network resources</span></span>

<span data-ttu-id="7ea58-142">Először létre kell hoznunk egy alhálózati konfigurációt a virtuális hálózat létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7ea58-142">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="7ea58-143">Létrehozunk egy nyilvános IP-címet is, hogy csatlakozhassunk a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="7ea58-143">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="7ea58-144">Létrehozunk egy hálózati biztonsági csoportot, hogy biztonságossá tehessük a nyilvános cím elérését.</span><span class="sxs-lookup"><span data-stu-id="7ea58-144">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="7ea58-145">Végül létrehozzuk a virtuális NIC-t az összes előbbi erőforrás használatával.</span><span class="sxs-lookup"><span data-stu-id="7ea58-145">Finally we create the virtual NIC using all of the previous resources.</span></span>

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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="7ea58-146">A virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="7ea58-146">Create the virtual machine</span></span>

<span data-ttu-id="7ea58-147">Először is szükségünk lesz az operációs rendszerhez tartozó hitelesítő adatok egy készletére.</span><span class="sxs-lookup"><span data-stu-id="7ea58-147">First we need a set of credentials for the OS.</span></span>

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

<span data-ttu-id="7ea58-148">Most, hogy rendelkezünk a szükséges erőforrásokkal, létrehozhatjuk a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7ea58-148">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="7ea58-149">Ehhez a lépéshez létrehozunk egy VM-konfigurációs objektumot, majd ezzel a konfigurációval létrehozzuk a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7ea58-149">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="7ea58-150">A `New-AzureRmVM` parancs kimeneti eredményei akkor érhetők el, amikor a virtuális gép létrejött és használatra kész.</span><span class="sxs-lookup"><span data-stu-id="7ea58-150">The `New-AzureRmVM` command outputs results once the VM has been fully created and is ready to be used.</span></span>

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

<span data-ttu-id="7ea58-151">Most jelentkezzen be az újonnan létrehozott, Windows Server-alapú virtuális gépre a Távoli asztal szolgáltatással és a virtuális gép nyilvános IP-címével.</span><span class="sxs-lookup"><span data-stu-id="7ea58-151">Now sign in to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM.</span></span> <span data-ttu-id="7ea58-152">A következő parancs az előző szkriptben létrehozott nyilvános IP-címet jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7ea58-152">The following command displays the public IP address created in the previous script.</span></span>

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

<span data-ttu-id="7ea58-153">Windows-alapú rendszer használata esetén ezt a parancssorból az mstsc parancs használatával teheti meg:</span><span class="sxs-lookup"><span data-stu-id="7ea58-153">If you are on a Windows-based system, you can do this from the command line using the mstsc command:</span></span>

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="7ea58-154">A bejelentkezéshez ugyanazt a felhasználónév–jelszó kombinációt adja meg, amelyet a virtuális gép létrehozása során használt.</span><span class="sxs-lookup"><span data-stu-id="7ea58-154">Supply the same username/password combination you used when creating the VM to sign in.</span></span>

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="7ea58-155">Linux rendszerű virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="7ea58-155">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="7ea58-156">Az új linuxos virtuális gép létrehozásához előbb létre kell hoznunk a többi szükséges erőforrást, és egy konfigurációt kell hozzájuk rendelnünk.</span><span class="sxs-lookup"><span data-stu-id="7ea58-156">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="7ea58-157">Ezután ezzel a konfigurációval létrehozhatjuk a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7ea58-157">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="7ea58-158">Mindez feltételezi, hogy már létrehozta az erőforráscsoportot az előzőekben ismertetettek szerint.</span><span class="sxs-lookup"><span data-stu-id="7ea58-158">This assumes that you have already created the resource group as previously shown.</span></span> <span data-ttu-id="7ea58-159">Emellett szüksége lesz egy `id_rsa.pub` nevű nyilvános SSH-kulcsra a felhasználói profilja .ssh könyvtárában.</span><span class="sxs-lookup"><span data-stu-id="7ea58-159">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="7ea58-160">A szükséges hálózati erőforrások létrehozása</span><span class="sxs-lookup"><span data-stu-id="7ea58-160">Create the required network resources</span></span>

<span data-ttu-id="7ea58-161">Először létre kell hoznunk egy alhálózati konfigurációt a virtuális hálózat létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7ea58-161">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="7ea58-162">Létrehozunk egy nyilvános IP-címet is, hogy csatlakozhassunk a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="7ea58-162">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="7ea58-163">Létrehozunk egy hálózati biztonsági csoportot, hogy biztonságossá tehessük a nyilvános cím elérését.</span><span class="sxs-lookup"><span data-stu-id="7ea58-163">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="7ea58-164">Végül létrehozzuk a virtuális NIC-t az összes előbbi erőforrás használatával.</span><span class="sxs-lookup"><span data-stu-id="7ea58-164">Finally we create the virtual NIC using all of the previous resources.</span></span>

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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="7ea58-165">A virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="7ea58-165">Create the virtual machine</span></span>

<span data-ttu-id="7ea58-166">Most, hogy rendelkezünk a szükséges erőforrásokkal, létrehozhatjuk a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7ea58-166">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="7ea58-167">Ehhez a lépéshez létrehozunk egy VM-konfigurációs objektumot, majd ezzel a konfigurációval létrehozzuk a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7ea58-167">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

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

<span data-ttu-id="7ea58-168">Most, hogy a virtuális gép létrejött, bejelentkezhet az új Linux rendszerű virtuális gépre SSH használatával a létrehozott virtuális gép nyilvános IP-címével:</span><span class="sxs-lookup"><span data-stu-id="7ea58-168">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="7ea58-169">Egyéb erőforrások létrehozása az Azure-ban</span><span class="sxs-lookup"><span data-stu-id="7ea58-169">Creating other resources in Azure</span></span>

<span data-ttu-id="7ea58-170">Bemutattuk, hogyan hozhat létre erőforráscsoportot, valamint Linux és Windows Server rendszerű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7ea58-170">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="7ea58-171">Számos más típusú Azure-erőforrást is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="7ea58-171">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="7ea58-172">Például a következő parancs használatával létrehozhat egy Azure-beli hálózati terheléselosztót, amelyet aztán társíthat az újonnan létrehozott virtuális gépekkel:</span><span class="sxs-lookup"><span data-stu-id="7ea58-172">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="7ea58-173">Vagy létrehozhat egy új privát virtuális hálózatot (vagy az Azure-ban gyakran használt nevén „VNetet”) az infrastruktúránkhoz a következő paranccsal:</span><span class="sxs-lookup"><span data-stu-id="7ea58-173">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="7ea58-174">Az Azure és az Azure PowerShell attól igazán sokoldalúak, hogy nemcsak a felhőalapú infrastruktúrához használhatók, hanem felügyelt platformszolgáltatások kialakításához is.</span><span class="sxs-lookup"><span data-stu-id="7ea58-174">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="7ea58-175">A felügyelt platformszolgáltatásokat az infrastruktúrával kombinálva még nagyobb teljesítményű megoldások építhetők ki.</span><span class="sxs-lookup"><span data-stu-id="7ea58-175">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="7ea58-176">Például az Azure PowerShell használatával létrehozhat egy Azure AppService-t.</span><span class="sxs-lookup"><span data-stu-id="7ea58-176">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="7ea58-177">Az Azure AppService egy felügyelt platformszolgáltatás, amely nagyszerű megoldás a webappok üzemeltetésére anélkül, hogy aggódnia kellene az infrastruktúra miatt.</span><span class="sxs-lookup"><span data-stu-id="7ea58-177">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="7ea58-178">Az Azure AppService létrehozása után két új Azure webappot hozhat létre az AppService-ben a következő parancsokkal:</span><span class="sxs-lookup"><span data-stu-id="7ea58-178">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="7ea58-179">Üzembe helyezett erőforrások listázása</span><span class="sxs-lookup"><span data-stu-id="7ea58-179">Listing deployed resources</span></span>

<span data-ttu-id="7ea58-180">A `Get-AzureRmResource` parancsmag használatával listázhatja az Azure-ban futó erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="7ea58-180">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="7ea58-181">Az alábbi példa az új erőforráscsoportban létrehozott erőforrásokat mutatja be.</span><span class="sxs-lookup"><span data-stu-id="7ea58-181">The following example shows the resources we just created in the new resource group.</span></span>

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

## <a name="deleting-resources"></a><span data-ttu-id="7ea58-182">Erőforrások törlése</span><span class="sxs-lookup"><span data-stu-id="7ea58-182">Deleting resources</span></span>

<span data-ttu-id="7ea58-183">Az Azure-fiók tisztítása érdekében érdemes lehet törölnie a példában létrehozott erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="7ea58-183">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="7ea58-184">A `Remove-AzureRm*` parancsmagokkal törölheti a már nem szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="7ea58-184">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="7ea58-185">A létrehozott Windows rendszerű virtuális gép eltávolításához futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="7ea58-185">To remove the Windows VM we created, using the following command:</span></span>

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="7ea58-186">A rendszer rákérdez az erőforrás törlésének jóváhagyására.</span><span class="sxs-lookup"><span data-stu-id="7ea58-186">You will be prompted to confirm that you want to remove the resource.</span></span>

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="7ea58-187">Egyszerre több erőforrást is törölhet.</span><span class="sxs-lookup"><span data-stu-id="7ea58-187">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="7ea58-188">A következő parancs például törli a teljes „MyResourceGroup” erőforráscsoportot, amelyet ebben a bevezető oktatóanyagban az összes mintához használtunk.</span><span class="sxs-lookup"><span data-stu-id="7ea58-188">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="7ea58-189">Törli az erőforráscsoportot, és minden benne lévő erőforrást is.</span><span class="sxs-lookup"><span data-stu-id="7ea58-189">This removes the resource group and all of the resources in it.</span></span>

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="7ea58-190">Ez több percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="7ea58-190">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="7ea58-191">Minták letöltése</span><span class="sxs-lookup"><span data-stu-id="7ea58-191">Get samples</span></span>

<span data-ttu-id="7ea58-192">Az Azure PowerShell használatával kapcsolatos további tudnivalókért tekintse át a [Linux rendszerű virtuális gépek](/azure/virtual-machines/linux/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), a [Windows rendszerű virtuális gépek](/azure/virtual-machines/windows/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), a [Web Apps-alkalmazások](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) és az [SQL Database-adatbázisok](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) leggyakoribb szkriptjeit.</span><span class="sxs-lookup"><span data-stu-id="7ea58-192">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/linux/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/windows/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="7ea58-193">További lépések</span><span class="sxs-lookup"><span data-stu-id="7ea58-193">Next steps</span></span>

* [<span data-ttu-id="7ea58-194">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="7ea58-194">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="7ea58-195">Azure-előfizetések kezelése az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="7ea58-195">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="7ea58-196">Szolgáltatásnevek létrehozása az Azure PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="7ea58-196">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="7ea58-197">A régi kiadásokról való áttéréssel kapcsolatban olvassa át a [kibocsátási megjegyzéseket](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="7ea58-197">Read the [Release notes](./release-notes-azureps.md) about migrating from an older release.</span></span>
* <span data-ttu-id="7ea58-198">Segítség kérése a közösségtől:</span><span class="sxs-lookup"><span data-stu-id="7ea58-198">Get help from the community:</span></span>
  * [<span data-ttu-id="7ea58-199">Azure-fórum az MSDN-en</span><span class="sxs-lookup"><span data-stu-id="7ea58-199">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="7ea58-200">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="7ea58-200">stackoverflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
