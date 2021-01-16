---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 77299e9424f0a194776b1114146b76ef2be3329f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383275"
---
# <span data-ttu-id="6e1f6-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="6e1f6-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="6e1f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1f6-103">Eltávolítja egy Azure Synapse Analytics SQL-készlet naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6e1f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e1f6-104">SYNTAX</span></span>

### <span data-ttu-id="6e1f6-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e1f6-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e1f6-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e1f6-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e1f6-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e1f6-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e1f6-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e1f6-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e1f6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e1f6-109">DESCRIPTION</span></span>
<span data-ttu-id="6e1f6-110">A **Reset-AzSynapseSqlPoolAuditSetting** parancsmag eltávolítja az Azure Synapse Analytics SQL-készlet naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6e1f6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e1f6-111">EXAMPLES</span></span>

### <span data-ttu-id="6e1f6-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="6e1f6-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="6e1f6-113">Ez a parancs eltávolítja a ContosoSqlPool nevű SQL-készlet naplózási beállításait a ContosoWorkspace munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="6e1f6-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="6e1f6-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="6e1f6-115">Ez a parancs eltávolítja a ContosoSqlPool nevű SQL-készlet naplózási beállításait a ContosoWorkspace folyamaton keresztüli munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="6e1f6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e1f6-116">PARAMETERS</span></span>

### <span data-ttu-id="6e1f6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e1f6-117">-AsJob</span></span>
<span data-ttu-id="6e1f6-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6e1f6-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e1f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1f6-119">-DefaultProfile</span></span>
<span data-ttu-id="6e1f6-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e1f6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e1f6-121">-InputObject</span></span>
<span data-ttu-id="6e1f6-122">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e1f6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6e1f6-123">-Name</span></span>
<span data-ttu-id="6e1f6-124">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-124">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1f6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e1f6-125">-PassThru</span></span>
<span data-ttu-id="6e1f6-126">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6e1f6-127">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6e1f6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e1f6-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e1f6-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1f6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e1f6-130">-ResourceId</span></span>
<span data-ttu-id="6e1f6-131">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-131">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1f6-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6e1f6-132">-WorkspaceName</span></span>
<span data-ttu-id="6e1f6-133">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1f6-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6e1f6-134">-WorkspaceObject</span></span>
<span data-ttu-id="6e1f6-135">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e1f6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e1f6-136">-Confirm</span></span>
<span data-ttu-id="6e1f6-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e1f6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e1f6-138">-WhatIf</span></span>
<span data-ttu-id="6e1f6-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e1f6-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e1f6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1f6-141">CommonParameters</span></span>
<span data-ttu-id="6e1f6-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1f6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1f6-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e1f6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1f6-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e1f6-144">INPUTS</span></span>

### <span data-ttu-id="6e1f6-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6e1f6-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6e1f6-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6e1f6-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6e1f6-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e1f6-147">OUTPUTS</span></span>

### <span data-ttu-id="6e1f6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e1f6-148">System.Boolean</span></span>

## <span data-ttu-id="6e1f6-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e1f6-149">NOTES</span></span>

## <span data-ttu-id="6e1f6-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e1f6-150">RELATED LINKS</span></span>
