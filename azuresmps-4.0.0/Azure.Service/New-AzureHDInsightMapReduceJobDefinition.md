---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015916"
---
# <span data-ttu-id="c7974-101">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c7974-101">New-AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="c7974-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7974-102">SYNOPSIS</span></span>
<span data-ttu-id="c7974-103">Új MapReduce-feladatot határoz meg.</span><span class="sxs-lookup"><span data-stu-id="c7974-103">Defines a new MapReduce job.</span></span>

## <span data-ttu-id="c7974-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7974-104">SYNTAX</span></span>

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c7974-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7974-105">DESCRIPTION</span></span>
<span data-ttu-id="c7974-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="c7974-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="c7974-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="c7974-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="c7974-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="c7974-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="c7974-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="c7974-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="c7974-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="c7974-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="c7974-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c7974-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="c7974-112">A **New-AzureHDInsightMapReduceJobDefinition** parancsmag új MapReduce-feladatot határoz meg az Azure HDInsight-fürtökön való futtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="c7974-112">The **New-AzureHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job to run on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c7974-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c7974-113">EXAMPLES</span></span>

### <span data-ttu-id="c7974-114">1. példa: MapReduce-feladat meghatározása, a feladat futtatása és a kimenet beszerzése</span><span class="sxs-lookup"><span data-stu-id="c7974-114">Example 1: Define a MapReduce job, run the job, and get the output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="c7974-115">Az első parancs megkapja a jelenlegi előfizetés AZONOSÍTÓját, majd a $SubId változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c7974-115">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="c7974-116">A második parancs a MyCluster nevet a $Clustername változóhoz rendeli.</span><span class="sxs-lookup"><span data-stu-id="c7974-116">The second command assigns the name MyCluster to the $Clustername variable.</span></span>

<span data-ttu-id="c7974-117">A harmadik parancs a **New-AzureHDInsightMapReduceJobDefinition** parancsmagot használja MapReduce-feladatdefiníció létrehozásához, majd a $WordCountJob változóban való tárolásához.</span><span class="sxs-lookup"><span data-stu-id="c7974-117">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then store it in the $WordCountJob variable.</span></span>

<span data-ttu-id="c7974-118">A negyedik parancs az alábbi parancsmagok használatával hajtja végre a műveletek sorozatát:</span><span class="sxs-lookup"><span data-stu-id="c7974-118">The fourth command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="c7974-119">**Indítsa** el a AzureHDInsightJob, és indítsa el a feladatot $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="c7974-119">**Start-AzureHDInsightJob** to start the job on $ClusterName.</span></span> 
- <span data-ttu-id="c7974-120">**Várjon – AzureHDInsightJob** , amíg meg nem várja a feladatot, és meg kell jelenítenie a Befejezés felé irányuló előrehaladást.</span><span class="sxs-lookup"><span data-stu-id="c7974-120">**Wait-AzureHDInsightJob** to wait for the job to finish and to display the progress toward completion.</span></span>
- <span data-ttu-id="c7974-121">**Get-AzureHDInsightJobOutput** a projekt kimenetének beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="c7974-121">**Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="c7974-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7974-122">PARAMETERS</span></span>

### <span data-ttu-id="c7974-123">-Argumentumok</span><span class="sxs-lookup"><span data-stu-id="c7974-123">-Arguments</span></span>
<span data-ttu-id="c7974-124">Argumentumokat ad meg egy Hadoop-feladathoz.</span><span class="sxs-lookup"><span data-stu-id="c7974-124">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="c7974-125">Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="c7974-125">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="c7974-126">-Osztálynév</span><span class="sxs-lookup"><span data-stu-id="c7974-126">-ClassName</span></span>
<span data-ttu-id="c7974-127">A Java Archive (JAR) fájlban lévő Job osztály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7974-127">Specifies the name of the job class in the Java Archive (JAR) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7974-128">– Határozza meg</span><span class="sxs-lookup"><span data-stu-id="c7974-128">-Defines</span></span>
<span data-ttu-id="c7974-129">Itt adhatja meg a Hadoop konfigurációs értékeit a feladat futásakor.</span><span class="sxs-lookup"><span data-stu-id="c7974-129">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="c7974-130">-Files</span><span class="sxs-lookup"><span data-stu-id="c7974-130">-Files</span></span>
<span data-ttu-id="c7974-131">A projekthez szükséges WASB-fájlok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7974-131">Specifies an array of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="c7974-132">-JarFile</span><span class="sxs-lookup"><span data-stu-id="c7974-132">-JarFile</span></span>
<span data-ttu-id="c7974-133">Annak a JAR-fájlnak a teljesen minősített nevét adja meg, amely egy MapReduce-feladat kódját és függőségeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c7974-133">Specifies the fully qualified name of a JAR file that contains the code and dependencies of a MapReduce job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7974-134">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="c7974-134">-JobName</span></span>
<span data-ttu-id="c7974-135">Egy MapReduce-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7974-135">Specifies the name of a MapReduce job.</span></span>
<span data-ttu-id="c7974-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="c7974-136">This parameter is optional.</span></span>
<span data-ttu-id="c7974-137">Ha nem adja meg ezt a paramétert, a program az *Osztálynév* paraméter értékét használja.</span><span class="sxs-lookup"><span data-stu-id="c7974-137">If you do not specify this parameter, the value of the *ClassName* parameter is used.</span></span>

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

### <span data-ttu-id="c7974-138">-LibJars</span><span class="sxs-lookup"><span data-stu-id="c7974-138">-LibJars</span></span>
<span data-ttu-id="c7974-139">A projekt LibJar hivatkozásait adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7974-139">Specifies an array of LibJar references of the job.</span></span>

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

### <span data-ttu-id="c7974-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="c7974-140">-Profile</span></span>
<span data-ttu-id="c7974-141">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c7974-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7974-142">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c7974-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7974-143">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="c7974-143">-StatusFolder</span></span>
<span data-ttu-id="c7974-144">Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimenetét tartalmazza, valamint a kilépési kódot és a tevékenység naplóit.</span><span class="sxs-lookup"><span data-stu-id="c7974-144">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="c7974-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7974-145">CommonParameters</span></span>
<span data-ttu-id="c7974-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7974-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7974-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7974-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7974-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7974-148">INPUTS</span></span>

## <span data-ttu-id="c7974-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7974-149">OUTPUTS</span></span>

## <span data-ttu-id="c7974-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7974-150">NOTES</span></span>

## <span data-ttu-id="c7974-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7974-151">RELATED LINKS</span></span>

[<span data-ttu-id="c7974-152">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="c7974-152">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="c7974-153">Új – AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c7974-153">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="c7974-154">Új – AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c7974-154">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="c7974-155">Új – AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c7974-155">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="c7974-156">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c7974-156">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="c7974-157">Várjon-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c7974-157">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


