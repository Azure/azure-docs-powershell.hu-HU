---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: dea94d89bfd5384d8ec614259a5bb342cd9d186b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015653"
---
# <span data-ttu-id="e94c7-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="e94c7-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="e94c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e94c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e94c7-103">Egy Azure Synapse Analytics SQL-készlet naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e94c7-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e94c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e94c7-104">SYNTAX</span></span>

### <span data-ttu-id="e94c7-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e94c7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e94c7-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e94c7-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e94c7-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e94c7-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e94c7-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e94c7-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e94c7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e94c7-109">DESCRIPTION</span></span>
<span data-ttu-id="e94c7-110">A **Get-AzSynapseSqlPoolAuditSetting** parancsmag az Azure Synapse Analytics SQL-készlet naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e94c7-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e94c7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e94c7-111">EXAMPLES</span></span>

### <span data-ttu-id="e94c7-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e94c7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e94c7-113">Ez a parancs a ContosoWorkspace munkaterületen található ContosoSqlPool nevű SQL-készlet naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e94c7-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e94c7-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e94c7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="e94c7-115">Ez a parancs a ContosoSqlPool nevű SQL-készlet naplózási beállításait kapja meg a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="e94c7-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e94c7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e94c7-116">PARAMETERS</span></span>

### <span data-ttu-id="e94c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94c7-117">-DefaultProfile</span></span>
<span data-ttu-id="e94c7-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e94c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e94c7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e94c7-119">-InputObject</span></span>
<span data-ttu-id="e94c7-120">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="e94c7-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e94c7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e94c7-121">-Name</span></span>
<span data-ttu-id="e94c7-122">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="e94c7-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e94c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="e94c7-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e94c7-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94c7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e94c7-125">-ResourceId</span></span>
<span data-ttu-id="e94c7-126">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e94c7-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94c7-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e94c7-127">-WorkspaceName</span></span>
<span data-ttu-id="e94c7-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e94c7-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94c7-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e94c7-129">-WorkspaceObject</span></span>
<span data-ttu-id="e94c7-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="e94c7-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e94c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94c7-131">CommonParameters</span></span>
<span data-ttu-id="e94c7-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e94c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94c7-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e94c7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94c7-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e94c7-134">INPUTS</span></span>

### <span data-ttu-id="e94c7-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e94c7-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e94c7-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e94c7-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e94c7-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e94c7-137">OUTPUTS</span></span>

### <span data-ttu-id="e94c7-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="e94c7-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="e94c7-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e94c7-139">NOTES</span></span>

## <span data-ttu-id="e94c7-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e94c7-140">RELATED LINKS</span></span>
