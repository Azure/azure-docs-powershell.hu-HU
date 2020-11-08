---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3E3C9626-7AED-4B15-93D0-0B79AD17A834
online version: ''
schema: 2.0.0
ms.openlocfilehash: de4b768dbc6c97e84bccd4c8e0ef42f6f81a5b31
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016350"
---
# <span data-ttu-id="a6020-101">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a6020-101">Get-AzureHDInsightJob</span></span>

## <span data-ttu-id="a6020-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6020-102">SYNOPSIS</span></span>
<span data-ttu-id="a6020-103">Megkapja a HDInsight munkákat.</span><span class="sxs-lookup"><span data-stu-id="a6020-103">Gets HDInsight jobs.</span></span>

## <span data-ttu-id="a6020-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6020-104">SYNTAX</span></span>

### <span data-ttu-id="a6020-105">HDInsight-fürtök jobDetails-előzményeinek beszerzése (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6020-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Get-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] [-IgnoreSslErrors <Boolean>]
 [-JobId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a6020-106">HDInsight-fürtök jobDetails-előzményeinek beszerzése (adott előfizetési hitelesítő adatokkal)</span><span class="sxs-lookup"><span data-stu-id="a6020-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Get-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] [-JobId <String>] [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a6020-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6020-107">DESCRIPTION</span></span>
<span data-ttu-id="a6020-108">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="a6020-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="a6020-109">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="a6020-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="a6020-110">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="a6020-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="a6020-111">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="a6020-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="a6020-112">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="a6020-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="a6020-113">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a6020-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="a6020-114">A **Get-AzureHDInsightJob** parancsmag a legutóbbi Azure HDInsight-munkahelyeket kapja egy adott fürthöz, és fordított időrendi sorrendben jeleníti meg őket.</span><span class="sxs-lookup"><span data-stu-id="a6020-114">The **Get-AzureHDInsightJob** cmdlet gets recent Azure HDInsight jobs for a specified cluster and displays them in reverse chronological order.</span></span>

## <span data-ttu-id="a6020-115">Példák</span><span class="sxs-lookup"><span data-stu-id="a6020-115">EXAMPLES</span></span>

## <span data-ttu-id="a6020-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6020-116">PARAMETERS</span></span>

### <span data-ttu-id="a6020-117">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="a6020-117">-Certificate</span></span>
<span data-ttu-id="a6020-118">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6020-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="a6020-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="a6020-119">-Cluster</span></span>
<span data-ttu-id="a6020-120">Egy fürtöt ad meg.</span><span class="sxs-lookup"><span data-stu-id="a6020-120">Specifies a cluster.</span></span>
<span data-ttu-id="a6020-121">Ez a parancsmag azokat a HDInsight-feladatokat kapja meg, amelyek a megadott paraméter által megadott szektorcsoporton futnak.</span><span class="sxs-lookup"><span data-stu-id="a6020-121">This cmdlet gets HDInsight jobs that run on the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6020-122">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="a6020-122">-Credential</span></span>
<span data-ttu-id="a6020-123">Megadja a fürtök közvetlen HTTP-eléréséhez használt hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="a6020-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="a6020-124">Ezt a paramétert az *előfizetés* paraméter helyett úgy is megadhatja, hogy hitelesítse a hozzáférést egy fürthöz.</span><span class="sxs-lookup"><span data-stu-id="a6020-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6020-125">-Végpont</span><span class="sxs-lookup"><span data-stu-id="a6020-125">-Endpoint</span></span>
<span data-ttu-id="a6020-126">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6020-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="a6020-127">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="a6020-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="a6020-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="a6020-128">-HostedService</span></span>
<span data-ttu-id="a6020-129">Az HDInsight szolgáltatás névterét adja meg, ha nem szeretné használni az alapértelmezett névteret.</span><span class="sxs-lookup"><span data-stu-id="a6020-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="a6020-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="a6020-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="a6020-131">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="a6020-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="a6020-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="a6020-132">-JobId</span></span>
<span data-ttu-id="a6020-133">A beolvasott feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6020-133">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6020-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="a6020-134">-Profile</span></span>
<span data-ttu-id="a6020-135">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a6020-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a6020-136">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a6020-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6020-137">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="a6020-137">-Subscription</span></span>
<span data-ttu-id="a6020-138">A HDInsight feladatokat tartalmazó előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6020-138">Specifies the subscription that contains the HDInsight jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6020-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6020-139">CommonParameters</span></span>
<span data-ttu-id="a6020-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6020-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6020-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6020-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6020-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6020-142">INPUTS</span></span>

## <span data-ttu-id="a6020-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6020-143">OUTPUTS</span></span>

## <span data-ttu-id="a6020-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6020-144">NOTES</span></span>

## <span data-ttu-id="a6020-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6020-145">RELATED LINKS</span></span>

[<span data-ttu-id="a6020-146">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a6020-146">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="a6020-147">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a6020-147">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="a6020-148">Várjon-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a6020-148">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


