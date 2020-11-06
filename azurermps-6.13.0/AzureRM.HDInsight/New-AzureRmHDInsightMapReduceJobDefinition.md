---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 284bd75abb2a2deaeaf13ad6edeb16718cbcdacd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504423"
---
# <span data-ttu-id="cf32a-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cf32a-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="cf32a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf32a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf32a-103">Létrehoz egy MapReduce.</span><span class="sxs-lookup"><span data-stu-id="cf32a-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf32a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf32a-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf32a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf32a-105">DESCRIPTION</span></span>
<span data-ttu-id="cf32a-106">A **New-AzureRmHDInsightMapReduceJobDefinition** parancsmag új MapReduce-feladatot határoz meg az Azure HDInsight-fürtökkel való használathoz.</span><span class="sxs-lookup"><span data-stu-id="cf32a-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="cf32a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cf32a-107">EXAMPLES</span></span>

### <span data-ttu-id="cf32a-108">Példa 1: MapReduce-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="cf32a-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="cf32a-109">Ez a parancs létrehoz egy MapReduce-feladatdefiníció.</span><span class="sxs-lookup"><span data-stu-id="cf32a-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="cf32a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf32a-110">PARAMETERS</span></span>

### <span data-ttu-id="cf32a-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="cf32a-111">-Arguments</span></span>
<span data-ttu-id="cf32a-112">A feladathoz tartozó argumentumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf32a-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="cf32a-113">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="cf32a-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="cf32a-114">-Osztálynév</span><span class="sxs-lookup"><span data-stu-id="cf32a-114">-ClassName</span></span>
<span data-ttu-id="cf32a-115">A JAR-fájlban lévő Job osztályt adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf32a-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="cf32a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf32a-116">-DefaultProfile</span></span>
<span data-ttu-id="cf32a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cf32a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf32a-118">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="cf32a-118">-Defines</span></span>
<span data-ttu-id="cf32a-119">Itt adhatja meg a Hadoop konfigurációs értékeit, amelyeket a feladat futásakor be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="cf32a-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="cf32a-120">-Files</span><span class="sxs-lookup"><span data-stu-id="cf32a-120">-Files</span></span>
<span data-ttu-id="cf32a-121">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf32a-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="cf32a-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="cf32a-122">-JarFile</span></span>
<span data-ttu-id="cf32a-123">A feladathoz használni kívánt JAR-fájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf32a-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="cf32a-124">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="cf32a-124">-JobName</span></span>
<span data-ttu-id="cf32a-125">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf32a-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="cf32a-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="cf32a-126">-LibJars</span></span>
<span data-ttu-id="cf32a-127">A projekthez tartozó lib TÉGELYeket adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf32a-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="cf32a-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="cf32a-128">-StatusFolder</span></span>
<span data-ttu-id="cf32a-129">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cf32a-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="cf32a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf32a-130">CommonParameters</span></span>
<span data-ttu-id="cf32a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf32a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf32a-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf32a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf32a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf32a-133">INPUTS</span></span>

### <span data-ttu-id="cf32a-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="cf32a-134">None</span></span>

## <span data-ttu-id="cf32a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf32a-135">OUTPUTS</span></span>

### <span data-ttu-id="cf32a-136">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cf32a-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="cf32a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf32a-137">NOTES</span></span>

## <span data-ttu-id="cf32a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf32a-138">RELATED LINKS</span></span>

[<span data-ttu-id="cf32a-139">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cf32a-139">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


