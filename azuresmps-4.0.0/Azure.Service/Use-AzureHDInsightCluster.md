---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0BF58D9C-814E-4276-823F-D566DC99391C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 773af58d0ae9b4ca940240875b5cf9a8d3a0ffe7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015837"
---
# <span data-ttu-id="993e7-101">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="993e7-101">Use-AzureHDInsightCluster</span></span>

## <span data-ttu-id="993e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="993e7-102">SYNOPSIS</span></span>
<span data-ttu-id="993e7-103">Kijelöl egy HDInsight-fürtöt a Invoke-AzureHDInsightHiveJob parancsmag számára a feladatok elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="993e7-103">Selects an HDInsight cluster for the Invoke-AzureHDInsightHiveJob cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="993e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="993e7-104">SYNTAX</span></span>

```
Use-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="993e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="993e7-105">DESCRIPTION</span></span>
<span data-ttu-id="993e7-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="993e7-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="993e7-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="993e7-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="993e7-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="993e7-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="993e7-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="993e7-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="993e7-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="993e7-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="993e7-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="993e7-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="993e7-112">A **use-AzureHDInsightCluster** parancsmag kijelöli az Azure HDInsight-fürtöt az **hivatkozhat-AzureHDInsightHiveJob** parancsmagot, amellyel elküldhet feladatokat.</span><span class="sxs-lookup"><span data-stu-id="993e7-112">The **Use-AzureHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the **Invoke-AzureHDInsightHiveJob** cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="993e7-113">Példák</span><span class="sxs-lookup"><span data-stu-id="993e7-113">EXAMPLES</span></span>

## <span data-ttu-id="993e7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="993e7-114">PARAMETERS</span></span>

### <span data-ttu-id="993e7-115">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="993e7-115">-Certificate</span></span>
<span data-ttu-id="993e7-116">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="993e7-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="993e7-117">-Végpont</span><span class="sxs-lookup"><span data-stu-id="993e7-117">-Endpoint</span></span>
<span data-ttu-id="993e7-118">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="993e7-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="993e7-119">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="993e7-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="993e7-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="993e7-120">-HostedService</span></span>
<span data-ttu-id="993e7-121">Egy HDInsight-szolgáltatás névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="993e7-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="993e7-122">Ha nem adja meg ezt a paramétert, a program az alapértelmezett névteret használja.</span><span class="sxs-lookup"><span data-stu-id="993e7-122">If you do not specify this parameter, the default namespace is used.</span></span>

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

### <span data-ttu-id="993e7-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="993e7-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="993e7-124">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="993e7-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="993e7-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="993e7-125">-Name</span></span>
<span data-ttu-id="993e7-126">A **AzureHDInsightHiveJob** parancsmag által használt fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="993e7-126">Specifies the name of the cluster that is used by the **Invoke-AzureHDInsightHiveJob** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="993e7-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="993e7-127">-Profile</span></span>
<span data-ttu-id="993e7-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="993e7-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="993e7-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="993e7-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="993e7-130">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="993e7-130">-Subscription</span></span>
<span data-ttu-id="993e7-131">A használni kívánt HDInsight-szektorcsoportokat tartalmazó előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="993e7-131">Specifies the subscription that contains the HDInsight clusters to use.</span></span>

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

### <span data-ttu-id="993e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993e7-132">CommonParameters</span></span>
<span data-ttu-id="993e7-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="993e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993e7-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="993e7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993e7-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="993e7-135">INPUTS</span></span>

## <span data-ttu-id="993e7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="993e7-136">OUTPUTS</span></span>

## <span data-ttu-id="993e7-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="993e7-137">NOTES</span></span>

## <span data-ttu-id="993e7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="993e7-138">RELATED LINKS</span></span>

[<span data-ttu-id="993e7-139">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="993e7-139">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="993e7-140">Új – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="993e7-140">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="993e7-141">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="993e7-141">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)


