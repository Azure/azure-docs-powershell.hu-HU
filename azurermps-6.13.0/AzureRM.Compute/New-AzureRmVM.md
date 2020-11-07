---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: da307e1bc5bca5c3127e33a32bb4480148fe14a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673000"
---
# <span data-ttu-id="88fd2-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88fd2-101">New-AzureRmVM</span></span>

## <span data-ttu-id="88fd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="88fd2-103">Virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="88fd2-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88fd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88fd2-104">SYNTAX</span></span>

### <span data-ttu-id="88fd2-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88fd2-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88fd2-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="88fd2-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88fd2-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="88fd2-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88fd2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="88fd2-108">DESCRIPTION</span></span>
<span data-ttu-id="88fd2-109">A **New-AzureRmVM** parancsmag létrehoz egy virtuális gépet az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="88fd2-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="88fd2-110">Ez a parancsmag a virtuális gép objektumát bemenetként veszi át.</span><span class="sxs-lookup"><span data-stu-id="88fd2-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="88fd2-111">A New-AzureRmVMConfig parancsmag segítségével hozzon létre egy virtuálisgép-objektumot.</span><span class="sxs-lookup"><span data-stu-id="88fd2-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="88fd2-112">Más parancsmagok segítségével konfigurálhatja a virtuális gépet, például set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, add-AzureRmVMNetworkInterface és set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="88fd2-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>
<span data-ttu-id="88fd2-113">A `SimpleParameterSet` VM létrehozásának kényelmes módja, ha a virtuális VM-létrehozási argumentumokat nem kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="88fd2-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="88fd2-114">Példák</span><span class="sxs-lookup"><span data-stu-id="88fd2-114">EXAMPLES</span></span>

### <span data-ttu-id="88fd2-115">Példa 1: virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="88fd2-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

<span data-ttu-id="88fd2-116">Ebben a példában a parancsfájl bemutatja, hogy miként hozhat létre virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="88fd2-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="88fd2-117">A parancsfájl a virtuális gép felhasználónevét és jelszavát fogja kérni.</span><span class="sxs-lookup"><span data-stu-id="88fd2-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="88fd2-118">Ez a parancsfájl számos más parancsmagot használ.</span><span class="sxs-lookup"><span data-stu-id="88fd2-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="88fd2-119">2. példa: virtuális gép létrehozása egyéni felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="88fd2-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="88fd2-120">Ez a példa egy meglévő sys-prepped, általános egyéni operációs rendszer lemezképet hoz létre, és egy adatlemezt csatol hozzá, kiépít egy új hálózatot, telepíti a virtuális merevlemezt, és futtatja azt.</span><span class="sxs-lookup"><span data-stu-id="88fd2-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="88fd2-121">Ez a parancsfájl automatikusan használható a kikészítéshez, mert a helyi virtuális gép rendszergazdai hitelesítő adatait használja a felhasználói interakciót igénylő " **Get-hitelesítőadat** " helyett.</span><span class="sxs-lookup"><span data-stu-id="88fd2-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="88fd2-122">Ez a parancsfájl feltételezi, hogy már bejelentkezett az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="88fd2-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="88fd2-123">Bejelentkezési állapotát a **Get-AzureSubscription** parancsmag használatával ellenőrizheti.</span><span class="sxs-lookup"><span data-stu-id="88fd2-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

### <span data-ttu-id="88fd2-124">3. példa: virtuális VM-fájl létrehozása nyilvános IP nélküli piactérről</span><span class="sxs-lookup"><span data-stu-id="88fd2-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
```
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString <password> -AsPlainText -Force
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
$ComputerName = "MyVM"
$VMName = "MyVM"
$VMSize = "Standard_DS3"

$NetworkName = "MyNet"
$NICName = "MyNIC"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="88fd2-125">Ez a példa egy új hálózatot hoz létre, és egy nyilvános IP-cím vagy hálózati biztonsági csoport létrehozása nélkül telepíti a Windows VM-et a Piactérről.</span><span class="sxs-lookup"><span data-stu-id="88fd2-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="88fd2-126">Ez a parancsfájl automatikusan használható a kikészítéshez, mert a helyi virtuális gép rendszergazdai hitelesítő adatait használja a felhasználói interakciót igénylő " **Get-hitelesítőadat** " helyett.</span><span class="sxs-lookup"><span data-stu-id="88fd2-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="88fd2-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88fd2-127">PARAMETERS</span></span>

### <span data-ttu-id="88fd2-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="88fd2-128">-AddressPrefix</span></span>
<span data-ttu-id="88fd2-129">A virtuális hálózathoz tartozó cím előtagja, amelyet a VM rendszerhez hoz létre.</span><span class="sxs-lookup"><span data-stu-id="88fd2-129">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="88fd2-130">-AllocationMethod</span></span>
<span data-ttu-id="88fd2-131">A VM rendszerhez létrehozott nyilvános IP-cím IP-kiosztási módja.</span><span class="sxs-lookup"><span data-stu-id="88fd2-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88fd2-132">-AsJob</span></span>
<span data-ttu-id="88fd2-133">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="88fd2-133">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="88fd2-134">-AvailabilitySetName</span></span>
<span data-ttu-id="88fd2-135">Az elérhetőségi halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88fd2-135">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-136">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="88fd2-136">-Credential</span></span>
<span data-ttu-id="88fd2-137">A VM rendszergazdai hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="88fd2-137">The administrator credentials for the VM.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="88fd2-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="88fd2-139">Az adatlemezek méretét adja meg GB-ban.</span><span class="sxs-lookup"><span data-stu-id="88fd2-139">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88fd2-140">-DefaultProfile</span></span>
<span data-ttu-id="88fd2-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88fd2-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="88fd2-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="88fd2-143">Jelzi, hogy ez a parancsmag nem telepíti a **BG információs** bővítményt a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="88fd2-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="88fd2-144">-DiskFile</span></span>
<span data-ttu-id="88fd2-145">A virtuális merevlemez-fájl helyi elérési útja, amelyet fel kell tölteni a felhőbe, és létre kell hoznia a VM-et, és az utótagnak ". vhd"-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="88fd2-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="88fd2-146">-DomainNameLabel</span></span>
<span data-ttu-id="88fd2-147">A VM teljes tartománynevét (FQDN) tartalmazó aldomain címkéje.</span><span class="sxs-lookup"><span data-stu-id="88fd2-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="88fd2-148">Ez az űrlapon fog szerepelni `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="88fd2-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-149">-Kép</span><span class="sxs-lookup"><span data-stu-id="88fd2-149">-Image</span></span>
<span data-ttu-id="88fd2-150">Az a felhasználóbarát kép neve, amelyen a VM épül.</span><span class="sxs-lookup"><span data-stu-id="88fd2-150">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="88fd2-151">Ezek a következők: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-LEAP, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="88fd2-151">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ImageName

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="88fd2-152">-LicenseType</span></span>
<span data-ttu-id="88fd2-153">A licenc típusát adja meg, amely azt jelzi, hogy a virtuális gép képe vagy lemeze engedélyezett a helyszíni verzióban.</span><span class="sxs-lookup"><span data-stu-id="88fd2-153">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="88fd2-154">Ezt az értéket csak a Windows Server operációs rendszert tartalmazó képek esetén használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="88fd2-154">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="88fd2-155">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="88fd2-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88fd2-156">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="88fd2-156">Windows_Client</span></span>
- <span data-ttu-id="88fd2-157">Windows_Server ez az érték nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="88fd2-157">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="88fd2-158">Ha ezt a paramétert a frissítéshez adja meg, az értéknek meg kell egyeznie a virtuális gép kezdeti értékével.</span><span class="sxs-lookup"><span data-stu-id="88fd2-158">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-159">-Linux</span><span class="sxs-lookup"><span data-stu-id="88fd2-159">-Linux</span></span>
<span data-ttu-id="88fd2-160">Azt jelzi, hogy a lemezmeghajtó a Linux VM-re van-e megadva, ha meg van adva; vagy Windows, ha alapértelmezés szerint nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="88fd2-160">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-161">-Hely</span><span class="sxs-lookup"><span data-stu-id="88fd2-161">-Location</span></span>
<span data-ttu-id="88fd2-162">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88fd2-162">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-163">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88fd2-163">-Name</span></span>
<span data-ttu-id="88fd2-164">A VM-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="88fd2-164">The name of the VM resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-165">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="88fd2-165">-OpenPorts</span></span>
<span data-ttu-id="88fd2-166">A létrehozott VM-es hálózati biztonsági csoport (NSG) azon portjainak listája, amelyeket meg szeretne nyitni.</span><span class="sxs-lookup"><span data-stu-id="88fd2-166">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="88fd2-167">Az alapértelmezett érték a választott kép típusától függ (azaz Windows: 3389, 5985 és Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="88fd2-167">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-168">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="88fd2-168">-PublicIpAddressName</span></span>
<span data-ttu-id="88fd2-169">A létrehozott VM új (vagy meglévő) nyilvános IP-címének neve.</span><span class="sxs-lookup"><span data-stu-id="88fd2-169">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="88fd2-170">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="88fd2-170">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88fd2-171">-ResourceGroupName</span></span>
<span data-ttu-id="88fd2-172">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88fd2-172">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-173">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="88fd2-173">-SecurityGroupName</span></span>
<span data-ttu-id="88fd2-174">A létrehozott VM új (vagy meglévő) hálózati biztonsági csoportja (NSG) neve.</span><span class="sxs-lookup"><span data-stu-id="88fd2-174">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="88fd2-175">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="88fd2-175">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-176">-Méret</span><span class="sxs-lookup"><span data-stu-id="88fd2-176">-Size</span></span>
<span data-ttu-id="88fd2-177">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="88fd2-177">The Virtual Machine Size.</span></span>  <span data-ttu-id="88fd2-178">Az alapértelmezett érték a következő: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="88fd2-178">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-179">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="88fd2-179">-SubnetAddressPrefix</span></span>
<span data-ttu-id="88fd2-180">Annak az alhálózatnak a cím előtagja, amelyet a VM-hez fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="88fd2-180">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="88fd2-181">-SubnetName</span></span>
<span data-ttu-id="88fd2-182">A létrehozott VM új (vagy meglévő) alhálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="88fd2-182">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="88fd2-183">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="88fd2-183">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-184">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="88fd2-184">-SystemAssignedIdentity</span></span>
<span data-ttu-id="88fd2-185">Ha a paraméter létezik, akkor a VM a felügyelt rendszeridentitást rendeli hozzá az automatikusan generált adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="88fd2-185">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-186">-Címke</span><span class="sxs-lookup"><span data-stu-id="88fd2-186">-Tag</span></span>
<span data-ttu-id="88fd2-187">Itt adhatja meg, hogy az erőforrások és az erőforráscsoportok a name-Value pairek halmazával legyenek címkézve.</span><span class="sxs-lookup"><span data-stu-id="88fd2-187">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="88fd2-188">Ha címkéket ad az erőforrásokhoz, az erőforrásokat csoportosíthatja az erőforráscsoportok között, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="88fd2-188">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="88fd2-189">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkét tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="88fd2-189">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-190">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="88fd2-190">-UserAssignedIdentity</span></span>
<span data-ttu-id="88fd2-191">Annak a felügyelt szolgáltatás-identitásnak a neve, amelyet a VM-nek el kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="88fd2-191">The name of a managed service identity that should be assigned to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-192">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="88fd2-192">-VirtualNetworkName</span></span>
<span data-ttu-id="88fd2-193">A létrehozott VM új (vagy meglévő) virtuális hálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="88fd2-193">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="88fd2-194">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="88fd2-194">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-195">-VM</span><span class="sxs-lookup"><span data-stu-id="88fd2-195">-VM</span></span>
<span data-ttu-id="88fd2-196">A létrehozandó helyi virtuális gépet adja meg.</span><span class="sxs-lookup"><span data-stu-id="88fd2-196">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="88fd2-197">A virtuálisgép-objektum beolvasásához használja az New-AzureRmVMConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="88fd2-197">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="88fd2-198">Más parancsmagok segítségével konfigurálhatja a virtuális gépet, például set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage és add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="88fd2-198">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-199">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="88fd2-199">-Zone</span></span>
<span data-ttu-id="88fd2-200">A virtuális gép zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88fd2-200">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-201">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88fd2-201">-Confirm</span></span>
<span data-ttu-id="88fd2-202">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88fd2-202">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88fd2-203">-WhatIf</span></span>
<span data-ttu-id="88fd2-204">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88fd2-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88fd2-205">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88fd2-205">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fd2-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88fd2-206">CommonParameters</span></span>
<span data-ttu-id="88fd2-207">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88fd2-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88fd2-208">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88fd2-208">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88fd2-209">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88fd2-209">INPUTS</span></span>

### <span data-ttu-id="88fd2-210">System. String</span><span class="sxs-lookup"><span data-stu-id="88fd2-210">System.String</span></span>

### <span data-ttu-id="88fd2-211">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="88fd2-211">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="88fd2-212">System. string []</span><span class="sxs-lookup"><span data-stu-id="88fd2-212">System.String[]</span></span>

### <span data-ttu-id="88fd2-213">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="88fd2-213">System.Collections.Hashtable</span></span>

## <span data-ttu-id="88fd2-214">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88fd2-214">OUTPUTS</span></span>

### <span data-ttu-id="88fd2-215">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="88fd2-215">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="88fd2-216">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="88fd2-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="88fd2-217">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88fd2-217">NOTES</span></span>

## <span data-ttu-id="88fd2-218">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88fd2-218">RELATED LINKS</span></span>

[<span data-ttu-id="88fd2-219">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88fd2-219">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="88fd2-220">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88fd2-220">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="88fd2-221">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88fd2-221">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="88fd2-222">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88fd2-222">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="88fd2-223">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88fd2-223">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="88fd2-224">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88fd2-224">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="88fd2-225">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="88fd2-225">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="88fd2-226">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="88fd2-226">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="88fd2-227">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="88fd2-227">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="88fd2-228">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="88fd2-228">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="88fd2-229">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="88fd2-229">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="88fd2-230">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="88fd2-230">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


