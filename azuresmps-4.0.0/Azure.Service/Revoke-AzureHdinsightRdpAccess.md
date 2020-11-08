---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6818F49E-0A51-4D99-BC3D-5A90F1F30C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78caed4ac43f21a1afe21a8901bdcd77ba29e482
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015476"
---
# <span data-ttu-id="324f7-101">Revoke-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="324f7-101">Revoke-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="324f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="324f7-102">SYNOPSIS</span></span>
<span data-ttu-id="324f7-103">Letiltja az RDP-hozzáférést egy HDInsight-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="324f7-103">Disables RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="324f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="324f7-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="324f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="324f7-105">DESCRIPTION</span></span>
<span data-ttu-id="324f7-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="324f7-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="324f7-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="324f7-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="324f7-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="324f7-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="324f7-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="324f7-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="324f7-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="324f7-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="324f7-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="324f7-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="324f7-112">A **Visszavonás-AzureHDInsightRdpAccess** parancsmag letiltja a Remote Desktop Protocol (RDP) hozzáférést az Azure HDInsight-fürtökhöz.</span><span class="sxs-lookup"><span data-stu-id="324f7-112">The **Revoke-AzureHDInsightRdpAccess** cmdlet disables Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="324f7-113">Példák</span><span class="sxs-lookup"><span data-stu-id="324f7-113">EXAMPLES</span></span>

## <span data-ttu-id="324f7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="324f7-114">PARAMETERS</span></span>

### <span data-ttu-id="324f7-115">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="324f7-115">-Certificate</span></span>
<span data-ttu-id="324f7-116">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="324f7-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="324f7-117">-Végpont</span><span class="sxs-lookup"><span data-stu-id="324f7-117">-Endpoint</span></span>
<span data-ttu-id="324f7-118">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="324f7-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="324f7-119">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="324f7-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="324f7-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="324f7-120">-HostedService</span></span>
<span data-ttu-id="324f7-121">Egy HDInsight-szolgáltatás névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="324f7-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="324f7-122">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett névteret használja.</span><span class="sxs-lookup"><span data-stu-id="324f7-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="324f7-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="324f7-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="324f7-124">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="324f7-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="324f7-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="324f7-125">-Location</span></span>
<span data-ttu-id="324f7-126">Azt az Azure-területet adja meg, amelyben a fürt található.</span><span class="sxs-lookup"><span data-stu-id="324f7-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="324f7-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="324f7-127">-Name</span></span>
<span data-ttu-id="324f7-128">Egy Azure HDInsight-fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="324f7-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="324f7-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="324f7-129">-Profile</span></span>
<span data-ttu-id="324f7-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="324f7-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="324f7-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="324f7-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="324f7-132">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="324f7-132">-Subscription</span></span>
<span data-ttu-id="324f7-133">Az előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="324f7-133">Specifies a subscription.</span></span>
<span data-ttu-id="324f7-134">Ez a parancsmag visszavonja a Remote Desktop Protocol (RDP) hozzáférést a paraméter által megadott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="324f7-134">This cmdlet revokes Remote Desktop Protocol (RDP) access for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="324f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324f7-135">CommonParameters</span></span>
<span data-ttu-id="324f7-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="324f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324f7-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="324f7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324f7-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="324f7-138">INPUTS</span></span>

## <span data-ttu-id="324f7-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="324f7-139">OUTPUTS</span></span>

## <span data-ttu-id="324f7-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="324f7-140">NOTES</span></span>

## <span data-ttu-id="324f7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="324f7-141">RELATED LINKS</span></span>

[<span data-ttu-id="324f7-142">Grant-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="324f7-142">Grant-AzureHdinsightRdpAccess</span></span>](./Grant-AzureHdinsightRdpAccess.md)


