---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 52bc6e2c8dc2ddda1fbeb0e2c6a1be802df5dd46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194119"
---
# <span data-ttu-id="46c83-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="46c83-101">New-AzVM</span></span>

## <span data-ttu-id="46c83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46c83-102">SYNOPSIS</span></span>
<span data-ttu-id="46c83-103">Virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="46c83-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="46c83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46c83-104">SYNTAX</span></span>

### <span data-ttu-id="46c83-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46c83-105">SimpleParameterSet (Default)</span></span>
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

### <span data-ttu-id="46c83-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="46c83-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46c83-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="46c83-107">DiskFileParameterSet</span></span>
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

## <span data-ttu-id="46c83-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="46c83-108">DESCRIPTION</span></span>
<span data-ttu-id="46c83-109">A **New-AzVM** parancsmag létrehoz egy virtuális gépet az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="46c83-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="46c83-110">Ez a parancsmag a virtuális gép objektumát bemenetként veszi át.</span><span class="sxs-lookup"><span data-stu-id="46c83-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="46c83-111">A New-AzVMConfig parancsmag segítségével hozzon létre egy virtuálisgép-objektumot.</span><span class="sxs-lookup"><span data-stu-id="46c83-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="46c83-112">Más parancsmagok segítségével konfigurálhatja a virtuális gépet, például set-AzVMOperatingSystem, set-AzVMSourceImage, add-AzVMNetworkInterface és set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="46c83-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="46c83-113">A `SimpleParameterSet` VM létrehozásának kényelmes módja, ha a virtuális VM-létrehozási argumentumokat nem kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="46c83-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="46c83-114">Példák</span><span class="sxs-lookup"><span data-stu-id="46c83-114">EXAMPLES</span></span>

### <span data-ttu-id="46c83-115">Példa 1: virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="46c83-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="46c83-116">Ebben a példában a parancsfájl bemutatja, hogy miként hozhat létre virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="46c83-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="46c83-117">A parancsfájl a virtuális gép felhasználónevét és jelszavát fogja kérni.</span><span class="sxs-lookup"><span data-stu-id="46c83-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="46c83-118">Ez a parancsfájl számos más parancsmagot használ.</span><span class="sxs-lookup"><span data-stu-id="46c83-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="46c83-119">2. példa: virtuális gép létrehozása egyéni felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="46c83-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="46c83-120">Ez a példa egy meglévő sys-prepped, általános egyéni operációs rendszer lemezképet hoz létre, és egy adatlemezt csatol hozzá, kiépít egy új hálózatot, telepíti a virtuális merevlemezt, és futtatja azt.</span><span class="sxs-lookup"><span data-stu-id="46c83-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="46c83-121">Ez a parancsfájl automatikusan használható a kikészítéshez, mert a helyi virtuális gép rendszergazdai hitelesítő adatait használja a felhasználói interakciót igénylő " **Get-hitelesítőadat** " helyett.</span><span class="sxs-lookup"><span data-stu-id="46c83-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="46c83-122">Ez a parancsfájl feltételezi, hogy már bejelentkezett az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="46c83-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="46c83-123">Bejelentkezési állapotát a **Get-AzSubscription** parancsmag használatával ellenőrizheti.</span><span class="sxs-lookup"><span data-stu-id="46c83-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="46c83-124">3. példa: virtuális VM-fájl létrehozása nyilvános IP nélküli piactérről</span><span class="sxs-lookup"><span data-stu-id="46c83-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

<span data-ttu-id="46c83-125">Ez a példa egy új hálózatot hoz létre, és egy nyilvános IP-cím vagy hálózati biztonsági csoport létrehozása nélkül telepíti a Windows VM-et a Piactérről.</span><span class="sxs-lookup"><span data-stu-id="46c83-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="46c83-126">Ez a parancsfájl automatikusan használható a kikészítéshez, mert a helyi virtuális gép rendszergazdai hitelesítő adatait használja a felhasználói interakciót igénylő " **Get-hitelesítőadat** " helyett.</span><span class="sxs-lookup"><span data-stu-id="46c83-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="46c83-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46c83-127">PARAMETERS</span></span>

### <span data-ttu-id="46c83-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="46c83-128">-AddressPrefix</span></span>
<span data-ttu-id="46c83-129">A virtuális hálózathoz tartozó cím előtagja, amelyet a VM rendszerhez hoz létre.</span><span class="sxs-lookup"><span data-stu-id="46c83-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="46c83-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="46c83-130">-AllocationMethod</span></span>
<span data-ttu-id="46c83-131">A VM rendszerhez létrehozott nyilvános IP-cím IP-kiosztási módja.</span><span class="sxs-lookup"><span data-stu-id="46c83-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="46c83-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46c83-132">-AsJob</span></span>
<span data-ttu-id="46c83-133">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="46c83-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="46c83-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="46c83-134">-AvailabilitySetName</span></span>
<span data-ttu-id="46c83-135">Az elérhetőségi halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46c83-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="46c83-136">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="46c83-136">-Credential</span></span>
<span data-ttu-id="46c83-137">A VM rendszergazdai hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="46c83-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="46c83-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="46c83-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="46c83-139">Az adatlemezek méretét adja meg GB-ban.</span><span class="sxs-lookup"><span data-stu-id="46c83-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="46c83-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c83-140">-DefaultProfile</span></span>
<span data-ttu-id="46c83-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46c83-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46c83-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="46c83-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="46c83-143">Jelzi, hogy ez a parancsmag nem telepíti a **BG információs** bővítményt a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="46c83-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="46c83-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="46c83-144">-DiskFile</span></span>
<span data-ttu-id="46c83-145">A virtuális merevlemez-fájl helyi elérési útja, amelyet fel kell tölteni a felhőbe, és létre kell hoznia a VM-et, és az utótagnak ". vhd"-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="46c83-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="46c83-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="46c83-146">-DomainNameLabel</span></span>
<span data-ttu-id="46c83-147">A VM teljes tartománynevét (FQDN) tartalmazó aldomain címkéje.</span><span class="sxs-lookup"><span data-stu-id="46c83-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="46c83-148">Ez az űrlapon fog szerepelni `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="46c83-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="46c83-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="46c83-149">-EnableUltraSSD</span></span>
<span data-ttu-id="46c83-150">UltraSSD-lemezek használata a VM-hez.</span><span class="sxs-lookup"><span data-stu-id="46c83-150">Use UltraSSD disks for the vm.</span></span>

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

### <span data-ttu-id="46c83-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="46c83-151">-EvictionPolicy</span></span>
<span data-ttu-id="46c83-152">Az Azure spot Virtual Machine kilakoltatási házirendje.</span><span class="sxs-lookup"><span data-stu-id="46c83-152">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="46c83-153">A támogatott értékek "kifoglalás" és "Törlés".</span><span class="sxs-lookup"><span data-stu-id="46c83-153">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="46c83-154">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="46c83-154">-HostGroupId</span></span>
<span data-ttu-id="46c83-155">A virtuális gép által a dedikált szolgáltató csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="46c83-155">Specifies the dedicated host group the virtual machine will reside in.</span></span>

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

### <span data-ttu-id="46c83-156">-Állomásazonosító</span><span class="sxs-lookup"><span data-stu-id="46c83-156">-HostId</span></span>
<span data-ttu-id="46c83-157">Az állomás azonosítója</span><span class="sxs-lookup"><span data-stu-id="46c83-157">The Id of Host</span></span>

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

### <span data-ttu-id="46c83-158">-Kép</span><span class="sxs-lookup"><span data-stu-id="46c83-158">-Image</span></span>
<span data-ttu-id="46c83-159">Az a felhasználóbarát kép neve, amelyen a VM épül.</span><span class="sxs-lookup"><span data-stu-id="46c83-159">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="46c83-160">Ezek a következők: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-LEAP, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="46c83-160">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="46c83-161">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="46c83-161">-LicenseType</span></span>
<span data-ttu-id="46c83-162">A licenc típusát adja meg, amely azt jelzi, hogy a virtuális gép képe vagy lemeze engedélyezett a helyszíni verzióban.</span><span class="sxs-lookup"><span data-stu-id="46c83-162">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="46c83-163">Ezt az értéket csak a Windows Server operációs rendszert tartalmazó képek esetén használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="46c83-163">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="46c83-164">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="46c83-164">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46c83-165">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="46c83-165">Windows_Client</span></span>
- <span data-ttu-id="46c83-166">Windows_Server ez az érték nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="46c83-166">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="46c83-167">Ha ezt a paramétert a frissítéshez adja meg, az értéknek meg kell egyeznie a virtuális gép kezdeti értékével.</span><span class="sxs-lookup"><span data-stu-id="46c83-167">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="46c83-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="46c83-168">-Linux</span></span>
<span data-ttu-id="46c83-169">Azt jelzi, hogy a lemezmeghajtó a Linux VM-re van-e megadva, ha meg van adva; vagy Windows, ha alapértelmezés szerint nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="46c83-169">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="46c83-170">-Hely</span><span class="sxs-lookup"><span data-stu-id="46c83-170">-Location</span></span>
<span data-ttu-id="46c83-171">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46c83-171">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="46c83-172">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="46c83-172">-MaxPrice</span></span>
<span data-ttu-id="46c83-173">Az alacsony prioritású virtuális gép számlázásának maximális ára.</span><span class="sxs-lookup"><span data-stu-id="46c83-173">The max price of the billing of a low priority virtual machine.</span></span>

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

### <span data-ttu-id="46c83-174">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="46c83-174">-EncryptionAtHost</span></span>
<span data-ttu-id="46c83-175">A EncryptionAtHost tulajdonságot a felhasználó használhatja fel a virtuális gép vagy a virtuálisgép-készlet adatkészlet-titkosításának engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="46c83-175">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="46c83-176">Ezzel engedélyezi az összes lemez titkosítását, például az erőforrás/Temp diskt az állomáson.</span><span class="sxs-lookup"><span data-stu-id="46c83-176">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="46c83-177">Alapértelmezés: az állomáson a titkosítás le lesz tiltva, kivéve ha a tulajdonság értéke igaz az erőforrás esetében.</span><span class="sxs-lookup"><span data-stu-id="46c83-177">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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


### <span data-ttu-id="46c83-178">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46c83-178">-Name</span></span>
<span data-ttu-id="46c83-179">A VM-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="46c83-179">The name of the VM resource.</span></span>

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

### <span data-ttu-id="46c83-180">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="46c83-180">-OpenPorts</span></span>
<span data-ttu-id="46c83-181">A létrehozott VM-es hálózati biztonsági csoport (NSG) azon portjainak listája, amelyeket meg szeretne nyitni.</span><span class="sxs-lookup"><span data-stu-id="46c83-181">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="46c83-182">Az alapértelmezett érték a választott kép típusától függ (azaz Windows: 3389, 5985 és Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="46c83-182">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="46c83-183">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="46c83-183">-Priority</span></span>
<span data-ttu-id="46c83-184">A virtuális gép prioritása.</span><span class="sxs-lookup"><span data-stu-id="46c83-184">The priority for the virtual machine.</span></span>  <span data-ttu-id="46c83-185">Csak a támogatott értékek "normál", "spot" és "Low".</span><span class="sxs-lookup"><span data-stu-id="46c83-185">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="46c83-186">"Normál": a normál virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="46c83-186">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="46c83-187">A "spot" a direkt virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="46c83-187">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="46c83-188">Az "alacsony" a direkt virtuális gép is, de a helyére "spot" lép.</span><span class="sxs-lookup"><span data-stu-id="46c83-188">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="46c83-189">Kérjük, hogy az "alacsony" helyett a "spot" értéket használja.</span><span class="sxs-lookup"><span data-stu-id="46c83-189">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="46c83-190">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="46c83-190">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="46c83-191">Az ezzel a virtuális géppel használható közelségi hely csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="46c83-191">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="46c83-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="46c83-192">-PublicIpAddressName</span></span>
<span data-ttu-id="46c83-193">A létrehozott VM új (vagy meglévő) nyilvános IP-címének neve.</span><span class="sxs-lookup"><span data-stu-id="46c83-193">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="46c83-194">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="46c83-194">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="46c83-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46c83-195">-ResourceGroupName</span></span>
<span data-ttu-id="46c83-196">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46c83-196">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="46c83-197">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="46c83-197">-SecurityGroupName</span></span>
<span data-ttu-id="46c83-198">A létrehozott VM új (vagy meglévő) hálózati biztonsági csoportja (NSG) neve.</span><span class="sxs-lookup"><span data-stu-id="46c83-198">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="46c83-199">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="46c83-199">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="46c83-200">-Méret</span><span class="sxs-lookup"><span data-stu-id="46c83-200">-Size</span></span>
<span data-ttu-id="46c83-201">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="46c83-201">The Virtual Machine Size.</span></span>  <span data-ttu-id="46c83-202">Az alapértelmezett érték a következő: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="46c83-202">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="46c83-203">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="46c83-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="46c83-204">Annak az alhálózatnak a cím előtagja, amelyet a VM-hez fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="46c83-204">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="46c83-205">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="46c83-205">-SubnetName</span></span>
<span data-ttu-id="46c83-206">A létrehozott VM új (vagy meglévő) alhálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="46c83-206">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="46c83-207">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="46c83-207">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="46c83-208">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="46c83-208">-SystemAssignedIdentity</span></span>
<span data-ttu-id="46c83-209">Ha a paraméter létezik, akkor a VM a felügyelt rendszeridentitást rendeli hozzá az automatikusan generált adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="46c83-209">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="46c83-210">-Címke</span><span class="sxs-lookup"><span data-stu-id="46c83-210">-Tag</span></span>
<span data-ttu-id="46c83-211">Itt adhatja meg, hogy az erőforrások és az erőforráscsoportok a name-Value pairek halmazával legyenek címkézve.</span><span class="sxs-lookup"><span data-stu-id="46c83-211">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="46c83-212">Ha címkéket ad az erőforrásokhoz, az erőforrásokat csoportosíthatja az erőforráscsoportok között, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="46c83-212">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="46c83-213">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkét tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="46c83-213">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="46c83-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="46c83-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="46c83-215">Annak a felügyelt szolgáltatás-identitásnak a neve, amelyet a VM-nek el kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="46c83-215">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="46c83-216">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="46c83-216">-VirtualNetworkName</span></span>
<span data-ttu-id="46c83-217">A létrehozott VM új (vagy meglévő) virtuális hálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="46c83-217">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="46c83-218">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="46c83-218">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="46c83-219">-VM</span><span class="sxs-lookup"><span data-stu-id="46c83-219">-VM</span></span>
<span data-ttu-id="46c83-220">A létrehozandó helyi virtuális gépet adja meg.</span><span class="sxs-lookup"><span data-stu-id="46c83-220">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="46c83-221">A virtuálisgép-objektum beolvasásához használja az New-AzVMConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="46c83-221">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="46c83-222">Más parancsmagok segítségével konfigurálhatja a virtuális gépet, például set-AzVMOperatingSystem, set-AzVMSourceImage és add-AzVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="46c83-222">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="46c83-223">-VmssId</span><span class="sxs-lookup"><span data-stu-id="46c83-223">-VmssId</span></span>
<span data-ttu-id="46c83-224">Annak a virtuálisgép-készletnek az azonosítója, amelyhez a virtuális gép társítva van</span><span class="sxs-lookup"><span data-stu-id="46c83-224">The ID of Virtual Machine Scale Set that this VM will be associated with</span></span>

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

### <span data-ttu-id="46c83-225">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="46c83-225">-Zone</span></span>
<span data-ttu-id="46c83-226">A virtuális gép zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="46c83-226">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="46c83-227">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46c83-227">-Confirm</span></span>
<span data-ttu-id="46c83-228">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46c83-228">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c83-229">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c83-229">-WhatIf</span></span>
<span data-ttu-id="46c83-230">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46c83-230">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46c83-231">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46c83-231">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c83-232">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c83-232">CommonParameters</span></span>
<span data-ttu-id="46c83-233">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46c83-233">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c83-234">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="46c83-234">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c83-235">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46c83-235">INPUTS</span></span>

### <span data-ttu-id="46c83-236">System. String</span><span class="sxs-lookup"><span data-stu-id="46c83-236">System.String</span></span>

### <span data-ttu-id="46c83-237">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="46c83-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="46c83-238">System. string []</span><span class="sxs-lookup"><span data-stu-id="46c83-238">System.String[]</span></span>

### <span data-ttu-id="46c83-239">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="46c83-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="46c83-240">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46c83-240">OUTPUTS</span></span>

### <span data-ttu-id="46c83-241">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="46c83-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="46c83-242">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="46c83-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="46c83-243">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46c83-243">NOTES</span></span>

## <span data-ttu-id="46c83-244">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46c83-244">RELATED LINKS</span></span>

[<span data-ttu-id="46c83-245">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="46c83-245">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="46c83-246">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="46c83-246">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="46c83-247">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="46c83-247">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="46c83-248">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="46c83-248">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="46c83-249">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="46c83-249">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="46c83-250">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="46c83-250">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="46c83-251">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="46c83-251">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="46c83-252">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="46c83-252">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="46c83-253">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="46c83-253">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="46c83-254">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="46c83-254">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="46c83-255">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="46c83-255">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="46c83-256">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="46c83-256">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)

