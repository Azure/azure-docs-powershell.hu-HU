---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162850"
---
# <span data-ttu-id="fd9fe-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="fd9fe-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="fd9fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd9fe-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9fe-103">Egy Azure Synapse Analytics SQL-készlet naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fd9fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd9fe-104">SYNTAX</span></span>

### <span data-ttu-id="fd9fe-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd9fe-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd9fe-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd9fe-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd9fe-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd9fe-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd9fe-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd9fe-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd9fe-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd9fe-109">DESCRIPTION</span></span>
<span data-ttu-id="fd9fe-110">A **Get-AzSynapseSqlPoolAuditSetting** parancsmag az Azure Synapse Analytics SQL-készlet naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fd9fe-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd9fe-111">EXAMPLES</span></span>

### <span data-ttu-id="fd9fe-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="fd9fe-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="fd9fe-113">Ez a parancs a ContosoWorkspace munkaterületen található ContosoSqlPool nevű SQL-készlet naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="fd9fe-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="fd9fe-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="fd9fe-115">Ez a parancs a ContosoSqlPool nevű SQL-készlet naplózási beállításait kapja meg a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="fd9fe-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd9fe-116">PARAMETERS</span></span>

### <span data-ttu-id="fd9fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9fe-117">-DefaultProfile</span></span>
<span data-ttu-id="fd9fe-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd9fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd9fe-119">-InputObject</span></span>
<span data-ttu-id="fd9fe-120">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fd9fe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fd9fe-121">-Name</span></span>
<span data-ttu-id="fd9fe-122">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="fd9fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd9fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd9fe-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-124">Resource group name.</span></span>

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

### <span data-ttu-id="fd9fe-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd9fe-125">-ResourceId</span></span>
<span data-ttu-id="fd9fe-126">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="fd9fe-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd9fe-127">-WorkspaceName</span></span>
<span data-ttu-id="fd9fe-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fd9fe-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fd9fe-129">-WorkspaceObject</span></span>
<span data-ttu-id="fd9fe-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fd9fe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9fe-131">CommonParameters</span></span>
<span data-ttu-id="fd9fe-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd9fe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9fe-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd9fe-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9fe-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd9fe-134">INPUTS</span></span>

### <span data-ttu-id="fd9fe-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd9fe-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fd9fe-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="fd9fe-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="fd9fe-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd9fe-137">OUTPUTS</span></span>

### <span data-ttu-id="fd9fe-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="fd9fe-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="fd9fe-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd9fe-139">NOTES</span></span>

## <span data-ttu-id="fd9fe-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd9fe-140">RELATED LINKS</span></span>
