---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016351"
---
# <span data-ttu-id="48c98-101">Get-AzureHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="48c98-101">Get-AzureHDInsightProperties</span></span>

## <span data-ttu-id="48c98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48c98-102">SYNOPSIS</span></span>
<span data-ttu-id="48c98-103">A HDInsight szolgáltatáshoz tartozó tulajdonságokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="48c98-103">Gets properties specific to an HDInsight service.</span></span>

## <span data-ttu-id="48c98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48c98-104">SYNTAX</span></span>

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="48c98-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48c98-105">DESCRIPTION</span></span>
<span data-ttu-id="48c98-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="48c98-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="48c98-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="48c98-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="48c98-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="48c98-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="48c98-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="48c98-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="48c98-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="48c98-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="48c98-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="48c98-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="48c98-112">A **Get-AzureHDInsightProperties** parancsmag az Azure HDInsight szolgáltatáshoz tartozó tulajdonságokat kapja, például az elérhető Azure-régiók listáját, a HDInsight, valamint a rendelkezésre álló számítási kapacitást.</span><span class="sxs-lookup"><span data-stu-id="48c98-112">The **Get-AzureHDInsightProperties** cmdlet gets properties specific to an Azure HDInsight service, such as a list of available Azure regions, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="48c98-113">Példák</span><span class="sxs-lookup"><span data-stu-id="48c98-113">EXAMPLES</span></span>

### <span data-ttu-id="48c98-114">Példa 1: HDInsight tulajdonságainak beszerzése előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="48c98-114">Example 1: Get HDInsight properties for a subscription</span></span>
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

<span data-ttu-id="48c98-115">Az első parancs megkapja az aktuális Azure-előfizetés nevét, majd a $SubName változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="48c98-115">The first command gets the name of the current Azure subscription, and then stores it in the $SubName variable.</span></span>

<span data-ttu-id="48c98-116">A második parancs az előfizetéshez tartozó HDInsight-tulajdonságokat kapja meg a $SubName.</span><span class="sxs-lookup"><span data-stu-id="48c98-116">The second command gets the HDInsight properties for the subscription in $SubName.</span></span>

## <span data-ttu-id="48c98-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48c98-117">PARAMETERS</span></span>

### <span data-ttu-id="48c98-118">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="48c98-118">-Certificate</span></span>
<span data-ttu-id="48c98-119">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="48c98-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="48c98-120">-Végpont</span><span class="sxs-lookup"><span data-stu-id="48c98-120">-Endpoint</span></span>
<span data-ttu-id="48c98-121">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="48c98-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="48c98-122">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="48c98-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="48c98-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="48c98-123">-HostedService</span></span>
<span data-ttu-id="48c98-124">Egy HDInsight-szolgáltatás névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48c98-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="48c98-125">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett névteret használja.</span><span class="sxs-lookup"><span data-stu-id="48c98-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="48c98-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="48c98-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="48c98-127">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="48c98-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="48c98-128">-Helyek</span><span class="sxs-lookup"><span data-stu-id="48c98-128">-Locations</span></span>
<span data-ttu-id="48c98-129">Jelzi, hogy ez a parancsmag az Azure régiók listáját kapja, ahol a HDInsight szolgáltatás elérhető.</span><span class="sxs-lookup"><span data-stu-id="48c98-129">Indicates that this cmdlet gets the list of Azure regions where the HDInsight service is available.</span></span>

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

### <span data-ttu-id="48c98-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="48c98-130">-Profile</span></span>
<span data-ttu-id="48c98-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="48c98-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="48c98-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="48c98-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48c98-133">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="48c98-133">-Subscription</span></span>
<span data-ttu-id="48c98-134">A HDInsight tulajdonságokat tartalmazó előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="48c98-134">Specifies the subscription that contains the HDInsight properties to get.</span></span>

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

### <span data-ttu-id="48c98-135">-Verziók</span><span class="sxs-lookup"><span data-stu-id="48c98-135">-Versions</span></span>
<span data-ttu-id="48c98-136">Azt jelzi, hogy ez a parancsmag az előfizetéshez tartozó szolgáltatásban elérhető HDInsight-verziók listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="48c98-136">Indicates that this cmdlet gets the list of HDInsight cluster versions that are available in the service for a subscription.</span></span>

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

### <span data-ttu-id="48c98-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c98-137">CommonParameters</span></span>
<span data-ttu-id="48c98-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48c98-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c98-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c98-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c98-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48c98-140">INPUTS</span></span>

## <span data-ttu-id="48c98-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48c98-141">OUTPUTS</span></span>

## <span data-ttu-id="48c98-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48c98-142">NOTES</span></span>

## <span data-ttu-id="48c98-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48c98-143">RELATED LINKS</span></span>

