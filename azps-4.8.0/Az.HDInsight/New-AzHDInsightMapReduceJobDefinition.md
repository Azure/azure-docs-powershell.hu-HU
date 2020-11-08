---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 45278426ee25337bd484a46b533c72f49dbe9586
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024772"
---
# <span data-ttu-id="6cc72-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6cc72-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="6cc72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cc72-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc72-103">Létrehoz egy MapReduce.</span><span class="sxs-lookup"><span data-stu-id="6cc72-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="6cc72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cc72-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cc72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cc72-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc72-106">A **New-AzHDInsightMapReduceJobDefinition** parancsmag új MapReduce-feladatot határoz meg az Azure HDInsight-fürtökkel való használathoz.</span><span class="sxs-lookup"><span data-stu-id="6cc72-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6cc72-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6cc72-107">EXAMPLES</span></span>

### <span data-ttu-id="6cc72-108">Példa 1: MapReduce-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="6cc72-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="6cc72-109">Ez a parancs létrehoz egy MapReduce-feladatdefiníció.</span><span class="sxs-lookup"><span data-stu-id="6cc72-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="6cc72-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cc72-110">PARAMETERS</span></span>

### <span data-ttu-id="6cc72-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="6cc72-111">-Arguments</span></span>
<span data-ttu-id="6cc72-112">A feladathoz tartozó argumentumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc72-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="6cc72-113">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="6cc72-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="6cc72-114">-Osztálynév</span><span class="sxs-lookup"><span data-stu-id="6cc72-114">-ClassName</span></span>
<span data-ttu-id="6cc72-115">A JAR-fájlban lévő Job osztályt adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc72-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="6cc72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc72-116">-DefaultProfile</span></span>
<span data-ttu-id="6cc72-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6cc72-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cc72-118">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="6cc72-118">-Defines</span></span>
<span data-ttu-id="6cc72-119">Itt adhatja meg a Hadoop konfigurációs értékeit, amelyeket a feladat futásakor be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="6cc72-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="6cc72-120">-Files</span><span class="sxs-lookup"><span data-stu-id="6cc72-120">-Files</span></span>
<span data-ttu-id="6cc72-121">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc72-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="6cc72-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="6cc72-122">-JarFile</span></span>
<span data-ttu-id="6cc72-123">A feladathoz használni kívánt JAR-fájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc72-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="6cc72-124">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="6cc72-124">-JobName</span></span>
<span data-ttu-id="6cc72-125">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc72-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="6cc72-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="6cc72-126">-LibJars</span></span>
<span data-ttu-id="6cc72-127">A projekthez tartozó lib TÉGELYeket adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc72-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="6cc72-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="6cc72-128">-StatusFolder</span></span>
<span data-ttu-id="6cc72-129">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6cc72-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="6cc72-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc72-130">CommonParameters</span></span>
<span data-ttu-id="6cc72-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cc72-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc72-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc72-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc72-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cc72-133">INPUTS</span></span>

### <span data-ttu-id="6cc72-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="6cc72-134">None</span></span>

## <span data-ttu-id="6cc72-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cc72-135">OUTPUTS</span></span>

### <span data-ttu-id="6cc72-136">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6cc72-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="6cc72-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cc72-137">NOTES</span></span>

## <span data-ttu-id="6cc72-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cc72-138">RELATED LINKS</span></span>

[<span data-ttu-id="6cc72-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6cc72-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


