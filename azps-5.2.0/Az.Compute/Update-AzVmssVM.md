---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360847"
---
# <span data-ttu-id="830e2-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="830e2-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="830e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="830e2-102">SYNOPSIS</span></span>
<span data-ttu-id="830e2-103">Frissíti a Vmss VM állapotát.</span><span class="sxs-lookup"><span data-stu-id="830e2-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="830e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="830e2-104">SYNTAX</span></span>

### <span data-ttu-id="830e2-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="830e2-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="830e2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="830e2-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="830e2-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="830e2-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="830e2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="830e2-108">DESCRIPTION</span></span>
<span data-ttu-id="830e2-109">Frissíti a Vmss VM állapotát.</span><span class="sxs-lookup"><span data-stu-id="830e2-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="830e2-110">Jelenleg az egyetlen engedélyezett frissítés a felügyelt adatlemez hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="830e2-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="830e2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="830e2-111">EXAMPLES</span></span>

### <span data-ttu-id="830e2-112">1. példa: Felügyelt adatlemez hozzáadása Vmss VM-hez New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="830e2-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="830e2-113">Az első parancs egy meglévő felügyelt lemezhez jut.</span><span class="sxs-lookup"><span data-stu-id="830e2-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="830e2-114">A következő parancs létrehoz egy adatlemez-objektumot a felügyelt lemezzel.</span><span class="sxs-lookup"><span data-stu-id="830e2-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="830e2-115">A következő parancs egy meglévő Vmss VM-et kap, amelyet az erőforráscsoport neve, a vmss neve és a példányazonosító ad meg.</span><span class="sxs-lookup"><span data-stu-id="830e2-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="830e2-116">Az utolsó parancs egy új adatlemez hozzáadásával frissíti a Vmss VM-et.</span><span class="sxs-lookup"><span data-stu-id="830e2-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="830e2-117">2. példa: Felügyelt adatlemez hozzáadása Vmss VM-hez Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="830e2-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="830e2-118">Az első parancs egy meglévő felügyelt lemezhez jut.</span><span class="sxs-lookup"><span data-stu-id="830e2-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="830e2-119">A következő parancs egy meglévő Vmss VM-et kap, amelyet az erőforráscsoport neve, a vmss neve és a példányazonosító ad meg.</span><span class="sxs-lookup"><span data-stu-id="830e2-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="830e2-120">A következő parancs hozzáadja a felügyelt lemezt a helyileg tárolt Vmss VM-hez a $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="830e2-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="830e2-121">Az utolsó parancs frissíti a Vmss VM-et hozzáadott adatlemezzel.</span><span class="sxs-lookup"><span data-stu-id="830e2-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="830e2-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="830e2-122">Example 3</span></span>

<span data-ttu-id="830e2-123">Frissíti a Vmss VM állapotát.</span><span class="sxs-lookup"><span data-stu-id="830e2-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="830e2-124">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="830e2-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="830e2-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="830e2-125">PARAMETERS</span></span>

### <span data-ttu-id="830e2-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="830e2-126">-AsJob</span></span>
<span data-ttu-id="830e2-127">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="830e2-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="830e2-128">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="830e2-128">-DataDisk</span></span>

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

### <span data-ttu-id="830e2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830e2-129">-DefaultProfile</span></span>
<span data-ttu-id="830e2-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="830e2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="830e2-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="830e2-131">-InstanceId</span></span>
<span data-ttu-id="830e2-132">A VMSS VM példányazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="830e2-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="830e2-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="830e2-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="830e2-134">Azt jelzi, hogy a virtuális gép méretaránykészletét (VM) nem szabad törlésnek tekinteni a méretarányos művelet során.</span><span class="sxs-lookup"><span data-stu-id="830e2-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830e2-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="830e2-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="830e2-136">Azt jelzi, hogy a VMSS-en kezdeményezett modellfrissítéseket és -műveleteket (beleértve a méretarányt) nem kell alkalmazni a VMSS VM-en.</span><span class="sxs-lookup"><span data-stu-id="830e2-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830e2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="830e2-137">-ResourceGroupName</span></span>
<span data-ttu-id="830e2-138">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="830e2-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="830e2-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="830e2-139">-ResourceId</span></span>
<span data-ttu-id="830e2-140">A virtuális gép méretaránykészletének VM-hez szükséges erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="830e2-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="830e2-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="830e2-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="830e2-142">Local virtual machine scale set VM object</span><span class="sxs-lookup"><span data-stu-id="830e2-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="830e2-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="830e2-143">-VMScaleSetName</span></span>
<span data-ttu-id="830e2-144">A virtuális gép méretaránykészletének neve</span><span class="sxs-lookup"><span data-stu-id="830e2-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="830e2-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="830e2-145">-Confirm</span></span>
<span data-ttu-id="830e2-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="830e2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="830e2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="830e2-147">-WhatIf</span></span>
<span data-ttu-id="830e2-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="830e2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="830e2-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="830e2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="830e2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830e2-150">CommonParameters</span></span>
<span data-ttu-id="830e2-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="830e2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830e2-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="830e2-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830e2-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="830e2-153">INPUTS</span></span>

### <span data-ttu-id="830e2-154">System.String</span><span class="sxs-lookup"><span data-stu-id="830e2-154">System.String</span></span>

### <span data-ttu-id="830e2-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="830e2-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="830e2-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="830e2-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="830e2-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="830e2-157">OUTPUTS</span></span>

### <span data-ttu-id="830e2-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="830e2-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="830e2-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="830e2-159">NOTES</span></span>

## <span data-ttu-id="830e2-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="830e2-160">RELATED LINKS</span></span>
