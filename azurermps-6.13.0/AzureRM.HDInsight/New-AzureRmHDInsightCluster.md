---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: b10fe80fb0a58267212912f554d044b2715fd1d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496124"
---
# <span data-ttu-id="7f18a-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="7f18a-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="7f18a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f18a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f18a-103">Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="7f18a-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f18a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f18a-104">SYNTAX</span></span>

### <span data-ttu-id="7f18a-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f18a-105">Default (Default)</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f18a-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="7f18a-106">CertificateFilePath</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f18a-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="7f18a-107">CertificateFileContents</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f18a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f18a-108">DESCRIPTION</span></span>
<span data-ttu-id="7f18a-109">A New-AzureHDInsightCluster Azure HDInsight-fürtöt hoz létre a megadott paraméterekkel vagy a New-AzureRmHDInsightClusterConfig parancsmaggal létrehozott konfigurációs objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="7f18a-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="7f18a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7f18a-110">EXAMPLES</span></span>

### <span data-ttu-id="7f18a-111">Példa 1: Azure HDInsight-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="7f18a-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightCluster `
            -ClusterType Hadoop `
            -OSType Windows `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="7f18a-112">Ez a parancs létrehoz egy fürtöt az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="7f18a-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="7f18a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f18a-113">PARAMETERS</span></span>

### <span data-ttu-id="7f18a-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="7f18a-114">-AadTenantId</span></span>
<span data-ttu-id="7f18a-115">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="7f18a-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="7f18a-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="7f18a-117">A fürt további Azure-tárolási fiókjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="7f18a-118">A Add-AzureRmHDInsightStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="7f18a-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="7f18a-119">-CertificateFileContents</span></span>
<span data-ttu-id="7f18a-120">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="7f18a-121">-CertificateFilePath</span></span>
<span data-ttu-id="7f18a-122">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="7f18a-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="7f18a-123">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="7f18a-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7f18a-124">-CertificatePassword</span></span>
<span data-ttu-id="7f18a-125">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="7f18a-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="7f18a-126">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="7f18a-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-127">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="7f18a-127">-ClusterName</span></span>
<span data-ttu-id="7f18a-128">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-128">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="7f18a-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="7f18a-130">A fürthöz tartozó munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-130">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="7f18a-131">-ClusterTier</span></span>
<span data-ttu-id="7f18a-132">A HDInsight-szektorcsoport rétegének meghatározása</span><span class="sxs-lookup"><span data-stu-id="7f18a-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="7f18a-133">Alapértelmezés szerint ez a normál.</span><span class="sxs-lookup"><span data-stu-id="7f18a-133">By default, this is Standard.</span></span>
<span data-ttu-id="7f18a-134">A prémium szint csak Linux-fürtökkel használható, és lehetővé teszi néhány új funkció használatát.</span><span class="sxs-lookup"><span data-stu-id="7f18a-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="7f18a-135">-ClusterType</span></span>
<span data-ttu-id="7f18a-136">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="7f18a-137">A beállítások a következők: Hadoop, HBase, Storm, szikra</span><span class="sxs-lookup"><span data-stu-id="7f18a-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="7f18a-138">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-139">-Config</span><span class="sxs-lookup"><span data-stu-id="7f18a-139">-Config</span></span>
<span data-ttu-id="7f18a-140">Azt a szektorcsoport-objektumot adja meg, amellyel a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="7f18a-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="7f18a-141">Ezt az objektumot az New-AzureRmHDInsightClusterConfig parancsmag segítségével hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="7f18a-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-142">-Konfigurációk</span><span class="sxs-lookup"><span data-stu-id="7f18a-142">-Configurations</span></span>
<span data-ttu-id="7f18a-143">A HDInsight-fürt konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="7f18a-144">A Add-AzureRmHDInsightConfigValues parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="7f18a-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f18a-145">-DefaultProfile</span></span>
<span data-ttu-id="7f18a-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f18a-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7f18a-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="7f18a-148">A HDInsight-fürtöt használó alapértelmezett Azure-tárterülethez tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="7f18a-149">A Set-AzureRmHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="7f18a-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7f18a-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="7f18a-151">Annak az alapértelmezett Azure-tárterületnek a nevét adja meg, amelyet a HDInsight-fürt használni fog.</span><span class="sxs-lookup"><span data-stu-id="7f18a-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="7f18a-152">A Set-AzureRmHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="7f18a-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7f18a-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="7f18a-154">A HDInsight-fürtöt használó alapértelmezett tárterület-fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="7f18a-155">A lehetséges értékek a AzureStorage és a AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="7f18a-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="7f18a-156">Az alapértelmezett érték a AzureStorage, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="7f18a-156">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7f18a-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="7f18a-158">Annak az alapértelmezett tárolónak a nevét adja meg, amely a HDInsight-fürtöt használó alapértelmezett Azure Storage fiókban található.</span><span class="sxs-lookup"><span data-stu-id="7f18a-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="7f18a-159">A Set-AzureRmHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="7f18a-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="7f18a-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="7f18a-161">Megadja az elérési utat az adattó-tároló fiókban, amelyet a HDInsight-fürt alapértelmezett fájlrendszerként fog használni.</span><span class="sxs-lookup"><span data-stu-id="7f18a-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="7f18a-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="7f18a-163">Itt adhatja meg a fürtben a munkavégző csomópont szerepkörrel rendelkező lemezek számát.</span><span class="sxs-lookup"><span data-stu-id="7f18a-163">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="7f18a-164">-EdgeNodeSize</span></span>
<span data-ttu-id="7f18a-165">Az Edge csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="7f18a-166">Használja a Get-AzureRmVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="7f18a-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="7f18a-167">Ez a paraméter csak a RServer-fürtök esetében érvényes.</span><span class="sxs-lookup"><span data-stu-id="7f18a-167">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="7f18a-168">-HeadNodeSize</span></span>
<span data-ttu-id="7f18a-169">A fej csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="7f18a-170">Használja a Get-AzureRmVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="7f18a-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="7f18a-171">-HiveMetastore</span></span>
<span data-ttu-id="7f18a-172">A kaptár metaadatait tároló SQL-adatbázist adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="7f18a-173">A Add-AzureRmHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="7f18a-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="7f18a-174">-HttpCredential</span></span>
<span data-ttu-id="7f18a-175">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="7f18a-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-176">-Hely</span><span class="sxs-lookup"><span data-stu-id="7f18a-176">-Location</span></span>
<span data-ttu-id="7f18a-177">A fürt helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-177">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7f18a-178">-ObjectId</span></span>
<span data-ttu-id="7f18a-179">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="7f18a-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="7f18a-180">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="7f18a-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="7f18a-181">-OozieMetastore</span></span>
<span data-ttu-id="7f18a-182">Megadja a Oozie metaadatait tároló SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="7f18a-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="7f18a-183">A Add-AzureRmHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="7f18a-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="7f18a-184">-OSType</span></span>
<span data-ttu-id="7f18a-185">A fürt operációs rendszerét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="7f18a-186">A beállítások a következők: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="7f18a-186">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="7f18a-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="7f18a-188">Itt adhatja meg a fürthöz az RDP-hozzáféréssel való hozzáférés időpontját DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="7f18a-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="7f18a-189">-RdpCredential</span></span>
<span data-ttu-id="7f18a-190">A fürt távoli asztali (RDP) hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="7f18a-191">Ez csak Windows-fürtök esetén használható.</span><span class="sxs-lookup"><span data-stu-id="7f18a-191">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f18a-192">-ResourceGroupName</span></span>
<span data-ttu-id="7f18a-193">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-193">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="7f18a-194">-ScriptActions</span></span>
<span data-ttu-id="7f18a-195">Megadja, hogy milyen parancsfájl-műveletek legyenek futtathatók a fürtökön a fürtök létrehozása végén.</span><span class="sxs-lookup"><span data-stu-id="7f18a-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="7f18a-196">Másik lehetőségként használhatja a bővítmények AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="7f18a-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="7f18a-197">-SecurityProfile</span></span>
<span data-ttu-id="7f18a-198">A biztonságos fürtök létrehozásához használt biztonsággal kapcsolatos tulajdonságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="7f18a-199">A Add-AzureRmHDInsightSecurityProfile parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="7f18a-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="7f18a-200">-SshCredential</span></span>
<span data-ttu-id="7f18a-201">Itt adhatja meg az SSH-kapcsolatokhoz használt SSH-hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="7f18a-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="7f18a-202">Ez csak a Linux-fürtök esetében érhető el.</span><span class="sxs-lookup"><span data-stu-id="7f18a-202">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="7f18a-203">-SshPublicKey</span></span>
<span data-ttu-id="7f18a-204">Az SSH-kapcsolatokhoz használt nyilvános kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="7f18a-205">Ez csak a Linux-fürtök esetében érhető el.</span><span class="sxs-lookup"><span data-stu-id="7f18a-205">This is only for Linux clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="7f18a-206">-SubnetName</span></span>
<span data-ttu-id="7f18a-207">A fürt kiválasztott virtuális hálózatán belüli alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-208">-Verzió</span><span class="sxs-lookup"><span data-stu-id="7f18a-208">-Version</span></span>
<span data-ttu-id="7f18a-209">A HDInsight-fürt HDI-változatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-209">Specifies the HDI version of the HDInsight cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="7f18a-210">-VirtualNetworkId</span></span>
<span data-ttu-id="7f18a-211">Annak a virtuális hálózatnak az AZONOSÍTÓját adja meg, amelybe a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="7f18a-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="7f18a-212">-WorkerNodeSize</span></span>
<span data-ttu-id="7f18a-213">A munkavégző csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="7f18a-214">Használja a Get-AzureRmVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="7f18a-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="7f18a-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="7f18a-216">A Zookeeper csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f18a-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="7f18a-217">Használja a Get-AzureRmVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="7f18a-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="7f18a-218">Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="7f18a-218">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f18a-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f18a-219">CommonParameters</span></span>
<span data-ttu-id="7f18a-220">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f18a-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f18a-221">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f18a-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f18a-222">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f18a-222">INPUTS</span></span>

### <span data-ttu-id="7f18a-223">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="7f18a-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="7f18a-224">Paraméterek: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7f18a-224">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="7f18a-225">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f18a-225">OUTPUTS</span></span>

### <span data-ttu-id="7f18a-226">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="7f18a-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="7f18a-227">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f18a-227">NOTES</span></span>
<span data-ttu-id="7f18a-228">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="7f18a-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="7f18a-229">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f18a-229">RELATED LINKS</span></span>

[<span data-ttu-id="7f18a-230">Új – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="7f18a-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

