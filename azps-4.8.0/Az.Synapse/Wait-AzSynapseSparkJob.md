---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183454"
---
# <span data-ttu-id="08858-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="08858-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="08858-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08858-102">SYNOPSIS</span></span>
<span data-ttu-id="08858-103">Várakozás a szinapszis-statisztika kitöltésére.</span><span class="sxs-lookup"><span data-stu-id="08858-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="08858-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08858-104">SYNTAX</span></span>

### <span data-ttu-id="08858-105">WaitSparkJobByIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08858-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08858-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08858-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08858-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08858-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08858-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="08858-108">DESCRIPTION</span></span>
<span data-ttu-id="08858-109">A **WAIT-AzSynapseSparkJob** parancsmag várja az Azure szinapszis Analytics-feladatot a befejezéshez.</span><span class="sxs-lookup"><span data-stu-id="08858-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="08858-110">Példák</span><span class="sxs-lookup"><span data-stu-id="08858-110">EXAMPLES</span></span>

### <span data-ttu-id="08858-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08858-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="08858-112">A parancs megvárja, hogy a megadott azonosítót végrehajtva végezze el a feladatot.</span><span class="sxs-lookup"><span data-stu-id="08858-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="08858-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08858-113">PARAMETERS</span></span>

### <span data-ttu-id="08858-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08858-114">-DefaultProfile</span></span>
<span data-ttu-id="08858-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08858-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08858-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="08858-116">-LivyId</span></span>
<span data-ttu-id="08858-117">A Spark-feladat azonosítója</span><span class="sxs-lookup"><span data-stu-id="08858-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="08858-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="08858-118">-SparkJobObject</span></span>
<span data-ttu-id="08858-119">Szikra a projekt bemeneti objektuma, általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="08858-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="08858-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="08858-120">-SparkPoolName</span></span>
<span data-ttu-id="08858-121">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="08858-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="08858-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="08858-122">-SparkPoolObject</span></span>
<span data-ttu-id="08858-123">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="08858-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="08858-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="08858-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="08858-125">A hiba kijavítása előtt megvárni kívánt maximális idő. Az alapértelmezett érték az, hogy soha ne legyen időtúllépés.</span><span class="sxs-lookup"><span data-stu-id="08858-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="08858-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="08858-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="08858-127">A lekérdezési intervallum a feladat állapotának ellenőrzése között másodpercben.</span><span class="sxs-lookup"><span data-stu-id="08858-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="08858-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="08858-128">-WorkspaceName</span></span>
<span data-ttu-id="08858-129">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="08858-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="08858-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08858-130">CommonParameters</span></span>
<span data-ttu-id="08858-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08858-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08858-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="08858-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08858-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08858-133">INPUTS</span></span>

### <span data-ttu-id="08858-134">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="08858-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="08858-135">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="08858-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="08858-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08858-136">OUTPUTS</span></span>

### <span data-ttu-id="08858-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08858-137">System.Boolean</span></span>

## <span data-ttu-id="08858-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08858-138">NOTES</span></span>

## <span data-ttu-id="08858-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08858-139">RELATED LINKS</span></span>
