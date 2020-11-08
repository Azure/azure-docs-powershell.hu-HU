---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015764"
---
# <span data-ttu-id="b59c8-101">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b59c8-101">Stop-AzureHDInsightJob</span></span>

## <span data-ttu-id="b59c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b59c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b59c8-103">Leállít egy HDInsight-feladatot.</span><span class="sxs-lookup"><span data-stu-id="b59c8-103">Stops an HDInsight job.</span></span>

## <span data-ttu-id="b59c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b59c8-104">SYNTAX</span></span>

### <span data-ttu-id="b59c8-105">Az jobDetails indítása HDInsight-fürtön (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b59c8-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b59c8-106">Az jobDetails indítása HDInsight-fürtön (adott előfizetési hitelesítő adatokkal)</span><span class="sxs-lookup"><span data-stu-id="b59c8-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b59c8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b59c8-107">DESCRIPTION</span></span>
<span data-ttu-id="b59c8-108">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="b59c8-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b59c8-109">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="b59c8-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b59c8-110">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="b59c8-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b59c8-111">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="b59c8-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b59c8-112">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="b59c8-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b59c8-113">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b59c8-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b59c8-114">A **stop-AzureHDInsightJob** parancsmag egy Azure HDInsight-feladatot állít le a megadott fürtön.</span><span class="sxs-lookup"><span data-stu-id="b59c8-114">The **Stop-AzureHDInsightJob** cmdlet stops an Azure HDInsight job on the specified cluster.</span></span>

## <span data-ttu-id="b59c8-115">Példák</span><span class="sxs-lookup"><span data-stu-id="b59c8-115">EXAMPLES</span></span>

## <span data-ttu-id="b59c8-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b59c8-116">PARAMETERS</span></span>

### <span data-ttu-id="b59c8-117">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="b59c8-117">-Certificate</span></span>
<span data-ttu-id="b59c8-118">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59c8-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="b59c8-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="b59c8-119">-Cluster</span></span>
<span data-ttu-id="b59c8-120">Egy fürtöt ad meg.</span><span class="sxs-lookup"><span data-stu-id="b59c8-120">Specifies a cluster.</span></span>
<span data-ttu-id="b59c8-121">Ezzel a parancsmaggal megszüntetheti a fürtön futó olyan feladatot, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="b59c8-121">This cmdlet stops a job that runs on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b59c8-122">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="b59c8-122">-Credential</span></span>
<span data-ttu-id="b59c8-123">Megadja a fürtök közvetlen HTTP-eléréséhez használt hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b59c8-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="b59c8-124">Ezt a paramétert az *előfizetés* paraméter helyett úgy is megadhatja, hogy hitelesítse a hozzáférést egy fürthöz.</span><span class="sxs-lookup"><span data-stu-id="b59c8-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

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

### <span data-ttu-id="b59c8-125">-Végpont</span><span class="sxs-lookup"><span data-stu-id="b59c8-125">-Endpoint</span></span>
<span data-ttu-id="b59c8-126">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59c8-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="b59c8-127">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="b59c8-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="b59c8-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="b59c8-128">-HostedService</span></span>
<span data-ttu-id="b59c8-129">Az HDInsight szolgáltatás névterét adja meg, ha nem szeretné használni az alapértelmezett névteret.</span><span class="sxs-lookup"><span data-stu-id="b59c8-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="b59c8-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="b59c8-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="b59c8-131">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="b59c8-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="b59c8-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="b59c8-132">-JobId</span></span>
<span data-ttu-id="b59c8-133">A HDInsight feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59c8-133">Specifies the ID of the HDInsight job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b59c8-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="b59c8-134">-Profile</span></span>
<span data-ttu-id="b59c8-135">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b59c8-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b59c8-136">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b59c8-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b59c8-137">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="b59c8-137">-Subscription</span></span>
<span data-ttu-id="b59c8-138">Az előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59c8-138">Specifies a subscription.</span></span>
<span data-ttu-id="b59c8-139">Ez a parancsmag leállítja a paraméter által megadott előfizetéshez tartozó munkát.</span><span class="sxs-lookup"><span data-stu-id="b59c8-139">This cmdlet stops a job for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="b59c8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59c8-140">CommonParameters</span></span>
<span data-ttu-id="b59c8-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b59c8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59c8-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b59c8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59c8-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b59c8-143">INPUTS</span></span>

## <span data-ttu-id="b59c8-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b59c8-144">OUTPUTS</span></span>

## <span data-ttu-id="b59c8-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b59c8-145">NOTES</span></span>

## <span data-ttu-id="b59c8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b59c8-146">RELATED LINKS</span></span>

[<span data-ttu-id="b59c8-147">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b59c8-147">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="b59c8-148">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b59c8-148">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="b59c8-149">Várjon-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b59c8-149">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


