---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015920"
---
# <span data-ttu-id="f994f-101">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f994f-101">New-AzureHDInsightClusterConfig</span></span>

## <span data-ttu-id="f994f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f994f-102">SYNOPSIS</span></span>
<span data-ttu-id="f994f-103">Nem állandó HDInsight-fürtös konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f994f-103">Creates a non-persisted HDInsight cluster configuration.</span></span>

## <span data-ttu-id="f994f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f994f-104">SYNTAX</span></span>

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f994f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f994f-105">DESCRIPTION</span></span>
<span data-ttu-id="f994f-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="f994f-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f994f-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="f994f-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f994f-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="f994f-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f994f-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f994f-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f994f-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="f994f-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f994f-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f994f-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f994f-112">A **New-AzureHDInsightClusterConfig** parancsmag létrehoz egy nem állandó Azure HDInsight-fürtös konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f994f-112">The **New-AzureHDInsightClusterConfig** cmdlet creates a non-persisted Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="f994f-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f994f-113">EXAMPLES</span></span>

### <span data-ttu-id="f994f-114">1. példa: fürtkonfigurációs konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="f994f-114">Example 1: Create a cluster configuration</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="f994f-115">Az első parancs a **Get-AzureSubscription** parancsmagot használja a jelenlegi előfizetés-azonosító beolvasásához, majd a $SubId változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f994f-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="f994f-116">A második és a harmadik parancs a **Get-AzureStorageKey** parancsmagot használja a MyBlobStorage és a MySecondBlobStorage elsődleges tárterületének megadásához, majd a billentyűket a $Key 1 és $Key 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f994f-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="f994f-117">A negyedik, az ötödik és a hatodik parancs a **Get-hitelesítőadat** parancsmagot használja az aktuális előfizetéshez tartozó hitelesítő adatok beszerzéséhez, valamint a Oozie és a kaptárhoz, majd a hitelesítő adatok tárolása a változókban.</span><span class="sxs-lookup"><span data-stu-id="f994f-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="f994f-118">A végleges parancs az alábbi parancsmagok használatával hajtja végre a műveletek sorozatát:</span><span class="sxs-lookup"><span data-stu-id="f994f-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="f994f-119">**Új – AzureHDInsightClusterConfig** : HDInsight-fürtkonfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f994f-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="f994f-120">**Set-AzureHDInsightDefaultStorage** : beállíthatja a konfiguráció alapértelmezett tárolási fiókját a MyBlobStorage.blob.Core.Windows.net értékre.</span><span class="sxs-lookup"><span data-stu-id="f994f-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="f994f-121">**Add-AzureHDInsightStorage** : a MySecondBlobStorage.blob.Core.Windows.net nevű második tárolási fiók felvétele a konfigurációba.</span><span class="sxs-lookup"><span data-stu-id="f994f-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="f994f-122">**Add-AzureHDInsightMetastore** : adjon hozzá egy Metastore a Oozie-hoz, és egy Metastore a kaptár számára a konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="f994f-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="f994f-123">**Új – AzureHDInsightCluster** : hozzon létre egy HDInsight-fürtöt az új konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="f994f-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="f994f-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f994f-124">PARAMETERS</span></span>

### <span data-ttu-id="f994f-125">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="f994f-125">-ClusterSizeInNodes</span></span>
<span data-ttu-id="f994f-126">A fürtökhöz létrehozandó adatcsomópontok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f994f-126">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f994f-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="f994f-127">-ClusterType</span></span>
<span data-ttu-id="f994f-128">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f994f-128">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f994f-129">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="f994f-129">-DataNodeVMSize</span></span>
<span data-ttu-id="f994f-130">Az adatcsomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f994f-130">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f994f-131">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="f994f-131">-HeadNodeVMSize</span></span>
<span data-ttu-id="f994f-132">A fürthöz tartozó Head csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f994f-132">Specifies the virtual machine size of the head node for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f994f-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="f994f-133">-Profile</span></span>
<span data-ttu-id="f994f-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f994f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f994f-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f994f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f994f-136">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f994f-136">-SubnetName</span></span>
<span data-ttu-id="f994f-137">Az alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f994f-137">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f994f-138">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f994f-138">-VirtualNetworkId</span></span>
<span data-ttu-id="f994f-139">Annak a virtuális hálózatnak az AZONOSÍTÓját adja meg, amelybe a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="f994f-139">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f994f-140">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="f994f-140">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="f994f-141">Annak a virtuális gépnek a méretét adja meg, amely a HBase vagy a viharos fürtök ZooKeeper csomópontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f994f-141">Specifies the size of the virtual machine for the ZooKeeper node for an HBase or Storm cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f994f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f994f-142">CommonParameters</span></span>
<span data-ttu-id="f994f-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f994f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f994f-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f994f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f994f-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f994f-145">INPUTS</span></span>

## <span data-ttu-id="f994f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f994f-146">OUTPUTS</span></span>

## <span data-ttu-id="f994f-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f994f-147">NOTES</span></span>

## <span data-ttu-id="f994f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f994f-148">RELATED LINKS</span></span>

[<span data-ttu-id="f994f-149">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="f994f-149">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="f994f-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="f994f-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="f994f-151">Új – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f994f-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="f994f-152">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="f994f-152">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


