---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186756"
---
# <span data-ttu-id="d2862-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="d2862-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="d2862-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2862-102">SYNOPSIS</span></span>
<span data-ttu-id="d2862-103">Frissíti a Vmss VM állapotát.</span><span class="sxs-lookup"><span data-stu-id="d2862-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="d2862-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2862-104">SYNTAX</span></span>

### <span data-ttu-id="d2862-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2862-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2862-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d2862-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2862-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d2862-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2862-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2862-108">DESCRIPTION</span></span>
<span data-ttu-id="d2862-109">Frissíti a Vmss VM állapotát.</span><span class="sxs-lookup"><span data-stu-id="d2862-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="d2862-110">Az egyetlen engedélyezett frissítés most már csak egy felügyelt adatlemezt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="d2862-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="d2862-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d2862-111">EXAMPLES</span></span>

### <span data-ttu-id="d2862-112">1. példa: felügyelt adatlemez felvétele Vmss VM-New-AzVMDataDisk használatával</span><span class="sxs-lookup"><span data-stu-id="d2862-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="d2862-113">Az első parancs a meglévő távtárolású lemezt kapja.</span><span class="sxs-lookup"><span data-stu-id="d2862-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="d2862-114">A következő parancs létrehoz egy Data Disk-objektumot a kezelt lemezzel.</span><span class="sxs-lookup"><span data-stu-id="d2862-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="d2862-115">A következő parancs beolvassa a létező Vmss VM nevet, amelyet az erőforráscsoport neve, a Vmss neve és a példány azonosítója adott meg.</span><span class="sxs-lookup"><span data-stu-id="d2862-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="d2862-116">A végleges parancs új adatlemez hozzáadásával frissíti a Vmss VM-et.</span><span class="sxs-lookup"><span data-stu-id="d2862-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="d2862-117">2. példa: felügyelt adatlemez felvétele Vmss VM-Add-AzVMDataDisk használatával</span><span class="sxs-lookup"><span data-stu-id="d2862-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="d2862-118">Az első parancs a meglévő távtárolású lemezt kapja.</span><span class="sxs-lookup"><span data-stu-id="d2862-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="d2862-119">A következő parancs beolvassa a létező Vmss VM nevet, amelyet az erőforráscsoport neve, a Vmss neve és a példány azonosítója adott meg.</span><span class="sxs-lookup"><span data-stu-id="d2862-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="d2862-120">A következő parancs hozzáadja a távtárolású meghajtót az $VmssVM helyileg tárolt Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="d2862-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="d2862-121">A végleges parancs frissíti a Vmss VM-et a hozzáadott adatlemezzel.</span><span class="sxs-lookup"><span data-stu-id="d2862-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="d2862-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="d2862-122">Example 3</span></span>

<span data-ttu-id="d2862-123">Frissíti a Vmss VM állapotát.</span><span class="sxs-lookup"><span data-stu-id="d2862-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="d2862-124">autogenerated</span><span class="sxs-lookup"><span data-stu-id="d2862-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="d2862-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2862-125">PARAMETERS</span></span>

### <span data-ttu-id="d2862-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2862-126">-AsJob</span></span>
<span data-ttu-id="d2862-127">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d2862-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2862-128">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="d2862-128">-DataDisk</span></span>

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

### <span data-ttu-id="d2862-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2862-129">-DefaultProfile</span></span>
<span data-ttu-id="d2862-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2862-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2862-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d2862-131">-InstanceId</span></span>
<span data-ttu-id="d2862-132">A VMSS VM példányának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2862-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="d2862-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="d2862-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="d2862-134">Azt jelzi, hogy a virtuális gép méretarányát a VM-es verzió nem veszi figyelembe a törlést a méretarányos művelet során.</span><span class="sxs-lookup"><span data-stu-id="d2862-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="d2862-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="d2862-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="d2862-136">Azt jelzi, hogy a VMSS kezdeményezett modell-vagy műveleteket (többek között a méretarányt) nem kell alkalmazni a VMSS VM-re.</span><span class="sxs-lookup"><span data-stu-id="d2862-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="d2862-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2862-137">-ResourceGroupName</span></span>
<span data-ttu-id="d2862-138">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2862-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="d2862-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2862-139">-ResourceId</span></span>
<span data-ttu-id="d2862-140">A virtuális gép méretarányos VM-készletének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d2862-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="d2862-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="d2862-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="d2862-142">Helyi virtuális gép méretarány beállítása VM objektum</span><span class="sxs-lookup"><span data-stu-id="d2862-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="d2862-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d2862-143">-VMScaleSetName</span></span>
<span data-ttu-id="d2862-144">A virtuális gép méretarányának beállítása</span><span class="sxs-lookup"><span data-stu-id="d2862-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="d2862-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d2862-145">-Confirm</span></span>
<span data-ttu-id="d2862-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d2862-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2862-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2862-147">-WhatIf</span></span>
<span data-ttu-id="d2862-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d2862-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2862-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2862-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2862-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2862-150">CommonParameters</span></span>
<span data-ttu-id="d2862-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2862-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2862-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d2862-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2862-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2862-153">INPUTS</span></span>

### <span data-ttu-id="d2862-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d2862-154">System.String</span></span>

### <span data-ttu-id="d2862-155">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="d2862-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="d2862-156">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="d2862-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="d2862-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2862-157">OUTPUTS</span></span>

### <span data-ttu-id="d2862-158">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="d2862-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="d2862-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2862-159">NOTES</span></span>

## <span data-ttu-id="d2862-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2862-160">RELATED LINKS</span></span>
