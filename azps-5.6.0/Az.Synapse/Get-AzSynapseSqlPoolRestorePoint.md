---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: ef4684cd6f4c852a9833dfdbe8c26ae1df6d326e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920145"
---
# <span data-ttu-id="cacd7-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="cacd7-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="cacd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cacd7-102">SYNOPSIS</span></span>
<span data-ttu-id="cacd7-103">Beolvassa a különálló visszaállítási pontokat, amelyekből a Synapse Analytics SQL-készlet visszaállítható.</span><span class="sxs-lookup"><span data-stu-id="cacd7-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="cacd7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cacd7-104">SYNTAX</span></span>

### <span data-ttu-id="cacd7-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cacd7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cacd7-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cacd7-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cacd7-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cacd7-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cacd7-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cacd7-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cacd7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cacd7-109">DESCRIPTION</span></span>
<span data-ttu-id="cacd7-110">A **Get-AzSynapseSqlPoolRestorePoint** parancsmag beolvassa a különálló visszaállítási pontokat, amelyekből az Azure Synapse Analytics SQL-készlet visszaállítható.</span><span class="sxs-lookup"><span data-stu-id="cacd7-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="cacd7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cacd7-111">EXAMPLES</span></span>

### <span data-ttu-id="cacd7-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="cacd7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="cacd7-113">Ez a parancs visszaadja a ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet összes rendelkezésre álló visszaállítási pontot.</span><span class="sxs-lookup"><span data-stu-id="cacd7-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="cacd7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cacd7-114">PARAMETERS</span></span>

### <span data-ttu-id="cacd7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cacd7-115">-DefaultProfile</span></span>
<span data-ttu-id="cacd7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cacd7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cacd7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cacd7-117">-InputObject</span></span>
<span data-ttu-id="cacd7-118">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="cacd7-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cacd7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cacd7-119">-Name</span></span>
<span data-ttu-id="cacd7-120">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="cacd7-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="cacd7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cacd7-121">-ResourceGroupName</span></span>
<span data-ttu-id="cacd7-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cacd7-122">Resource group name.</span></span>

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

### <span data-ttu-id="cacd7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cacd7-123">-ResourceId</span></span>
<span data-ttu-id="cacd7-124">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cacd7-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="cacd7-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cacd7-125">-WorkspaceName</span></span>
<span data-ttu-id="cacd7-126">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="cacd7-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cacd7-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cacd7-127">-WorkspaceObject</span></span>
<span data-ttu-id="cacd7-128">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="cacd7-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cacd7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cacd7-129">CommonParameters</span></span>
<span data-ttu-id="cacd7-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cacd7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cacd7-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cacd7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cacd7-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cacd7-132">INPUTS</span></span>

### <span data-ttu-id="cacd7-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cacd7-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cacd7-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="cacd7-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="cacd7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cacd7-135">OUTPUTS</span></span>

### <span data-ttu-id="cacd7-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span><span class="sxs-lookup"><span data-stu-id="cacd7-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="cacd7-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cacd7-137">NOTES</span></span>

## <span data-ttu-id="cacd7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cacd7-138">RELATED LINKS</span></span>
