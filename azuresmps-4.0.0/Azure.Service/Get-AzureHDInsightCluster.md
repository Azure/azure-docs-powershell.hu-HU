---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d0ea12e873604360114b02bb89d9bde12c9e70e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015644"
---
# <span data-ttu-id="33df7-101">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="33df7-101">Get-AzureHDInsightCluster</span></span>

## <span data-ttu-id="33df7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33df7-102">SYNOPSIS</span></span>
<span data-ttu-id="33df7-103">Kap egy HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="33df7-103">Gets an HDInsight cluster.</span></span>

## <span data-ttu-id="33df7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33df7-104">SYNTAX</span></span>

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="33df7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="33df7-105">DESCRIPTION</span></span>
<span data-ttu-id="33df7-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="33df7-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="33df7-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="33df7-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="33df7-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="33df7-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="33df7-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="33df7-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="33df7-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="33df7-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="33df7-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="33df7-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="33df7-112">A **Get-AzureHDInsightCluster** parancsmag a jelenlegi előfizetéshez az Azure HDInsight szolgáltatás-fürtöket kapja.</span><span class="sxs-lookup"><span data-stu-id="33df7-112">The **Get-AzureHDInsightCluster** cmdlet gets the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="33df7-113">A *Name* paraméterrel egy adott szektorcsoportot is beszerezhet.</span><span class="sxs-lookup"><span data-stu-id="33df7-113">You can use the *Name* parameter to get a specific cluster.</span></span>

## <span data-ttu-id="33df7-114">Példák</span><span class="sxs-lookup"><span data-stu-id="33df7-114">EXAMPLES</span></span>

### <span data-ttu-id="33df7-115">Példa 1: a fürtök beszerzése előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="33df7-115">Example 1: Get the clusters in a subscription</span></span>
```
PS C:\> Get-AzureHDInsightCluster
```

<span data-ttu-id="33df7-116">Ez a parancs a jelenlegi előfizetésben lévő HDInsight-fürtökről kap információkat.</span><span class="sxs-lookup"><span data-stu-id="33df7-116">This command gets information about the HDInsight clusters in the current subscription.</span></span>

## <span data-ttu-id="33df7-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33df7-117">PARAMETERS</span></span>

### <span data-ttu-id="33df7-118">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="33df7-118">-Certificate</span></span>
<span data-ttu-id="33df7-119">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="33df7-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="33df7-120">-Végpont</span><span class="sxs-lookup"><span data-stu-id="33df7-120">-Endpoint</span></span>
<span data-ttu-id="33df7-121">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="33df7-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="33df7-122">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="33df7-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="33df7-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="33df7-123">-HostedService</span></span>
<span data-ttu-id="33df7-124">Egy HDInsight-szolgáltatás névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33df7-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="33df7-125">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett névteret használja.</span><span class="sxs-lookup"><span data-stu-id="33df7-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="33df7-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="33df7-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="33df7-127">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="33df7-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="33df7-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="33df7-128">-Name</span></span>
<span data-ttu-id="33df7-129">A beolvasott HDInsight-fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33df7-129">Specifies the name of an HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33df7-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="33df7-130">-Profile</span></span>
<span data-ttu-id="33df7-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="33df7-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="33df7-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="33df7-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33df7-133">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="33df7-133">-Subscription</span></span>
<span data-ttu-id="33df7-134">A HDInsight-fürtöt tartalmazó előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="33df7-134">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

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

### <span data-ttu-id="33df7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33df7-135">CommonParameters</span></span>
<span data-ttu-id="33df7-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33df7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33df7-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33df7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33df7-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33df7-138">INPUTS</span></span>

## <span data-ttu-id="33df7-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33df7-139">OUTPUTS</span></span>

## <span data-ttu-id="33df7-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33df7-140">NOTES</span></span>

## <span data-ttu-id="33df7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33df7-141">RELATED LINKS</span></span>

[<span data-ttu-id="33df7-142">Új – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="33df7-142">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="33df7-143">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="33df7-143">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="33df7-144">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="33df7-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


