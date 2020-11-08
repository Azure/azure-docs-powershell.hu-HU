---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 771B7CB2-88F6-4FC5-9DB0-E623D231E51A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdbf7778ca2d7498d7f33586f7e9e50e0955c521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015962"
---
# <span data-ttu-id="28646-101">Set-AzureHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="28646-101">Set-AzureHDInsightClusterSize</span></span>

## <span data-ttu-id="28646-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28646-102">SYNOPSIS</span></span>
<span data-ttu-id="28646-103">A HDInsight-fürtök adatcsomópontjainak számát állítja be.</span><span class="sxs-lookup"><span data-stu-id="28646-103">Sets the number of data nodes for an HDInsight cluster.</span></span>

## <span data-ttu-id="28646-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28646-104">SYNTAX</span></span>

### <span data-ttu-id="28646-105">A szektorcsoport méretének beállítása a név nevű csomópontokban</span><span class="sxs-lookup"><span data-stu-id="28646-105">Set cluster size in nodes with name.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> -Name <String> [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="28646-106">A szektorcsoportok méretének beállítása a fürtöket a csővezetéket szolgáltató csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="28646-106">Set cluster size in nodes with cluster from pipeline.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> [-Force] -Cluster <AzureHDInsightCluster>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="28646-107">Fürt név szerint (adott előfizetési hitelesítő adatokkal)</span><span class="sxs-lookup"><span data-stu-id="28646-107">Cluster By Name (with Specific Subscription Credential)</span></span>
```
Set-AzureHDInsightClusterSize [-Certificate <X509Certificate2>] [-Subscription <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="28646-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="28646-108">DESCRIPTION</span></span>
<span data-ttu-id="28646-109">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="28646-109">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="28646-110">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="28646-110">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="28646-111">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="28646-111">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="28646-112">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="28646-112">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="28646-113">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="28646-113">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="28646-114">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="28646-114">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="28646-115">A **set-AzureHDInsightClusterSize** parancsmag az Azure HDInsight-fürtök adatcsomópontjainak számát állítja be.</span><span class="sxs-lookup"><span data-stu-id="28646-115">The **Set-AzureHDInsightClusterSize** cmdlet sets the number of data nodes for an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="28646-116">Példák</span><span class="sxs-lookup"><span data-stu-id="28646-116">EXAMPLES</span></span>

## <span data-ttu-id="28646-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28646-117">PARAMETERS</span></span>

### <span data-ttu-id="28646-118">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="28646-118">-Certificate</span></span>
<span data-ttu-id="28646-119">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28646-119">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28646-120">-Cluster</span><span class="sxs-lookup"><span data-stu-id="28646-120">-Cluster</span></span>
<span data-ttu-id="28646-121">Az átméretezni kívánt szektorcsoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="28646-121">Specifies the cluster to resize.</span></span>

```yaml
Type: AzureHDInsightCluster
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28646-122">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="28646-122">-ClusterSizeInNodes</span></span>
<span data-ttu-id="28646-123">A fürtökhöz létrehozandó adatcsomópontok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28646-123">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with name.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28646-124">-Végpont</span><span class="sxs-lookup"><span data-stu-id="28646-124">-Endpoint</span></span>
<span data-ttu-id="28646-125">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="28646-125">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="28646-126">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="28646-126">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28646-127">-Force</span><span class="sxs-lookup"><span data-stu-id="28646-127">-Force</span></span>
<span data-ttu-id="28646-128">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="28646-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Set cluster size in nodes with name., Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28646-129">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="28646-129">-IgnoreSslErrors</span></span>
<span data-ttu-id="28646-130">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="28646-130">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28646-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28646-131">-Name</span></span>
<span data-ttu-id="28646-132">Az átméretezni kívánt HDInsight-szektorcsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28646-132">Specifies the name of the HDInsight cluster to resize.</span></span>

```yaml
Type: String
Parameter Sets: Set cluster size in nodes with name.
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28646-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="28646-133">-Profile</span></span>
<span data-ttu-id="28646-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="28646-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28646-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="28646-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28646-136">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="28646-136">-Subscription</span></span>
<span data-ttu-id="28646-137">Az előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="28646-137">Specifies a subscription.</span></span>
<span data-ttu-id="28646-138">Ez a parancsmag a paraméter által megadott előfizetéshez tartozó szektorcsoport-méretet adja meg.</span><span class="sxs-lookup"><span data-stu-id="28646-138">This cmdlet sets the cluster size for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28646-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28646-139">CommonParameters</span></span>
<span data-ttu-id="28646-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28646-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28646-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28646-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28646-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28646-142">INPUTS</span></span>

## <span data-ttu-id="28646-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28646-143">OUTPUTS</span></span>

## <span data-ttu-id="28646-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28646-144">NOTES</span></span>

## <span data-ttu-id="28646-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28646-145">RELATED LINKS</span></span>

