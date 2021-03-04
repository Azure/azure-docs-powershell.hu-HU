---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: ea4674adaf1069a4681ab4943ad16685540378ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933065"
---
# <span data-ttu-id="1f26a-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="1f26a-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="1f26a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f26a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f26a-103">Run command on the Virtual Machine Scale Set VM.</span><span class="sxs-lookup"><span data-stu-id="1f26a-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="1f26a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1f26a-104">SYNTAX</span></span>

### <span data-ttu-id="1f26a-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f26a-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f26a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1f26a-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f26a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1f26a-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f26a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1f26a-108">DESCRIPTION</span></span>
<span data-ttu-id="1f26a-109">Futtatás parancs meghívása a Virtuálisgép-méretarány-készlet VM-en.</span><span class="sxs-lookup"><span data-stu-id="1f26a-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="1f26a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1f26a-110">EXAMPLES</span></span>

### <span data-ttu-id="1f26a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1f26a-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="1f26a-112">Meghívhatja a RunPowerShellScript futtatás parancsát úgy, hogy felülírja az "sample.ps1" parancsfájlt és a "0" azonosítójú VIRTUÁLIS GÉP azonosító paramétereit az "rgname" erőforráscsoport virtuális gépi méretskálát (vmssname) készletében.</span><span class="sxs-lookup"><span data-stu-id="1f26a-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="1f26a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1f26a-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="1f26a-114">Meghívhatja a RunPowerShellScript futtatás parancsát úgy, hogy felülírja az "sample.ps1" parancsfájlt és a "0" azonosítójú VIRTUÁLIS GÉP azonosító paramétereit az "rgname" erőforráscsoport virtuális gépi méretskálát (vmssname) készletében.</span><span class="sxs-lookup"><span data-stu-id="1f26a-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="1f26a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f26a-115">PARAMETERS</span></span>

### <span data-ttu-id="1f26a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f26a-116">-AsJob</span></span>
<span data-ttu-id="1f26a-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1f26a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f26a-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="1f26a-118">-CommandId</span></span>
<span data-ttu-id="1f26a-119">A futtatás parancsazonosítója.</span><span class="sxs-lookup"><span data-stu-id="1f26a-119">The run command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f26a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f26a-120">-DefaultProfile</span></span>
<span data-ttu-id="1f26a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f26a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f26a-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1f26a-122">-InstanceId</span></span>
<span data-ttu-id="1f26a-123">A virtuális gép méretezéskészletének VM-példányazonosítója.</span><span class="sxs-lookup"><span data-stu-id="1f26a-123">The instance ID of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="1f26a-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="1f26a-124">-Parameter</span></span>
<span data-ttu-id="1f26a-125">A futtatás parancsparaméterek.</span><span class="sxs-lookup"><span data-stu-id="1f26a-125">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f26a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f26a-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f26a-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1f26a-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f26a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f26a-128">-ResourceId</span></span>
<span data-ttu-id="1f26a-129">A virtuális gép méretaránykészletének VM-hez szükséges erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1f26a-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="1f26a-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="1f26a-130">-ScriptPath</span></span>
<span data-ttu-id="1f26a-131">A végrehajtandó parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="1f26a-131">Path of the script to be executed.</span></span>  <span data-ttu-id="1f26a-132">Ha ezt az értéket adta meg, a parancsprogram felülírja a parancsprogram alapértelmezett parancsprogramját.</span><span class="sxs-lookup"><span data-stu-id="1f26a-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="1f26a-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1f26a-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="1f26a-134">A PS virtuális gép méretezési beállítása VM-objektum.</span><span class="sxs-lookup"><span data-stu-id="1f26a-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26a-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1f26a-135">-VMScaleSetName</span></span>
<span data-ttu-id="1f26a-136">A virtuális gép méretaránykészletének VM-nek a neve.</span><span class="sxs-lookup"><span data-stu-id="1f26a-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="1f26a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f26a-137">-Confirm</span></span>
<span data-ttu-id="1f26a-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1f26a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f26a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f26a-139">-WhatIf</span></span>
<span data-ttu-id="1f26a-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1f26a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f26a-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f26a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f26a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f26a-142">CommonParameters</span></span>
<span data-ttu-id="1f26a-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f26a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f26a-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f26a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f26a-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f26a-145">INPUTS</span></span>

### <span data-ttu-id="1f26a-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1f26a-146">System.String</span></span>

### <span data-ttu-id="1f26a-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1f26a-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="1f26a-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f26a-148">OUTPUTS</span></span>

### <span data-ttu-id="1f26a-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="1f26a-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="1f26a-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1f26a-150">NOTES</span></span>

## <span data-ttu-id="1f26a-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f26a-151">RELATED LINKS</span></span>
