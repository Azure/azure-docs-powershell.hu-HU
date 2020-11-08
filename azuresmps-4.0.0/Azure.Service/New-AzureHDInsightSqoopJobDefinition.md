---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E11AAB11-0CBF-4746-91D7-4D5E64801C29
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6dba4c331a69093f49c95728c028eaaf5d0bdb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015915"
---
# <span data-ttu-id="3828a-101">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3828a-101">New-AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="3828a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3828a-102">SYNOPSIS</span></span>
<span data-ttu-id="3828a-103">Új Sqoop-feladatot határoz meg.</span><span class="sxs-lookup"><span data-stu-id="3828a-103">Defines a new Sqoop job.</span></span>

## <span data-ttu-id="3828a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3828a-104">SYNTAX</span></span>

```
New-AzureHDInsightSqoopJobDefinition [-Command <String>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3828a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3828a-105">DESCRIPTION</span></span>
<span data-ttu-id="3828a-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="3828a-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="3828a-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="3828a-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="3828a-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="3828a-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="3828a-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="3828a-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="3828a-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="3828a-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="3828a-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3828a-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="3828a-112">A **New-AzureHDInsightSqoopJobDefinition** parancsmag létrehoz egy Sqoop feladatot az Azure HDInsight-fürtökön való futtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="3828a-112">The **New-AzureHDInsightSqoopJobDefinition** cmdlet creates a Sqoop job to run on an Azure HDInsight cluster.</span></span>

<span data-ttu-id="3828a-113">A Sqoop egy eszköz, amellyel átviheti az adatátvitelt a Hadoop-fürtök és a relációs adatbázisok között.</span><span class="sxs-lookup"><span data-stu-id="3828a-113">Sqoop is a tool to transfer data between Hadoop clusters and relational databases.</span></span>
<span data-ttu-id="3828a-114">Az Sqoop segítségével az SQL Server-adatbázisokból származó adatok importálhatók Hadoop-es elosztott fájlrendszerbe (HDFS), az adatok átalakítása a Hadoop MapReduce, majd az adatok exportálása az HDFS az SQL Server-adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="3828a-114">You can use Sqoop to import data from a SQL Server database to a Hadoop Distributed File System (HDFS), transform the data with Hadoop MapReduce, and then export the data from the HDFS back to the SQL Server database.</span></span>

## <span data-ttu-id="3828a-115">Példák</span><span class="sxs-lookup"><span data-stu-id="3828a-115">EXAMPLES</span></span>

### <span data-ttu-id="3828a-116">1. példa: az adatimportálás</span><span class="sxs-lookup"><span data-stu-id="3828a-116">Example 1: Import data</span></span>
```
PS C:\>$SqoopJobDef = New-AzureHDInsightSqoopJobDefinition -Command "import --connect jdbc:sqlserver://<SQLDatabaseServerName>.database.windows.net:1433;username=<SQLDatabasUsername>@<SQLDatabaseServerName>; password=<SQLDatabasePassword>; database=<SQLDatabaseDatabaseName> --table <TableName> --target-dir wasb://<ContainerName>@<WindowsAzureStorageAccountName>.blob.core.windows.net/<Path>"
```

<span data-ttu-id="3828a-117">Ez a parancs olyan Sqoop-feladatot határoz meg, amely egy AzureSQL kiszolgálói adatbázisból egy HDInsight-fürtbe importálja az összes sort, majd a $SqoopJobDef változóban tárolja a feladatdefiníció értékét.</span><span class="sxs-lookup"><span data-stu-id="3828a-117">This command defines a Sqoop job that imports all of the rows in a table from an AzureSQL Server database to an HDInsight cluster, and then stores the job definition in the $SqoopJobDef variable.</span></span>

## <span data-ttu-id="3828a-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3828a-118">PARAMETERS</span></span>

### <span data-ttu-id="3828a-119">-Command</span><span class="sxs-lookup"><span data-stu-id="3828a-119">-Command</span></span>
<span data-ttu-id="3828a-120">A Sqoop parancsot és annak argumentumait adja meg.</span><span class="sxs-lookup"><span data-stu-id="3828a-120">Specifies a Sqoop command and its arguments.</span></span>

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

### <span data-ttu-id="3828a-121">-Fájl</span><span class="sxs-lookup"><span data-stu-id="3828a-121">-File</span></span>
<span data-ttu-id="3828a-122">A futtatandó parancsokat tartalmazó parancsfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3828a-122">Specifies the path to a script file that contains the commands to run.</span></span>
<span data-ttu-id="3828a-123">A parancsfájlnak a WASB-on kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3828a-123">The script file must be located on WASB.</span></span>

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

### <span data-ttu-id="3828a-124">-Files</span><span class="sxs-lookup"><span data-stu-id="3828a-124">-Files</span></span>
<span data-ttu-id="3828a-125">A projekthez szükséges WASB-fájlok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3828a-125">Specifies the collection of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="3828a-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="3828a-126">-Profile</span></span>
<span data-ttu-id="3828a-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3828a-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3828a-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3828a-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3828a-129">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="3828a-129">-StatusFolder</span></span>
<span data-ttu-id="3828a-130">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimenetét tartalmazza, valamint a kilépési kódot és a tevékenység naplóit.</span><span class="sxs-lookup"><span data-stu-id="3828a-130">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="3828a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3828a-131">CommonParameters</span></span>
<span data-ttu-id="3828a-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3828a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3828a-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3828a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3828a-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3828a-134">INPUTS</span></span>

## <span data-ttu-id="3828a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3828a-135">OUTPUTS</span></span>

## <span data-ttu-id="3828a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3828a-136">NOTES</span></span>

## <span data-ttu-id="3828a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3828a-137">RELATED LINKS</span></span>

[<span data-ttu-id="3828a-138">Új – AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3828a-138">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="3828a-139">Új – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3828a-139">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="3828a-140">Új – AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3828a-140">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="3828a-141">Új – AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3828a-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


