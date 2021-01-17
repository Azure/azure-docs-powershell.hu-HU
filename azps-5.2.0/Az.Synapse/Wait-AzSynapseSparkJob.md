---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372678"
---
# <span data-ttu-id="40d47-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="40d47-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="40d47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40d47-102">SYNOPSIS</span></span>
<span data-ttu-id="40d47-103">Megvárja, amíg befejeződik a Synapse Analytics Spark-feladat.</span><span class="sxs-lookup"><span data-stu-id="40d47-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="40d47-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40d47-104">SYNTAX</span></span>

### <span data-ttu-id="40d47-105">WaitSparkByByIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40d47-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40d47-106">WaitSparkByByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d47-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40d47-107">WaitSparkByByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d47-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40d47-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40d47-108">DESCRIPTION</span></span>
<span data-ttu-id="40d47-109">A **Wait-AzSynapseSpark Job** parancsmag megvárja, amíg befejeződik az Azure Synapse Analytics-feladat.</span><span class="sxs-lookup"><span data-stu-id="40d47-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="40d47-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40d47-110">EXAMPLES</span></span>

### <span data-ttu-id="40d47-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="40d47-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="40d47-112">Ez a parancs megvárja, amíg a megadott azonosítójú feladat befejeződik.</span><span class="sxs-lookup"><span data-stu-id="40d47-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="40d47-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40d47-113">PARAMETERS</span></span>

### <span data-ttu-id="40d47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d47-114">-DefaultProfile</span></span>
<span data-ttu-id="40d47-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40d47-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d47-116">-SiyId</span><span class="sxs-lookup"><span data-stu-id="40d47-116">-LivyId</span></span>
<span data-ttu-id="40d47-117">Az értékgörbe-feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="40d47-117">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdParameterSet, WaitSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d47-118">-SparkObject</span><span class="sxs-lookup"><span data-stu-id="40d47-118">-SparkJobObject</span></span>
<span data-ttu-id="40d47-119">Spark job input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="40d47-119">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40d47-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="40d47-120">-SparkPoolName</span></span>
<span data-ttu-id="40d47-121">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="40d47-121">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d47-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="40d47-122">-SparkPoolObject</span></span>
<span data-ttu-id="40d47-123">Spark pool input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="40d47-123">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: WaitSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40d47-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="40d47-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="40d47-125">A maximális várakozási idő a hiba előtt. Az alapértelmezett érték az, hogy soha ne időtúllépést.</span><span class="sxs-lookup"><span data-stu-id="40d47-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="40d47-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="40d47-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="40d47-127">A feladat állapotának ellenőrzése közötti szavazási időköz másodpercben.</span><span class="sxs-lookup"><span data-stu-id="40d47-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="40d47-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="40d47-128">-WorkspaceName</span></span>
<span data-ttu-id="40d47-129">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="40d47-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d47-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d47-130">CommonParameters</span></span>
<span data-ttu-id="40d47-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d47-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d47-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40d47-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d47-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40d47-133">INPUTS</span></span>

### <span data-ttu-id="40d47-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="40d47-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="40d47-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="40d47-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="40d47-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40d47-136">OUTPUTS</span></span>

### <span data-ttu-id="40d47-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40d47-137">System.Boolean</span></span>

## <span data-ttu-id="40d47-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40d47-138">NOTES</span></span>

## <span data-ttu-id="40d47-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40d47-139">RELATED LINKS</span></span>
