---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383849"
---
# <span data-ttu-id="f5cbf-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="f5cbf-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="f5cbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="f5cbf-103">Egy Azure Synapse Analytics SQL-készlet naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f5cbf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f5cbf-104">SYNTAX</span></span>

### <span data-ttu-id="f5cbf-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5cbf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5cbf-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5cbf-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5cbf-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5cbf-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5cbf-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5cbf-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5cbf-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f5cbf-109">DESCRIPTION</span></span>
<span data-ttu-id="f5cbf-110">A **Get-AzSynapseSqlPoolAuditSetting** parancsmag az Azure Synapse Analytics SQL-készlet naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f5cbf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f5cbf-111">EXAMPLES</span></span>

### <span data-ttu-id="f5cbf-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="f5cbf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="f5cbf-113">Ez a parancs a ContosoWorkspace munkaterületen található ContosoSqlPool nevű SQL-készlet naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="f5cbf-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="f5cbf-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="f5cbf-115">Ez a parancs a ContosoSqlPool nevű SQL-készlet naplózási beállításait kapja meg a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f5cbf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5cbf-116">PARAMETERS</span></span>

### <span data-ttu-id="f5cbf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5cbf-117">-DefaultProfile</span></span>
<span data-ttu-id="f5cbf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5cbf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5cbf-119">-InputObject</span></span>
<span data-ttu-id="f5cbf-120">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f5cbf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f5cbf-121">-Name</span></span>
<span data-ttu-id="f5cbf-122">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="f5cbf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5cbf-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5cbf-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-124">Resource group name.</span></span>

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

### <span data-ttu-id="f5cbf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5cbf-125">-ResourceId</span></span>
<span data-ttu-id="f5cbf-126">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="f5cbf-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5cbf-127">-WorkspaceName</span></span>
<span data-ttu-id="f5cbf-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f5cbf-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f5cbf-129">-WorkspaceObject</span></span>
<span data-ttu-id="f5cbf-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f5cbf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5cbf-131">CommonParameters</span></span>
<span data-ttu-id="f5cbf-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5cbf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5cbf-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5cbf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5cbf-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5cbf-134">INPUTS</span></span>

### <span data-ttu-id="f5cbf-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f5cbf-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f5cbf-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f5cbf-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f5cbf-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5cbf-137">OUTPUTS</span></span>

### <span data-ttu-id="f5cbf-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="f5cbf-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="f5cbf-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f5cbf-139">NOTES</span></span>

## <span data-ttu-id="f5cbf-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5cbf-140">RELATED LINKS</span></span>
