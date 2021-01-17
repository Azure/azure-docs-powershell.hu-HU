---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356521"
---
# <span data-ttu-id="d30e4-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="d30e4-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="d30e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d30e4-102">SYNOPSIS</span></span>
<span data-ttu-id="d30e4-103">Új visszaállítási pontot hoz létre egy Azure Synapse Analytics SQL-készletben.</span><span class="sxs-lookup"><span data-stu-id="d30e4-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d30e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d30e4-104">SYNTAX</span></span>

### <span data-ttu-id="d30e4-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d30e4-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d30e4-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d30e4-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d30e4-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d30e4-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d30e4-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d30e4-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d30e4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d30e4-109">DESCRIPTION</span></span>
<span data-ttu-id="d30e4-110">A **New-AzSynapseSqlPoolRestorePoint** parancsmag létrehoz egy új visszaállítási pontot, amelyből az Azure Synapse Analytics SQL-készlet visszaállítható.</span><span class="sxs-lookup"><span data-stu-id="d30e4-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="d30e4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d30e4-111">EXAMPLES</span></span>

### <span data-ttu-id="d30e4-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="d30e4-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="d30e4-113">Ez a parancs létrehozza a ContosoSqlPool nevű SQL-készlet visszaállítási pontját a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="d30e4-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="d30e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d30e4-114">PARAMETERS</span></span>

### <span data-ttu-id="d30e4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d30e4-115">-AsJob</span></span>
<span data-ttu-id="d30e4-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d30e4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d30e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d30e4-117">-DefaultProfile</span></span>
<span data-ttu-id="d30e4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d30e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d30e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d30e4-119">-InputObject</span></span>
<span data-ttu-id="d30e4-120">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="d30e4-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d30e4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d30e4-121">-Name</span></span>
<span data-ttu-id="d30e4-122">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="d30e4-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d30e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="d30e4-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d30e4-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30e4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d30e4-125">-ResourceId</span></span>
<span data-ttu-id="d30e4-126">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d30e4-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30e4-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="d30e4-127">-RestorePointLabel</span></span>
<span data-ttu-id="d30e4-128">Előfordulhat, hogy a visszaállítási pont címkéje nem egyedi.</span><span class="sxs-lookup"><span data-stu-id="d30e4-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="d30e4-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d30e4-129">-WorkspaceName</span></span>
<span data-ttu-id="d30e4-130">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="d30e4-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30e4-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d30e4-131">-WorkspaceObject</span></span>
<span data-ttu-id="d30e4-132">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="d30e4-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d30e4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d30e4-133">-Confirm</span></span>
<span data-ttu-id="d30e4-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d30e4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d30e4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d30e4-135">-WhatIf</span></span>
<span data-ttu-id="d30e4-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d30e4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d30e4-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d30e4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d30e4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d30e4-138">CommonParameters</span></span>
<span data-ttu-id="d30e4-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d30e4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d30e4-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d30e4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d30e4-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d30e4-141">INPUTS</span></span>

### <span data-ttu-id="d30e4-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d30e4-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d30e4-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d30e4-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d30e4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d30e4-144">OUTPUTS</span></span>

### <span data-ttu-id="d30e4-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="d30e4-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="d30e4-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d30e4-146">NOTES</span></span>

## <span data-ttu-id="d30e4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d30e4-147">RELATED LINKS</span></span>
