---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209006"
---
# <span data-ttu-id="92fef-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="92fef-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="92fef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92fef-102">SYNOPSIS</span></span>
<span data-ttu-id="92fef-103">Eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait egy munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="92fef-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="92fef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92fef-104">SYNTAX</span></span>

### <span data-ttu-id="92fef-105">ClearByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92fef-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92fef-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92fef-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92fef-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92fef-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92fef-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92fef-108">DESCRIPTION</span></span>
<span data-ttu-id="92fef-109">A **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** parancsmag eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait az Azure Synapse Analytics Workspace-ból.</span><span class="sxs-lookup"><span data-stu-id="92fef-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="92fef-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92fef-110">EXAMPLES</span></span>

### <span data-ttu-id="92fef-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="92fef-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="92fef-112">Ez a parancs eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="92fef-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="92fef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92fef-113">PARAMETERS</span></span>

### <span data-ttu-id="92fef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92fef-114">-AsJob</span></span>
<span data-ttu-id="92fef-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="92fef-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92fef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92fef-116">-DefaultProfile</span></span>
<span data-ttu-id="92fef-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92fef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92fef-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92fef-118">-InputObject</span></span>
<span data-ttu-id="92fef-119">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="92fef-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92fef-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92fef-120">-PassThru</span></span>
<span data-ttu-id="92fef-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="92fef-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="92fef-122">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="92fef-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="92fef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92fef-123">-ResourceGroupName</span></span>
<span data-ttu-id="92fef-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92fef-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fef-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92fef-125">-ResourceId</span></span>
<span data-ttu-id="92fef-126">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92fef-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fef-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="92fef-127">-WorkspaceName</span></span>
<span data-ttu-id="92fef-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="92fef-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fef-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92fef-129">-Confirm</span></span>
<span data-ttu-id="92fef-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="92fef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92fef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92fef-131">-WhatIf</span></span>
<span data-ttu-id="92fef-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="92fef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92fef-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92fef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92fef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92fef-134">CommonParameters</span></span>
<span data-ttu-id="92fef-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92fef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92fef-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92fef-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92fef-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92fef-137">INPUTS</span></span>

### <span data-ttu-id="92fef-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="92fef-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="92fef-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92fef-139">OUTPUTS</span></span>

### <span data-ttu-id="92fef-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92fef-140">System.Boolean</span></span>

## <span data-ttu-id="92fef-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92fef-141">NOTES</span></span>

## <span data-ttu-id="92fef-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92fef-142">RELATED LINKS</span></span>
