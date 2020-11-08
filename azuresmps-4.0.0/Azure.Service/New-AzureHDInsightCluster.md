---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015923"
---
# <span data-ttu-id="9fca7-101">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9fca7-101">New-AzureHDInsightCluster</span></span>

## <span data-ttu-id="9fca7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fca7-102">SYNOPSIS</span></span>
<span data-ttu-id="9fca7-103">HDInsight-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9fca7-103">Creates an HDInsight cluster.</span></span>

## <span data-ttu-id="9fca7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fca7-104">SYNTAX</span></span>

### <span data-ttu-id="9fca7-105">Cluster by config (adott előfizetési hitelesítő adatokkal) (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9fca7-105">Cluster By Config (with Specific Subscription Credential) (Default)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9fca7-106">Fürt név szerint (adott előfizetési hitelesítő adatokkal)</span><span class="sxs-lookup"><span data-stu-id="9fca7-106">Cluster By Name (with Specific Subscription Credential)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9fca7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fca7-107">DESCRIPTION</span></span>
<span data-ttu-id="9fca7-108">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="9fca7-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="9fca7-109">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="9fca7-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="9fca7-110">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="9fca7-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="9fca7-111">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="9fca7-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="9fca7-112">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="9fca7-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="9fca7-113">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9fca7-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="9fca7-114">A **New-AzureHDInsightCluster** parancsmag az Azure HDInsight-fürtöt a megadott paraméterekkel vagy a **New-AzureHDInsightClusterConfig** parancsmaggal létrehozott konfigurációs objektum használatával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="9fca7-114">The **New-AzureHDInsightCluster** cmdlet creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

## <span data-ttu-id="9fca7-115">Példák</span><span class="sxs-lookup"><span data-stu-id="9fca7-115">EXAMPLES</span></span>

### <span data-ttu-id="9fca7-116">Példa 1: HDInsight-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="9fca7-116">Example 1: Create an HDInsight cluster</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential 
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="9fca7-117">Ez a példa létrehoz egy HDInsight-fürtöt az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="9fca7-117">This example creates an HDInsight cluster for the current subscription.</span></span>

<span data-ttu-id="9fca7-118">Az első parancs a **Get-AzureSubscription** parancsmagot használja a jelenlegi előfizetés-azonosító beolvasásához, majd a $SubId változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9fca7-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="9fca7-119">A második és a harmadik parancs a **Get-AzureStorageKey** parancsmagot használja a MyBlobStorage és a MySecondBlobStorage elsődleges tárterületének megadásához, majd a billentyűket a $Key 1 és $Key 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9fca7-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="9fca7-120">A negyedik, az ötödik és a hatodik parancs a **Get-hitelesítőadat** parancsmagot használja az aktuális előfizetéshez tartozó hitelesítő adatok beszerzéséhez, valamint a Oozie és a kaptárhoz, majd a hitelesítő adatok tárolása a változókban.</span><span class="sxs-lookup"><span data-stu-id="9fca7-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="9fca7-121">A végleges parancs az alábbi parancsmagok használatával hajtja végre a műveletek sorozatát:</span><span class="sxs-lookup"><span data-stu-id="9fca7-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="9fca7-122">**Új – AzureHDInsightClusterConfig** : HDInsight-fürtkonfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="9fca7-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="9fca7-123">**Set-AzureHDInsightDefaultStorage** : beállíthatja a konfiguráció alapértelmezett tárolási fiókját a MyBlobStorage.blob.Core.Windows.net értékre.</span><span class="sxs-lookup"><span data-stu-id="9fca7-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="9fca7-124">**Add-AzureHDInsightStorage** : a MySecondBlobStorage.blob.Core.Windows.net nevű második tárolási fiók felvétele a konfigurációba.</span><span class="sxs-lookup"><span data-stu-id="9fca7-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="9fca7-125">**Add-AzureHDInsightMetastore** : adjon hozzá egy Metastore a Oozie-hoz, és egy Metastore a kaptár számára a konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="9fca7-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="9fca7-126">**Új – AzureHDInsightCluster** : hozzon létre egy HDInsight-fürtöt az új konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="9fca7-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="9fca7-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fca7-127">PARAMETERS</span></span>

### <span data-ttu-id="9fca7-128">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="9fca7-128">-Certificate</span></span>
<span data-ttu-id="9fca7-129">Az Azure-előfizetés kezelési tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-129">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="9fca7-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="9fca7-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="9fca7-131">A fürtökhöz létrehozandó adatcsomópontok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-131">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-132">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="9fca7-132">-ClusterType</span></span>
<span data-ttu-id="9fca7-133">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-133">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-134">-Config</span><span class="sxs-lookup"><span data-stu-id="9fca7-134">-Config</span></span>
<span data-ttu-id="9fca7-135">A **New-AzureHDInsightClusterConfig** parancsmaggal létrehozott konfigurációs objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-135">Specifies a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-136">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="9fca7-136">-Credential</span></span>
<span data-ttu-id="9fca7-137">A Hadoop-fürtök távolról való eléréséhez használt alapértelmezett fiókhoz használt HDInsight felhasználói hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-137">Specifies the user credentials for HDInsight to use for the default account that is used to remotely access a Hadoop cluster.</span></span>
<span data-ttu-id="9fca7-138">Ezek a hitelesítő adatok eltérnek a felhasználó előfizetési hitelesítő adataitól.</span><span class="sxs-lookup"><span data-stu-id="9fca7-138">These credentials are distinct from the subscription credentials of the user.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-139">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="9fca7-139">-DataNodeVMSize</span></span>
<span data-ttu-id="9fca7-140">Az adatcsomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-140">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9fca7-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="9fca7-142">A HDInsight-fürtöt használó alapértelmezett tárterület-fiókhoz tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-142">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9fca7-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="9fca7-144">A HDInsight-fürtöt használó alapértelmezett tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-144">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-145">-DefaultStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="9fca7-145">-DefaultStorageContainerName</span></span>
<span data-ttu-id="9fca7-146">Annak az alapértelmezett tárolónak a nevét adja meg az alapértelmezett Azure Storage-fiókban, amelyet egy HDInsight-fürt használ.</span><span class="sxs-lookup"><span data-stu-id="9fca7-146">Specifies the name of the default container in the default Azure storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-147">-Végpont</span><span class="sxs-lookup"><span data-stu-id="9fca7-147">-EndPoint</span></span>
<span data-ttu-id="9fca7-148">Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-148">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="9fca7-149">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.</span><span class="sxs-lookup"><span data-stu-id="9fca7-149">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="9fca7-150">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="9fca7-150">-HeadNodeVMSize</span></span>
<span data-ttu-id="9fca7-151">A fej csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-151">Specifies the size of the virtual machine for the head node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-152">-HostedService</span><span class="sxs-lookup"><span data-stu-id="9fca7-152">-HostedService</span></span>
<span data-ttu-id="9fca7-153">Egy HDInsight-szolgáltatás névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-153">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="9fca7-154">Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett névteret használja.</span><span class="sxs-lookup"><span data-stu-id="9fca7-154">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="9fca7-155">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="9fca7-155">-IgnoreSslErrors</span></span>
<span data-ttu-id="9fca7-156">Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.</span><span class="sxs-lookup"><span data-stu-id="9fca7-156">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="9fca7-157">-Hely</span><span class="sxs-lookup"><span data-stu-id="9fca7-157">-Location</span></span>
<span data-ttu-id="9fca7-158">Azt a régiót adja meg, amelybe HDInsight-fürtöt szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="9fca7-158">Specifies the region in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-159">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9fca7-159">-Name</span></span>
<span data-ttu-id="9fca7-160">A létrehozandó Azure HDInsight-fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-160">Specifies the name of the Azure HDInsight cluster to create.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-161">-OSType</span><span class="sxs-lookup"><span data-stu-id="9fca7-161">-OSType</span></span>
<span data-ttu-id="9fca7-162">A fürt operációs rendszerét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-162">Specifies the operating system for a cluster.</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-163">-Profil</span><span class="sxs-lookup"><span data-stu-id="9fca7-163">-Profile</span></span>
<span data-ttu-id="9fca7-164">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9fca7-164">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9fca7-165">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9fca7-165">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9fca7-166">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="9fca7-166">-RdpAccessExpiry</span></span>
<span data-ttu-id="9fca7-167">Itt adhatja meg a fürthöz az RDP-hozzáféréssel való hozzáférés időpontját **datetime** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="9fca7-167">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-168">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="9fca7-168">-RdpCredential</span></span>
<span data-ttu-id="9fca7-169">A fürtök RDP-elérésének hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-169">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-170">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="9fca7-170">-SshCredential</span></span>
<span data-ttu-id="9fca7-171">A HDInsight-fürt biztonságos rendszerhéj-(SSH) felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-171">Specifies the Secure Shell (SSH) user name and password for the HDInsight cluster.</span></span>
<span data-ttu-id="9fca7-172">Ez a paraméter csak Linux-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="9fca7-172">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-173">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="9fca7-173">-SshPublicKey</span></span>
<span data-ttu-id="9fca7-174">A HDInsight-fürtök SSH-beli nyilvános kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-174">Specifies the SSH public key for an HDInsight cluster.</span></span>
<span data-ttu-id="9fca7-175">Ez a paraméter csak Linux-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="9fca7-175">This parameter is valid only for Linux clusters.</span></span>

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

### <span data-ttu-id="9fca7-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="9fca7-176">-SubnetName</span></span>
<span data-ttu-id="9fca7-177">Az alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-177">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-178">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="9fca7-178">-Subscription</span></span>
<span data-ttu-id="9fca7-179">Azt az Azure-előfizetést adja meg, amelyben HDInsight-fürtöt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="9fca7-179">Specifies the Azure subscription in which to create an HDInsight cluster.</span></span>

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

### <span data-ttu-id="9fca7-180">-Verzió</span><span class="sxs-lookup"><span data-stu-id="9fca7-180">-Version</span></span>
<span data-ttu-id="9fca7-181">A létrehozandó HDInsight-fürt verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-181">Specifies the HDInsight cluster version to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-182">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9fca7-182">-VirtualNetworkId</span></span>
<span data-ttu-id="9fca7-183">Annak a virtuális hálózatnak az AZONOSÍTÓját adja meg, amelybe a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="9fca7-183">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-184">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="9fca7-184">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="9fca7-185">A ZooKeeper csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fca7-185">Specifies the size of the virtual machine for the ZooKeeper node.</span></span>
<span data-ttu-id="9fca7-186">Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="9fca7-186">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fca7-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fca7-187">CommonParameters</span></span>
<span data-ttu-id="9fca7-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fca7-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fca7-189">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fca7-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fca7-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fca7-190">INPUTS</span></span>

## <span data-ttu-id="9fca7-191">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fca7-191">OUTPUTS</span></span>

## <span data-ttu-id="9fca7-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fca7-192">NOTES</span></span>

## <span data-ttu-id="9fca7-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fca7-193">RELATED LINKS</span></span>

[<span data-ttu-id="9fca7-194">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="9fca7-194">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="9fca7-195">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="9fca7-195">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="9fca7-196">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9fca7-196">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="9fca7-197">Új – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="9fca7-197">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="9fca7-198">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9fca7-198">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="9fca7-199">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="9fca7-199">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)

[<span data-ttu-id="9fca7-200">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9fca7-200">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


