---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 21c15b0395479a1a22e6b8420a97a3a7c0b75bce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480815"
---
# <span data-ttu-id="b6dd2-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6dd2-101">New-AzVM</span></span>

## <span data-ttu-id="b6dd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6dd2-103">Virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="b6dd2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b6dd2-104">SYNTAX</span></span>

### <span data-ttu-id="b6dd2-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6dd2-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>]
 [-HostId <String>] [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6dd2-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6dd2-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6dd2-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6dd2-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6dd2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b6dd2-108">DESCRIPTION</span></span>
<span data-ttu-id="b6dd2-109">A **New-AzVM parancsmag** létrehoz egy virtuális gépet az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="b6dd2-110">Ez a parancsmag bemenetként virtuális gépi objektumot vesz fel.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="b6dd2-111">Virtuális New-AzVMConfig létrehozásához használja a New-AzVMConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="b6dd2-112">A virtuális gép konfigurálhat más parancsmagokat is, például a Set-AzVMOperatingSystem, a Set-AzVMSourceImage, az Add-AzVMNetworkInterface és a Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="b6dd2-113">Ez a módszer kényelmes módszert biztosít a VM létrehozásához azáltal, hogy a `SimpleParameterSet` vm létrehozásának gyakori argumentumait opcionálisra teszi.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="b6dd2-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b6dd2-114">EXAMPLES</span></span>

### <span data-ttu-id="b6dd2-115">1. példa: Virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="b6dd2-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm -Credential (Get-Credential)

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

<span data-ttu-id="b6dd2-116">Az alábbi példa parancsprogram bemutatja, hogy miként hozhat létre virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="b6dd2-117">A parancsfájl kérni fogja a virtuális gép felhasználónevét és jelszavát.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="b6dd2-118">Ez a parancsprogram számos más parancsmagot használ.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="b6dd2-119">2. példa: Virtuális gép létrehozása egyéni felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="b6dd2-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="b6dd2-120">Ez a példa egy meglévő, sys prepped, generalized custom operating system image fájlt vesz fel, és csatol hozzá egy adatlemezt, kirendel egy új hálózatot, telepíti a VHD-t, és futtatja azt.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="b6dd2-121">Ez a parancsfájl használható az automatikus kiépítéshez, mivel a helyi virtuális gép rendszergazdájának hitelesítő adatait használja a szövegben ahelyett, hogy felhasználói beavatkozást igénylő **Get-Credentialt** hív meg.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="b6dd2-122">Ez a parancsfájl abból indul ki, hogy Már be van jelentkezve az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="b6dd2-123">A bejelentkezési állapotát a **Get-AzSubscription** parancsmag használatával tudja megerősíteni.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="b6dd2-124">3. példa: Virtuális gép létrehozása nyilvános IP-cím nélküli piactéri képből</span><span class="sxs-lookup"><span data-stu-id="b6dd2-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="b6dd2-125">Ebben a példában egy új hálózatot hoz létre, és nyilvános IP-cím vagy hálózati biztonsági csoport létrehozása nélkül telepíti a Windows VM-et a Piactérről.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="b6dd2-126">Ez a parancsfájl használható az automatikus kiépítéshez, mivel a helyi virtuális gép rendszergazdájának hitelesítő adatait használja a szövegben ahelyett, hogy felhasználói beavatkozást igénylő **Get-Credentialt** hív meg.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="b6dd2-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6dd2-127">PARAMETERS</span></span>

### <span data-ttu-id="b6dd2-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b6dd2-128">-AddressPrefix</span></span>
<span data-ttu-id="b6dd2-129">A virtuális hálózat címelőtagja, amely a VM-hez fog létrejönni.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="b6dd2-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="b6dd2-130">-AllocationMethod</span></span>
<span data-ttu-id="b6dd2-131">A virtuális géphez létrehozva a nyilvános IP-cím IP-kiosztási módszere.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="b6dd2-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6dd2-132">-AsJob</span></span>
<span data-ttu-id="b6dd2-133">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b6dd2-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="b6dd2-134">-AvailabilitySetName</span></span>
<span data-ttu-id="b6dd2-135">Megadja az elérhetőségi készlet nevét.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="b6dd2-136">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="b6dd2-136">-Credential</span></span>
<span data-ttu-id="b6dd2-137">A virtuális gép rendszergazdai hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="b6dd2-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="b6dd2-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="b6dd2-139">Az adatlemezek mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="b6dd2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6dd2-140">-DefaultProfile</span></span>
<span data-ttu-id="b6dd2-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6dd2-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="b6dd2-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="b6dd2-143">Azt jelzi, hogy ez a parancsmag nem telepíti a **BG-információ** bővítményt a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="b6dd2-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="b6dd2-144">-DiskFile</span></span>
<span data-ttu-id="b6dd2-145">A virtuális merevlemez-fájl felhőbe való feltöltésére és a virtuális gép létrehozására használt helyi elérési út, utótagja pedig a ".vhd" lehet.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="b6dd2-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="b6dd2-146">-DomainNameLabel</span></span>
<span data-ttu-id="b6dd2-147">A VM teljes tartománynevének (FQDN) altartománycímkéje.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="b6dd2-148">Ez az űrlap `{domainNameLabel}.{location}.cloudapp.azure.com` lesz.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="b6dd2-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="b6dd2-149">-EnableUltraSSD</span></span>
<span data-ttu-id="b6dd2-150">A vmhez használjon UltraSSD-lemezeket.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-150">Use UltraSSD disks for the vm.</span></span>

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

### <span data-ttu-id="b6dd2-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6dd2-151">-EvictionPolicy</span></span>
<span data-ttu-id="b6dd2-152">Az Azure Spot virtuális gépre vonatkozó kilakoltatási házirend.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-152">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="b6dd2-153">A támogatott értékek a "Deallocate" és a "Delete".</span><span class="sxs-lookup"><span data-stu-id="b6dd2-153">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="b6dd2-154">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="b6dd2-154">-HostGroupId</span></span>
<span data-ttu-id="b6dd2-155">Megadja azt a dedikált állomáscsoportot, ahol a virtuális gép található.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-155">Specifies the dedicated host group the virtual machine will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6dd2-156">-HostId</span><span class="sxs-lookup"><span data-stu-id="b6dd2-156">-HostId</span></span>
<span data-ttu-id="b6dd2-157">A host azonosítója</span><span class="sxs-lookup"><span data-stu-id="b6dd2-157">The Id of Host</span></span>

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

### <span data-ttu-id="b6dd2-158">-Image</span><span class="sxs-lookup"><span data-stu-id="b6dd2-158">-Image</span></span>
<span data-ttu-id="b6dd2-159">A rövid kép neve, amelyre a VM épülni fog.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-159">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="b6dd2-160">Ezek közé tartoznak a következők: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Ubuntu, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-160">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="b6dd2-161">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b6dd2-161">-LicenseType</span></span>
<span data-ttu-id="b6dd2-162">Egy licenctípust ad meg, amely azt jelzi, hogy a virtuális gép lemezképe vagy lemeze a helyszínen lett licenccel.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-162">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="b6dd2-163">A Windows Server lehetséges értékei:</span><span class="sxs-lookup"><span data-stu-id="b6dd2-163">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="b6dd2-164">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="b6dd2-164">Windows_Client</span></span>
- <span data-ttu-id="b6dd2-165">Windows_Server Linux Server operációs rendszer lehetséges értékei:</span><span class="sxs-lookup"><span data-stu-id="b6dd2-165">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="b6dd2-166">RHEL_BYOS (RHEL)</span><span class="sxs-lookup"><span data-stu-id="b6dd2-166">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="b6dd2-167">SLES_BYOS (SUSE)</span><span class="sxs-lookup"><span data-stu-id="b6dd2-167">SLES_BYOS (for SUSE)</span></span> 

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

### <span data-ttu-id="b6dd2-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="b6dd2-168">-Linux</span></span>
<span data-ttu-id="b6dd2-169">Azt jelzi, hogy a lemezfájl Linux VM-re van-e adva, ha meg van adva; vagy a Windowst, ha az alapértelmezés szerint nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-169">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="b6dd2-170">-Location</span><span class="sxs-lookup"><span data-stu-id="b6dd2-170">-Location</span></span>
<span data-ttu-id="b6dd2-171">Megadja a virtuális gép helyét.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-171">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="b6dd2-172">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="b6dd2-172">-MaxPrice</span></span>
<span data-ttu-id="b6dd2-173">Az alacsony prioritású virtuális gép számlázásának maximális ára.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-173">The max price of the billing of a low priority virtual machine.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6dd2-174">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="b6dd2-174">-EncryptionAtHost</span></span>
<span data-ttu-id="b6dd2-175">A EncryptionAtHost tulajdonságot a felhasználó használhatja a kérésben a gazdatitkosítás engedélyezéséhez vagy letiltásához a virtuális gép vagy virtuális gép méretarányának beállítására.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-175">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="b6dd2-176">Ez lehetővé teszi a titkosítást az összes lemezen, beleértve magában az erőforrás-/ideiglenes lemezen is.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-176">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="b6dd2-177">Alapértelmezett: A gazdaszámítógép titkosítása le lesz tiltva, hacsak ez a tulajdonság nincs igazra állítva az erőforrásra nézve.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-177">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskParameterSet
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="b6dd2-178">-Name</span><span class="sxs-lookup"><span data-stu-id="b6dd2-178">-Name</span></span>
<span data-ttu-id="b6dd2-179">A VM-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-179">The name of the VM resource.</span></span>

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

### <span data-ttu-id="b6dd2-180">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="b6dd2-180">-OpenPorts</span></span>
<span data-ttu-id="b6dd2-181">A létrehozott virtuális gép hálózati biztonsági csoportjában (NSG) megnyílik a portok listája.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-181">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="b6dd2-182">Az alapértelmezett érték a kiválasztott kép típusától függ (Windows: 3389, 5985 és Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="b6dd2-182">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="b6dd2-183">-Priority</span><span class="sxs-lookup"><span data-stu-id="b6dd2-183">-Priority</span></span>
<span data-ttu-id="b6dd2-184">A virtuális gép prioritása.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-184">The priority for the virtual machine.</span></span>  <span data-ttu-id="b6dd2-185">Csak a "Normál", a "Direkt" és a "Gyenge" érték támogatott.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-185">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="b6dd2-186">A "Regular" normál virtuális géphez való.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-186">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="b6dd2-187">A "Spot" a direkt virtuális gépekhez való.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-187">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="b6dd2-188">A "Low" a direkt virtuális gépre is igaz, de a "Spot" (Direkt) szövegre cseréli.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-188">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="b6dd2-189">A "Gyenge" helyett használja a "Spot" (Direkt) használhatja.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-189">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="b6dd2-190">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="b6dd2-190">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="b6dd2-191">Az ezzel a virtuális géppel használható Közelség elhelyezési csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-191">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6dd2-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="b6dd2-192">-PublicIpAddressName</span></span>
<span data-ttu-id="b6dd2-193">A létrehozott virtuális gép által használt új (vagy meglévő) nyilvános IP-cím neve.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-193">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="b6dd2-194">Ha nincs megadva, a program létrehoz egy nevet.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-194">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="b6dd2-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6dd2-195">-ResourceGroupName</span></span>
<span data-ttu-id="b6dd2-196">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-196">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b6dd2-197">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="b6dd2-197">-SecurityGroupName</span></span>
<span data-ttu-id="b6dd2-198">A létrehozott virtuális gép által használt új (vagy meglévő) hálózati biztonsági csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-198">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="b6dd2-199">Ha nincs megadva, a program létrehoz egy nevet.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-199">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="b6dd2-200">-Size</span><span class="sxs-lookup"><span data-stu-id="b6dd2-200">-Size</span></span>
<span data-ttu-id="b6dd2-201">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-201">The Virtual Machine Size.</span></span>  <span data-ttu-id="b6dd2-202">Az alapértelmezett érték a következő: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-202">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="b6dd2-203">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b6dd2-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="b6dd2-204">Az alhálózat címelőtagja, amely a VM-hez fog létrejönni.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-204">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="b6dd2-205">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b6dd2-205">-SubnetName</span></span>
<span data-ttu-id="b6dd2-206">A létrehozott virtuális gép által használt új (vagy meglévő) alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-206">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="b6dd2-207">Ha nincs megadva, a program létrehoz egy nevet.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-207">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="b6dd2-208">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b6dd2-208">-SystemAssignedIdentity</span></span>
<span data-ttu-id="b6dd2-209">Ha a paraméter jelen van, akkor a VM-hez egy automatikusan létrehozott felügyelt rendszer-identitás van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-209">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="b6dd2-210">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6dd2-210">-Tag</span></span>
<span data-ttu-id="b6dd2-211">Azt adja meg, hogy az erőforrások és az erőforráscsoportok névérték-párokkal címkézhatók.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-211">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="b6dd2-212">Ha címkéket ad az erőforrásokhoz, több erőforráscsoportban csoportosíthatók az erőforrások, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-212">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="b6dd2-213">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkével lehet.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-213">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="b6dd2-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b6dd2-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="b6dd2-215">Annak a felügyelt szolgáltatás-identitásnak a neve, amely a virtuális géphez van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-215">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="b6dd2-216">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b6dd2-216">-VirtualNetworkName</span></span>
<span data-ttu-id="b6dd2-217">A létrehozott virtuális gép által használt új (vagy meglévő) virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-217">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="b6dd2-218">Ha nincs megadva, a program létrehoz egy nevet.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-218">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="b6dd2-219">-VM</span><span class="sxs-lookup"><span data-stu-id="b6dd2-219">-VM</span></span>
<span data-ttu-id="b6dd2-220">Létrehoz egy helyi virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-220">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="b6dd2-221">Virtuális gépi objektum beszerzéséhez használja a New-AzVMConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-221">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="b6dd2-222">A virtuális gép konfigurálható más parancsmagokkal is, például a Set-AzVMOperatingSystem, a Set-AzVMSourceImage és az Add-AzVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-222">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="b6dd2-223">-VmssId</span><span class="sxs-lookup"><span data-stu-id="b6dd2-223">-VmssId</span></span>
<span data-ttu-id="b6dd2-224">A virtuális gép méretarány-készletének azonosítója, amelyhez a virtuális gép társítva lesz</span><span class="sxs-lookup"><span data-stu-id="b6dd2-224">The ID of Virtual Machine Scale Set that this VM will be associated with</span></span>

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

### <span data-ttu-id="b6dd2-225">-Zone</span><span class="sxs-lookup"><span data-stu-id="b6dd2-225">-Zone</span></span>
<span data-ttu-id="b6dd2-226">A virtuális gép zónalistát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-226">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="b6dd2-227">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6dd2-227">-Confirm</span></span>
<span data-ttu-id="b6dd2-228">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-228">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6dd2-229">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6dd2-229">-WhatIf</span></span>
<span data-ttu-id="b6dd2-230">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-230">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6dd2-231">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-231">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6dd2-232">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6dd2-232">CommonParameters</span></span>
<span data-ttu-id="b6dd2-233">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6dd2-233">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6dd2-234">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6dd2-234">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6dd2-235">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6dd2-235">INPUTS</span></span>

### <span data-ttu-id="b6dd2-236">System.String</span><span class="sxs-lookup"><span data-stu-id="b6dd2-236">System.String</span></span>

### <span data-ttu-id="b6dd2-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b6dd2-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b6dd2-238">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b6dd2-238">System.String[]</span></span>

### <span data-ttu-id="b6dd2-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6dd2-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b6dd2-240">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6dd2-240">OUTPUTS</span></span>

### <span data-ttu-id="b6dd2-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b6dd2-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="b6dd2-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b6dd2-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b6dd2-243">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b6dd2-243">NOTES</span></span>

## <span data-ttu-id="b6dd2-244">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6dd2-244">RELATED LINKS</span></span>

[<span data-ttu-id="b6dd2-245">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6dd2-245">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b6dd2-246">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6dd2-246">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b6dd2-247">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6dd2-247">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="b6dd2-248">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6dd2-248">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="b6dd2-249">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6dd2-249">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="b6dd2-250">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6dd2-250">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="b6dd2-251">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b6dd2-251">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="b6dd2-252">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b6dd2-252">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="b6dd2-253">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b6dd2-253">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="b6dd2-254">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b6dd2-254">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="b6dd2-255">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="b6dd2-255">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="b6dd2-256">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="b6dd2-256">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


