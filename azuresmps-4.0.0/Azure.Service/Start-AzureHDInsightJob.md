---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0308c3ff5bee358a82d74d452784f42c69bc7c32
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015424"
---
# <span data-ttu-id="b70fa-101">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b70fa-101">Start-AzureHDInsightJob</span></span>

## <span data-ttu-id="b70fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b70fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b70fa-103">Elindít egy HDInsight-feladatot.</span><span class="sxs-lookup"><span data-stu-id="b70fa-103">Starts an HDInsight job.</span></span>

## <span data-ttu-id="b70fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b70fa-104">SYNTAX</span></span>

### <span data-ttu-id="b70fa-105">Az jobDetails indítása HDInsight-fürtön (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b70fa-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b70fa-106">Az jobDetails indítása HDInsight-fürtön (adott előfizetési hitelesítő adatokkal)</span><span class="sxs-lookup"><span data-stu-id="b70fa-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b70fa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b70fa-107">DESCRIPTION</span></span>
<span data-ttu-id="b70fa-108">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="b70fa-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b70fa-109">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="b70fa-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b70fa-110">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="b70fa-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b70fa-111">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="b70fa-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b70fa-112">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="b70fa-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b70fa-113">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b70fa-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b70fa-114">A **Start-AzureHDInsightJob** parancsmag egy meghatározott Azure HDInsight-feladatot indít egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="b70fa-114">The **Start-AzureHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="b70fa-115">A kiindulási feladat lehet MapReduce-munka, adatfolyam-munka, kaptár-feladat vagy sertés-munka.</span><span class="sxs-lookup"><span data-stu-id="b70fa-115">The job to start can be a MapReduce job, a streaming job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="b70fa-116">Példák</span><span class="sxs-lookup"><span data-stu-id="b70fa-116">EXAMPLES</span></span>

### <span data-ttu-id="b70fa-117">1. példa: HDInsight-feladat indítása</span><span class="sxs-lookup"><span data-stu-id="b70fa-117">Example 1: Start an HDInsight job</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="b70fa-118">Az első parancs a jelenlegi előfizetési azonosítót kapja, majd a $SubId változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b70fa-118">The first command gets the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="b70fa-119">A második parancs a Cluster01 nevet a $ClusterName változóhoz rendeli.</span><span class="sxs-lookup"><span data-stu-id="b70fa-119">The second command assigns the name Cluster01 to the $ClusterName variable.</span></span>

<span data-ttu-id="b70fa-120">A harmadik parancs a **New-AzureHDInsightMapReduceJobDefinition** parancsmagot használja MapReduce-feladatdefiníció létrehozásához, majd a $WordCountJob változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b70fa-120">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="b70fa-121">A végleges parancs a pipeline operátor segítségével átadja a $WordCountJob a **Start-AzureHDInsightJob** parancsmagnak a feladat megkezdéséhez.</span><span class="sxs-lookup"><span data-stu-id="b70fa-121">The final command uses the pipeline operator to pass the $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="b70fa-122">A feladat elkezdése után a program átadja a feladatot a **várakozási AzureHDInsightJob** parancsmagnak, amely megvárja a feladat befejezését, mielőtt a munkát a **Get-AzureHDInsightJobOutput** parancsmagba továbbítja.</span><span class="sxs-lookup"><span data-stu-id="b70fa-122">After the job starts, it is passed to the **Wait-AzureHDInsightJob** cmdlet, which waits for the job to complete before passing it to the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="b70fa-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b70fa-123">PARAMETERS</span></span>

### <span data-ttu-id="b70fa-124">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="b70fa-124">-Certificate</span></span>
<span data-ttu-id="b70fa-125">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b70fa-125">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70fa-126">-Cluster</span><span class="sxs-lookup"><span data-stu-id="b70fa-126">-Cluster</span></span>
<span data-ttu-id="b70fa-127">Egy fürtöt ad meg.</span><span class="sxs-lookup"><span data-stu-id="b70fa-127">Specifies a cluster.</span></span>
<span data-ttu-id="b70fa-128">Ez a parancsmag olyan munkát indít a fürtön, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="b70fa-128">This cmdlet starts a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b70fa-129">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="b70fa-129">-Credential</span></span>
<span data-ttu-id="b70fa-130">A fürt hitelesítő adatait adja meg a közvetlen HTTP-hozzáféréshez.</span><span class="sxs-lookup"><span data-stu-id="b70fa-130">Specifies cluster credentials for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="b70fa-131">Ezt a paramétert az *előfizetés* paraméter helyett úgy is megadhatja, hogy hitelesítse a hozzáférést egy fürthöz.</span><span class="sxs-lookup"><span data-stu-id="b70fa-131">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70fa-132">-Végpont</span><span class="sxs-lookup"><span data-stu-id="b70fa-132">-Endpoint</span></span>
<span data-ttu-id="b70fa-133">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b70fa-133">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="b70fa-134">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="b70fa-134">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70fa-135">-HostedService</span><span class="sxs-lookup"><span data-stu-id="b70fa-135">-HostedService</span></span>
<span data-ttu-id="b70fa-136">Az HDInsight szolgáltatás névterét adja meg, ha nem szeretné használni az alapértelmezett névteret.</span><span class="sxs-lookup"><span data-stu-id="b70fa-136">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70fa-137">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="b70fa-137">-IgnoreSslErrors</span></span>
<span data-ttu-id="b70fa-138">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="b70fa-138">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70fa-139">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="b70fa-139">-JobDefinition</span></span>
<span data-ttu-id="b70fa-140">A Microsoft Azure-hoz való csatlakozáskor használandó végpontot adja meg, ha a végpont eltér az alapértelmezetttől.</span><span class="sxs-lookup"><span data-stu-id="b70fa-140">Specifies the endpoint to use when connecting to Microsoft Azure if the endpoint is different from the default.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b70fa-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="b70fa-141">-Profile</span></span>
<span data-ttu-id="b70fa-142">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b70fa-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b70fa-143">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b70fa-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b70fa-144">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="b70fa-144">-Subscription</span></span>
<span data-ttu-id="b70fa-145">Az előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="b70fa-145">Specifies a subscription.</span></span>
<span data-ttu-id="b70fa-146">Ez a parancsmag elindítja a megfelelő feladatot az előfizetéshez, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="b70fa-146">This cmdlet starts a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70fa-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70fa-147">CommonParameters</span></span>
<span data-ttu-id="b70fa-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b70fa-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70fa-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b70fa-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70fa-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b70fa-150">INPUTS</span></span>

## <span data-ttu-id="b70fa-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b70fa-151">OUTPUTS</span></span>

## <span data-ttu-id="b70fa-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b70fa-152">NOTES</span></span>

## <span data-ttu-id="b70fa-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b70fa-153">RELATED LINKS</span></span>

[<span data-ttu-id="b70fa-154">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b70fa-154">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="b70fa-155">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="b70fa-155">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="b70fa-156">Új – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b70fa-156">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="b70fa-157">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b70fa-157">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="b70fa-158">Várjon-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b70fa-158">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


