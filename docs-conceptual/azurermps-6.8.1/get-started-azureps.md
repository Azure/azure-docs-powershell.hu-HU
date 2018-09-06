---
title: Ismerkedés az Azure PowerShell-lel
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 5354a75e969e084d6457d0566a516705f365476f
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/06/2018
ms.locfileid: "43384090"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="19107-102">Ismerkedés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="19107-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="19107-103">Az Azure PowerShell az Azure-erőforrások parancssori kezelésére és adminisztrálására, valamint az Azure Resource Manageren futtatható automatizálási szkriptek létrehozására készült.</span><span class="sxs-lookup"><span data-stu-id="19107-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="19107-104">Használhatja a böngészőjében az [Azure Cloud Shell-lel](/azure/cloud-shell/overview), vagy telepítheti a helyi gépen.</span><span class="sxs-lookup"><span data-stu-id="19107-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="19107-105">A cikk segítséget nyújt az Azure PowerShell használatának megkezdésében, és ismerteti az alapvető fogalmakat.</span><span class="sxs-lookup"><span data-stu-id="19107-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="19107-106">Az Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="19107-106">Install Azure PowerShell</span></span>

<span data-ttu-id="19107-107">Első lépésként győződjön meg róla, hogy az Azure PowerShell legújabb verziója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="19107-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="19107-108">A legújabb kiadással kapcsolatos információkért lásd a [kibocsátási megjegyzéseket](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="19107-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="19107-109">[Telepítse az Azure PowerShellt](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="19107-109">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="19107-110">A telepítés sikerességének ellenőrzéséhez futtassa a `Get-Module AzureRM -ListAvailable` parancsot a parancssorról.</span><span class="sxs-lookup"><span data-stu-id="19107-110">To verify the installation was successful, run `Get-Module AzureRM -ListAvailable` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="19107-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="19107-111">Azure Cloud Shell</span></span>

<span data-ttu-id="19107-112">Első lépésként a legegyszerűbb módszer, ha [elindítja a Cloud Shellt](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="19107-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="19107-113">Indítsa el a Cloud Shellt az Azure Portal felső navigációs szakaszából.</span><span class="sxs-lookup"><span data-stu-id="19107-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell ikon](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="19107-115">Válassza ki a használni kívánt előfizetést, és hozzon létre egy tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="19107-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![Tárfiók létrehozása](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="19107-117">A tároló létrehozása után a Cloud Shell megnyit egy PowerShell-munkamenetet a böngészőben.</span><span class="sxs-lookup"><span data-stu-id="19107-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell a PowerShellhez](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="19107-119">Telepítheti az Azure PowerShellt, és helyileg is használhatja PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="19107-119">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="19107-120">Bejelentkezés az Azure-ba</span><span class="sxs-lookup"><span data-stu-id="19107-120">Sign in to Azure</span></span>

<span data-ttu-id="19107-121">Interaktív bejelentkezés:</span><span class="sxs-lookup"><span data-stu-id="19107-121">Sign on interactively:</span></span>

1. <span data-ttu-id="19107-122">Gépelje be: `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="19107-122">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="19107-123">Egy párbeszédpanel jelenik meg, amelyen meg kell adnia Azure-beli hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="19107-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="19107-124">Az -Environment kapcsoló lehetővé teszi a bejelentkezést az Azure China vagy az Azure Germany szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="19107-124">Option '-Environment' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="19107-125">például: Connect-AzureRmAccount -Environment AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="19107-125">e.g. Connect-AzureRmAccount -Environment AzureChinaCloud</span></span>

2. <span data-ttu-id="19107-126">Írja be a fiókjához tartozó e-mail-címet és jelszót.</span><span class="sxs-lookup"><span data-stu-id="19107-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="19107-127">Az Azure hitelesíti és menti a hitelesítő adatokat, majd bezárja az ablakot.</span><span class="sxs-lookup"><span data-stu-id="19107-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="19107-128">Miután bejelentkezett egy Azure-fiókba, az Azure PowerShell parancsmagjaival elérheti és kezelheti az előfizetésben lévő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="19107-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="19107-129">Windows rendszerű virtuális gép létrehozása egyszerű alapértelmezett beállítások használatával</span><span class="sxs-lookup"><span data-stu-id="19107-129">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="19107-130">A `New-AzureRmVM` parancsmag egy leegyszerűsített szintaxist biztosít, amely megkönnyíti az új virtuális gépek létrehozását.</span><span class="sxs-lookup"><span data-stu-id="19107-130">The `New-AzureRmVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="19107-131">Mindössze két paraméterértéket kell megadnia: a virtuális gép nevét, valamint a virtuális gép helyi rendszergazdai fiókjához tartozó hitelesítő adatok egy készletét.</span><span class="sxs-lookup"><span data-stu-id="19107-131">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="19107-132">Először hozza létre a hitelesítő objektumot.</span><span class="sxs-lookup"><span data-stu-id="19107-132">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="19107-133">Ezt követően hozza létre a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="19107-133">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

<span data-ttu-id="19107-134">Ez eddig nem volt bonyolult.</span><span class="sxs-lookup"><span data-stu-id="19107-134">That was easy.</span></span> <span data-ttu-id="19107-135">Felmerülhet azonban a kérdés, hogy milyen más elemek jönnek még létre, illetve hogy milyen lesz a virtuális gép konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="19107-135">But, you may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="19107-136">Először is lássuk az erőforráscsoportokat.</span><span class="sxs-lookup"><span data-stu-id="19107-136">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="19107-137">A **cloud-shell-storage-westus** erőforráscsoport a Cloud Shell első használatakor jön létre.</span><span class="sxs-lookup"><span data-stu-id="19107-137">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="19107-138">A **SampleVM** erőforráscsoportot a `New-AzureRmVM` parancsmag hozta létre.</span><span class="sxs-lookup"><span data-stu-id="19107-138">The **SampleVM** resource group was created by the `New-AzureRmVM` cmdlet.</span></span>

<span data-ttu-id="19107-139">Milyen egyéb erőforráscsoportok jöttek létre az új erőforráscsoportban?</span><span class="sxs-lookup"><span data-stu-id="19107-139">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

<span data-ttu-id="19107-140">További részleteket is lekérhet a virtuális géppel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="19107-140">Let's get some more details about the VM.</span></span> <span data-ttu-id="19107-141">Ez a példa bemutatja, hogyan kérhet le információt a virtuális gép létrehozásához használt rendszerképről.</span><span class="sxs-lookup"><span data-stu-id="19107-141">This examples shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="19107-142">Linux rendszerű, teljes konfigurációjú virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="19107-142">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="19107-143">Az előző példában egy egyszerűsített szintaxis és az alapértelmezett paraméterértékek használatával hozott létre egy Windows rendszerű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="19107-143">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="19107-144">Ebben a példában a virtuális gép összes beállításának Ön fogja megadni az értékét.</span><span class="sxs-lookup"><span data-stu-id="19107-144">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="19107-145">Hozzon létre egy erőforráscsoportot</span><span class="sxs-lookup"><span data-stu-id="19107-145">Create a resource group</span></span>

<span data-ttu-id="19107-146">Ebben a példában egy erőforráscsoportot szeretnénk létrehozni.</span><span class="sxs-lookup"><span data-stu-id="19107-146">For this example we want to create a Resource Group.</span></span> <span data-ttu-id="19107-147">Az Azure erőforráscsoportjaiban együtt kezelhet több olyan erőforrást, amelyeket logikailag egy csoportba kíván foglalni.</span><span class="sxs-lookup"><span data-stu-id="19107-147">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="19107-148">Például létrehozhat egy erőforráscsoportot egy alkalmazáshoz vagy projekthez, majd hozzáadhat egy virtuális gépet, egy adatbázist és egy CDN-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="19107-148">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="19107-149">Hozzunk létre egy erőforráscsoportot „MyResourceGroup” néven az Azure westeurope (Nyugat--Európa) régiójában.</span><span class="sxs-lookup"><span data-stu-id="19107-149">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="19107-150">Ehhez írja be a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="19107-150">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="19107-151">Ez az új erőforráscsoport fogja tartalmazni a létrehozni kívánt új virtuális géphez szükséges összes erőforrást.</span><span class="sxs-lookup"><span data-stu-id="19107-151">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="19107-152">Az új linuxos virtuális gép létrehozásához előbb létre kell hoznunk a többi szükséges erőforrást, és egy konfigurációt kell hozzájuk rendelnünk.</span><span class="sxs-lookup"><span data-stu-id="19107-152">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="19107-153">Ezután ezzel a konfigurációval létrehozhatjuk a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="19107-153">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="19107-154">Emellett szüksége lesz egy `id_rsa.pub` nevű nyilvános SSH-kulcsra a felhasználói profilja .ssh könyvtárában.</span><span class="sxs-lookup"><span data-stu-id="19107-154">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="19107-155">A szükséges hálózati erőforrások létrehozása</span><span class="sxs-lookup"><span data-stu-id="19107-155">Create the required network resources</span></span>

<span data-ttu-id="19107-156">Először létre kell hoznunk egy alhálózati konfigurációt a virtuális hálózat létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="19107-156">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="19107-157">Létrehozunk egy nyilvános IP-címet is, hogy csatlakozhassunk a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="19107-157">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="19107-158">Létrehozunk egy hálózati biztonsági csoportot, hogy biztonságossá tehessük a nyilvános cím elérését.</span><span class="sxs-lookup"><span data-stu-id="19107-158">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="19107-159">Végül létrehozzuk a virtuális NIC-t az összes előbbi erőforrás használatával.</span><span class="sxs-lookup"><span data-stu-id="19107-159">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
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

### <a name="create-the-vm-configuration"></a><span data-ttu-id="19107-160">A virtuális gép konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="19107-160">Create the VM configuration</span></span>

<span data-ttu-id="19107-161">Most, hogy rendelkezünk a szükséges erőforrásokkal, létrehozhatjuk a virtuális gép konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="19107-161">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="19107-162">A virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="19107-162">Create the virtual machine</span></span>

<span data-ttu-id="19107-163">A virtuális gép konfigurációs objektumával létrehozhatjuk a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="19107-163">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="19107-164">Most, hogy a virtuális gép létrejött, bejelentkezhet az új Linux rendszerű virtuális gépre SSH használatával a létrehozott virtuális gép nyilvános IP-címével:</span><span class="sxs-lookup"><span data-stu-id="19107-164">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```output
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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="19107-165">Egyéb erőforrások létrehozása az Azure-ban</span><span class="sxs-lookup"><span data-stu-id="19107-165">Creating other resources in Azure</span></span>

<span data-ttu-id="19107-166">Bemutattuk, hogyan hozhat létre erőforráscsoportot, valamint Linux és Windows Server rendszerű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="19107-166">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="19107-167">Számos más típusú Azure-erőforrást is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="19107-167">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="19107-168">Például a következő parancs használatával létrehozhat egy Azure-beli hálózati terheléselosztót, amelyet aztán társíthat az újonnan létrehozott virtuális gépekkel:</span><span class="sxs-lookup"><span data-stu-id="19107-168">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="19107-169">Vagy létrehozhat egy új privát virtuális hálózatot (vagy az Azure-ban gyakran használt nevén „VNetet”) az infrastruktúránkhoz a következő paranccsal:</span><span class="sxs-lookup"><span data-stu-id="19107-169">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="19107-170">Az Azure és az Azure PowerShell attól igazán sokoldalúak, hogy nemcsak a felhőalapú infrastruktúrához használhatók, hanem felügyelt platformszolgáltatások kialakításához is.</span><span class="sxs-lookup"><span data-stu-id="19107-170">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="19107-171">A felügyelt platformszolgáltatásokat az infrastruktúrával kombinálva még nagyobb teljesítményű megoldások építhetők ki.</span><span class="sxs-lookup"><span data-stu-id="19107-171">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="19107-172">Például az Azure PowerShell használatával létrehozhat egy Azure AppService-t.</span><span class="sxs-lookup"><span data-stu-id="19107-172">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="19107-173">Az Azure AppService egy felügyelt platformszolgáltatás, amely nagyszerű megoldás a webappok üzemeltetésére anélkül, hogy aggódnia kellene az infrastruktúra miatt.</span><span class="sxs-lookup"><span data-stu-id="19107-173">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="19107-174">Az Azure AppService létrehozása után két új Azure webappot hozhat létre az AppService-ben a következő parancsokkal:</span><span class="sxs-lookup"><span data-stu-id="19107-174">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="19107-175">Üzembe helyezett erőforrások listázása</span><span class="sxs-lookup"><span data-stu-id="19107-175">Listing deployed resources</span></span>

<span data-ttu-id="19107-176">A `Get-AzureRmResource` parancsmag használatával listázhatja az Azure-ban futó erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="19107-176">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="19107-177">Az alábbi példa az új erőforráscsoportban létrehozott erőforrásokat mutatja be.</span><span class="sxs-lookup"><span data-stu-id="19107-177">The following example shows the resources we just created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
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

## <a name="deleting-resources"></a><span data-ttu-id="19107-178">Erőforrások törlése</span><span class="sxs-lookup"><span data-stu-id="19107-178">Deleting resources</span></span>

<span data-ttu-id="19107-179">Az Azure-fiók tisztítása érdekében érdemes lehet törölnie a példában létrehozott erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="19107-179">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="19107-180">A `Remove-AzureRm*` parancsmagokkal törölheti a már nem szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="19107-180">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="19107-181">A létrehozott Windows rendszerű virtuális gép eltávolításához futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="19107-181">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="19107-182">A rendszer rákérdez az erőforrás törlésének jóváhagyására.</span><span class="sxs-lookup"><span data-stu-id="19107-182">You will be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="19107-183">Egyszerre több erőforrást is törölhet.</span><span class="sxs-lookup"><span data-stu-id="19107-183">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="19107-184">A következő parancs például törli a teljes „MyResourceGroup” erőforráscsoportot, amelyet ebben a bevezető oktatóanyagban az összes mintához használtunk.</span><span class="sxs-lookup"><span data-stu-id="19107-184">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="19107-185">Törli az erőforráscsoportot, és minden benne lévő erőforrást is.</span><span class="sxs-lookup"><span data-stu-id="19107-185">This removes the resource group and all of the resources in it.</span></span>

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="19107-186">Ez több percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="19107-186">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="19107-187">Minták letöltése</span><span class="sxs-lookup"><span data-stu-id="19107-187">Get samples</span></span>

<span data-ttu-id="19107-188">Az Azure PowerShell használatával kapcsolatos további tudnivalókért tekintse át a [Linux rendszerű virtuális gépek](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), a [Windows rendszerű virtuális gépek](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), a [Web Apps-alkalmazások](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) és az [SQL Database-adatbázisok](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) leggyakoribb szkriptjeit.</span><span class="sxs-lookup"><span data-stu-id="19107-188">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="19107-189">További lépések</span><span class="sxs-lookup"><span data-stu-id="19107-189">Next steps</span></span>

* [<span data-ttu-id="19107-190">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="19107-190">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="19107-191">Azure-előfizetések kezelése az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="19107-191">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="19107-192">Szolgáltatásnevek létrehozása az Azure PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="19107-192">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="19107-193">A régi kiadásokról való áttéréssel kapcsolatban olvassa át a kibocsátási megjegyzéseket: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="19107-193">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="19107-194">Segítség kérése a közösségtől:</span><span class="sxs-lookup"><span data-stu-id="19107-194">Get help from the community:</span></span>
  * [<span data-ttu-id="19107-195">Azure-fórum az MSDN-en</span><span class="sxs-lookup"><span data-stu-id="19107-195">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="19107-196">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="19107-196">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
