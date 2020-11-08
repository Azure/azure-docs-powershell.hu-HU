---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017479"
---
# <span data-ttu-id="be7c7-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="be7c7-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="be7c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="be7c7-103">A szinapszis-elemző Spark-medencét kapja.</span><span class="sxs-lookup"><span data-stu-id="be7c7-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="be7c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be7c7-104">SYNTAX</span></span>

### <span data-ttu-id="be7c7-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be7c7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be7c7-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be7c7-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be7c7-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be7c7-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be7c7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="be7c7-108">DESCRIPTION</span></span>
<span data-ttu-id="be7c7-109">A **Get-AzSynapseSparkPool** parancsmag információkat kap az Azure szinapszis Analytics Spark poolról.</span><span class="sxs-lookup"><span data-stu-id="be7c7-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="be7c7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="be7c7-110">EXAMPLES</span></span>

### <span data-ttu-id="be7c7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="be7c7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="be7c7-112">Ez a parancs egy munkaterület alatti összes szikra-készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="be7c7-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="be7c7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="be7c7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="be7c7-114">Ez a parancs a Spark-medencét a munkaterület ContosoWorkspace, a ContosoSparkPool név alatt kapja.</span><span class="sxs-lookup"><span data-stu-id="be7c7-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="be7c7-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="be7c7-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="be7c7-116">Ez a parancs a minden szikra-készletet egy munkaterületen keresztül, csővezetéken keresztül kapja.</span><span class="sxs-lookup"><span data-stu-id="be7c7-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="be7c7-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="be7c7-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="be7c7-118">Ez a parancs a megadott erőforrás-AZONOSÍTÓval rendelkező Spark-készletet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="be7c7-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="be7c7-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be7c7-119">PARAMETERS</span></span>

### <span data-ttu-id="be7c7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be7c7-120">-DefaultProfile</span></span>
<span data-ttu-id="be7c7-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be7c7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be7c7-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be7c7-122">-Name</span></span>
<span data-ttu-id="be7c7-123">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="be7c7-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7c7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be7c7-124">-ResourceGroupName</span></span>
<span data-ttu-id="be7c7-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="be7c7-125">Resource group name.</span></span>

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

### <span data-ttu-id="be7c7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be7c7-126">-ResourceId</span></span>
<span data-ttu-id="be7c7-127">A szinapszis szikra készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="be7c7-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="be7c7-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="be7c7-128">-WorkspaceName</span></span>
<span data-ttu-id="be7c7-129">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="be7c7-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="be7c7-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="be7c7-130">-WorkspaceObject</span></span>
<span data-ttu-id="be7c7-131">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="be7c7-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="be7c7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be7c7-132">CommonParameters</span></span>
<span data-ttu-id="be7c7-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be7c7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be7c7-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="be7c7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be7c7-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be7c7-135">INPUTS</span></span>

### <span data-ttu-id="be7c7-136">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="be7c7-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="be7c7-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be7c7-137">OUTPUTS</span></span>

### <span data-ttu-id="be7c7-138">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="be7c7-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="be7c7-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be7c7-139">NOTES</span></span>

## <span data-ttu-id="be7c7-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be7c7-140">RELATED LINKS</span></span>
