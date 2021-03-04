---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 07d71e8fa7cd5c19cfc6f4aab8d27e5c5758b41c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942697"
---
# <span data-ttu-id="db6b9-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="db6b9-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="db6b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="db6b9-103">Beállítja az operációs rendszer lemeztulajdonságokat egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="db6b9-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="db6b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db6b9-104">SYNTAX</span></span>

### <span data-ttu-id="db6b9-105">DefaultParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db6b9-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db6b9-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="db6b9-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db6b9-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="db6b9-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db6b9-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="db6b9-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db6b9-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="db6b9-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db6b9-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db6b9-110">DESCRIPTION</span></span>
<span data-ttu-id="db6b9-111">A **Set-AzVMOSDisk** parancsmag beállítja az operációs rendszer lemeztulajdonságokat egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="db6b9-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="db6b9-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db6b9-112">EXAMPLES</span></span>

### <span data-ttu-id="db6b9-113">1. példa: Tulajdonságok beállítása virtuális gépen platformképről</span><span class="sxs-lookup"><span data-stu-id="db6b9-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="db6b9-114">Az első parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet13 nevű elérhetőségi halmazt kapja, majd az objektumot a $AvailabilitySet tárolja.</span><span class="sxs-lookup"><span data-stu-id="db6b9-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="db6b9-115">A második parancs létrehoz egy virtuális gépobjektumot, majd a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="db6b9-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="db6b9-116">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="db6b9-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="db6b9-117">A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="db6b9-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="db6b9-118">Az utolsó parancs beállítja a tulajdonságokat a virtuális gépen a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="db6b9-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="db6b9-119">2. példa: Tulajdonságokat állít be egy virtuális gépen általános felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="db6b9-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="db6b9-120">Az első parancs az Erőforráscsoport11 nevű erőforráscsoportBan az AvailabilitySet13 nevű elérhetőségi halmazt kapja, és az objektumot a $AvailabilitySet tárolja.</span><span class="sxs-lookup"><span data-stu-id="db6b9-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="db6b9-121">A második parancs létrehoz egy virtuális gépi objektumot, és azt a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="db6b9-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="db6b9-122">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="db6b9-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="db6b9-123">A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="db6b9-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="db6b9-124">Az utolsó parancs beállítja a tulajdonságokat a virtuális gépen a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="db6b9-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="db6b9-125">3. példa: Egy virtuális gép tulajdonságainak beállítása speciális felhasználói kép alapján</span><span class="sxs-lookup"><span data-stu-id="db6b9-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="db6b9-126">Az első parancs az Erőforráscsoport11 nevű erőforráscsoportBan az AvailabilitySet13 nevű elérhetőségi halmazt kapja, és az objektumot a $AvailabilitySet tárolja.</span><span class="sxs-lookup"><span data-stu-id="db6b9-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="db6b9-127">A második parancs létrehoz egy virtuális gépi objektumot, és azt a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="db6b9-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="db6b9-128">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="db6b9-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="db6b9-129">A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="db6b9-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="db6b9-130">Az utolsó parancs beállítja a tulajdonságokat a virtuális gépen a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="db6b9-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="db6b9-131">4. példa: A lemeztitkosítási beállítások megadása virtuális gép operációs rendszer lemezén</span><span class="sxs-lookup"><span data-stu-id="db6b9-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="db6b9-132">Ebben a példában egy virtuális gép operációs rendszer lemezén adhatja meg a lemeztitkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="db6b9-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="db6b9-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db6b9-133">PARAMETERS</span></span>

### <span data-ttu-id="db6b9-134">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="db6b9-134">-Caching</span></span>
<span data-ttu-id="db6b9-135">Az operációs rendszer lemezének gyorsítótárazása.</span><span class="sxs-lookup"><span data-stu-id="db6b9-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="db6b9-136">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="db6b9-136">Valid values are:</span></span> 
- <span data-ttu-id="db6b9-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="db6b9-137">ReadOnly</span></span>
- <span data-ttu-id="db6b9-138">ReadWrite The default value is ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="db6b9-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="db6b9-139">A gyorsítótárazás értékének módosítása esetén a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="db6b9-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="db6b9-140">Ez a beállítás befolyásolja a lemez teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="db6b9-140">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="db6b9-141">-CreateOption</span></span>
<span data-ttu-id="db6b9-142">Azt adja meg, hogy ez a parancsmag egy platformról vagy egy felhasználói képről hoz-e létre egy lemezt a virtuális gépben, vagy egy meglévő lemezt csatol.</span><span class="sxs-lookup"><span data-stu-id="db6b9-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="db6b9-143">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="db6b9-143">Valid values are:</span></span> 
- <span data-ttu-id="db6b9-144">Csatolás 2010.</span><span class="sxs-lookup"><span data-stu-id="db6b9-144">Attach.</span></span>
<span data-ttu-id="db6b9-145">Akkor válassza ezt a lehetőséget, ha egy speciális lemezről hoz létre virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="db6b9-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="db6b9-146">Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri paramétert.*</span><span class="sxs-lookup"><span data-stu-id="db6b9-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="db6b9-147">Ehelyett használja a Set-AzVMSourceImage parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="db6b9-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="db6b9-148">A *Windows* vagy *a Linux* paramétereit használva is meg kell mondania az Azure platformnak a VHD operációs rendszer típusát.</span><span class="sxs-lookup"><span data-stu-id="db6b9-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="db6b9-149">A *VhdUri* paraméter elég ahhoz, hogy meg tudja mondani az azure platformnak a csatolható lemez helyét.</span><span class="sxs-lookup"><span data-stu-id="db6b9-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="db6b9-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="db6b9-150">FromImage.</span></span>
<span data-ttu-id="db6b9-151">Ezzel a beállítással virtuális gépet hozhat létre platformképből vagy általánosított felhasználói képből.</span><span class="sxs-lookup"><span data-stu-id="db6b9-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="db6b9-152">Általánosított felhasználói lemezkép esetén a *SourceImageUri* paramétert és a *Windows* vagy *Linux* paramétereket is meg kell adnia ahhoz, hogy az Azure platformon a **Set-AzVMSourceImage** parancsmag használata helyett meg tudja mondani az operációs rendszer merevlemezének helyét és típusát.</span><span class="sxs-lookup"><span data-stu-id="db6b9-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="db6b9-153">Platformkép esetén a *VhdUri* paraméter elegendő.</span><span class="sxs-lookup"><span data-stu-id="db6b9-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="db6b9-154">Üres.</span><span class="sxs-lookup"><span data-stu-id="db6b9-154">Empty.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6b9-155">-DefaultProfile</span></span>
<span data-ttu-id="db6b9-156">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db6b9-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6b9-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="db6b9-157">-DiffDiskSetting</span></span>
<span data-ttu-id="db6b9-158">Az operációs rendszer lemezének eltérő lemezbeállításai.</span><span class="sxs-lookup"><span data-stu-id="db6b9-158">Specifies the differencing disk settings for operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="db6b9-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="db6b9-160">A lemeztitkosítási kulcs helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="db6b9-160">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="db6b9-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="db6b9-162">A lemeztitkosítási kulcsot tartalmazó kulcstár erőforrásazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6b9-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="db6b9-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="db6b9-164">Az ügyfél által felügyelt lemeztitkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6b9-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="db6b9-165">Ez csak felügyelt lemezhez lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="db6b9-165">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="db6b9-166">-DiskSizeInGB</span></span>
<span data-ttu-id="db6b9-167">Az operációs rendszer lemezének mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="db6b9-167">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="db6b9-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="db6b9-169">A kulcstitkosítási kulcs helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="db6b9-169">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="db6b9-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="db6b9-171">A kulcstitkosítási kulcsot tartalmazó kulcstár erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="db6b9-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="db6b9-172">-Linux</span></span>
<span data-ttu-id="db6b9-173">Azt jelzi, hogy a felhasználó képének operációs rendszere Linux.</span><span class="sxs-lookup"><span data-stu-id="db6b9-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="db6b9-174">Adja meg ezt a paramétert a felhasználói képalapú virtuális gép központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="db6b9-174">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="db6b9-175">-ManagedDiskId</span></span>
<span data-ttu-id="db6b9-176">Egy felügyelt lemez azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6b9-176">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-177">-Name</span><span class="sxs-lookup"><span data-stu-id="db6b9-177">-Name</span></span>
<span data-ttu-id="db6b9-178">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6b9-178">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="db6b9-179">-SourceImageUri</span></span>
<span data-ttu-id="db6b9-180">A VHD URI azonosítóját adja meg a felhasználói képek esetében.</span><span class="sxs-lookup"><span data-stu-id="db6b9-180">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="db6b9-181">-StorageAccountType</span></span>
<span data-ttu-id="db6b9-182">A felügyelt lemez tárfióktípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6b9-182">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="db6b9-183">-VhdUri</span></span>
<span data-ttu-id="db6b9-184">Egy virtuális merevlemez (VHD) egységes erőforrás-azonosítóját (URI) adja meg.</span><span class="sxs-lookup"><span data-stu-id="db6b9-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="db6b9-185">Képalapú virtuális gép esetén ez a paraméter azt a VHD-fájlt adja meg, amely platformkép vagy felhasználói kép megadása esetén hozható létre.</span><span class="sxs-lookup"><span data-stu-id="db6b9-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="db6b9-186">Ez az a hely, amelyből a rendszer a bináris nagy objektumot (BLOB) a virtuális gép indításaként másolja.</span><span class="sxs-lookup"><span data-stu-id="db6b9-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="db6b9-187">Lemezalapú virtuális gép rendszerindítási forgatókönyve esetén ez a paraméter azt a VHD-fájlt adja meg, amely a virtuális gép által közvetlenül az indításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="db6b9-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-188">-VM</span><span class="sxs-lookup"><span data-stu-id="db6b9-188">-VM</span></span>
<span data-ttu-id="db6b9-189">Megadja azt a helyi virtuális gépobjektumot, amelyen meg kell állítani az operációs rendszer lemeztulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="db6b9-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="db6b9-190">Virtuális gépi objektum beszerzéséhez használja a Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="db6b9-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="db6b9-191">-Windows</span></span>
<span data-ttu-id="db6b9-192">Azt jelzi, hogy a felhasználói képen a Windows operációs rendszer látható.</span><span class="sxs-lookup"><span data-stu-id="db6b9-192">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6b9-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="db6b9-193">-WriteAccelerator</span></span>
<span data-ttu-id="db6b9-194">Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e az operációs rendszer lemezén.</span><span class="sxs-lookup"><span data-stu-id="db6b9-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="db6b9-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6b9-195">CommonParameters</span></span>
<span data-ttu-id="db6b9-196">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6b9-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6b9-197">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db6b9-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6b9-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db6b9-198">INPUTS</span></span>

### <span data-ttu-id="db6b9-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="db6b9-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="db6b9-200">System.String</span><span class="sxs-lookup"><span data-stu-id="db6b9-200">System.String</span></span>

## <span data-ttu-id="db6b9-201">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db6b9-201">OUTPUTS</span></span>

### <span data-ttu-id="db6b9-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="db6b9-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="db6b9-203">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db6b9-203">NOTES</span></span>

## <span data-ttu-id="db6b9-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db6b9-204">RELATED LINKS</span></span>

[<span data-ttu-id="db6b9-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="db6b9-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="db6b9-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="db6b9-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="db6b9-207">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="db6b9-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


