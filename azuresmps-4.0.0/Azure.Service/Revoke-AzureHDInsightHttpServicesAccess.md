---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A1DFA523-B532-4902-838D-74C8CA97A335
online version: ''
schema: 2.0.0
ms.openlocfilehash: f85d12100eb5b2b093eea252ac308e8a45cf1c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016434"
---
# <span data-ttu-id="6c04e-101">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6c04e-101">Revoke-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="6c04e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c04e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c04e-103">Letiltja a fürtök HTTP-elérését.</span><span class="sxs-lookup"><span data-stu-id="6c04e-103">Disables HTTP access to a cluster.</span></span>

## <span data-ttu-id="6c04e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c04e-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 [-IgnoreSslErrors <Boolean>] [-Endpoint <Uri>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6c04e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c04e-105">DESCRIPTION</span></span>
<span data-ttu-id="6c04e-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="6c04e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="6c04e-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="6c04e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="6c04e-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="6c04e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="6c04e-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="6c04e-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="6c04e-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="6c04e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="6c04e-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6c04e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="6c04e-112">A **Visszavonás-AzureHDInsightHttpServicesAccess** parancsmag letiltja a fürtök elérését az ODBC, az Ambari, a Oozie és a WebHCatalog Web Services szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="6c04e-112">The **Revoke-AzureHDInsightHttpServicesAccess** cmdlet disables HTTP access to a cluster for ODBC, Ambari, Oozie and WebHCatalog web services.</span></span>

## <span data-ttu-id="6c04e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="6c04e-113">EXAMPLES</span></span>

## <span data-ttu-id="6c04e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c04e-114">PARAMETERS</span></span>

### <span data-ttu-id="6c04e-115">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="6c04e-115">-Certificate</span></span>
<span data-ttu-id="6c04e-116">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c04e-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="6c04e-117">-Végpont</span><span class="sxs-lookup"><span data-stu-id="6c04e-117">-Endpoint</span></span>
<span data-ttu-id="6c04e-118">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c04e-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="6c04e-119">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="6c04e-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="6c04e-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="6c04e-120">-HostedService</span></span>
<span data-ttu-id="6c04e-121">Az HDInsight szolgáltatás névterét adja meg, ha nem szeretné használni az alapértelmezett névteret.</span><span class="sxs-lookup"><span data-stu-id="6c04e-121">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="6c04e-122">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="6c04e-122">-IgnoreSslErrors</span></span>
<span data-ttu-id="6c04e-123">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="6c04e-123">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="6c04e-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="6c04e-124">-Location</span></span>
<span data-ttu-id="6c04e-125">Azt a régiót adja meg, amelyben egy HDInsight-fürt található.</span><span class="sxs-lookup"><span data-stu-id="6c04e-125">Specifies the region in which an HDInsight cluster is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c04e-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c04e-126">-Name</span></span>
<span data-ttu-id="6c04e-127">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c04e-127">Specifies the name of a cluster.</span></span>
<span data-ttu-id="6c04e-128">Ez a parancsmag letiltja a fürt HTTP-elérését, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="6c04e-128">This cmdlet disables HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="6c04e-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="6c04e-129">-Profile</span></span>
<span data-ttu-id="6c04e-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6c04e-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c04e-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6c04e-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c04e-132">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="6c04e-132">-Subscription</span></span>
<span data-ttu-id="6c04e-133">A visszavonni kívánt HDInsight-fürtöt tartalmazó előfizetési fiókot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c04e-133">Specifies the subscription account that contains the HDInsight cluster to revoke.</span></span>

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

### <span data-ttu-id="6c04e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c04e-134">CommonParameters</span></span>
<span data-ttu-id="6c04e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c04e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c04e-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c04e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c04e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c04e-137">INPUTS</span></span>

## <span data-ttu-id="6c04e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c04e-138">OUTPUTS</span></span>

## <span data-ttu-id="6c04e-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c04e-139">NOTES</span></span>

## <span data-ttu-id="6c04e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c04e-140">RELATED LINKS</span></span>

[<span data-ttu-id="6c04e-141">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6c04e-141">Grant-AzureHDInsightHttpServicesAccess</span></span>](./Grant-AzureHDInsightHttpServicesAccess.md)


