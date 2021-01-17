---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 4f9fe1ef3ab16812553eb6ea22909ce37bd5ee69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469658"
---
# <span data-ttu-id="b9d77-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b9d77-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="b9d77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9d77-102">SYNOPSIS</span></span>
<span data-ttu-id="b9d77-103">Létrehozza a Streaming MapReduce feladatobjektumot.</span><span class="sxs-lookup"><span data-stu-id="b9d77-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="b9d77-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9d77-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9d77-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9d77-105">DESCRIPTION</span></span>
<span data-ttu-id="b9d77-106">A **New-AzHDInsightStreamingMapReduce JobDefinition** parancsmag definiálja a Streaming MapReduce job objectot azure HDInsight-fürthöz való használatra.</span><span class="sxs-lookup"><span data-stu-id="b9d77-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b9d77-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9d77-107">EXAMPLES</span></span>

### <span data-ttu-id="b9d77-108">1. példa: Streaming MapReduce feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="b9d77-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="b9d77-109">Ez a parancs létrehozza a Streaming MapReduce feladatdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="b9d77-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="b9d77-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9d77-110">PARAMETERS</span></span>

### <span data-ttu-id="b9d77-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="b9d77-111">-Arguments</span></span>
<span data-ttu-id="b9d77-112">Egy tömböt ad meg a feladat argumentumaiból.</span><span class="sxs-lookup"><span data-stu-id="b9d77-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="b9d77-113">Az argumentumokat a függvény parancssori argumentumként minden tevékenységnek továbbkűni.</span><span class="sxs-lookup"><span data-stu-id="b9d77-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="b9d77-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="b9d77-114">-CommandEnvironment</span></span>
<span data-ttu-id="b9d77-115">Parancssori környezeti változók tömbje, amelyek akkor állíthatók be, amikor egy feladat munkavégi csomópontokon fut.</span><span class="sxs-lookup"><span data-stu-id="b9d77-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="b9d77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9d77-116">-DefaultProfile</span></span>
<span data-ttu-id="b9d77-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b9d77-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9d77-118">-Definiál</span><span class="sxs-lookup"><span data-stu-id="b9d77-118">-Defines</span></span>
<span data-ttu-id="b9d77-119">Megadja a Hadoop konfigurációs értékeit, amelyek a feladat futtatásakor adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="b9d77-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="b9d77-120">-File</span><span class="sxs-lookup"><span data-stu-id="b9d77-120">-File</span></span>
<span data-ttu-id="b9d77-121">A futtatni kívánt lekérdezést tartalmazó fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9d77-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="b9d77-122">Ezt a paramétert használhatja a *Lekérdezés paraméter* helyett.</span><span class="sxs-lookup"><span data-stu-id="b9d77-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b9d77-123">-Files</span><span class="sxs-lookup"><span data-stu-id="b9d77-123">-Files</span></span>
<span data-ttu-id="b9d77-124">A Hive-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9d77-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b9d77-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="b9d77-125">-InputPath</span></span>
<span data-ttu-id="b9d77-126">A bemeneti fájlok elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9d77-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="b9d77-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="b9d77-127">-Mapper</span></span>
<span data-ttu-id="b9d77-128">Egy Mapper-fájlnevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="b9d77-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="b9d77-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b9d77-129">-OutputPath</span></span>
<span data-ttu-id="b9d77-130">A feladat kimenetének elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9d77-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="b9d77-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="b9d77-131">-Reducer</span></span>
<span data-ttu-id="b9d77-132">Egy reducer fájlnevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="b9d77-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="b9d77-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b9d77-133">-StatusFolder</span></span>
<span data-ttu-id="b9d77-134">Megadja annak a mappának a helyét, amely a feladat normál kimenetét és hibakimenetét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b9d77-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b9d77-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9d77-135">CommonParameters</span></span>
<span data-ttu-id="b9d77-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9d77-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9d77-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9d77-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9d77-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9d77-138">INPUTS</span></span>

### <span data-ttu-id="b9d77-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="b9d77-139">None</span></span>

## <span data-ttu-id="b9d77-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9d77-140">OUTPUTS</span></span>

### <span data-ttu-id="b9d77-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduce ParanccsDefinition</span><span class="sxs-lookup"><span data-stu-id="b9d77-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="b9d77-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9d77-142">NOTES</span></span>

## <span data-ttu-id="b9d77-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9d77-143">RELATED LINKS</span></span>

[<span data-ttu-id="b9d77-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b9d77-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


