---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: d5dc3afe69495e5fef8c0a1ad5a9d155fd15d295
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671195"
---
# <span data-ttu-id="2a5a7-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="2a5a7-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="2a5a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5a7-103">Frissíti a Vmss VM állapotát.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="2a5a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a5a7-104">SYNTAX</span></span>

### <span data-ttu-id="2a5a7-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a5a7-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a5a7-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2a5a7-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a5a7-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2a5a7-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a5a7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a5a7-108">DESCRIPTION</span></span>
<span data-ttu-id="2a5a7-109">Frissíti a Vmss VM állapotát.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="2a5a7-110">Az egyetlen engedélyezett frissítés most már csak egy felügyelt adatlemezt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="2a5a7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2a5a7-111">EXAMPLES</span></span>

### <span data-ttu-id="2a5a7-112">1. példa: felügyelt adatlemez felvétele Vmss VM-New-AzVMDataDisk használatával</span><span class="sxs-lookup"><span data-stu-id="2a5a7-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="2a5a7-113">Az első parancs a meglévő távtárolású lemezt kapja.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="2a5a7-114">A következő parancs létrehoz egy Data Disk-objektumot a kezelt lemezzel.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="2a5a7-115">A következő parancs beolvassa a létező Vmss VM nevet, amelyet az erőforráscsoport neve, a Vmss neve és a példány azonosítója adott meg.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="2a5a7-116">A végleges parancs új adatlemez hozzáadásával frissíti a Vmss VM-et.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="2a5a7-117">2. példa: felügyelt adatlemez felvétele Vmss VM-Add-AzVMDataDisk használatával</span><span class="sxs-lookup"><span data-stu-id="2a5a7-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="2a5a7-118">Az első parancs a meglévő távtárolású lemezt kapja.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="2a5a7-119">A következő parancs beolvassa a létező Vmss VM nevet, amelyet az erőforráscsoport neve, a Vmss neve és a példány azonosítója adott meg.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="2a5a7-120">A következő parancs hozzáadja a távtárolású meghajtót az $VmssVM helyileg tárolt Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="2a5a7-121">A végleges parancs frissíti a Vmss VM-et a hozzáadott adatlemezzel.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="2a5a7-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a5a7-122">PARAMETERS</span></span>

### <span data-ttu-id="2a5a7-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a5a7-123">-AsJob</span></span>
<span data-ttu-id="2a5a7-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2a5a7-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a5a7-125">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="2a5a7-125">-DataDisk</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a5a7-126">-DefaultProfile</span></span>
<span data-ttu-id="2a5a7-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a5a7-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2a5a7-128">-InstanceId</span></span>
<span data-ttu-id="2a5a7-129">A VMSS VM példányának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-129">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a5a7-130">-ResourceGroupName</span></span>
<span data-ttu-id="2a5a7-131">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a5a7-132">-ResourceId</span></span>
<span data-ttu-id="2a5a7-133">A virtuális gép méretarányos VM-készletének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2a5a7-133">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-134">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2a5a7-134">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="2a5a7-135">Helyi virtuális gép méretarány beállítása VM objektum</span><span class="sxs-lookup"><span data-stu-id="2a5a7-135">Local virtual machine scale set VM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-136">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2a5a7-136">-VMScaleSetName</span></span>
<span data-ttu-id="2a5a7-137">A virtuális gép méretarányának beállítása</span><span class="sxs-lookup"><span data-stu-id="2a5a7-137">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2a5a7-138">-Confirm</span></span>
<span data-ttu-id="2a5a7-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a5a7-140">-WhatIf</span></span>
<span data-ttu-id="2a5a7-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a5a7-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a5a7-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5a7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5a7-143">CommonParameters</span></span>
<span data-ttu-id="2a5a7-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a5a7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5a7-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a5a7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5a7-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a5a7-146">INPUTS</span></span>

### <span data-ttu-id="2a5a7-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2a5a7-147">System.String</span></span>

### <span data-ttu-id="2a5a7-148">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="2a5a7-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="2a5a7-149">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2a5a7-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2a5a7-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a5a7-150">OUTPUTS</span></span>

### <span data-ttu-id="2a5a7-151">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2a5a7-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2a5a7-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a5a7-152">NOTES</span></span>

## <span data-ttu-id="2a5a7-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a5a7-153">RELATED LINKS</span></span>
