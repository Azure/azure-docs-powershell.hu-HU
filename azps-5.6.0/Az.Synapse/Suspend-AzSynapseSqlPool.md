---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: d0249098c8414a38adecc4112449174496656b78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011270"
---
# <span data-ttu-id="e2aea-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e2aea-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e2aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2aea-102">SYNOPSIS</span></span>
<span data-ttu-id="e2aea-103">Felfüggeszti a Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="e2aea-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e2aea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2aea-104">SYNTAX</span></span>

### <span data-ttu-id="e2aea-105">SuspendByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2aea-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2aea-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2aea-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2aea-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2aea-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2aea-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2aea-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2aea-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2aea-109">DESCRIPTION</span></span>
<span data-ttu-id="e2aea-110">A **Suspend-AzSynapseSqlPool** parancsmag felfüggeszti az Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="e2aea-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e2aea-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2aea-111">EXAMPLES</span></span>

### <span data-ttu-id="e2aea-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e2aea-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e2aea-113">Ez a parancs felfüggeszti az aktív Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="e2aea-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e2aea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2aea-114">PARAMETERS</span></span>

### <span data-ttu-id="e2aea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2aea-115">-AsJob</span></span>
<span data-ttu-id="e2aea-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e2aea-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2aea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2aea-117">-DefaultProfile</span></span>
<span data-ttu-id="e2aea-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2aea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2aea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2aea-119">-InputObject</span></span>
<span data-ttu-id="e2aea-120">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="e2aea-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2aea-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e2aea-121">-Name</span></span>
<span data-ttu-id="e2aea-122">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="e2aea-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2aea-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2aea-123">-PassThru</span></span>
<span data-ttu-id="e2aea-124">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="e2aea-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e2aea-125">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="e2aea-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e2aea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2aea-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2aea-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2aea-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2aea-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2aea-128">-ResourceId</span></span>
<span data-ttu-id="e2aea-129">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e2aea-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2aea-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e2aea-130">-WorkspaceName</span></span>
<span data-ttu-id="e2aea-131">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e2aea-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2aea-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e2aea-132">-WorkspaceObject</span></span>
<span data-ttu-id="e2aea-133">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="e2aea-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2aea-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2aea-134">-Confirm</span></span>
<span data-ttu-id="e2aea-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e2aea-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2aea-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2aea-136">-WhatIf</span></span>
<span data-ttu-id="e2aea-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e2aea-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2aea-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2aea-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2aea-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2aea-139">CommonParameters</span></span>
<span data-ttu-id="e2aea-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2aea-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2aea-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2aea-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2aea-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2aea-142">INPUTS</span></span>

### <span data-ttu-id="e2aea-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e2aea-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e2aea-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e2aea-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e2aea-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2aea-145">OUTPUTS</span></span>

### <span data-ttu-id="e2aea-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e2aea-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e2aea-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2aea-147">NOTES</span></span>

## <span data-ttu-id="e2aea-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2aea-148">RELATED LINKS</span></span>
