---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 81f9e57bd2d815616cfc856246ff6950230f7112
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671368"
---
# <span data-ttu-id="a2212-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a2212-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="a2212-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2212-102">SYNOPSIS</span></span>
<span data-ttu-id="a2212-103">Adatlemez felvétele a Vmss VM-be</span><span class="sxs-lookup"><span data-stu-id="a2212-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="a2212-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2212-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2212-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2212-105">DESCRIPTION</span></span>
<span data-ttu-id="a2212-106">Az **Add-AzVmssVMDataDisk** parancsmag egy Vmss VM-es adatlemezt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="a2212-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="a2212-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a2212-107">EXAMPLES</span></span>

### <span data-ttu-id="a2212-108">1. példa: felügyelt adatlemez felvétele Vmss VM-be</span><span class="sxs-lookup"><span data-stu-id="a2212-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="a2212-109">Az első parancs a meglévő távtárolású lemezt kapja.</span><span class="sxs-lookup"><span data-stu-id="a2212-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="a2212-110">A következő parancs beolvassa a létező Vmss VM nevet, amelyet az erőforráscsoport neve, a Vmss neve és a példány azonosítója adott meg.</span><span class="sxs-lookup"><span data-stu-id="a2212-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="a2212-111">A következő parancs hozzáadja a távtárolású meghajtót az $VmssVM helyileg tárolt Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="a2212-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="a2212-112">A végleges parancs frissíti a Vmss VM-et a hozzáadott adatlemezzel.</span><span class="sxs-lookup"><span data-stu-id="a2212-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="a2212-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2212-113">PARAMETERS</span></span>

### <span data-ttu-id="a2212-114">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="a2212-114">-Caching</span></span>
<span data-ttu-id="a2212-115">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2212-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="a2212-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a2212-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a2212-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a2212-117">ReadOnly</span></span>
- <span data-ttu-id="a2212-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a2212-118">ReadWrite</span></span>
- <span data-ttu-id="a2212-119">Nincs az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="a2212-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="a2212-120">Az érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="a2212-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="a2212-121">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="a2212-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="a2212-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="a2212-122">-CreateOption</span></span>
<span data-ttu-id="a2212-123">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="a2212-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="a2212-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a2212-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a2212-125">Csatolja.</span><span class="sxs-lookup"><span data-stu-id="a2212-125">Attach.</span></span>
<span data-ttu-id="a2212-126">Ezt a lehetőséget választva virtuális gépet hozhat létre egy speciális merevlemezről.</span><span class="sxs-lookup"><span data-stu-id="a2212-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="a2212-127">Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="a2212-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="a2212-128">A *VhdUri* mindent meg kell tennie ahhoz, hogy az Azure platform a virtuális merevlemez (VHD) helyét a virtuális gép adatlemezéhez csatolja.</span><span class="sxs-lookup"><span data-stu-id="a2212-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="a2212-129">Üres.</span><span class="sxs-lookup"><span data-stu-id="a2212-129">Empty.</span></span>
<span data-ttu-id="a2212-130">Ezzel a beállítással üres adatlemezt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="a2212-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="a2212-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="a2212-131">FromImage.</span></span>
<span data-ttu-id="a2212-132">Ezt a lehetőséget választva virtuális gépet hozhat létre általános képből vagy lemezről.</span><span class="sxs-lookup"><span data-stu-id="a2212-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="a2212-133">Ha ezt a beállítást választja, akkor a *SourceImageUri* paramétert is meg kell adnia, hogy az Azure platform a VHD-fájlnak az adatlemezhez való csatolását adja.</span><span class="sxs-lookup"><span data-stu-id="a2212-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="a2212-134">A *VhdUri* paraméter az a hely, ahol az ADATlemez VHD-adatlemeze a virtuális gép általi használat után tárolódik.</span><span class="sxs-lookup"><span data-stu-id="a2212-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="a2212-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2212-135">-DefaultProfile</span></span>
<span data-ttu-id="a2212-136">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2212-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2212-137">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a2212-137">-DiskSizeInGB</span></span>
<span data-ttu-id="a2212-138">Itt adhatja meg a virtuális géphez csatolni kívánt üres lemez méretét gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="a2212-138">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="a2212-139">-LUN</span><span class="sxs-lookup"><span data-stu-id="a2212-139">-Lun</span></span>
<span data-ttu-id="a2212-140">Az adatlemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2212-140">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="a2212-141">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="a2212-141">-ManagedDiskId</span></span>
<span data-ttu-id="a2212-142">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2212-142">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="a2212-143">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a2212-143">-StorageAccountType</span></span>
<span data-ttu-id="a2212-144">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2212-144">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="a2212-145">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a2212-145">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="a2212-146">A helyi Virtual Machine Scale set VM objektumát adja hozzá az adatlemez hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="a2212-146">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="a2212-147">A **Get-AzVmssVM** parancsmaggal virtuális gép méretarány-set VM-objektum beszerzése használható.</span><span class="sxs-lookup"><span data-stu-id="a2212-147">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="a2212-148">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="a2212-148">-WriteAccelerator</span></span>
<span data-ttu-id="a2212-149">Itt adhatja meg, hogy a WriteAccelerator engedélyezve vagy Letiltva van-e egy felügyelt adatlemezen.</span><span class="sxs-lookup"><span data-stu-id="a2212-149">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="a2212-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2212-150">CommonParameters</span></span>
<span data-ttu-id="a2212-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2212-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2212-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2212-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2212-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2212-153">INPUTS</span></span>

### <span data-ttu-id="a2212-154">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a2212-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="a2212-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a2212-155">System.Int32</span></span>

### <span data-ttu-id="a2212-156">System. String</span><span class="sxs-lookup"><span data-stu-id="a2212-156">System.String</span></span>

### <span data-ttu-id="a2212-157">Microsoft. Azure. Management. kiszámítás. models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="a2212-157">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="a2212-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2212-158">OUTPUTS</span></span>

### <span data-ttu-id="a2212-159">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a2212-159">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="a2212-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2212-160">NOTES</span></span>

## <span data-ttu-id="a2212-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2212-161">RELATED LINKS</span></span>
