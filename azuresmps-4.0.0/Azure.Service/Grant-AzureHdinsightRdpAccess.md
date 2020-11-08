---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 95CCEB79-EAC4-4F56-B289-5401F976E5F5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92b2c005f855ccf99e8bae4d8db8445ba7e63dad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016262"
---
# <span data-ttu-id="0b2ee-101">Grant-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="0b2ee-101">Grant-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="0b2ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b2ee-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2ee-103">RDP-hozzáférést ad egy HDInsight-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-103">Grants RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="0b2ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b2ee-104">SYNTAX</span></span>

```
Grant-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -RdpCredential <PSCredential> -RdpAccessExpiry <DateTime> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0b2ee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b2ee-105">DESCRIPTION</span></span>
<span data-ttu-id="0b2ee-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="0b2ee-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="0b2ee-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="0b2ee-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="0b2ee-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="0b2ee-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="0b2ee-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="0b2ee-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0b2ee-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="0b2ee-112">A **Grant-AzureHDInsightRdpAccess** parancsmag RDP (Remote Desktop Protocol) hozzáférést ad az Azure HDInsight-fürtökhöz.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-112">The **Grant-AzureHDInsightRdpAccess** cmdlet grants Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0b2ee-113">Példák</span><span class="sxs-lookup"><span data-stu-id="0b2ee-113">EXAMPLES</span></span>

## <span data-ttu-id="0b2ee-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b2ee-114">PARAMETERS</span></span>

### <span data-ttu-id="0b2ee-115">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="0b2ee-115">-Certificate</span></span>
<span data-ttu-id="0b2ee-116">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="0b2ee-117">-Végpont</span><span class="sxs-lookup"><span data-stu-id="0b2ee-117">-Endpoint</span></span>
<span data-ttu-id="0b2ee-118">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="0b2ee-119">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="0b2ee-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="0b2ee-120">-HostedService</span></span>
<span data-ttu-id="0b2ee-121">Egy HDInsight-szolgáltatás névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="0b2ee-122">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett névteret használja.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="0b2ee-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="0b2ee-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="0b2ee-124">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="0b2ee-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="0b2ee-125">-Location</span></span>
<span data-ttu-id="0b2ee-126">Azt az Azure-területet adja meg, amelyben a fürt található.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="0b2ee-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0b2ee-127">-Name</span></span>
<span data-ttu-id="0b2ee-128">Egy Azure HDInsight-fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="0b2ee-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="0b2ee-129">-Profile</span></span>
<span data-ttu-id="0b2ee-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b2ee-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b2ee-132">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="0b2ee-132">-RdpAccessExpiry</span></span>
<span data-ttu-id="0b2ee-133">Itt adhatja meg a fürthöz az RDP-hozzáféréssel való hozzáférés időpontját **datetime** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-133">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2ee-134">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="0b2ee-134">-RdpCredential</span></span>
<span data-ttu-id="0b2ee-135">A fürtök RDP-elérésének hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-135">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2ee-136">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="0b2ee-136">-Subscription</span></span>
<span data-ttu-id="0b2ee-137">Azt az előfizetést adja meg, amely a hozzáférést biztosító HDInsight-fürtöt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0b2ee-137">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="0b2ee-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2ee-138">CommonParameters</span></span>
<span data-ttu-id="0b2ee-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b2ee-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2ee-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2ee-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2ee-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b2ee-141">INPUTS</span></span>

## <span data-ttu-id="0b2ee-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b2ee-142">OUTPUTS</span></span>

## <span data-ttu-id="0b2ee-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b2ee-143">NOTES</span></span>

## <span data-ttu-id="0b2ee-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b2ee-144">RELATED LINKS</span></span>

[<span data-ttu-id="0b2ee-145">Visszavonás-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="0b2ee-145">Revoke-AzureHdinsightRdpAccess</span></span>](./Revoke-AzureHdinsightRdpAccess.md)


