---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015640"
---
# <span data-ttu-id="b5a66-101">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="b5a66-101">Get-AzureHDInsightJobOutput</span></span>

## <span data-ttu-id="b5a66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5a66-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a66-103">A napló kimenetének lekérdezése a projekthez.</span><span class="sxs-lookup"><span data-stu-id="b5a66-103">Gets the log output for a job.</span></span>

## <span data-ttu-id="b5a66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5a66-104">SYNTAX</span></span>

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b5a66-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5a66-105">DESCRIPTION</span></span>
<span data-ttu-id="b5a66-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="b5a66-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b5a66-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="b5a66-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b5a66-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="b5a66-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b5a66-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a Linux-alapú fürtök létrehozása az [Azure PowerShell használatával HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)című témakört.</span><span class="sxs-lookup"><span data-stu-id="b5a66-109">For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in [HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b5a66-110">Ha többet szeretne tudni arról, hogy miként küldhet feladatokat az Azure PowerShell és más megközelítések segítségével, olvassa el [az Hadoop-feladatok elküldése az HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="b5a66-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b5a66-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight-parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b5a66-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b5a66-112">A **Get-AzureHDInsightJobOutput** parancsmag a fürthöz társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="b5a66-112">The **Get-AzureHDInsightJobOutput** cmdlet gets the log output for a job from the storage account associated with a cluster.</span></span>
<span data-ttu-id="b5a66-113">Különböző típusú beosztásokat kaphat, például a normál kimenetet, a normál hibát, a tevékenység naplókat és a naplók összegzését.</span><span class="sxs-lookup"><span data-stu-id="b5a66-113">You can get various types of job logs including standard output, standard error, task logs, and a summary of the task logs.</span></span>

## <span data-ttu-id="b5a66-114">Példák</span><span class="sxs-lookup"><span data-stu-id="b5a66-114">EXAMPLES</span></span>

### <span data-ttu-id="b5a66-115">Példa 1: projekt kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="b5a66-115">Example 1: Get job output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

<span data-ttu-id="b5a66-116">Az első parancs megkapja a jelenlegi előfizetés AZONOSÍTÓját, majd a $SubId változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b5a66-116">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="b5a66-117">A második parancs a MyCluster nevet a $Clustername változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b5a66-117">The second command stores the name MyCluster in the $Clustername variable.</span></span>

<span data-ttu-id="b5a66-118">A harmadik parancs létrehoz egy MapReduce, majd a $WordCountJob változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b5a66-118">The third command creates a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>
<span data-ttu-id="b5a66-119">A parancs átadja a feladatot $WordCountJob a **Start-AzureHDInsightJob** parancsmaggal a feladat indításához.</span><span class="sxs-lookup"><span data-stu-id="b5a66-119">The command passes the job in $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="b5a66-120">A **várakozás-AzureHDInsightJob** parancsmagot is átadja $WordCountJob a feladat befejezéséhez, majd a **Get-AzureHDInsightJobOutput** a projekt kimenetének beszerzéséhez használja.</span><span class="sxs-lookup"><span data-stu-id="b5a66-120">It also passes $WordCountJob to the **Wait-AzureHDInsightJob** cmdlet to wait for the job to finish, and then it uses **Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="b5a66-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5a66-121">PARAMETERS</span></span>

### <span data-ttu-id="b5a66-122">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="b5a66-122">-Certificate</span></span>
<span data-ttu-id="b5a66-123">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5a66-123">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a66-124">-Cluster</span><span class="sxs-lookup"><span data-stu-id="b5a66-124">-Cluster</span></span>
<span data-ttu-id="b5a66-125">Egy fürtöt ad meg.</span><span class="sxs-lookup"><span data-stu-id="b5a66-125">Specifies a cluster.</span></span>
<span data-ttu-id="b5a66-126">Ez a parancsmag olyan munkanaplókat kap a fürttől, amelyeket ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="b5a66-126">This cmdlet gets job logs from the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a66-127">-DownloadTaskLogs</span><span class="sxs-lookup"><span data-stu-id="b5a66-127">-DownloadTaskLogs</span></span>
<span data-ttu-id="b5a66-128">Azt jelzi, hogy ez a parancsmag a feladat naplóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b5a66-128">Indicates that this cmdlet gets the task logs for a job.</span></span>

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

### <span data-ttu-id="b5a66-129">-Végpont</span><span class="sxs-lookup"><span data-stu-id="b5a66-129">-Endpoint</span></span>
<span data-ttu-id="b5a66-130">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5a66-130">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="b5a66-131">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="b5a66-131">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a66-132">-HostedService</span><span class="sxs-lookup"><span data-stu-id="b5a66-132">-HostedService</span></span>
<span data-ttu-id="b5a66-133">Az HDInsight szolgáltatás névterét adja meg, ha nem szeretné használni az alapértelmezett névteret.</span><span class="sxs-lookup"><span data-stu-id="b5a66-133">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a66-134">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="b5a66-134">-IgnoreSslErrors</span></span>
<span data-ttu-id="b5a66-135">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="b5a66-135">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a66-136">-JobId</span><span class="sxs-lookup"><span data-stu-id="b5a66-136">-JobId</span></span>
<span data-ttu-id="b5a66-137">A beolvasott feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5a66-137">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a66-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="b5a66-138">-Profile</span></span>
<span data-ttu-id="b5a66-139">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b5a66-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5a66-140">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b5a66-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5a66-141">-StandardError</span><span class="sxs-lookup"><span data-stu-id="b5a66-141">-StandardError</span></span>
<span data-ttu-id="b5a66-142">Azt jelzi, hogy ez a parancsmag a projekt StdErr kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="b5a66-142">Indicates that this cmdlet gets the StdErr output of a job.</span></span>

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

### <span data-ttu-id="b5a66-143">-StandardOutput</span><span class="sxs-lookup"><span data-stu-id="b5a66-143">-StandardOutput</span></span>
<span data-ttu-id="b5a66-144">Azt jelzi, hogy ez a parancsmag a projekt SdtOut kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="b5a66-144">Indicates that this cmdlet gets the SdtOut output of a job.</span></span>

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

### <span data-ttu-id="b5a66-145">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5a66-145">-Subscription</span></span>
<span data-ttu-id="b5a66-146">A HDInsight-fürtöt tartalmazó előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5a66-146">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a66-147">-TaskLogsDirectory</span><span class="sxs-lookup"><span data-stu-id="b5a66-147">-TaskLogsDirectory</span></span>
<span data-ttu-id="b5a66-148">Itt adhatja meg, hogy melyik helyi mappa tárolja a feladatok naplóit.</span><span class="sxs-lookup"><span data-stu-id="b5a66-148">Specifies a local folder in which to store tasks logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a66-149">-TaskSummary</span><span class="sxs-lookup"><span data-stu-id="b5a66-149">-TaskSummary</span></span>
<span data-ttu-id="b5a66-150">Azt jelzi, hogy ez a parancsmag a műveletnapló összegzését kapja.</span><span class="sxs-lookup"><span data-stu-id="b5a66-150">Indicates that this cmdlets gets the task log summary.</span></span>

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

### <span data-ttu-id="b5a66-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a66-151">CommonParameters</span></span>
<span data-ttu-id="b5a66-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5a66-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a66-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a66-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a66-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5a66-154">INPUTS</span></span>

## <span data-ttu-id="b5a66-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5a66-155">OUTPUTS</span></span>

## <span data-ttu-id="b5a66-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5a66-156">NOTES</span></span>

## <span data-ttu-id="b5a66-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5a66-157">RELATED LINKS</span></span>

[<span data-ttu-id="b5a66-158">Új – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b5a66-158">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="b5a66-159">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b5a66-159">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="b5a66-160">Várjon-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b5a66-160">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)
