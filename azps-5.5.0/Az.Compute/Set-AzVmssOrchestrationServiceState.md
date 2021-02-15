---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164171"
---
# <span data-ttu-id="6bc3a-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="6bc3a-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="6bc3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc3a-103">Beállítja a vmss szolgáltatás állapotát.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="6bc3a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6bc3a-104">SYNTAX</span></span>

### <span data-ttu-id="6bc3a-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6bc3a-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bc3a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6bc3a-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bc3a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6bc3a-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bc3a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6bc3a-108">DESCRIPTION</span></span>
<span data-ttu-id="6bc3a-109">Beállítja a vmss szolgáltatás állapotát.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="6bc3a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6bc3a-110">EXAMPLES</span></span>

### <span data-ttu-id="6bc3a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6bc3a-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="6bc3a-112">Ez a parancs felfüggeszti az automatikus javítási szolgáltatást a VMSS "vmss1" rendszerében az "rg" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="6bc3a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6bc3a-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="6bc3a-114">Ez a parancs az "rg" erőforráscsoport VMSS "vmss1" rendszerében folytatja az automatikus javítási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="6bc3a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bc3a-115">PARAMETERS</span></span>

### <span data-ttu-id="6bc3a-116">-Művelet</span><span class="sxs-lookup"><span data-stu-id="6bc3a-116">-Action</span></span>
<span data-ttu-id="6bc3a-117">Az végrehajtani szükséges művelet.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-117">The action to be performed.</span></span>  <span data-ttu-id="6bc3a-118">Lehetséges értékek: Folytatás, Felfüggesztés.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-118">Possible values are: Resume, Suspend.</span></span>

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

### <span data-ttu-id="6bc3a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bc3a-119">-AsJob</span></span>
<span data-ttu-id="6bc3a-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6bc3a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bc3a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc3a-121">-DefaultProfile</span></span>
<span data-ttu-id="6bc3a-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bc3a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bc3a-123">-InputObject</span></span>
<span data-ttu-id="6bc3a-124">A virtuális gép méretaránykészletének helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-124">The local object of the virtual machine scale set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc3a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bc3a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6bc3a-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="6bc3a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bc3a-127">-ResourceId</span></span>
<span data-ttu-id="6bc3a-128">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="6bc3a-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6bc3a-129">-ServiceName</span></span>
<span data-ttu-id="6bc3a-130">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-130">The name of the service.</span></span>

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

### <span data-ttu-id="6bc3a-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6bc3a-131">-VMScaleSetName</span></span>
<span data-ttu-id="6bc3a-132">A virtuális gép méretaránykészletének neve.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6bc3a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bc3a-133">-Confirm</span></span>
<span data-ttu-id="6bc3a-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bc3a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bc3a-135">-WhatIf</span></span>
<span data-ttu-id="6bc3a-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bc3a-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bc3a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc3a-138">CommonParameters</span></span>
<span data-ttu-id="6bc3a-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bc3a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc3a-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bc3a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc3a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bc3a-141">INPUTS</span></span>

### <span data-ttu-id="6bc3a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6bc3a-142">System.String</span></span>

### <span data-ttu-id="6bc3a-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6bc3a-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6bc3a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bc3a-144">OUTPUTS</span></span>

### <span data-ttu-id="6bc3a-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6bc3a-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6bc3a-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6bc3a-146">NOTES</span></span>

## <span data-ttu-id="6bc3a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bc3a-147">RELATED LINKS</span></span>
