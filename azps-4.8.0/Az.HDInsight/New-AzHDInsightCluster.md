---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 9008cb1dba2c39a2c552b2395f4115ca50a17fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024790"
---
# <span data-ttu-id="1f2fd-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1f2fd-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="1f2fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f2fd-102">SYNOPSIS</span></span>
<span data-ttu-id="1f2fd-103">Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="1f2fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f2fd-104">SYNTAX</span></span>

### <span data-ttu-id="1f2fd-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f2fd-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>]
 [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f2fd-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="1f2fd-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f2fd-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="1f2fd-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f2fd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f2fd-108">DESCRIPTION</span></span>
<span data-ttu-id="1f2fd-109">A New-AzHDInsightCluster Azure HDInsight-fürtöt hoz létre a megadott paraméterekkel vagy a New-AzHDInsightClusterConfig parancsmaggal létrehozott konfigurációs objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="1f2fd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1f2fd-110">EXAMPLES</span></span>

### <span data-ttu-id="1f2fd-111">Példa 1: Azure HDInsight-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="1f2fd-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="1f2fd-112">Ez a parancs létrehoz egy fürtöt az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="1f2fd-113">2. példa: fürt létrehozása ügyfél által felügyelt kulcsos lemezzel</span><span class="sxs-lookup"><span data-stu-id="1f2fd-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="1f2fd-114">3. példa: az Azure HDInsight-fürtök létrehozása, amely engedélyezi a titkosítást az átvitelben</span><span class="sxs-lookup"><span data-stu-id="1f2fd-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="1f2fd-115">4. példa: Azure HDInsight-fürt létrehozása privát hivatkozás funkcióval</span><span class="sxs-lookup"><span data-stu-id="1f2fd-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetresourceid"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="1f2fd-116">Példa 5: az Azure HDInsight-fürtök létrehozása, amely lehetővé teszi a titkosítást az állomáson</span><span class="sxs-lookup"><span data-stu-id="1f2fd-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="1f2fd-117">6. példa: hozzon létre egy Azure HDInsight-fürtöt, amely lehetővé teszi az automéretarányt.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

## <span data-ttu-id="1f2fd-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f2fd-118">PARAMETERS</span></span>

### <span data-ttu-id="1f2fd-119">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="1f2fd-119">-AadTenantId</span></span>
<span data-ttu-id="1f2fd-120">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-120">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="1f2fd-121">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="1f2fd-121">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="1f2fd-122">A fürt további Azure-tárolási fiókjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-122">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="1f2fd-123">A Add-AzHDInsightStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-123">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="1f2fd-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1f2fd-124">-ApplicationId</span></span>
<span data-ttu-id="1f2fd-125">Az Azure Data Lake elérési útjának beszerzése vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-125">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="1f2fd-126">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1f2fd-126">-AssignedIdentity</span></span>
<span data-ttu-id="1f2fd-127">A hozzárendelt identitás beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-127">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="1f2fd-128">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f2fd-128">-AutoscaleConfiguration</span></span>
<span data-ttu-id="1f2fd-129">Az automatikus méretezés beállítása vagy beállítása</span><span class="sxs-lookup"><span data-stu-id="1f2fd-129">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2fd-130">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="1f2fd-130">-CertificateFileContents</span></span>
<span data-ttu-id="1f2fd-131">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-131">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="1f2fd-132">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="1f2fd-132">-CertificateFilePath</span></span>
<span data-ttu-id="1f2fd-133">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-133">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="1f2fd-134">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-134">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="1f2fd-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1f2fd-135">-CertificatePassword</span></span>
<span data-ttu-id="1f2fd-136">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-136">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="1f2fd-137">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="1f2fd-138">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="1f2fd-138">-ClusterName</span></span>
<span data-ttu-id="1f2fd-139">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-139">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="1f2fd-140">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="1f2fd-140">-ClusterSizeInNodes</span></span>
<span data-ttu-id="1f2fd-141">A fürthöz tartozó munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-141">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="1f2fd-142">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="1f2fd-142">-ClusterTier</span></span>
<span data-ttu-id="1f2fd-143">A HDInsight-szektorcsoport rétegének meghatározása</span><span class="sxs-lookup"><span data-stu-id="1f2fd-143">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="1f2fd-144">Alapértelmezés szerint ez a normál.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-144">By default, this is Standard.</span></span>
<span data-ttu-id="1f2fd-145">A prémium szint csak Linux-fürtökkel használható, és lehetővé teszi néhány új funkció használatát.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-145">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="1f2fd-146">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="1f2fd-146">-ClusterType</span></span>
<span data-ttu-id="1f2fd-147">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-147">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="1f2fd-148">A következő lehetőségek közül választhat: Hadoop, HBase, vihar, szikra, INTERACTIVEHIVE, Kafka és RServer</span><span class="sxs-lookup"><span data-stu-id="1f2fd-148">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="1f2fd-149">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="1f2fd-149">-ComponentVersion</span></span>
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

### <span data-ttu-id="1f2fd-150">-Config</span><span class="sxs-lookup"><span data-stu-id="1f2fd-150">-Config</span></span>
<span data-ttu-id="1f2fd-151">Azt a szektorcsoport-objektumot adja meg, amellyel a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-151">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="1f2fd-152">Ezt az objektumot az New-AzHDInsightClusterConfig parancsmag segítségével hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-152">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="1f2fd-153">-Konfigurációk</span><span class="sxs-lookup"><span data-stu-id="1f2fd-153">-Configurations</span></span>
<span data-ttu-id="1f2fd-154">A HDInsight-fürt konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-154">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="1f2fd-155">A Add-AzHDInsightConfigValues parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-155">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="1f2fd-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f2fd-156">-DefaultProfile</span></span>
<span data-ttu-id="1f2fd-157">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1f2fd-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2fd-158">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1f2fd-158">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="1f2fd-159">A HDInsight-fürtöt használó alapértelmezett Azure-tárterülethez tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-159">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="1f2fd-160">A Set-AzHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-160">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="1f2fd-161">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1f2fd-161">-DefaultStorageAccountName</span></span>
<span data-ttu-id="1f2fd-162">Annak az alapértelmezett Azure-tárterületnek a nevét adja meg, amelyet a HDInsight-fürt használni fog.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-162">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="1f2fd-163">A Set-AzHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-163">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="1f2fd-164">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="1f2fd-164">-DefaultStorageAccountType</span></span>
<span data-ttu-id="1f2fd-165">A HDInsight-fürtöt használó alapértelmezett tárterület-fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-165">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="1f2fd-166">A lehetséges értékek a AzureStorage és a AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-166">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="1f2fd-167">Az alapértelmezett érték a AzureStorage, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-167">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="1f2fd-168">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1f2fd-168">-DefaultStorageContainer</span></span>
<span data-ttu-id="1f2fd-169">Annak az alapértelmezett tárolónak a nevét adja meg, amely a HDInsight-fürtöt használó alapértelmezett Azure Storage fiókban található.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-169">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="1f2fd-170">A Set-AzHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-170">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="1f2fd-171">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="1f2fd-171">-DefaultStorageRootPath</span></span>
<span data-ttu-id="1f2fd-172">Megadja az elérési utat az adattó-tároló fiókban, amelyet a HDInsight-fürt alapértelmezett fájlrendszerként fog használni.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-172">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="1f2fd-173">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="1f2fd-173">-DisksPerWorkerNode</span></span>
<span data-ttu-id="1f2fd-174">Itt adhatja meg a fürtben a munkavégző csomópont szerepkörrel rendelkező lemezek számát.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-174">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="1f2fd-175">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="1f2fd-175">-EdgeNodeSize</span></span>
<span data-ttu-id="1f2fd-176">Az Edge csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-176">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="1f2fd-177">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-177">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="1f2fd-178">Ez a paraméter csak a RServer-fürtök esetében érvényes.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-178">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="1f2fd-179">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1f2fd-179">-EncryptionAlgorithm</span></span>
<span data-ttu-id="1f2fd-180">A titkosítási algoritmust kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-180">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2fd-181">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="1f2fd-181">-EncryptionAtHost</span></span>
<span data-ttu-id="1f2fd-182">Beilleszti vagy beállítja azt a jelölőt, amely azt jelzi, hogy engedélyezve van-e a titkosítás az állomáson.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-182">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2fd-183">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="1f2fd-183">-EncryptionInTransit</span></span>
<span data-ttu-id="1f2fd-184">Beilleszti vagy beállítja azt a jelölőt, amely azt jelzi, hogy engedélyezve van-e a titkosítás a továbbításban.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-184">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2fd-185">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="1f2fd-185">-EncryptionKeyName</span></span>
<span data-ttu-id="1f2fd-186">A titkosítási kulcs nevének beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="1f2fd-186">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="1f2fd-187">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="1f2fd-187">-EncryptionKeyVersion</span></span>
<span data-ttu-id="1f2fd-188">A titkosító kulcs verziójának beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="1f2fd-188">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="1f2fd-189">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="1f2fd-189">-EncryptionVaultUri</span></span>
<span data-ttu-id="1f2fd-190">A titkosítási tároló URI-azonosítójának beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-190">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="1f2fd-191">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="1f2fd-191">-HeadNodeSize</span></span>
<span data-ttu-id="1f2fd-192">A fej csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-192">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="1f2fd-193">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-193">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="1f2fd-194">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="1f2fd-194">-HiveMetastore</span></span>
<span data-ttu-id="1f2fd-195">A kaptár metaadatait tároló SQL-adatbázist adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-195">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="1f2fd-196">A Add-AzHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-196">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="1f2fd-197">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="1f2fd-197">-HttpCredential</span></span>
<span data-ttu-id="1f2fd-198">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-198">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="1f2fd-199">-Hely</span><span class="sxs-lookup"><span data-stu-id="1f2fd-199">-Location</span></span>
<span data-ttu-id="1f2fd-200">A fürt helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-200">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="1f2fd-201">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="1f2fd-201">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="1f2fd-202">A minimálisan támogatott TLS-verziót kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-202">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="1f2fd-203">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1f2fd-203">-ObjectId</span></span>
<span data-ttu-id="1f2fd-204">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-204">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="1f2fd-205">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-205">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="1f2fd-206">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="1f2fd-206">-OozieMetastore</span></span>
<span data-ttu-id="1f2fd-207">Megadja a Oozie metaadatait tároló SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-207">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="1f2fd-208">A Add-AzHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-208">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="1f2fd-209">-OSType</span><span class="sxs-lookup"><span data-stu-id="1f2fd-209">-OSType</span></span>
<span data-ttu-id="1f2fd-210">A fürt operációs rendszerét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-210">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="1f2fd-211">A beállítások a következők: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="1f2fd-211">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="1f2fd-212">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="1f2fd-212">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="1f2fd-213">Beilleszti vagy beállítja a kimenő hozzáférési típust a nyilvános hálózatra.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-213">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2fd-214">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="1f2fd-214">-PublicNetworkAccessType</span></span>
<span data-ttu-id="1f2fd-215">A nyilvános hálózat elérési típusának beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="1f2fd-215">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2fd-216">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="1f2fd-216">-RdpAccessExpiry</span></span>
<span data-ttu-id="1f2fd-217">Itt adhatja meg a fürthöz az RDP-hozzáféréssel való hozzáférés időpontját DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-217">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="1f2fd-218">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="1f2fd-218">-RdpCredential</span></span>
<span data-ttu-id="1f2fd-219">A fürt távoli asztali (RDP) hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-219">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="1f2fd-220">Ez csak Windows-fürtök esetén használható.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-220">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="1f2fd-221">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f2fd-221">-ResourceGroupName</span></span>
<span data-ttu-id="1f2fd-222">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-222">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1f2fd-223">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="1f2fd-223">-ScriptActions</span></span>
<span data-ttu-id="1f2fd-224">Megadja, hogy milyen parancsfájl-műveletek legyenek futtathatók a fürtökön a fürtök létrehozása végén.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-224">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="1f2fd-225">Másik lehetőségként használhatja a bővítmények AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-225">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="1f2fd-226">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="1f2fd-226">-SecurityProfile</span></span>
<span data-ttu-id="1f2fd-227">A biztonságos fürtök létrehozásához használt biztonsággal kapcsolatos tulajdonságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-227">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="1f2fd-228">A Add-AzHDInsightSecurityProfile parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-228">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="1f2fd-229">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="1f2fd-229">-SshCredential</span></span>
<span data-ttu-id="1f2fd-230">Itt adhatja meg az SSH-kapcsolatokhoz használt SSH-hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-230">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="1f2fd-231">Ez csak a Linux-fürtök esetében érhető el.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-231">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="1f2fd-232">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="1f2fd-232">-SshPublicKey</span></span>
<span data-ttu-id="1f2fd-233">Az SSH-kapcsolatokhoz használt nyilvános kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-233">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="1f2fd-234">Ez csak a Linux-fürtök esetében érhető el.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="1f2fd-235">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="1f2fd-235">-SubnetName</span></span>
<span data-ttu-id="1f2fd-236">A fürt kiválasztott virtuális hálózatán belüli alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-236">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="1f2fd-237">-Verzió</span><span class="sxs-lookup"><span data-stu-id="1f2fd-237">-Version</span></span>
<span data-ttu-id="1f2fd-238">A HDInsight-fürt HDI-változatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-238">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="1f2fd-239">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="1f2fd-239">-VirtualNetworkId</span></span>
<span data-ttu-id="1f2fd-240">Annak a virtuális hálózatnak az AZONOSÍTÓját adja meg, amelybe a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-240">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="1f2fd-241">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="1f2fd-241">-WorkerNodeSize</span></span>
<span data-ttu-id="1f2fd-242">A munkavégző csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-242">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="1f2fd-243">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-243">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="1f2fd-244">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="1f2fd-244">-ZookeeperNodeSize</span></span>
<span data-ttu-id="1f2fd-245">A Zookeeper csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-245">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="1f2fd-246">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-246">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="1f2fd-247">Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-247">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="1f2fd-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f2fd-248">CommonParameters</span></span>
<span data-ttu-id="1f2fd-249">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f2fd-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f2fd-250">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1f2fd-250">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f2fd-251">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f2fd-251">INPUTS</span></span>

### <span data-ttu-id="1f2fd-252">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="1f2fd-252">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="1f2fd-253">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f2fd-253">OUTPUTS</span></span>

### <span data-ttu-id="1f2fd-254">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1f2fd-254">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="1f2fd-255">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f2fd-255">NOTES</span></span>
<span data-ttu-id="1f2fd-256">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="1f2fd-256">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="1f2fd-257">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f2fd-257">RELATED LINKS</span></span>

[<span data-ttu-id="1f2fd-258">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="1f2fd-258">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

