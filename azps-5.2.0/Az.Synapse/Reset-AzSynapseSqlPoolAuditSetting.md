---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 77299e9424f0a194776b1114146b76ef2be3329f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329052"
---
# <span data-ttu-id="d4279-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="d4279-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="d4279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4279-102">SYNOPSIS</span></span>
<span data-ttu-id="d4279-103">Eltávolítja egy Azure Synapse Analytics SQL-készlet naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="d4279-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d4279-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4279-104">SYNTAX</span></span>

### <span data-ttu-id="d4279-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4279-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4279-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4279-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4279-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4279-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4279-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4279-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4279-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4279-109">DESCRIPTION</span></span>
<span data-ttu-id="d4279-110">A **Reset-AzSynapseSqlPoolAuditSetting** parancsmag eltávolítja az Azure Synapse Analytics SQL-készlet naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="d4279-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d4279-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4279-111">EXAMPLES</span></span>

### <span data-ttu-id="d4279-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="d4279-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="d4279-113">Ez a parancs eltávolítja a ContosoSqlPool nevű SQL-készlet naplózási beállításait a ContosoWorkspace munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d4279-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d4279-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="d4279-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="d4279-115">Ez a parancs eltávolítja a ContosoSqlPool nevű SQL-készlet naplózási beállításait a ContosoWorkspace folyamaton keresztüli munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d4279-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d4279-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4279-116">PARAMETERS</span></span>

### <span data-ttu-id="d4279-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4279-117">-AsJob</span></span>
<span data-ttu-id="d4279-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d4279-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4279-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4279-119">-DefaultProfile</span></span>
<span data-ttu-id="d4279-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4279-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4279-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4279-121">-InputObject</span></span>
<span data-ttu-id="d4279-122">SQL-készlet bemeneti objektuma, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="d4279-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d4279-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d4279-123">-Name</span></span>
<span data-ttu-id="d4279-124">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="d4279-124">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="d4279-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4279-125">-PassThru</span></span>
<span data-ttu-id="d4279-126">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="d4279-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d4279-127">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="d4279-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d4279-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4279-128">-ResourceGroupName</span></span>
<span data-ttu-id="d4279-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4279-129">Resource group name.</span></span>

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

### <span data-ttu-id="d4279-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4279-130">-ResourceId</span></span>
<span data-ttu-id="d4279-131">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d4279-131">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="d4279-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d4279-132">-WorkspaceName</span></span>
<span data-ttu-id="d4279-133">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="d4279-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d4279-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d4279-134">-WorkspaceObject</span></span>
<span data-ttu-id="d4279-135">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="d4279-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d4279-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4279-136">-Confirm</span></span>
<span data-ttu-id="d4279-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d4279-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4279-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4279-138">-WhatIf</span></span>
<span data-ttu-id="d4279-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d4279-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4279-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4279-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4279-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4279-141">CommonParameters</span></span>
<span data-ttu-id="d4279-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4279-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4279-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4279-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4279-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4279-144">INPUTS</span></span>

### <span data-ttu-id="d4279-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d4279-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d4279-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d4279-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d4279-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4279-147">OUTPUTS</span></span>

### <span data-ttu-id="d4279-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4279-148">System.Boolean</span></span>

## <span data-ttu-id="d4279-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4279-149">NOTES</span></span>

## <span data-ttu-id="d4279-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4279-150">RELATED LINKS</span></span>
