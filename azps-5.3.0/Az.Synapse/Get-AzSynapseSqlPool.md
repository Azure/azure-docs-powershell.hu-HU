---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 8199b14cf7b41eb99bb17f1692e762a07e127f26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383877"
---
# <span data-ttu-id="b33a0-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b33a0-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="b33a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b33a0-102">SYNOPSIS</span></span>
<span data-ttu-id="b33a0-103">Synapse Analytics SQL-készletet kap.</span><span class="sxs-lookup"><span data-stu-id="b33a0-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b33a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b33a0-104">SYNTAX</span></span>

### <span data-ttu-id="b33a0-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b33a0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b33a0-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b33a0-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b33a0-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b33a0-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b33a0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b33a0-108">DESCRIPTION</span></span>
<span data-ttu-id="b33a0-109">A **Get-AzSynapseSqlPool** parancsmag információkat kap az Azure Synapse Analytics SQL-készletről.</span><span class="sxs-lookup"><span data-stu-id="b33a0-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b33a0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b33a0-110">EXAMPLES</span></span>

### <span data-ttu-id="b33a0-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b33a0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b33a0-112">Ez a parancs az összes SQL-készletet egy munkaterület alá kapja.</span><span class="sxs-lookup"><span data-stu-id="b33a0-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="b33a0-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b33a0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="b33a0-114">Ez a parancs a ContosoWorkspace munkaterület alatti SQL-készletet kapja ContosoSqlPool néven.</span><span class="sxs-lookup"><span data-stu-id="b33a0-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="b33a0-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="b33a0-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="b33a0-116">Ez a parancs az összes SQL-készletet egy munkaterület alatt, folyamaton keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b33a0-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="b33a0-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="b33a0-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="b33a0-118">Ez a parancs a megadott erőforrás-azonosítójú SQL-készletet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b33a0-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="b33a0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b33a0-119">PARAMETERS</span></span>

### <span data-ttu-id="b33a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b33a0-120">-DefaultProfile</span></span>
<span data-ttu-id="b33a0-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b33a0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b33a0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b33a0-122">-Name</span></span>
<span data-ttu-id="b33a0-123">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="b33a0-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SqlPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b33a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b33a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="b33a0-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b33a0-125">Resource group name.</span></span>

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

### <span data-ttu-id="b33a0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b33a0-126">-ResourceId</span></span>
<span data-ttu-id="b33a0-127">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b33a0-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="b33a0-128">-Version</span><span class="sxs-lookup"><span data-stu-id="b33a0-128">-Version</span></span>
<span data-ttu-id="b33a0-129">[Ez a funkció korlátozott előzetes verzióban érhető el, kezdetben csak bizonyos előfizetések számára érhető el.] A Synapse SQL-készlet verziója.</span><span class="sxs-lookup"><span data-stu-id="b33a0-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="b33a0-130">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="b33a0-130">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b33a0-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b33a0-131">-WorkspaceName</span></span>
<span data-ttu-id="b33a0-132">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="b33a0-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b33a0-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b33a0-133">-WorkspaceObject</span></span>
<span data-ttu-id="b33a0-134">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="b33a0-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b33a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b33a0-135">CommonParameters</span></span>
<span data-ttu-id="b33a0-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b33a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b33a0-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b33a0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b33a0-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b33a0-138">INPUTS</span></span>

### <span data-ttu-id="b33a0-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b33a0-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b33a0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b33a0-140">OUTPUTS</span></span>

### <span data-ttu-id="b33a0-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b33a0-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="b33a0-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b33a0-142">NOTES</span></span>

## <span data-ttu-id="b33a0-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b33a0-143">RELATED LINKS</span></span>
