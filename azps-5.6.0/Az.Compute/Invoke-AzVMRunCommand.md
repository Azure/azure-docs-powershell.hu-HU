---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 8eaf939839a668ea817d8f3529fced76ef71d22e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004581"
---
# <span data-ttu-id="615a0-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="615a0-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="615a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="615a0-102">SYNOPSIS</span></span>
<span data-ttu-id="615a0-103">Futtason egy parancsot a VM-en.</span><span class="sxs-lookup"><span data-stu-id="615a0-103">Run a command on the VM.</span></span>

## <span data-ttu-id="615a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="615a0-104">SYNTAX</span></span>

### <span data-ttu-id="615a0-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="615a0-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="615a0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="615a0-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="615a0-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="615a0-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="615a0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="615a0-108">DESCRIPTION</span></span>
<span data-ttu-id="615a0-109">Futtassa a parancsot a VM-en.</span><span class="sxs-lookup"><span data-stu-id="615a0-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="615a0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="615a0-110">EXAMPLES</span></span>

### <span data-ttu-id="615a0-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="615a0-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="615a0-112">Meghívhatja a RunPowerShellScript futtatás parancsát úgy, hogy felülírja a "sample.ps1" parancsfájlt és a vmname (vmname) vmname paraméterét az "rgname" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="615a0-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="615a0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="615a0-113">PARAMETERS</span></span>

### <span data-ttu-id="615a0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="615a0-114">-AsJob</span></span>
<span data-ttu-id="615a0-115">Futtassa a parancsmagot a háttérben, és a folyamat nyomon követéséhez adja vissza a feladatobjektumot.</span><span class="sxs-lookup"><span data-stu-id="615a0-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="615a0-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="615a0-116">-CommandId</span></span>
<span data-ttu-id="615a0-117">A futtatás parancsazonosítója.</span><span class="sxs-lookup"><span data-stu-id="615a0-117">The run command ID.</span></span>

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

### <span data-ttu-id="615a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="615a0-118">-DefaultProfile</span></span>
<span data-ttu-id="615a0-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="615a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="615a0-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="615a0-120">-Parameter</span></span>
<span data-ttu-id="615a0-121">A futtatás parancsparaméterek.</span><span class="sxs-lookup"><span data-stu-id="615a0-121">The run command parameters.</span></span>

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

### <span data-ttu-id="615a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="615a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="615a0-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="615a0-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="615a0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="615a0-124">-ResourceId</span></span>
<span data-ttu-id="615a0-125">A virtuális gép erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="615a0-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="615a0-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="615a0-126">-ScriptPath</span></span>
<span data-ttu-id="615a0-127">A végrehajtandó parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="615a0-127">Path of the script to be executed.</span></span>  <span data-ttu-id="615a0-128">Ha ezt az értéket adta meg, a parancsprogram felülírja a parancsprogram alapértelmezett parancsprogramját.</span><span class="sxs-lookup"><span data-stu-id="615a0-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="615a0-129">-VM</span><span class="sxs-lookup"><span data-stu-id="615a0-129">-VM</span></span>
<span data-ttu-id="615a0-130">A PS virtuális gép objektum.</span><span class="sxs-lookup"><span data-stu-id="615a0-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="615a0-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="615a0-131">-VMName</span></span>
<span data-ttu-id="615a0-132">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="615a0-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="615a0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="615a0-133">-Confirm</span></span>
<span data-ttu-id="615a0-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="615a0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="615a0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="615a0-135">-WhatIf</span></span>
<span data-ttu-id="615a0-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="615a0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="615a0-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="615a0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="615a0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="615a0-138">CommonParameters</span></span>
<span data-ttu-id="615a0-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="615a0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="615a0-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="615a0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="615a0-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="615a0-141">INPUTS</span></span>

### <span data-ttu-id="615a0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="615a0-142">System.String</span></span>

### <span data-ttu-id="615a0-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="615a0-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="615a0-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="615a0-144">OUTPUTS</span></span>

### <span data-ttu-id="615a0-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="615a0-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="615a0-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="615a0-146">NOTES</span></span>

## <span data-ttu-id="615a0-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="615a0-147">RELATED LINKS</span></span>
