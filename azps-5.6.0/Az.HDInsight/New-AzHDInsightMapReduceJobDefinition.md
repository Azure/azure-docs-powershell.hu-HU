---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 7ea8831b3fdb9f6d5b11f5419f05dd34313d100f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013590"
---
# <span data-ttu-id="17b89-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="17b89-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="17b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b89-102">SYNOPSIS</span></span>
<span data-ttu-id="17b89-103">MapReduce-feladatobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="17b89-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="17b89-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="17b89-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17b89-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="17b89-105">DESCRIPTION</span></span>
<span data-ttu-id="17b89-106">A **New-AzHDInsightMapReduce JobDefinition** parancsmag új MapReduce-feladatot határoz meg azure HDInsight-fürthöz való használatra.</span><span class="sxs-lookup"><span data-stu-id="17b89-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="17b89-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="17b89-107">EXAMPLES</span></span>

### <span data-ttu-id="17b89-108">1. példa: MapReduce-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="17b89-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="17b89-109">Ezzel a paranccsal MapReduce-feladatdefiníciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="17b89-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="17b89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17b89-110">PARAMETERS</span></span>

### <span data-ttu-id="17b89-111">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="17b89-111">-Arguments</span></span>
<span data-ttu-id="17b89-112">Egy tömböt ad meg a feladat argumentumaiból.</span><span class="sxs-lookup"><span data-stu-id="17b89-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="17b89-113">Az argumentumokat a függvény parancssori argumentumként minden tevékenységnek továbbkűni.</span><span class="sxs-lookup"><span data-stu-id="17b89-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="17b89-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="17b89-114">-ClassName</span></span>
<span data-ttu-id="17b89-115">A JAR-fájlban található feladatosztályt adja meg.</span><span class="sxs-lookup"><span data-stu-id="17b89-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="17b89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b89-116">-DefaultProfile</span></span>
<span data-ttu-id="17b89-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="17b89-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17b89-118">-Definiál</span><span class="sxs-lookup"><span data-stu-id="17b89-118">-Defines</span></span>
<span data-ttu-id="17b89-119">Megadja a Hadoop konfigurációs értékeit, amelyek a feladat futtatásakor adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="17b89-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="17b89-120">-Files</span><span class="sxs-lookup"><span data-stu-id="17b89-120">-Files</span></span>
<span data-ttu-id="17b89-121">A Hive-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17b89-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="17b89-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="17b89-122">-JarFile</span></span>
<span data-ttu-id="17b89-123">A feladathoz használni kívánt JAR-fájl.</span><span class="sxs-lookup"><span data-stu-id="17b89-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="17b89-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="17b89-124">-JobName</span></span>
<span data-ttu-id="17b89-125">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17b89-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="17b89-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="17b89-126">-LibJars</span></span>
<span data-ttu-id="17b89-127">A feladathoz a lib JARS-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="17b89-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="17b89-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="17b89-128">-StatusFolder</span></span>
<span data-ttu-id="17b89-129">Megadja annak a mappának a helyét, amely a feladat normál kimenetét és hibakimenetét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="17b89-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="17b89-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b89-130">CommonParameters</span></span>
<span data-ttu-id="17b89-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b89-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b89-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17b89-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b89-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17b89-133">INPUTS</span></span>

### <span data-ttu-id="17b89-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="17b89-134">None</span></span>

## <span data-ttu-id="17b89-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17b89-135">OUTPUTS</span></span>

### <span data-ttu-id="17b89-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceÚtDefinition</span><span class="sxs-lookup"><span data-stu-id="17b89-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="17b89-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="17b89-137">NOTES</span></span>

## <span data-ttu-id="17b89-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17b89-138">RELATED LINKS</span></span>

[<span data-ttu-id="17b89-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="17b89-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


