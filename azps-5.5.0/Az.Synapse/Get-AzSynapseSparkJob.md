---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162851"
---
# <span data-ttu-id="25d6a-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="25d6a-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="25d6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="25d6a-103">Synapse Analytics Spark-feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="25d6a-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="25d6a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25d6a-104">SYNTAX</span></span>

### <span data-ttu-id="25d6a-105">GetSparkBeállítássByIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25d6a-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d6a-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25d6a-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25d6a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25d6a-107">DESCRIPTION</span></span>
<span data-ttu-id="25d6a-108">A **Get-AzSynapseSpark Job** parancsmag egy Azure Synapse Analytics Spark-feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="25d6a-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="25d6a-109">Ha nem ad meg feladatot, ez a parancsmag kapja meg az összes feladatot.</span><span class="sxs-lookup"><span data-stu-id="25d6a-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="25d6a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25d6a-110">EXAMPLES</span></span>

### <span data-ttu-id="25d6a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="25d6a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="25d6a-112">Ez a parancs az összes munkakört egy értékkészlet alatt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="25d6a-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="25d6a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="25d6a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="25d6a-114">Ez a parancs a megadott azonosítóval kapja meg a feladatot.</span><span class="sxs-lookup"><span data-stu-id="25d6a-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="25d6a-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="25d6a-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="25d6a-116">Ez a parancs a megadott alkalmazásazonosítóval kapja meg a feladatot.</span><span class="sxs-lookup"><span data-stu-id="25d6a-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="25d6a-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="25d6a-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="25d6a-118">Ez a parancs egy sparkkészlet alatt található összes feladathoz folyamaton keresztül jut el.</span><span class="sxs-lookup"><span data-stu-id="25d6a-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="25d6a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25d6a-119">PARAMETERS</span></span>

### <span data-ttu-id="25d6a-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="25d6a-120">-ApplicationId</span></span>
<span data-ttu-id="25d6a-121">A munkamenet alkalmazásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="25d6a-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="25d6a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d6a-122">-DefaultProfile</span></span>
<span data-ttu-id="25d6a-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25d6a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25d6a-124">-SiyId</span><span class="sxs-lookup"><span data-stu-id="25d6a-124">-LivyId</span></span>
<span data-ttu-id="25d6a-125">Az értékgörbe-feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="25d6a-125">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="25d6a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="25d6a-126">-Name</span></span>
<span data-ttu-id="25d6a-127">Az Értékgörbe-feladat neve.</span><span class="sxs-lookup"><span data-stu-id="25d6a-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="25d6a-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="25d6a-128">-SparkPoolName</span></span>
<span data-ttu-id="25d6a-129">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="25d6a-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="25d6a-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="25d6a-130">-SparkPoolObject</span></span>
<span data-ttu-id="25d6a-131">Spark pool input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="25d6a-131">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="25d6a-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="25d6a-132">-WorkspaceName</span></span>
<span data-ttu-id="25d6a-133">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="25d6a-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="25d6a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d6a-134">CommonParameters</span></span>
<span data-ttu-id="25d6a-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d6a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d6a-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25d6a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d6a-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25d6a-137">INPUTS</span></span>

### <span data-ttu-id="25d6a-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="25d6a-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="25d6a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25d6a-139">OUTPUTS</span></span>

### <span data-ttu-id="25d6a-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="25d6a-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="25d6a-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25d6a-141">NOTES</span></span>

## <span data-ttu-id="25d6a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25d6a-142">RELATED LINKS</span></span>
