---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: f4592a371e528c7779e07251bf79677dac47e6df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466057"
---
# <span data-ttu-id="8165a-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8165a-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="8165a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8165a-102">SYNOPSIS</span></span>
<span data-ttu-id="8165a-103">Azure HDInsight-fürtöt hoz létre a megadott erőforráscsoportban az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="8165a-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="8165a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8165a-104">SYNTAX</span></span>

### <span data-ttu-id="8165a-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8165a-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-StorageAccountManagedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker] [-KafkaClientGroupId <String>]
 [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>] [-PrivateLink <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8165a-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="8165a-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8165a-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="8165a-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8165a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8165a-108">DESCRIPTION</span></span>
<span data-ttu-id="8165a-109">A New-AzHDInsightCluster azure HDInsight-fürtöt hoz létre a megadott paraméterek vagy egy, a New-AzHDInsightClusterConfig parancsmag használatával létrehozott konfigurációs objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="8165a-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="8165a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8165a-110">EXAMPLES</span></span>

### <span data-ttu-id="8165a-111">1. példa: Azure HDInsight-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="8165a-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="8165a-112">Ez a parancs létrehoz egy fürtöt az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="8165a-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="8165a-113">2. példa: Ügyfél által kezelt kulcs lemeztitkosítással létrehozott fürt</span><span class="sxs-lookup"><span data-stu-id="8165a-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="8165a-114">3. példa: Azure HDInsight-fürt létrehozása, amely titkosítást tesz lehetővé az átvitel során</span><span class="sxs-lookup"><span data-stu-id="8165a-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="8165a-115">4. példa: Azure HDInsight-fürt létrehozása a továbbítás kimenő és privát csatolási funkcióval</span><span class="sxs-lookup"><span data-stu-id="8165a-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
        $subnetName="yoursubnetname"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -ResourceProviderConnection Outbound -PrivateLink Enabled `
```

### <span data-ttu-id="8165a-116">5. példa: Azure HDInsight-fürt létrehozása, amely lehetővé teszi a titkosítást az állomásnál</span><span class="sxs-lookup"><span data-stu-id="8165a-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="8165a-117">6. példa: Hozzon létre egy Azure HDInsight-fürtöt, amely engedélyezi az automatikus méretezést.</span><span class="sxs-lookup"><span data-stu-id="8165a-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="8165a-118">7. példa: Azure HDInsight-fürt létrehozása a Kafka rest proxyval.</span><span class="sxs-lookup"><span data-stu-id="8165a-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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

        # Kafka Rest Proxy configuration info
        $kafkaClientGroupName = "yourclientgroupname"
        $kafkaClientGroupId = "yourclientgroupid"
        $kafkaManagementNodeSize = "Standard_D4_v2"
        $disksPerWorkerNode = 2

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Kafka `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -KafkaClientGroupId  $kafkaClientGroupId -KafkaClientGroupName $kafkaClientGroupName `
            -KafkaManagementNodeSize $kafkaManagementNodeSize -DisksPerWorkerNode $disksPerWorkerNode
```

### <span data-ttu-id="8165a-119">8. példa: Azure HDInsight-fürt létrehozása Azure Data Lake Gen2-tárhellyel.</span><span class="sxs-lookup"><span data-stu-id="8165a-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageManagedIdentity = "yourstorageusermanagedidentity"
        $storageFileSystem = "filesystem01"
        $storageAccountType=AzureDataLakeStorageGen2

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
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountManagedIdentity $storageManagedIdentity `
            -StorageFileSystem $storageFileSystem `
            -StorageAccountType $storageAccountType `
            -SshCredential $clusterCreds
```

### <span data-ttu-id="8165a-120">9. példa: Azure HDInsight-fürt létrehozása nagyvállalati biztonsági csomaggal (ESP) és a HDInsight ID Broker engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="8165a-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = "yourstorageaccountaccesskey"
        $storageContainer = "yourcontainer01"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # ESP configuration
        $domainResourceId = "your Azure AD Domin Service resource id"
        $domainUser = "yourdomainuser"
        $domainPassword = "yourdoaminpasswd"
        $domainPassword = ConvertTo-SecureString $domainPassword -AsPlainText -Force
        $domainCredential = New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
        $clusterUserGroupDns = "dominusergroup"
        $ldapUrls = "ldaps://{your domain name}:636"

        $clusterTier = Premium
        $vnetId = "yourvnetid"
        $subnetName = "yoursubnetname"
        $assignedIdentity = "your user managed assigned identity resourcee id"

        #Create security profile
        $config= New-AzHDInsightClusterConfig|Add-AzHDInsightSecurityProfile -DomainResourceId $domainResourceId -DomainUserCredential $domainCredential -LdapsUrls $ldapUrls -ClusterUsersGroupDNs $clusterUserGroupDns

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusteTier $clusterTier `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $vnetId -SubnetName $subnetName `
            -AssignedIdentity $assignedIdentity `
            -SecurityProfile $config.SecurityProfile -EnableIDBroker
```

## <span data-ttu-id="8165a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8165a-121">PARAMETERS</span></span>

### <span data-ttu-id="8165a-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="8165a-122">-AadTenantId</span></span>
<span data-ttu-id="8165a-123">Az Azure Data Lake Store elérésekor használt Azure AD bérlőazonosító.</span><span class="sxs-lookup"><span data-stu-id="8165a-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8165a-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="8165a-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="8165a-125">A fürt további Azure Storage-fiókjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="8165a-126">Másik lehetőségként használhatja a Add-AzHDInsightStorage parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8165a-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="8165a-127">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="8165a-127">-AmbariDatabase</span></span>
<span data-ttu-id="8165a-128">Beállítja vagy beállítja az adatbázist ambarihoz.</span><span class="sxs-lookup"><span data-stu-id="8165a-128">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="8165a-129">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8165a-129">-ApplicationId</span></span>
<span data-ttu-id="8165a-130">Beállítja vagy beállítja az Egyszerű szolgáltatásalkalmazás-azonosítót az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="8165a-130">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="8165a-131">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8165a-131">-AssignedIdentity</span></span>
<span data-ttu-id="8165a-132">Beállítja vagy beállítja a hozzárendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="8165a-132">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="8165a-133">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8165a-133">-AutoscaleConfiguration</span></span>
<span data-ttu-id="8165a-134">Beállítja vagy beállítja az automatikus skálázás konfigurációját</span><span class="sxs-lookup"><span data-stu-id="8165a-134">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="8165a-135">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="8165a-135">-CertificateFileContents</span></span>
<span data-ttu-id="8165a-136">Megadja annak a tanúsítványnak a fájl tartalmát, amely az Azure Data Lake Store elérésekor használatos.</span><span class="sxs-lookup"><span data-stu-id="8165a-136">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8165a-137">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="8165a-137">-CertificateFilePath</span></span>
<span data-ttu-id="8165a-138">Megadja annak a tanúsítványnak a fájl elérési útját, amely a szolgáltatásnévként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="8165a-138">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="8165a-139">A fürt ezt fogja használni az Azure Data Lake Store elérésekor.</span><span class="sxs-lookup"><span data-stu-id="8165a-139">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8165a-140">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8165a-140">-CertificatePassword</span></span>
<span data-ttu-id="8165a-141">Megadja annak a tanúsítványnak a jelszavát, amely a szolgáltatásnévként való hitelesítéshez használatos.</span><span class="sxs-lookup"><span data-stu-id="8165a-141">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="8165a-142">A fürt ezt fogja használni az Azure Data Lake Store elérésekor.</span><span class="sxs-lookup"><span data-stu-id="8165a-142">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8165a-143">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8165a-143">-ClusterName</span></span>
<span data-ttu-id="8165a-144">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-144">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8165a-145">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="8165a-145">-ClusterSizeInNodes</span></span>
<span data-ttu-id="8165a-146">A fürt dolgozói csomópontjainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-146">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="8165a-147">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="8165a-147">-ClusterTier</span></span>
<span data-ttu-id="8165a-148">A HDInsight-fürtréteget adja meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-148">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="8165a-149">Alapértelmezés szerint ez a Szabványos.</span><span class="sxs-lookup"><span data-stu-id="8165a-149">By default, this is Standard.</span></span>
<span data-ttu-id="8165a-150">A prémium szint csak Linux-fürtökhöz használható, és lehetővé teszi egyes új funkciók használatát.</span><span class="sxs-lookup"><span data-stu-id="8165a-150">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="8165a-151">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="8165a-151">-ClusterType</span></span>
<span data-ttu-id="8165a-152">A létrehozni szükséges fürt típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-152">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="8165a-153">A beállítások a következőek: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka és RServer</span><span class="sxs-lookup"><span data-stu-id="8165a-153">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="8165a-154">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="8165a-154">-ComponentVersion</span></span>
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

### <span data-ttu-id="8165a-155">-Config</span><span class="sxs-lookup"><span data-stu-id="8165a-155">-Config</span></span>
<span data-ttu-id="8165a-156">A fürt létrehozásához használt fürtobjektum.</span><span class="sxs-lookup"><span data-stu-id="8165a-156">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="8165a-157">Ezt az objektumot a New-AzHDInsightClusterConfig használatával lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="8165a-157">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="8165a-158">- Konfigurációk</span><span class="sxs-lookup"><span data-stu-id="8165a-158">-Configurations</span></span>
<span data-ttu-id="8165a-159">A HDInsight-fürt konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-159">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="8165a-160">Másik lehetőségként használhatja a Add-AzHDInsightConfigValues parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8165a-160">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="8165a-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8165a-161">-DefaultProfile</span></span>
<span data-ttu-id="8165a-162">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8165a-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8165a-163">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="8165a-163">-DisksPerWorkerNode</span></span>
<span data-ttu-id="8165a-164">Meghatározza a munkavégi csomópont szerepkörhöz a fürtben lévő lemezeket.</span><span class="sxs-lookup"><span data-stu-id="8165a-164">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="8165a-165">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="8165a-165">-EdgeNodeSize</span></span>
<span data-ttu-id="8165a-166">A virtuális gép mérete a peremcsomóponthoz.</span><span class="sxs-lookup"><span data-stu-id="8165a-166">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="8165a-167">A Get-AzVMSize a MEGFELELŐ VM-méretekért, és tekintse meg a HDInsight árazási lapját.</span><span class="sxs-lookup"><span data-stu-id="8165a-167">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="8165a-168">Ez a paraméter csak RServer-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="8165a-168">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="8165a-169">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="8165a-169">-EnableIDBroker</span></span>
<span data-ttu-id="8165a-170">Engedélyezi a HDInsight Identity Broker funkciót.</span><span class="sxs-lookup"><span data-stu-id="8165a-170">Enables HDInsight Identity Broker feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8165a-171">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="8165a-171">-EncryptionAlgorithm</span></span>
<span data-ttu-id="8165a-172">Beállítja vagy beállítja a titkosítási algoritmust.</span><span class="sxs-lookup"><span data-stu-id="8165a-172">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="8165a-173">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="8165a-173">-EncryptionAtHost</span></span>
<span data-ttu-id="8165a-174">Beállítja vagy beállítja a jelölőt, amely jelzi, hogy engedélyezi-e a titkosítást a gazdaszámítógépen.</span><span class="sxs-lookup"><span data-stu-id="8165a-174">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="8165a-175">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="8165a-175">-EncryptionInTransit</span></span>
<span data-ttu-id="8165a-176">Beállítja vagy beállítja a jelölőt, amely jelzi, hogy engedélyezi-e a titkosítást az átvitel során.</span><span class="sxs-lookup"><span data-stu-id="8165a-176">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="8165a-177">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="8165a-177">-EncryptionKeyName</span></span>
<span data-ttu-id="8165a-178">Beállítja vagy beállítja a titkosítási kulcs nevét.</span><span class="sxs-lookup"><span data-stu-id="8165a-178">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="8165a-179">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="8165a-179">-EncryptionKeyVersion</span></span>
<span data-ttu-id="8165a-180">Beállítja vagy beállítja a titkosítási kulcs verzióját.</span><span class="sxs-lookup"><span data-stu-id="8165a-180">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="8165a-181">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="8165a-181">-EncryptionVaultUri</span></span>
<span data-ttu-id="8165a-182">Beállítja vagy beállítja a titkosítási tároló uri-ját.</span><span class="sxs-lookup"><span data-stu-id="8165a-182">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="8165a-183">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="8165a-183">-HeadNodeSize</span></span>
<span data-ttu-id="8165a-184">A Head csomópont virtuális gépének mérete.</span><span class="sxs-lookup"><span data-stu-id="8165a-184">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="8165a-185">A Get-AzVMSize a MEGFELELŐ VM-méretekért, és tekintse meg a HDInsight árazási lapját.</span><span class="sxs-lookup"><span data-stu-id="8165a-185">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="8165a-186">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="8165a-186">-HiveMetastore</span></span>
<span data-ttu-id="8165a-187">Megadja, hogy az SQL-adatbázis tárolja a Hive-metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="8165a-187">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="8165a-188">Másik lehetőségként használhatja a Add-AzHDInsightMetastore parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8165a-188">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="8165a-189">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="8165a-189">-HttpCredential</span></span>
<span data-ttu-id="8165a-190">A fürt bejelentkezési (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="8165a-190">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="8165a-191">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="8165a-191">-KafkaClientGroupId</span></span>
<span data-ttu-id="8165a-192">Beállítja vagy beállítja a Kafka rest proxy hozzáférésének ügyfélcsoport-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="8165a-192">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="8165a-193">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="8165a-193">-KafkaClientGroupName</span></span>
<span data-ttu-id="8165a-194">Beállítja vagy beállítja a Kafka rest proxy hozzáférésének ügyfélcsoportnevét.</span><span class="sxs-lookup"><span data-stu-id="8165a-194">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="8165a-195">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="8165a-195">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="8165a-196">Beállítja vagy beállítja a Kafka felügyeleti csomópont méretét.</span><span class="sxs-lookup"><span data-stu-id="8165a-196">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="8165a-197">-Location</span><span class="sxs-lookup"><span data-stu-id="8165a-197">-Location</span></span>
<span data-ttu-id="8165a-198">A fürt helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-198">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="8165a-199">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8165a-199">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="8165a-200">Beállítja vagy beállítja a minimálisan támogatott TLS-verziót.</span><span class="sxs-lookup"><span data-stu-id="8165a-200">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="8165a-201">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8165a-201">-ObjectId</span></span>
<span data-ttu-id="8165a-202">A fürtöt képviselő Azure AD-szolgáltatásnév Azure AD-objektumazonosítóját (GUID azonosítóját) adja meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-202">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="8165a-203">A fürt ezt fogja használni az Azure Data Lake Store elérésekor.</span><span class="sxs-lookup"><span data-stu-id="8165a-203">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8165a-204">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="8165a-204">-OozieMetastore</span></span>
<span data-ttu-id="8165a-205">Megadja az Oozie-metaadatokat tároló SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="8165a-205">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="8165a-206">Másik lehetőségként használhatja a Add-AzHDInsightMetastore parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8165a-206">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="8165a-207">-OSType</span><span class="sxs-lookup"><span data-stu-id="8165a-207">-OSType</span></span>
<span data-ttu-id="8165a-208">A fürt operációs rendszerét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-208">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="8165a-209">A lehetőségek a következőek: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="8165a-209">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="8165a-210">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="8165a-210">-PrivateLink</span></span>
<span data-ttu-id="8165a-211">Beállítja vagy beállítja a személyes hivatkozás típusát.</span><span class="sxs-lookup"><span data-stu-id="8165a-211">Gets or sets the private link type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8165a-212">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="8165a-212">-RdpAccessExpiry</span></span>
<span data-ttu-id="8165a-213">A távoli asztali protokoll (RDP) fürthöz való hozzáférésének lejáratát adja meg DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="8165a-213">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="8165a-214">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="8165a-214">-RdpCredential</span></span>
<span data-ttu-id="8165a-215">A távoli asztal (RDP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="8165a-215">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="8165a-216">Ez csak Windows-fürtök esetén van így.</span><span class="sxs-lookup"><span data-stu-id="8165a-216">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="8165a-217">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8165a-217">-ResourceGroupName</span></span>
<span data-ttu-id="8165a-218">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-218">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8165a-219">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="8165a-219">-ResourceProviderConnection</span></span>
<span data-ttu-id="8165a-220">Beállítja vagy beállítja az erőforrás-szolgáltató kapcsolattípusát.</span><span class="sxs-lookup"><span data-stu-id="8165a-220">Gets or sets the resource provider connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8165a-221">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="8165a-221">-ScriptActions</span></span>
<span data-ttu-id="8165a-222">Megadja a fürt létrehozási végén a fürtön futtatható parancsfájl-műveleteket.</span><span class="sxs-lookup"><span data-stu-id="8165a-222">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="8165a-223">Használhatja az Add-AzHDInsightScriptAction bővítményt is.</span><span class="sxs-lookup"><span data-stu-id="8165a-223">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="8165a-224">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="8165a-224">-SecurityProfile</span></span>
<span data-ttu-id="8165a-225">Megadja a biztonságos fürt létrehozásához használt, biztonsággal kapcsolatos tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="8165a-225">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="8165a-226">Másik lehetőségként használhatja a Add-AzHDInsightSecurityProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8165a-226">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="8165a-227">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="8165a-227">-SshCredential</span></span>
<span data-ttu-id="8165a-228">Az SSH-kapcsolatokhoz használt SSH hitelesítő adatokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-228">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="8165a-229">Ez csak Linux-fürtök esetén használható.</span><span class="sxs-lookup"><span data-stu-id="8165a-229">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="8165a-230">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="8165a-230">-SshPublicKey</span></span>
<span data-ttu-id="8165a-231">Az SSH-kapcsolatokhoz használt nyilvános kulcs.</span><span class="sxs-lookup"><span data-stu-id="8165a-231">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="8165a-232">Ez csak Linux-fürtök esetén használható.</span><span class="sxs-lookup"><span data-stu-id="8165a-232">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="8165a-233">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8165a-233">-StorageAccountKey</span></span>
<span data-ttu-id="8165a-234">Beállítja vagy beállítja a Tárfiók hozzáférési kulcsát a tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="8165a-234">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="8165a-235">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="8165a-235">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="8165a-236">Beállítja vagy beállítja a tárfiók felügyelt identitását.</span><span class="sxs-lookup"><span data-stu-id="8165a-236">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="8165a-237">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8165a-237">-StorageAccountResourceId</span></span>
<span data-ttu-id="8165a-238">Beállítja vagy beállítja a tárfiók tárerőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="8165a-238">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="8165a-239">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8165a-239">-StorageAccountType</span></span>
<span data-ttu-id="8165a-240">Beállítja vagy beállítja a tárfiók típusát.</span><span class="sxs-lookup"><span data-stu-id="8165a-240">Gets or sets the type of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8165a-241">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="8165a-241">-StorageContainer</span></span>
<span data-ttu-id="8165a-242">Beállítja vagy beállítja a StorageContainer nevét az alapértelmezett Azure Storage-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="8165a-242">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="8165a-243">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="8165a-243">-StorageFileSystem</span></span>
<span data-ttu-id="8165a-244">Beállítja vagy beállítja az alapértelmezett Azure Data Lake Storage Gen2-fiók fájlrendszerét.</span><span class="sxs-lookup"><span data-stu-id="8165a-244">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="8165a-245">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="8165a-245">-StorageRootPath</span></span>
<span data-ttu-id="8165a-246">Beállítja vagy beállítja a fürt gyökér elérési útját az alapértelmezett Data Lake Store-fiókban.</span><span class="sxs-lookup"><span data-stu-id="8165a-246">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="8165a-247">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8165a-247">-SubnetName</span></span>
<span data-ttu-id="8165a-248">Beállítja vagy beállítja ennek a HDInsight-fürtnek az alhálózatnevét.</span><span class="sxs-lookup"><span data-stu-id="8165a-248">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8165a-249">-Version</span><span class="sxs-lookup"><span data-stu-id="8165a-249">-Version</span></span>
<span data-ttu-id="8165a-250">A HDInsight-fürt HDI-verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8165a-250">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="8165a-251">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8165a-251">-VirtualNetworkId</span></span>
<span data-ttu-id="8165a-252">Annak a virtuális hálózatnak az azonosítója, amelybe a fürtöt ki kellépítenünk.</span><span class="sxs-lookup"><span data-stu-id="8165a-252">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="8165a-253">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="8165a-253">-WorkerNodeSize</span></span>
<span data-ttu-id="8165a-254">A Munkavégző csomópont virtuális gépének mérete.</span><span class="sxs-lookup"><span data-stu-id="8165a-254">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="8165a-255">A Get-AzVMSize a MEGFELELŐ VM-méretekért, és tekintse meg a HDInsight árazási lapját.</span><span class="sxs-lookup"><span data-stu-id="8165a-255">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="8165a-256">-ÁllatmemónisnodeSize</span><span class="sxs-lookup"><span data-stu-id="8165a-256">-ZookeeperNodeSize</span></span>
<span data-ttu-id="8165a-257">Az Állatkezelő csomópont virtuális gépének mérete.</span><span class="sxs-lookup"><span data-stu-id="8165a-257">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="8165a-258">A Get-AzVMSize a MEGFELELŐ VM-méretekért, és tekintse meg a HDInsight árazási lapját.</span><span class="sxs-lookup"><span data-stu-id="8165a-258">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="8165a-259">Ez a paraméter csak HBase vagy Storm fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="8165a-259">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="8165a-260">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8165a-260">CommonParameters</span></span>
<span data-ttu-id="8165a-261">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8165a-261">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8165a-262">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8165a-262">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8165a-263">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8165a-263">INPUTS</span></span>

### <span data-ttu-id="8165a-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="8165a-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="8165a-265">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8165a-265">OUTPUTS</span></span>

### <span data-ttu-id="8165a-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8165a-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="8165a-267">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8165a-267">NOTES</span></span>
<span data-ttu-id="8165a-268">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hadoop, hdinsight, hd, insight</span><span class="sxs-lookup"><span data-stu-id="8165a-268">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="8165a-269">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8165a-269">RELATED LINKS</span></span>

[<span data-ttu-id="8165a-270">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8165a-270">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

