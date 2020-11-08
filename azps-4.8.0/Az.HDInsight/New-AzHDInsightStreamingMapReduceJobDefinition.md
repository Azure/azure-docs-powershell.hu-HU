---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: adfa71fb251950f1946b3a43f030ff32b656ec50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024769"
---
# <span data-ttu-id="1fbe7-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1fbe7-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="1fbe7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1fbe7-102">SYNOPSIS</span></span>
<span data-ttu-id="1fbe7-103">Adatfolyam-MapReduce hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="1fbe7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1fbe7-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fbe7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1fbe7-105">DESCRIPTION</span></span>
<span data-ttu-id="1fbe7-106">A **New-AzHDInsightStreamingMapReduceJobDefinition** parancsmag egy folyamatos átviteli MapReduce-objektumot határoz meg az Azure HDInsight-fürtökkel való használatra.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1fbe7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1fbe7-107">EXAMPLES</span></span>

### <span data-ttu-id="1fbe7-108">1. példa: adatfolyam-MapReduce-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="1fbe7-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="1fbe7-109">Ez a parancs adatfolyam-MapReduce hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="1fbe7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1fbe7-110">PARAMETERS</span></span>

### <span data-ttu-id="1fbe7-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="1fbe7-111">-Arguments</span></span>
<span data-ttu-id="1fbe7-112">A feladathoz tartozó argumentumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="1fbe7-113">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fbe7-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="1fbe7-114">-CommandEnvironment</span></span>
<span data-ttu-id="1fbe7-115">A parancssori környezeti változók tömbjét adja meg, amelyet akkor állíthat be, ha egy feladat a munkavégző csomópontokon fut.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fbe7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fbe7-116">-DefaultProfile</span></span>
<span data-ttu-id="1fbe7-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1fbe7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fbe7-118">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="1fbe7-118">-Defines</span></span>
<span data-ttu-id="1fbe7-119">Itt adhatja meg a Hadoop konfigurációs értékeit, amelyeket a feladat futásakor be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fbe7-120">-Fájl</span><span class="sxs-lookup"><span data-stu-id="1fbe7-120">-File</span></span>
<span data-ttu-id="1fbe7-121">A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="1fbe7-122">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="1fbe7-123">-Files</span><span class="sxs-lookup"><span data-stu-id="1fbe7-123">-Files</span></span>
<span data-ttu-id="1fbe7-124">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-124">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fbe7-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="1fbe7-125">-InputPath</span></span>
<span data-ttu-id="1fbe7-126">A bemeneti fájlok elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-126">Specifies the path to the input files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fbe7-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="1fbe7-127">-Mapper</span></span>
<span data-ttu-id="1fbe7-128">A Mapper-fájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="1fbe7-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="1fbe7-129">-OutputPath</span></span>
<span data-ttu-id="1fbe7-130">A projekt kimenetének elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="1fbe7-131">-Szűkítő</span><span class="sxs-lookup"><span data-stu-id="1fbe7-131">-Reducer</span></span>
<span data-ttu-id="1fbe7-132">A szűkítő fájlnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="1fbe7-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="1fbe7-133">-StatusFolder</span></span>
<span data-ttu-id="1fbe7-134">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1fbe7-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="1fbe7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fbe7-135">CommonParameters</span></span>
<span data-ttu-id="1fbe7-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1fbe7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fbe7-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fbe7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fbe7-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fbe7-138">INPUTS</span></span>

### <span data-ttu-id="1fbe7-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="1fbe7-139">None</span></span>

## <span data-ttu-id="1fbe7-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fbe7-140">OUTPUTS</span></span>

### <span data-ttu-id="1fbe7-141">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1fbe7-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="1fbe7-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1fbe7-142">NOTES</span></span>

## <span data-ttu-id="1fbe7-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fbe7-143">RELATED LINKS</span></span>

[<span data-ttu-id="1fbe7-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1fbe7-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


