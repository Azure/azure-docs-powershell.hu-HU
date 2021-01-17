---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359363"
---
# <span data-ttu-id="18502-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="18502-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="18502-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18502-102">SYNOPSIS</span></span>
<span data-ttu-id="18502-103">Beolvassa a különálló visszaállítási pontokat, amelyekből a Synapse Analytics SQL-készlet visszaállítható.</span><span class="sxs-lookup"><span data-stu-id="18502-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="18502-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18502-104">SYNTAX</span></span>

### <span data-ttu-id="18502-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18502-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18502-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18502-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18502-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18502-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18502-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18502-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18502-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18502-109">DESCRIPTION</span></span>
<span data-ttu-id="18502-110">A **Get-AzSynapseSqlPoolRestorePoint** parancsmag beolvassa a különálló visszaállítási pontokat, amelyekből az Azure Synapse Analytics SQL-készlet visszaállítható.</span><span class="sxs-lookup"><span data-stu-id="18502-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="18502-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18502-111">EXAMPLES</span></span>

### <span data-ttu-id="18502-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="18502-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="18502-113">Ez a parancs visszaadja a ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet összes rendelkezésre álló visszaállítási pontot.</span><span class="sxs-lookup"><span data-stu-id="18502-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="18502-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18502-114">PARAMETERS</span></span>

### <span data-ttu-id="18502-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18502-115">-DefaultProfile</span></span>
<span data-ttu-id="18502-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18502-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18502-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18502-117">-InputObject</span></span>
<span data-ttu-id="18502-118">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="18502-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="18502-119">-Name</span><span class="sxs-lookup"><span data-stu-id="18502-119">-Name</span></span>
<span data-ttu-id="18502-120">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="18502-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="18502-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18502-121">-ResourceGroupName</span></span>
<span data-ttu-id="18502-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="18502-122">Resource group name.</span></span>

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

### <span data-ttu-id="18502-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18502-123">-ResourceId</span></span>
<span data-ttu-id="18502-124">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="18502-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="18502-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="18502-125">-WorkspaceName</span></span>
<span data-ttu-id="18502-126">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="18502-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="18502-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="18502-127">-WorkspaceObject</span></span>
<span data-ttu-id="18502-128">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="18502-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="18502-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18502-129">CommonParameters</span></span>
<span data-ttu-id="18502-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18502-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18502-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18502-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18502-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18502-132">INPUTS</span></span>

### <span data-ttu-id="18502-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="18502-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="18502-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="18502-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="18502-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18502-135">OUTPUTS</span></span>

### <span data-ttu-id="18502-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span><span class="sxs-lookup"><span data-stu-id="18502-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="18502-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18502-137">NOTES</span></span>

## <span data-ttu-id="18502-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18502-138">RELATED LINKS</span></span>
