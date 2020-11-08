---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E3D22B03-2997-4F2C-895E-AE0993FD7C92
online version: ''
schema: 2.0.0
ms.openlocfilehash: bfd3e1f2bb5d057dec8a7bee5929ba5c67c8d53d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016498"
---
# <span data-ttu-id="5ef8a-101">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5ef8a-101">Grant-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="5ef8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ef8a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef8a-103">HTTP-hozzáférést ad egy fürthöz.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-103">Grants HTTP access to a cluster.</span></span>

## <span data-ttu-id="5ef8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ef8a-104">SYNTAX</span></span>

```
Grant-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Credential <PSCredential> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5ef8a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ef8a-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef8a-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="5ef8a-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="5ef8a-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="5ef8a-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="5ef8a-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="5ef8a-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="5ef8a-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="5ef8a-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5ef8a-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="5ef8a-112">A **Grant-AzureHDInsightHttpServicesAccess** parancsmag az Azure HDInsight-fürtökhöz az ODBC, a Ambari, a Oozie és a webes szolgáltatások segítségével http-hozzáférést ad.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-112">The **Grant-AzureHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie, and web services.</span></span>

## <span data-ttu-id="5ef8a-113">Példák</span><span class="sxs-lookup"><span data-stu-id="5ef8a-113">EXAMPLES</span></span>

## <span data-ttu-id="5ef8a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ef8a-114">PARAMETERS</span></span>

### <span data-ttu-id="5ef8a-115">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="5ef8a-115">-Certificate</span></span>
<span data-ttu-id="5ef8a-116">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="5ef8a-117">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="5ef8a-117">-Credential</span></span>
<span data-ttu-id="5ef8a-118">A HTTP-hozzáféréshez használt felhasználónevet és jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-118">Specifies a user name and password for HTTP access.</span></span>

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

### <span data-ttu-id="5ef8a-119">-Végpont</span><span class="sxs-lookup"><span data-stu-id="5ef8a-119">-Endpoint</span></span>
<span data-ttu-id="5ef8a-120">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-120">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="5ef8a-121">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-121">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="5ef8a-122">-HostedService</span><span class="sxs-lookup"><span data-stu-id="5ef8a-122">-HostedService</span></span>
<span data-ttu-id="5ef8a-123">Egy HDInsight-szolgáltatás névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-123">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="5ef8a-124">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett névteret használja.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-124">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="5ef8a-125">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="5ef8a-125">-IgnoreSslErrors</span></span>
<span data-ttu-id="5ef8a-126">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-126">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="5ef8a-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="5ef8a-127">-Location</span></span>
<span data-ttu-id="5ef8a-128">Azt az Azure-területet adja meg, amelyben a fürt található.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-128">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="5ef8a-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ef8a-129">-Name</span></span>
<span data-ttu-id="5ef8a-130">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-130">Specifies the name of a cluster.</span></span>
<span data-ttu-id="5ef8a-131">Ez a parancsmag HTTP-hozzáférést biztosít a fürthöz, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-131">This cmdlet grants HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ef8a-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="5ef8a-132">-Profile</span></span>
<span data-ttu-id="5ef8a-133">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ef8a-134">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ef8a-135">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="5ef8a-135">-Subscription</span></span>
<span data-ttu-id="5ef8a-136">Azt az előfizetést adja meg, amely a hozzáférést biztosító HDInsight-fürtöt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5ef8a-136">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="5ef8a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef8a-137">CommonParameters</span></span>
<span data-ttu-id="5ef8a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ef8a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef8a-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ef8a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef8a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ef8a-140">INPUTS</span></span>

## <span data-ttu-id="5ef8a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ef8a-141">OUTPUTS</span></span>

## <span data-ttu-id="5ef8a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ef8a-142">NOTES</span></span>

## <span data-ttu-id="5ef8a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ef8a-143">RELATED LINKS</span></span>

[<span data-ttu-id="5ef8a-144">Visszavonás-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5ef8a-144">Revoke-AzureHDInsightHttpServicesAccess</span></span>](./Revoke-AzureHDInsightHttpServicesAccess.md)


