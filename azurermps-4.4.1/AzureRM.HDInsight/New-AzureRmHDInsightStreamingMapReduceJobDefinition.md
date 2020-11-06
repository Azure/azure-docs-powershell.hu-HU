---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 526f2005f1c6594128af7e259e2ccb0aa296a71b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504164"
---
# <span data-ttu-id="1fc59-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1fc59-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="1fc59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1fc59-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc59-103">Adatfolyam-MapReduce hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1fc59-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fc59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1fc59-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fc59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1fc59-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc59-106">A **New-AzureRmHDInsightStreamingMapReduceJobDefinition** parancsmag egy folyamatos átviteli MapReduce-objektumot határoz meg az Azure HDInsight-fürtökkel való használatra.</span><span class="sxs-lookup"><span data-stu-id="1fc59-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1fc59-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1fc59-107">EXAMPLES</span></span>

### <span data-ttu-id="1fc59-108">1. példa: adatfolyam-MapReduce-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="1fc59-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="1fc59-109">Ez a parancs adatfolyam-MapReduce hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1fc59-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="1fc59-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1fc59-110">PARAMETERS</span></span>

### <span data-ttu-id="1fc59-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="1fc59-111">-Arguments</span></span>
<span data-ttu-id="1fc59-112">A feladathoz tartozó argumentumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc59-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="1fc59-113">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="1fc59-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="1fc59-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="1fc59-114">-CommandEnvironment</span></span>
<span data-ttu-id="1fc59-115">A parancssori környezeti változók tömbjét adja meg, amelyet akkor állíthat be, ha egy feladat a munkavégző csomópontokon fut.</span><span class="sxs-lookup"><span data-stu-id="1fc59-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="1fc59-116">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="1fc59-116">-Defines</span></span>
<span data-ttu-id="1fc59-117">Itt adhatja meg a Hadoop konfigurációs értékeit, amelyeket a feladat futásakor be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="1fc59-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="1fc59-118">-Fájl</span><span class="sxs-lookup"><span data-stu-id="1fc59-118">-File</span></span>
<span data-ttu-id="1fc59-119">A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc59-119">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="1fc59-120">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="1fc59-120">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="1fc59-121">-Files</span><span class="sxs-lookup"><span data-stu-id="1fc59-121">-Files</span></span>
<span data-ttu-id="1fc59-122">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc59-122">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="1fc59-123">-InputPath</span><span class="sxs-lookup"><span data-stu-id="1fc59-123">-InputPath</span></span>
<span data-ttu-id="1fc59-124">A bemeneti fájlok elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc59-124">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="1fc59-125">-Mapper</span><span class="sxs-lookup"><span data-stu-id="1fc59-125">-Mapper</span></span>
<span data-ttu-id="1fc59-126">A Mapper-fájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc59-126">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="1fc59-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="1fc59-127">-OutputPath</span></span>
<span data-ttu-id="1fc59-128">A projekt kimenetének elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc59-128">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="1fc59-129">-Szűkítő</span><span class="sxs-lookup"><span data-stu-id="1fc59-129">-Reducer</span></span>
<span data-ttu-id="1fc59-130">A szűkítő fájlnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc59-130">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="1fc59-131">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="1fc59-131">-StatusFolder</span></span>
<span data-ttu-id="1fc59-132">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1fc59-132">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="1fc59-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc59-133">-DefaultProfile</span></span>
<span data-ttu-id="1fc59-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fc59-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc59-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc59-135">CommonParameters</span></span>
<span data-ttu-id="1fc59-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1fc59-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc59-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc59-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc59-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fc59-138">INPUTS</span></span>

## <span data-ttu-id="1fc59-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fc59-139">OUTPUTS</span></span>

### <span data-ttu-id="1fc59-140">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1fc59-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="1fc59-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1fc59-141">NOTES</span></span>

## <span data-ttu-id="1fc59-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fc59-142">RELATED LINKS</span></span>

[<span data-ttu-id="1fc59-143">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1fc59-143">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


