---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187959"
---
# <span data-ttu-id="2e674-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="2e674-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="2e674-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e674-102">SYNOPSIS</span></span>
<span data-ttu-id="2e674-103">Egy szinapszis-elemző szikra munkát kap.</span><span class="sxs-lookup"><span data-stu-id="2e674-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="2e674-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e674-104">SYNTAX</span></span>

### <span data-ttu-id="2e674-105">GetSparkJobsByIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e674-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e674-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e674-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e674-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e674-107">DESCRIPTION</span></span>
<span data-ttu-id="2e674-108">A **Get-AzSynapseSparkJob** parancsmag az Azure szinapszis Analytics Spark-feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="2e674-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="2e674-109">Ha nem ad meg feladatot, ez a parancsmag minden feladatot beilleszt.</span><span class="sxs-lookup"><span data-stu-id="2e674-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="2e674-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2e674-110">EXAMPLES</span></span>

### <span data-ttu-id="2e674-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2e674-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="2e674-112">Ez a parancs egy Spark-medence alatti minden munkahelyhez jut.</span><span class="sxs-lookup"><span data-stu-id="2e674-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="2e674-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2e674-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="2e674-114">Ez a parancs a megadott AZONOSÍTÓval kapja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="2e674-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="2e674-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="2e674-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="2e674-116">Ez a parancs a megadott alkalmazásspecifikus AZONOSÍTÓval kapja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="2e674-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="2e674-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="2e674-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="2e674-118">Ez a parancs a szikra alatt a csővezetéken keresztül minden munkahelyhez bekerül.</span><span class="sxs-lookup"><span data-stu-id="2e674-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="2e674-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e674-119">PARAMETERS</span></span>

### <span data-ttu-id="2e674-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2e674-120">-ApplicationId</span></span>
<span data-ttu-id="2e674-121">A munkamenet alkalmazásspecifikus azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e674-121">The Application identifier of the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e674-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e674-122">-DefaultProfile</span></span>
<span data-ttu-id="2e674-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e674-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e674-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="2e674-124">-LivyId</span></span>
<span data-ttu-id="2e674-125">A Spark-feladat azonosítója</span><span class="sxs-lookup"><span data-stu-id="2e674-125">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e674-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e674-126">-Name</span></span>
<span data-ttu-id="2e674-127">A szikra munkahelyének neve.</span><span class="sxs-lookup"><span data-stu-id="2e674-127">Name of Spark job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e674-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="2e674-128">-SparkPoolName</span></span>
<span data-ttu-id="2e674-129">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="2e674-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e674-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="2e674-130">-SparkPoolObject</span></span>
<span data-ttu-id="2e674-131">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="2e674-131">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetSparkJobsByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e674-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2e674-132">-WorkspaceName</span></span>
<span data-ttu-id="2e674-133">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="2e674-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e674-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e674-134">CommonParameters</span></span>
<span data-ttu-id="2e674-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e674-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e674-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e674-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e674-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e674-137">INPUTS</span></span>

### <span data-ttu-id="2e674-138">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="2e674-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="2e674-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e674-139">OUTPUTS</span></span>

### <span data-ttu-id="2e674-140">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="2e674-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="2e674-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e674-141">NOTES</span></span>

## <span data-ttu-id="2e674-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e674-142">RELATED LINKS</span></span>
