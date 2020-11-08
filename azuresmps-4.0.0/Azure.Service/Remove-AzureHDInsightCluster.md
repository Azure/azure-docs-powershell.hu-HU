---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 7D73D37B-17EE-4FF8-9A21-D2014D5417D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa779907648ca8e8e1288394d562c86b6102d9ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016476"
---
# <span data-ttu-id="01f58-101">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="01f58-101">Remove-AzureHDInsightCluster</span></span>

## <span data-ttu-id="01f58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01f58-102">SYNOPSIS</span></span>
<span data-ttu-id="01f58-103">HDInsight-fürtöt töröl egy előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="01f58-103">Deletes an HDInsight cluster from a subscription.</span></span>

## <span data-ttu-id="01f58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01f58-104">SYNTAX</span></span>

```
Remove-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="01f58-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01f58-105">DESCRIPTION</span></span>
<span data-ttu-id="01f58-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="01f58-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="01f58-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="01f58-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="01f58-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="01f58-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="01f58-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="01f58-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="01f58-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="01f58-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="01f58-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="01f58-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="01f58-112">A **Remove-AzureHDInsightCluster** parancsmag az előfizetésből törli a megadott HDInsight-fürtszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="01f58-112">The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="01f58-113">Ezzel a művelettel a Hadoop elosztott fájlrendszerében (HDFS) tárolt adatok is törlődnek.</span><span class="sxs-lookup"><span data-stu-id="01f58-113">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="01f58-114">A rendszer nem törli a kapcsolódó Azure-tárterületi fiókban tárolt adatait.</span><span class="sxs-lookup"><span data-stu-id="01f58-114">Data stored in the associated Azure Storage account is not deleted.</span></span>

## <span data-ttu-id="01f58-115">Példák</span><span class="sxs-lookup"><span data-stu-id="01f58-115">EXAMPLES</span></span>

### <span data-ttu-id="01f58-116">1. példa: fürt eltávolítása</span><span class="sxs-lookup"><span data-stu-id="01f58-116">Example 1: Remove a cluster</span></span>
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

<span data-ttu-id="01f58-117">Ez a parancs törli a HDICluster nevű HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="01f58-117">This command deletes the HDInsight cluster named HDICluster.</span></span>

## <span data-ttu-id="01f58-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01f58-118">PARAMETERS</span></span>

### <span data-ttu-id="01f58-119">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="01f58-119">-Certificate</span></span>
<span data-ttu-id="01f58-120">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="01f58-120">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="01f58-121">-Végpont</span><span class="sxs-lookup"><span data-stu-id="01f58-121">-Endpoint</span></span>
<span data-ttu-id="01f58-122">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="01f58-122">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="01f58-123">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="01f58-123">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="01f58-124">-HostedService</span><span class="sxs-lookup"><span data-stu-id="01f58-124">-HostedService</span></span>
<span data-ttu-id="01f58-125">Az HDInsight szolgáltatás névterét adja meg, ha nem szeretné használni az alapértelmezett névteret.</span><span class="sxs-lookup"><span data-stu-id="01f58-125">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="01f58-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="01f58-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="01f58-127">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="01f58-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="01f58-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="01f58-128">-Name</span></span>
<span data-ttu-id="01f58-129">Az eltávolítandó HDInsight-fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01f58-129">Specifies the name of the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="01f58-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="01f58-130">-Profile</span></span>
<span data-ttu-id="01f58-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="01f58-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="01f58-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="01f58-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01f58-133">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="01f58-133">-Subscription</span></span>
<span data-ttu-id="01f58-134">Azt az előfizetési fiókot adja meg, amely az eltávolítandó HDInsight-fürtöt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="01f58-134">Specifies the subscription account that contains the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="01f58-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f58-135">CommonParameters</span></span>
<span data-ttu-id="01f58-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01f58-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f58-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f58-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f58-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01f58-138">INPUTS</span></span>

## <span data-ttu-id="01f58-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01f58-139">OUTPUTS</span></span>

## <span data-ttu-id="01f58-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01f58-140">NOTES</span></span>

## <span data-ttu-id="01f58-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01f58-141">RELATED LINKS</span></span>

[<span data-ttu-id="01f58-142">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="01f58-142">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="01f58-143">Új – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="01f58-143">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="01f58-144">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="01f58-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


