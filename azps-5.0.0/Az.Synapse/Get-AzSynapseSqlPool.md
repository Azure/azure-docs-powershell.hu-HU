---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: d37012ee5188b6dea15968aee8659387e06a87f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186610"
---
# <span data-ttu-id="4c49e-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4c49e-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="4c49e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c49e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c49e-103">A szinapszis Analytics SQL-készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="4c49e-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4c49e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c49e-104">SYNTAX</span></span>

### <span data-ttu-id="4c49e-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c49e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c49e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c49e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c49e-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c49e-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c49e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c49e-108">DESCRIPTION</span></span>
<span data-ttu-id="4c49e-109">A **Get-AzSynapseSqlPool** parancsmag információkat kap az Azure SZINAPSZIS Analytics SQL poolról.</span><span class="sxs-lookup"><span data-stu-id="4c49e-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4c49e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4c49e-110">EXAMPLES</span></span>

### <span data-ttu-id="4c49e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4c49e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="4c49e-112">Ez a parancs minden SQL-készletet beolvas egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="4c49e-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="4c49e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4c49e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="4c49e-114">Ez a parancs az SQL-készletet az ContosoSqlPool nevű munkaterület-ContosoWorkspace kapja.</span><span class="sxs-lookup"><span data-stu-id="4c49e-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="4c49e-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="4c49e-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="4c49e-116">Ez a parancs az összes SQL-készletet egy munkaterületen keresztül, a csővezetéken keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4c49e-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="4c49e-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="4c49e-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="4c49e-118">Ez a parancs az SQL-készletet a megadott erőforrás-AZONOSÍTÓval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4c49e-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="4c49e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c49e-119">PARAMETERS</span></span>

### <span data-ttu-id="4c49e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c49e-120">-DefaultProfile</span></span>
<span data-ttu-id="4c49e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c49e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c49e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c49e-122">-Name</span></span>
<span data-ttu-id="4c49e-123">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="4c49e-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c49e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c49e-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c49e-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4c49e-125">Resource group name.</span></span>

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

### <span data-ttu-id="4c49e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c49e-126">-ResourceId</span></span>
<span data-ttu-id="4c49e-127">A szinapszis SQL Pool erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4c49e-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="4c49e-128">-Verzió</span><span class="sxs-lookup"><span data-stu-id="4c49e-128">-Version</span></span>
<span data-ttu-id="4c49e-129">[Ez a funkció egy korlátozott előzetes verzió, amely eredetileg csak bizonyos előfizetésekhez érhető el.] A szinapszis SQL Pool verziója.</span><span class="sxs-lookup"><span data-stu-id="4c49e-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="4c49e-130">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="4c49e-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="4c49e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4c49e-131">-WorkspaceName</span></span>
<span data-ttu-id="4c49e-132">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="4c49e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4c49e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4c49e-133">-WorkspaceObject</span></span>
<span data-ttu-id="4c49e-134">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="4c49e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4c49e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c49e-135">CommonParameters</span></span>
<span data-ttu-id="4c49e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c49e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c49e-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4c49e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c49e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c49e-138">INPUTS</span></span>

### <span data-ttu-id="4c49e-139">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4c49e-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4c49e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c49e-140">OUTPUTS</span></span>

### <span data-ttu-id="4c49e-141">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4c49e-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4c49e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c49e-142">NOTES</span></span>

## <span data-ttu-id="4c49e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c49e-143">RELATED LINKS</span></span>
