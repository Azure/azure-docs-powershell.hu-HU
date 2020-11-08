---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 824F6302-6285-4AEC-A63C-E2519DE4C7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2597d66e87de682bbf5702085612f7338d75deac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016009"
---
# <span data-ttu-id="da7a7-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="da7a7-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="da7a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da7a7-102">SYNOPSIS</span></span>
<span data-ttu-id="da7a7-103">Új adatfolyam-MapReduce-feladatot határoz meg.</span><span class="sxs-lookup"><span data-stu-id="da7a7-103">Defines a new streaming MapReduce job.</span></span>

## <span data-ttu-id="da7a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da7a7-104">SYNTAX</span></span>

```
New-AzureHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-CmdEnv <String[]>]
 [-Combiner <String>] [-Defines <Hashtable>] [-Files <String[]>] [-InputPath <String>] [-JobName <String>]
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="da7a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da7a7-105">DESCRIPTION</span></span>
<span data-ttu-id="da7a7-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="da7a7-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="da7a7-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="da7a7-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="da7a7-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="da7a7-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="da7a7-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="da7a7-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="da7a7-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="da7a7-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="da7a7-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="da7a7-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="da7a7-112">A **New-AzureHDInsightStreamingMapReduceJobDefinition** parancsmag olyan új feladatdefiníció-objektumot határoz meg, amely a Hadoop-adatfolyam-feladatok paramétereit jelöli.</span><span class="sxs-lookup"><span data-stu-id="da7a7-112">The **New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet defines a new job definition object that represents the parameters of a Hadoop streaming job.</span></span>

## <span data-ttu-id="da7a7-113">Példák</span><span class="sxs-lookup"><span data-stu-id="da7a7-113">EXAMPLES</span></span>

### <span data-ttu-id="da7a7-114">1. példa: adatfolyam-MapReduce-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="da7a7-114">Example 1: Create a streaming MapReduce job definition</span></span>
```
PS C:\>$StreamingWordCount = New-AzureHDInsightStreamingMapReduceJobDefinition -Files "/Example/Apps/WordCount.exe", "/Example/Apps/Cat.exe" -InputPath "/Example/Data/Gutenberg/Davinci.txt" -OutputPath "/Example/Data/StreamingOutput/WordCount.txt" -Mapper "Cat.exe" -Reducer "WordCount.exe"
```

<span data-ttu-id="da7a7-115">Ez a parancs létrehozza a megadott adatfolyam-MapReduce, majd a $StreamingWordCount változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="da7a7-115">This command creates the specified streaming MapReduce job definition, and then stores it in the $StreamingWordCount variable.</span></span>

## <span data-ttu-id="da7a7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da7a7-116">PARAMETERS</span></span>

### <span data-ttu-id="da7a7-117">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="da7a7-117">-Arguments</span></span>
<span data-ttu-id="da7a7-118">Argumentumokat ad meg egy Hadoop-feladathoz.</span><span class="sxs-lookup"><span data-stu-id="da7a7-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="da7a7-119">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="da7a7-119">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-120">-CmdEnv</span><span class="sxs-lookup"><span data-stu-id="da7a7-120">-CmdEnv</span></span>
<span data-ttu-id="da7a7-121">A parancssori környezeti változók tömbök sorát adja meg, amelyekkel beállítható, hogy egy feladat az adatcsomópontokon fusson.</span><span class="sxs-lookup"><span data-stu-id="da7a7-121">Specifies an array of command-line environment variables to set when a job runs on data nodes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-122">-Combining</span><span class="sxs-lookup"><span data-stu-id="da7a7-122">-Combiner</span></span>
<span data-ttu-id="da7a7-123">Egy kombináló fájlnevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="da7a7-123">Specifies a Combiner file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-124">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="da7a7-124">-Defines</span></span>
<span data-ttu-id="da7a7-125">Itt adhatja meg a Hadoop konfigurációs értékeit a feladat futásakor.</span><span class="sxs-lookup"><span data-stu-id="da7a7-125">Specifies Hadoop configuration values to set when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-126">-Files</span><span class="sxs-lookup"><span data-stu-id="da7a7-126">-Files</span></span>
<span data-ttu-id="da7a7-127">A projekthez szükséges fájlok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da7a7-127">Specifies an array of files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-128">-InputPath</span><span class="sxs-lookup"><span data-stu-id="da7a7-128">-InputPath</span></span>
<span data-ttu-id="da7a7-129">A bemeneti fájlok WASB elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="da7a7-129">Specifies the WASB path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Input

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-130">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="da7a7-130">-JobName</span></span>
<span data-ttu-id="da7a7-131">Az új MapReduce-feladatdefiníció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da7a7-131">Specifies the name of the new MapReduce job definition.</span></span>
<span data-ttu-id="da7a7-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="da7a7-132">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-133">-Mapper</span><span class="sxs-lookup"><span data-stu-id="da7a7-133">-Mapper</span></span>
<span data-ttu-id="da7a7-134">A Mapper-fájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da7a7-134">Specifies a Mapper file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-135">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="da7a7-135">-OutputPath</span></span>
<span data-ttu-id="da7a7-136">A projekt kimenetének WASB elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="da7a7-136">Specifies the WASB path for the job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Output

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="da7a7-137">-Profile</span></span>
<span data-ttu-id="da7a7-138">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="da7a7-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da7a7-139">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="da7a7-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-140">-Szűkítő</span><span class="sxs-lookup"><span data-stu-id="da7a7-140">-Reducer</span></span>
<span data-ttu-id="da7a7-141">A szűkítő fájlnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da7a7-141">Specifies a Reducer file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-142">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="da7a7-142">-StatusFolder</span></span>
<span data-ttu-id="da7a7-143">Azt a mappát adja meg, amely a projekthez tartozó normál kimeneteket és hibák kimenetét tartalmazza, valamint a kilépési kódot és a tevékenység naplóit.</span><span class="sxs-lookup"><span data-stu-id="da7a7-143">Specifies the folder that contains the standard outputs and error outputs for the job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7a7-144">CommonParameters</span></span>
<span data-ttu-id="da7a7-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da7a7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7a7-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da7a7-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7a7-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da7a7-147">INPUTS</span></span>

## <span data-ttu-id="da7a7-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da7a7-148">OUTPUTS</span></span>

## <span data-ttu-id="da7a7-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da7a7-149">NOTES</span></span>

## <span data-ttu-id="da7a7-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da7a7-150">RELATED LINKS</span></span>

[<span data-ttu-id="da7a7-151">Új – AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="da7a7-151">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="da7a7-152">Új – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="da7a7-152">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="da7a7-153">Új – AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="da7a7-153">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="da7a7-154">Új – AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="da7a7-154">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)


