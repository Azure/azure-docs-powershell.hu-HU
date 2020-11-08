---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015917"
---
# <span data-ttu-id="066d5-101">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="066d5-101">New-AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="066d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="066d5-102">SYNOPSIS</span></span>
<span data-ttu-id="066d5-103">Új kaptár-feladatot határoz meg egy HDInsight-szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="066d5-103">Defines a new Hive job for an HDInsight service.</span></span>

## <span data-ttu-id="066d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="066d5-104">SYNTAX</span></span>

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="066d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="066d5-105">DESCRIPTION</span></span>
<span data-ttu-id="066d5-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="066d5-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="066d5-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="066d5-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="066d5-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="066d5-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="066d5-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="066d5-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="066d5-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="066d5-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="066d5-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="066d5-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="066d5-112">A **New-AzureHDInsightHiveJobDefinition** parancsmag egy olyan kaptár-feladatot határoz meg az Azure HDInsight szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="066d5-112">The **New-AzureHDInsightHiveJobDefinition** cmdlet defines a Hive job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="066d5-113">Példák</span><span class="sxs-lookup"><span data-stu-id="066d5-113">EXAMPLES</span></span>

### <span data-ttu-id="066d5-114">1. példa: a kaptár-feladatdefiníció létrehozása</span><span class="sxs-lookup"><span data-stu-id="066d5-114">Example 1: Create a Hive job definition</span></span>
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

<span data-ttu-id="066d5-115">Ez a parancs létrehoz egy olyan kaptár-munkadefiníciót, amely egy előre definiált lekérdezési karakterláncot használ, majd a $HiveJobDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="066d5-115">This command creates a Hive job definition that uses a pre-defined query string, and then stores it in the $HiveJobDefinition variable.</span></span>

## <span data-ttu-id="066d5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="066d5-116">PARAMETERS</span></span>

### <span data-ttu-id="066d5-117">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="066d5-117">-Arguments</span></span>
<span data-ttu-id="066d5-118">Argumentumokat ad meg egy Hadoop-feladathoz.</span><span class="sxs-lookup"><span data-stu-id="066d5-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="066d5-119">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="066d5-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="066d5-120">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="066d5-120">-Defines</span></span>
<span data-ttu-id="066d5-121">Itt adhatja meg, hogy mikor fusson a Hadoop konfigurációs értékek.</span><span class="sxs-lookup"><span data-stu-id="066d5-121">Specifies Hadoop configuration values to set for when a job runs.</span></span>

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

### <span data-ttu-id="066d5-122">-Fájl</span><span class="sxs-lookup"><span data-stu-id="066d5-122">-File</span></span>
<span data-ttu-id="066d5-123">A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="066d5-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="066d5-124">Ezt a paramétert a *query* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="066d5-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="066d5-125">-Files</span><span class="sxs-lookup"><span data-stu-id="066d5-125">-Files</span></span>
<span data-ttu-id="066d5-126">A kaptár-feladathoz társított fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="066d5-126">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="066d5-127">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="066d5-127">-JobName</span></span>
<span data-ttu-id="066d5-128">A definiálni kívánt kaptár-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="066d5-128">Specifies the name of the Hive job to define.</span></span>
<span data-ttu-id="066d5-129">Ha nem adja meg ezt a paramétert, a program az alapértelmezett nevet használja: "kaptár: \<first 100 characters of query\> ".</span><span class="sxs-lookup"><span data-stu-id="066d5-129">If you do not specify this parameter, the default name is used: "Hive: \<first 100 characters of query\>".</span></span>

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

### <span data-ttu-id="066d5-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="066d5-130">-Profile</span></span>
<span data-ttu-id="066d5-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="066d5-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="066d5-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="066d5-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="066d5-133">-Query</span><span class="sxs-lookup"><span data-stu-id="066d5-133">-Query</span></span>
<span data-ttu-id="066d5-134">A kaptár-lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="066d5-134">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="066d5-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="066d5-135">-RunAsFileJob</span></span>
<span data-ttu-id="066d5-136">Jelzi, hogy ez a parancsmag létrehoz egy fájlt az alapértelmezett Azure Storage-fiókban, amelyben a lekérdezés tárolható.</span><span class="sxs-lookup"><span data-stu-id="066d5-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="066d5-137">Ez a parancsmag elküldi azt a feladatot, amely parancsfájlként hivatkozik erre a fájlra.</span><span class="sxs-lookup"><span data-stu-id="066d5-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="066d5-138">Ezt a funkciót speciális karakterek (például százalék (%)) kezelésére használhatja. Ez a Templeton-on keresztül sikertelen volt, mert a Templeton URL-ként értelmezi a százalékos jellel ellátni kívánt lekérdezést.</span><span class="sxs-lookup"><span data-stu-id="066d5-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066d5-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="066d5-139">-StatusFolder</span></span>
<span data-ttu-id="066d5-140">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimenetét tartalmazza, valamint a kilépési kódot és a tevékenység naplóit.</span><span class="sxs-lookup"><span data-stu-id="066d5-140">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="066d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066d5-141">CommonParameters</span></span>
<span data-ttu-id="066d5-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="066d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066d5-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="066d5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066d5-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="066d5-144">INPUTS</span></span>

## <span data-ttu-id="066d5-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="066d5-145">OUTPUTS</span></span>

## <span data-ttu-id="066d5-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="066d5-146">NOTES</span></span>

## <span data-ttu-id="066d5-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="066d5-147">RELATED LINKS</span></span>

[<span data-ttu-id="066d5-148">Új – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="066d5-148">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="066d5-149">Új – AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="066d5-149">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="066d5-150">Új – AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="066d5-150">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="066d5-151">Új – AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="066d5-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


