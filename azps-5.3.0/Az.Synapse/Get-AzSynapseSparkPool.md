---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383989"
---
# <span data-ttu-id="28550-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="28550-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="28550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28550-102">SYNOPSIS</span></span>
<span data-ttu-id="28550-103">Egy Synapse Analytics spark-készletet kap.</span><span class="sxs-lookup"><span data-stu-id="28550-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="28550-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="28550-104">SYNTAX</span></span>

### <span data-ttu-id="28550-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28550-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28550-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28550-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28550-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28550-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28550-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="28550-108">DESCRIPTION</span></span>
<span data-ttu-id="28550-109">A **Get-AzSynapseSparkPool** parancsmag információkat kap egy Azure Synapse Analytics Spark-készletről.</span><span class="sxs-lookup"><span data-stu-id="28550-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="28550-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="28550-110">EXAMPLES</span></span>

### <span data-ttu-id="28550-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="28550-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="28550-112">Ez a parancs az összes Spark-készletet egy munkaterület alá kapja.</span><span class="sxs-lookup"><span data-stu-id="28550-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="28550-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="28550-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="28550-114">Ez a parancs a ContosoWorkspace munkaterület alatti Spark-készletet kapja ContosoSparkPool néven.</span><span class="sxs-lookup"><span data-stu-id="28550-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="28550-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="28550-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="28550-116">Ez a parancs az összes Spark-készletet egy munkaterületen keresztül kapja meg folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="28550-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="28550-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="28550-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="28550-118">Ez a parancs a megadott erőforrás-azonosítójú sparkkészletet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="28550-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="28550-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28550-119">PARAMETERS</span></span>

### <span data-ttu-id="28550-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28550-120">-DefaultProfile</span></span>
<span data-ttu-id="28550-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28550-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28550-122">-Name</span><span class="sxs-lookup"><span data-stu-id="28550-122">-Name</span></span>
<span data-ttu-id="28550-123">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="28550-123">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="28550-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28550-124">-ResourceGroupName</span></span>
<span data-ttu-id="28550-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="28550-125">Resource group name.</span></span>

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

### <span data-ttu-id="28550-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28550-126">-ResourceId</span></span>
<span data-ttu-id="28550-127">A Synapse Spark készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="28550-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="28550-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="28550-128">-WorkspaceName</span></span>
<span data-ttu-id="28550-129">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="28550-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="28550-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="28550-130">-WorkspaceObject</span></span>
<span data-ttu-id="28550-131">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="28550-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="28550-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28550-132">CommonParameters</span></span>
<span data-ttu-id="28550-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28550-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28550-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28550-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28550-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28550-135">INPUTS</span></span>

### <span data-ttu-id="28550-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="28550-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="28550-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28550-137">OUTPUTS</span></span>

### <span data-ttu-id="28550-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="28550-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="28550-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="28550-139">NOTES</span></span>

## <span data-ttu-id="28550-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28550-140">RELATED LINKS</span></span>
