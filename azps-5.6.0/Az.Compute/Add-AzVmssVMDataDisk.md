---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 2f2a6fc8c7e04798e0f2fd3095c2111f12bec65b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927369"
---
# <span data-ttu-id="f822c-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f822c-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="f822c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f822c-102">SYNOPSIS</span></span>
<span data-ttu-id="f822c-103">Adatlemezt ad a Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="f822c-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="f822c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f822c-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f822c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f822c-105">DESCRIPTION</span></span>
<span data-ttu-id="f822c-106">Az **Add-AzVmssVMDataDisk** parancsmag hozzáad egy adatlemezt a Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="f822c-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="f822c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f822c-107">EXAMPLES</span></span>

### <span data-ttu-id="f822c-108">1. példa: Felügyelt adatlemez hozzáadása Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="f822c-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="f822c-109">Az első parancs egy meglévő felügyelt lemezhez jut.</span><span class="sxs-lookup"><span data-stu-id="f822c-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="f822c-110">A következő parancs egy meglévő Vmss VM-et kap, amelyet az erőforráscsoport neve, a vmss neve és a példányazonosító ad meg.</span><span class="sxs-lookup"><span data-stu-id="f822c-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="f822c-111">A következő parancs hozzáadja a felügyelt lemezt a helyileg tárolt Vmss VM-hez a $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="f822c-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="f822c-112">Az utolsó parancs frissíti a Vmss VM-et hozzáadott adatlemezzel.</span><span class="sxs-lookup"><span data-stu-id="f822c-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="f822c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f822c-113">PARAMETERS</span></span>

### <span data-ttu-id="f822c-114">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="f822c-114">-Caching</span></span>
<span data-ttu-id="f822c-115">A lemez gyorsítótárazása.</span><span class="sxs-lookup"><span data-stu-id="f822c-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="f822c-116">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="f822c-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f822c-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f822c-117">ReadOnly</span></span>
- <span data-ttu-id="f822c-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f822c-118">ReadWrite</span></span>
- <span data-ttu-id="f822c-119">Nincs az alapértelmezett érték a Beolvasott érték.</span><span class="sxs-lookup"><span data-stu-id="f822c-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="f822c-120">Ha módosítja ezt az értéket, a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="f822c-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="f822c-121">Ez a beállítás befolyásolja a lemez konzisztenciáját és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="f822c-121">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f822c-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="f822c-122">-CreateOption</span></span>
<span data-ttu-id="f822c-123">Azt adja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépben egy platformról vagy egy felhasználói képről, létrehoz-e egy üres lemezt, vagy csatol-e egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="f822c-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="f822c-124">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="f822c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f822c-125">Csatolás 2010.</span><span class="sxs-lookup"><span data-stu-id="f822c-125">Attach.</span></span>
<span data-ttu-id="f822c-126">Akkor válassza ezt a lehetőséget, ha egy speciális lemezről hoz létre virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="f822c-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="f822c-127">Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri paramétert.*</span><span class="sxs-lookup"><span data-stu-id="f822c-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="f822c-128">A *VhdUri* szükséges ahhoz, hogy az Azure platformon meg tudja mondani a virtuális merevlemez (VHD) helyét, hogy adatlemezként csatolja a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="f822c-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="f822c-129">Üres.</span><span class="sxs-lookup"><span data-stu-id="f822c-129">Empty.</span></span>
<span data-ttu-id="f822c-130">Ezt megadásával üres adatlemezt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="f822c-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="f822c-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="f822c-131">FromImage.</span></span>
<span data-ttu-id="f822c-132">Akkor válassza ezt a lehetőséget, ha általánosított képből vagy lemezről hoz létre virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="f822c-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="f822c-133">Ha megadja ezt a beállítást, a *SourceImageUri* paramétert is meg kell adnia ahhoz, hogy az Azure-platformnak meg tudja határozni a VHD adatlemezként csatolható helyét.</span><span class="sxs-lookup"><span data-stu-id="f822c-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="f822c-134">A *VhdUri* paraméter a virtuális gép által használt adatlemez helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f822c-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f822c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f822c-135">-DefaultProfile</span></span>
<span data-ttu-id="f822c-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f822c-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f822c-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="f822c-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="f822c-138">Az ügyfél által felügyelt lemeztitkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f822c-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="f822c-139">Ez csak felügyelt lemezhez lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="f822c-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="f822c-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="f822c-140">-DiskSizeInGB</span></span>
<span data-ttu-id="f822c-141">Egy virtuális géphez csatolni kívánt üres lemez gigabájtban megadott mérete.</span><span class="sxs-lookup"><span data-stu-id="f822c-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f822c-142">-Lun</span><span class="sxs-lookup"><span data-stu-id="f822c-142">-Lun</span></span>
<span data-ttu-id="f822c-143">Egy adatlemez logikai egységszámát (LUN) adja meg.</span><span class="sxs-lookup"><span data-stu-id="f822c-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f822c-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="f822c-144">-ManagedDiskId</span></span>
<span data-ttu-id="f822c-145">Egy felügyelt lemez azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f822c-145">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f822c-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f822c-146">-StorageAccountType</span></span>
<span data-ttu-id="f822c-147">A felügyelt lemez tárfióktípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f822c-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="f822c-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f822c-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="f822c-149">Megadja azt a helyi virtuális gép méretarányú VM-objektumot, amelyhez adatlemezt szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="f822c-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="f822c-150">A **Get-AzVmssVM** parancsmag használatával virtuális gépi méretezésű VM-objektumot szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="f822c-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f822c-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="f822c-151">-WriteAccelerator</span></span>
<span data-ttu-id="f822c-152">Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e felügyelt adatlemezen.</span><span class="sxs-lookup"><span data-stu-id="f822c-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="f822c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f822c-153">CommonParameters</span></span>
<span data-ttu-id="f822c-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f822c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f822c-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f822c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f822c-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f822c-156">INPUTS</span></span>

### <span data-ttu-id="f822c-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f822c-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="f822c-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f822c-158">System.Int32</span></span>

### <span data-ttu-id="f822c-159">System.String</span><span class="sxs-lookup"><span data-stu-id="f822c-159">System.String</span></span>

### <span data-ttu-id="f822c-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="f822c-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="f822c-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f822c-161">OUTPUTS</span></span>

### <span data-ttu-id="f822c-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f822c-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="f822c-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f822c-163">NOTES</span></span>

## <span data-ttu-id="f822c-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f822c-164">RELATED LINKS</span></span>
