---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015832"
---
# <span data-ttu-id="653af-101">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="653af-101">Wait-AzureHDInsightJob</span></span>

## <span data-ttu-id="653af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="653af-102">SYNOPSIS</span></span>
<span data-ttu-id="653af-103">Megvárja a HDInsight-feladatok befejezését vagy kudarcát, és megjeleníti a feladat előrehaladását.</span><span class="sxs-lookup"><span data-stu-id="653af-103">Awaits the completion or failure of an HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="653af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="653af-104">SYNTAX</span></span>

### <span data-ttu-id="653af-105">HDInsight-fürtök jobDetails-előzményeinek beszerzése (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="653af-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="653af-106">HDInsight-fürtök jobDetails-előzményeinek beszerzése (adott előfizetési hitelesítő adatokkal)</span><span class="sxs-lookup"><span data-stu-id="653af-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="653af-107">Várjon egy feladatot a JobId egy HDInsight-fürtjén</span><span class="sxs-lookup"><span data-stu-id="653af-107">Wait Job with JobId on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="653af-108">Munka várakozása egy HDInsight-fürtön</span><span class="sxs-lookup"><span data-stu-id="653af-108">Wait Job with Job on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="653af-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="653af-109">DESCRIPTION</span></span>
<span data-ttu-id="653af-110">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="653af-110">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="653af-111">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="653af-111">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="653af-112">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="653af-112">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="653af-113">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="653af-113">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="653af-114">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="653af-114">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="653af-115">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="653af-115">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="653af-116">A **WAIT-AzureHDInsightJob** parancsmag várja az Azure HDInsight-feladatok befejezését vagy kudarcát, és megjeleníti a feladat előrehaladását.</span><span class="sxs-lookup"><span data-stu-id="653af-116">The **Wait-AzureHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="653af-117">Példák</span><span class="sxs-lookup"><span data-stu-id="653af-117">EXAMPLES</span></span>

### <span data-ttu-id="653af-118">Példa 1: feladat futtatása és várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="653af-118">Example 1: Run a job and wait for it to complete</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="653af-119">Az első parancs a jelenlegi Azure-előfizetési azonosítót kapja, majd a $SubId változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="653af-119">The first command gets the current Azure subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="653af-120">A második parancs a megadott fürtöt kapja, majd a $ClusterName változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="653af-120">The second command gets the specified cluster, and then stores it in the $ClusterName variable.</span></span>

<span data-ttu-id="653af-121">A harmadik parancs a **New-AzureHDInsightMapReduceJobDefinition** parancsmagot használja MapReduce-feladatdefiníció létrehozásához, majd a $WordCountJob változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="653af-121">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="653af-122">A negyedik parancs több parancsmagot használ a sorozatokban:</span><span class="sxs-lookup"><span data-stu-id="653af-122">The fourth command uses several cmdlets in sequence:</span></span> 

- <span data-ttu-id="653af-123">A munkafolyamatot a pipeline operátor segítségével átadja $WordCountJob a **Start-AzureHDInsightJob** parancsmagnak a feladat megkezdéséhez.</span><span class="sxs-lookup"><span data-stu-id="653af-123">It uses the pipeline operator to pass $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span> 
- <span data-ttu-id="653af-124">A feladatot átadják a **WAIT-AzureHDInsightJob** parancsmagnak, és a feladat befejezéséhez 3600 másodpercre kell várni.</span><span class="sxs-lookup"><span data-stu-id="653af-124">The job is passed to the **Wait-AzureHDInsightJob** cmdlet to wait 3600 seconds for the job to complete.</span></span> 
- <span data-ttu-id="653af-125">Ha befejezte a feladatot, a parancs a **Get-AzureHDInsightJobOutput** parancsmagot használja a projekt kimenetének beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="653af-125">If the job completes, the command uses the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="653af-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="653af-126">PARAMETERS</span></span>

### <span data-ttu-id="653af-127">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="653af-127">-Certificate</span></span>
<span data-ttu-id="653af-128">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="653af-128">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="653af-129">-Cluster</span><span class="sxs-lookup"><span data-stu-id="653af-129">-Cluster</span></span>
<span data-ttu-id="653af-130">Egy fürtöt ad meg.</span><span class="sxs-lookup"><span data-stu-id="653af-130">Specifies a cluster.</span></span>
<span data-ttu-id="653af-131">Ezzel a parancsmaggal egy olyan feladat vár, amelyet a megadott paraméter határoz meg a fürtben.</span><span class="sxs-lookup"><span data-stu-id="653af-131">This cmdlet waits for a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="653af-132">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="653af-132">-Credential</span></span>
<span data-ttu-id="653af-133">Megadja a fürtök közvetlen HTTP-eléréséhez használt hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="653af-133">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="653af-134">Ezt a paramétert az *előfizetés* paraméter helyett úgy is megadhatja, hogy hitelesítse a hozzáférést egy fürthöz.</span><span class="sxs-lookup"><span data-stu-id="653af-134">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="653af-135">-Végpont</span><span class="sxs-lookup"><span data-stu-id="653af-135">-Endpoint</span></span>
<span data-ttu-id="653af-136">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="653af-136">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="653af-137">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="653af-137">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="653af-138">-HostedService</span><span class="sxs-lookup"><span data-stu-id="653af-138">-HostedService</span></span>
<span data-ttu-id="653af-139">Egy HDInsight-szolgáltatás névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="653af-139">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="653af-140">Ha nem adja meg ezt a paramétert, a program az alapértelmezett névteret használja.</span><span class="sxs-lookup"><span data-stu-id="653af-140">If you do not specify this parameter, the default namespace is used.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="653af-141">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="653af-141">-IgnoreSslErrors</span></span>
<span data-ttu-id="653af-142">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="653af-142">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="653af-143">-Job</span><span class="sxs-lookup"><span data-stu-id="653af-143">-Job</span></span>
<span data-ttu-id="653af-144">Egy Azure HDInsight-feladatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="653af-144">Specifies an Azure HDInsight job.</span></span>

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="653af-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="653af-145">-JobId</span></span>
<span data-ttu-id="653af-146">Annak a feladatnak az AZONOSÍTÓját adja meg, amelyre várni szeretne.</span><span class="sxs-lookup"><span data-stu-id="653af-146">Specifies the ID of the job to wait for.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="653af-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="653af-147">-Profile</span></span>
<span data-ttu-id="653af-148">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="653af-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="653af-149">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="653af-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="653af-150">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="653af-150">-Subscription</span></span>
<span data-ttu-id="653af-151">Az előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="653af-151">Specifies a subscription.</span></span>
<span data-ttu-id="653af-152">Ezzel a parancsmaggal megvárja az előfizetéshez tartozó munkát, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="653af-152">This cmdlet waits for a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="653af-153">-WaitTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="653af-153">-WaitTimeoutInSeconds</span></span>
<span data-ttu-id="653af-154">A várakozási művelethez a másodpercben megadott időtúllépést adja meg.</span><span class="sxs-lookup"><span data-stu-id="653af-154">Specifies the time-out, in seconds, for the wait operation.</span></span>
<span data-ttu-id="653af-155">Ha az időtúllépés lejár a feladat befejezésekor, a parancsmag megszűnik.</span><span class="sxs-lookup"><span data-stu-id="653af-155">If the time-out expires before the job completes, the cmdlet ceases to run.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="653af-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="653af-156">CommonParameters</span></span>
<span data-ttu-id="653af-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="653af-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="653af-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="653af-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="653af-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="653af-159">INPUTS</span></span>

## <span data-ttu-id="653af-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="653af-160">OUTPUTS</span></span>

## <span data-ttu-id="653af-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="653af-161">NOTES</span></span>

## <span data-ttu-id="653af-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="653af-162">RELATED LINKS</span></span>

[<span data-ttu-id="653af-163">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="653af-163">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="653af-164">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="653af-164">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="653af-165">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="653af-165">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="653af-166">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="653af-166">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)


