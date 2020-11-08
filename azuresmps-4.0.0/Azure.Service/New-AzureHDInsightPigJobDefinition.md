---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016010"
---
# <span data-ttu-id="00d71-101">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="00d71-101">New-AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="00d71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00d71-102">SYNOPSIS</span></span>
<span data-ttu-id="00d71-103">Új Pig-feladatot határoz meg egy HDInsight szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="00d71-103">Defines a new Pig job for an HDInsight service.</span></span>

## <span data-ttu-id="00d71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00d71-104">SYNTAX</span></span>

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00d71-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="00d71-105">DESCRIPTION</span></span>
<span data-ttu-id="00d71-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="00d71-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="00d71-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="00d71-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="00d71-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="00d71-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="00d71-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="00d71-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="00d71-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="00d71-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="00d71-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="00d71-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="00d71-112">A **New-AzureHDInsightPigJobDefinition** definiál egy disznó-feladatot az Azure HDInsight szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="00d71-112">The **New-AzureHDInsightPigJobDefinition** defines a Pig job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="00d71-113">Példák</span><span class="sxs-lookup"><span data-stu-id="00d71-113">EXAMPLES</span></span>

### <span data-ttu-id="00d71-114">Példa 1: új Pig-feladat definiálása</span><span class="sxs-lookup"><span data-stu-id="00d71-114">Example 1: Define a new Pig job</span></span>
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

<span data-ttu-id="00d71-115">Az első parancs a karakterlánc értékét deklarálja, majd a $0 változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="00d71-115">The first command declares a string value, and then stores in the $0 variable.</span></span>

<span data-ttu-id="00d71-116">A második parancs létrehoz egy disznó-feladatot, majd a $QueryString változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="00d71-116">The second command creates a Pig job query, and then stores it in the $QueryString variable.</span></span>

<span data-ttu-id="00d71-117">A végleges parancs létrehoz egy olyan disznó-munkadefiníciót, amely a lekérdezést használja a $QueryString-ban, majd a $PigJobDefinition változóban tárolja a feladatdefiníció értékét.</span><span class="sxs-lookup"><span data-stu-id="00d71-117">The final command creates a Pig job definition that uses the query in $QueryString, and then stores the job definition in the $PigJobDefinition variable.</span></span>

## <span data-ttu-id="00d71-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00d71-118">PARAMETERS</span></span>

### <span data-ttu-id="00d71-119">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="00d71-119">-Arguments</span></span>
<span data-ttu-id="00d71-120">Argumentumok tömbjét adja meg a sertések feladatához.</span><span class="sxs-lookup"><span data-stu-id="00d71-120">Specifies an array of arguments for a Pig job.</span></span>
<span data-ttu-id="00d71-121">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="00d71-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="00d71-122">-Fájl</span><span class="sxs-lookup"><span data-stu-id="00d71-122">-File</span></span>
<span data-ttu-id="00d71-123">A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="00d71-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="00d71-124">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="00d71-124">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d71-125">-Files</span><span class="sxs-lookup"><span data-stu-id="00d71-125">-Files</span></span>
<span data-ttu-id="00d71-126">A disznó-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00d71-126">Specifies a collection of files that are associated with a Pig job.</span></span>

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

### <span data-ttu-id="00d71-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="00d71-127">-Profile</span></span>
<span data-ttu-id="00d71-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="00d71-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00d71-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="00d71-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00d71-130">-Query</span><span class="sxs-lookup"><span data-stu-id="00d71-130">-Query</span></span>
<span data-ttu-id="00d71-131">Egy Pig-Job lekérdezést ad meg.</span><span class="sxs-lookup"><span data-stu-id="00d71-131">Specifies a Pig job query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d71-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="00d71-132">-StatusFolder</span></span>
<span data-ttu-id="00d71-133">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimenetét tartalmazza, valamint a kilépési kódot és a tevékenység naplóit.</span><span class="sxs-lookup"><span data-stu-id="00d71-133">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="00d71-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d71-134">CommonParameters</span></span>
<span data-ttu-id="00d71-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00d71-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d71-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d71-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d71-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00d71-137">INPUTS</span></span>

## <span data-ttu-id="00d71-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00d71-138">OUTPUTS</span></span>

## <span data-ttu-id="00d71-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00d71-139">NOTES</span></span>

## <span data-ttu-id="00d71-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00d71-140">RELATED LINKS</span></span>

[<span data-ttu-id="00d71-141">Új – AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="00d71-141">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="00d71-142">Új – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="00d71-142">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="00d71-143">Új – AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="00d71-143">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="00d71-144">Új – AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="00d71-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


