---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 7b3bce866712565b5eeb6fc9deccc64f9da69891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504972"
---
# <span data-ttu-id="54d28-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="54d28-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="54d28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54d28-102">SYNOPSIS</span></span>
<span data-ttu-id="54d28-103">Létrehoz egy MapReduce.</span><span class="sxs-lookup"><span data-stu-id="54d28-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54d28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54d28-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54d28-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54d28-105">DESCRIPTION</span></span>
<span data-ttu-id="54d28-106">A **New-AzureRmHDInsightMapReduceJobDefinition** parancsmag új MapReduce-feladatot határoz meg az Azure HDInsight-fürtökkel való használathoz.</span><span class="sxs-lookup"><span data-stu-id="54d28-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="54d28-107">Példák</span><span class="sxs-lookup"><span data-stu-id="54d28-107">EXAMPLES</span></span>

### <span data-ttu-id="54d28-108">Példa 1: MapReduce-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="54d28-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="54d28-109">Ez a parancs létrehoz egy MapReduce-feladatdefiníció.</span><span class="sxs-lookup"><span data-stu-id="54d28-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="54d28-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54d28-110">PARAMETERS</span></span>

### <span data-ttu-id="54d28-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="54d28-111">-Arguments</span></span>
<span data-ttu-id="54d28-112">A feladathoz tartozó argumentumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54d28-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="54d28-113">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="54d28-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="54d28-114">-Osztálynév</span><span class="sxs-lookup"><span data-stu-id="54d28-114">-ClassName</span></span>
<span data-ttu-id="54d28-115">A JAR-fájlban lévő Job osztályt adja meg.</span><span class="sxs-lookup"><span data-stu-id="54d28-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="54d28-116">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="54d28-116">-Defines</span></span>
<span data-ttu-id="54d28-117">Itt adhatja meg a Hadoop konfigurációs értékeit, amelyeket a feladat futásakor be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="54d28-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="54d28-118">-Files</span><span class="sxs-lookup"><span data-stu-id="54d28-118">-Files</span></span>
<span data-ttu-id="54d28-119">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54d28-119">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="54d28-120">-JarFile</span><span class="sxs-lookup"><span data-stu-id="54d28-120">-JarFile</span></span>
<span data-ttu-id="54d28-121">A feladathoz használni kívánt JAR-fájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="54d28-121">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="54d28-122">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="54d28-122">-JobName</span></span>
<span data-ttu-id="54d28-123">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54d28-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="54d28-124">-LibJars</span><span class="sxs-lookup"><span data-stu-id="54d28-124">-LibJars</span></span>
<span data-ttu-id="54d28-125">A projekthez tartozó lib TÉGELYeket adja meg.</span><span class="sxs-lookup"><span data-stu-id="54d28-125">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="54d28-126">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="54d28-126">-StatusFolder</span></span>
<span data-ttu-id="54d28-127">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimeneteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="54d28-127">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="54d28-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d28-128">-DefaultProfile</span></span>
<span data-ttu-id="54d28-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54d28-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54d28-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d28-130">CommonParameters</span></span>
<span data-ttu-id="54d28-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54d28-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d28-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d28-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d28-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54d28-133">INPUTS</span></span>

## <span data-ttu-id="54d28-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54d28-134">OUTPUTS</span></span>

### <span data-ttu-id="54d28-135">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="54d28-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="54d28-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54d28-136">NOTES</span></span>

## <span data-ttu-id="54d28-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54d28-137">RELATED LINKS</span></span>

[<span data-ttu-id="54d28-138">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="54d28-138">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

