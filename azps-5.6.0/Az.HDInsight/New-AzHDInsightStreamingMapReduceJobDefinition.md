---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 60e0f8e6799a89d673b3c9ca7de7827b197440fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922433"
---
# <span data-ttu-id="08e5e-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="08e5e-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="08e5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="08e5e-103">Létrehozza a Streaming MapReduce feladatobjektumot.</span><span class="sxs-lookup"><span data-stu-id="08e5e-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="08e5e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="08e5e-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08e5e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="08e5e-105">DESCRIPTION</span></span>
<span data-ttu-id="08e5e-106">A **New-AzHDInsightStreamingMapReduce JobDefinition** parancsmag definiálja a Streaming MapReduce job objectot azure HDInsight-fürthöz való használatra.</span><span class="sxs-lookup"><span data-stu-id="08e5e-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="08e5e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="08e5e-107">EXAMPLES</span></span>

### <span data-ttu-id="08e5e-108">1. példa: Streaming MapReduce feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="08e5e-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="08e5e-109">Ez a parancs létrehozza a Streaming MapReduce feladatdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="08e5e-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="08e5e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08e5e-110">PARAMETERS</span></span>

### <span data-ttu-id="08e5e-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="08e5e-111">-Arguments</span></span>
<span data-ttu-id="08e5e-112">Egy tömböt ad meg a feladat argumentumaiból.</span><span class="sxs-lookup"><span data-stu-id="08e5e-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="08e5e-113">Az argumentumokat a függvény parancssori argumentumként minden tevékenységnek továbbkűni.</span><span class="sxs-lookup"><span data-stu-id="08e5e-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="08e5e-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="08e5e-114">-CommandEnvironment</span></span>
<span data-ttu-id="08e5e-115">Parancssori környezeti változók tömbje, amelyek akkor állíthatók be, amikor egy feladat munkavégi csomópontokon fut.</span><span class="sxs-lookup"><span data-stu-id="08e5e-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="08e5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e5e-116">-DefaultProfile</span></span>
<span data-ttu-id="08e5e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="08e5e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08e5e-118">-Definiál</span><span class="sxs-lookup"><span data-stu-id="08e5e-118">-Defines</span></span>
<span data-ttu-id="08e5e-119">Megadja a Hadoop konfigurációs értékeit, amelyek a feladat futtatásakor adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="08e5e-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="08e5e-120">-File</span><span class="sxs-lookup"><span data-stu-id="08e5e-120">-File</span></span>
<span data-ttu-id="08e5e-121">A futtatni kívánt lekérdezést tartalmazó fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="08e5e-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="08e5e-122">Ezt a paramétert használhatja a *Lekérdezés paraméter* helyett.</span><span class="sxs-lookup"><span data-stu-id="08e5e-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="08e5e-123">-Files</span><span class="sxs-lookup"><span data-stu-id="08e5e-123">-Files</span></span>
<span data-ttu-id="08e5e-124">A Hive-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08e5e-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="08e5e-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="08e5e-125">-InputPath</span></span>
<span data-ttu-id="08e5e-126">A bemeneti fájlok elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="08e5e-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="08e5e-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="08e5e-127">-Mapper</span></span>
<span data-ttu-id="08e5e-128">Egy Mapper-fájlnevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="08e5e-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="08e5e-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="08e5e-129">-OutputPath</span></span>
<span data-ttu-id="08e5e-130">A feladat kimenetének elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="08e5e-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="08e5e-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="08e5e-131">-Reducer</span></span>
<span data-ttu-id="08e5e-132">Egy reducer fájlnevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="08e5e-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="08e5e-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="08e5e-133">-StatusFolder</span></span>
<span data-ttu-id="08e5e-134">Megadja annak a mappának a helyét, amely a feladat normál kimenetét és hibakimenetét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="08e5e-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="08e5e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e5e-135">CommonParameters</span></span>
<span data-ttu-id="08e5e-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e5e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e5e-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08e5e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e5e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08e5e-138">INPUTS</span></span>

### <span data-ttu-id="08e5e-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="08e5e-139">None</span></span>

## <span data-ttu-id="08e5e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08e5e-140">OUTPUTS</span></span>

### <span data-ttu-id="08e5e-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduce ParanccsDefinition</span><span class="sxs-lookup"><span data-stu-id="08e5e-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="08e5e-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="08e5e-142">NOTES</span></span>

## <span data-ttu-id="08e5e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08e5e-143">RELATED LINKS</span></span>

[<span data-ttu-id="08e5e-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="08e5e-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


