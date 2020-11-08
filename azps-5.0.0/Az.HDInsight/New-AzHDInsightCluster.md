---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: b42b93bbecef5ec56495be632788bd1373ae9db1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185357"
---
# <span data-ttu-id="ee560-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ee560-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="ee560-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee560-102">SYNOPSIS</span></span>
<span data-ttu-id="ee560-103">Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="ee560-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="ee560-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee560-104">SYNTAX</span></span>

### <span data-ttu-id="ee560-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee560-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee560-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ee560-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee560-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ee560-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee560-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee560-108">DESCRIPTION</span></span>
<span data-ttu-id="ee560-109">A New-AzHDInsightCluster Azure HDInsight-fürtöt hoz létre a megadott paraméterekkel vagy a New-AzHDInsightClusterConfig parancsmaggal létrehozott konfigurációs objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="ee560-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ee560-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ee560-110">EXAMPLES</span></span>

### <span data-ttu-id="ee560-111">Példa 1: Azure HDInsight-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="ee560-111">Example 1: Create an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="ee560-112">Ez a parancs létrehoz egy fürtöt az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="ee560-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="ee560-113">2. példa: fürt létrehozása ügyfél által felügyelt kulcsos lemezzel</span><span class="sxs-lookup"><span data-stu-id="ee560-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
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

### <span data-ttu-id="ee560-114">3. példa: az Azure HDInsight-fürtök létrehozása, amely engedélyezi a titkosítást az átvitelben</span><span class="sxs-lookup"><span data-stu-id="ee560-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
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

### <span data-ttu-id="ee560-115">4. példa: Azure HDInsight-fürt létrehozása privát hivatkozás funkcióval</span><span class="sxs-lookup"><span data-stu-id="ee560-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
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
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="ee560-116">Példa 5: az Azure HDInsight-fürtök létrehozása, amely lehetővé teszi a titkosítást az állomáson</span><span class="sxs-lookup"><span data-stu-id="ee560-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
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

### <span data-ttu-id="ee560-117">6. példa: hozzon létre egy Azure HDInsight-fürtöt, amely lehetővé teszi az automéretarányt.</span><span class="sxs-lookup"><span data-stu-id="ee560-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
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

### <span data-ttu-id="ee560-118">7. példa: hozzon létre egy Azure HDInsight-fürtöt a Kafka Rest proxyval.</span><span class="sxs-lookup"><span data-stu-id="ee560-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
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

### <span data-ttu-id="ee560-119">8. példa: hozzon létre egy Azure HDInsight-fürtöt az Azure Data Lake Gen2-tárterülettel.</span><span class="sxs-lookup"><span data-stu-id="ee560-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="ee560-120">9. példa: az Azure HDInsight-alapú fürtök létrehozása nagyvállalati biztonsági csomaggal (ESP) és a HDInsight-AZONOSÍTÓk engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="ee560-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

## <span data-ttu-id="ee560-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee560-121">PARAMETERS</span></span>

### <span data-ttu-id="ee560-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="ee560-122">-AadTenantId</span></span>
<span data-ttu-id="ee560-123">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="ee560-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ee560-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="ee560-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="ee560-125">A fürt további Azure-tárolási fiókjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="ee560-126">A Add-AzHDInsightStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="ee560-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="ee560-127">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ee560-127">-ApplicationId</span></span>
<span data-ttu-id="ee560-128">Az Azure Data Lake elérési útjának beszerzése vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="ee560-128">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="ee560-129">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ee560-129">-AssignedIdentity</span></span>
<span data-ttu-id="ee560-130">A hozzárendelt identitás beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="ee560-130">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="ee560-131">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee560-131">-AutoscaleConfiguration</span></span>
<span data-ttu-id="ee560-132">Az automatikus méretezés beállítása vagy beállítása</span><span class="sxs-lookup"><span data-stu-id="ee560-132">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="ee560-133">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ee560-133">-CertificateFileContents</span></span>
<span data-ttu-id="ee560-134">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-134">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ee560-135">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ee560-135">-CertificateFilePath</span></span>
<span data-ttu-id="ee560-136">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="ee560-136">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ee560-137">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="ee560-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ee560-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ee560-138">-CertificatePassword</span></span>
<span data-ttu-id="ee560-139">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="ee560-139">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ee560-140">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="ee560-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ee560-141">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="ee560-141">-ClusterName</span></span>
<span data-ttu-id="ee560-142">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-142">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ee560-143">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="ee560-143">-ClusterSizeInNodes</span></span>
<span data-ttu-id="ee560-144">A fürthöz tartozó munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-144">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="ee560-145">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="ee560-145">-ClusterTier</span></span>
<span data-ttu-id="ee560-146">A HDInsight-szektorcsoport rétegének meghatározása</span><span class="sxs-lookup"><span data-stu-id="ee560-146">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="ee560-147">Alapértelmezés szerint ez a normál.</span><span class="sxs-lookup"><span data-stu-id="ee560-147">By default, this is Standard.</span></span>
<span data-ttu-id="ee560-148">A prémium szint csak Linux-fürtökkel használható, és lehetővé teszi néhány új funkció használatát.</span><span class="sxs-lookup"><span data-stu-id="ee560-148">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="ee560-149">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="ee560-149">-ClusterType</span></span>
<span data-ttu-id="ee560-150">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-150">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="ee560-151">A következő lehetőségek közül választhat: Hadoop, HBase, vihar, szikra, INTERACTIVEHIVE, Kafka és RServer</span><span class="sxs-lookup"><span data-stu-id="ee560-151">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="ee560-152">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="ee560-152">-ComponentVersion</span></span>
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

### <span data-ttu-id="ee560-153">-Config</span><span class="sxs-lookup"><span data-stu-id="ee560-153">-Config</span></span>
<span data-ttu-id="ee560-154">Azt a szektorcsoport-objektumot adja meg, amellyel a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="ee560-154">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="ee560-155">Ezt az objektumot az New-AzHDInsightClusterConfig parancsmag segítségével hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="ee560-155">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="ee560-156">-Konfigurációk</span><span class="sxs-lookup"><span data-stu-id="ee560-156">-Configurations</span></span>
<span data-ttu-id="ee560-157">A HDInsight-fürt konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-157">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="ee560-158">A Add-AzHDInsightConfigValues parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="ee560-158">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="ee560-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee560-159">-DefaultProfile</span></span>
<span data-ttu-id="ee560-160">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ee560-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee560-161">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="ee560-161">-DisksPerWorkerNode</span></span>
<span data-ttu-id="ee560-162">Itt adhatja meg a fürtben a munkavégző csomópont szerepkörrel rendelkező lemezek számát.</span><span class="sxs-lookup"><span data-stu-id="ee560-162">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="ee560-163">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="ee560-163">-EdgeNodeSize</span></span>
<span data-ttu-id="ee560-164">Az Edge csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-164">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="ee560-165">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="ee560-165">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="ee560-166">Ez a paraméter csak a RServer-fürtök esetében érvényes.</span><span class="sxs-lookup"><span data-stu-id="ee560-166">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="ee560-167">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="ee560-167">-EnableIDBroker</span></span>
<span data-ttu-id="ee560-168">Engedélyezi a HDInsight Identity Broker funkció használatát.</span><span class="sxs-lookup"><span data-stu-id="ee560-168">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="ee560-169">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ee560-169">-EncryptionAlgorithm</span></span>
<span data-ttu-id="ee560-170">A titkosítási algoritmust kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="ee560-170">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="ee560-171">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="ee560-171">-EncryptionAtHost</span></span>
<span data-ttu-id="ee560-172">Beilleszti vagy beállítja azt a jelölőt, amely azt jelzi, hogy engedélyezve van-e a titkosítás az állomáson.</span><span class="sxs-lookup"><span data-stu-id="ee560-172">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="ee560-173">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="ee560-173">-EncryptionInTransit</span></span>
<span data-ttu-id="ee560-174">Beilleszti vagy beállítja azt a jelölőt, amely azt jelzi, hogy engedélyezve van-e a titkosítás a továbbításban.</span><span class="sxs-lookup"><span data-stu-id="ee560-174">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="ee560-175">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="ee560-175">-EncryptionKeyName</span></span>
<span data-ttu-id="ee560-176">A titkosítási kulcs nevének beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="ee560-176">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="ee560-177">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="ee560-177">-EncryptionKeyVersion</span></span>
<span data-ttu-id="ee560-178">A titkosító kulcs verziójának beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="ee560-178">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="ee560-179">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="ee560-179">-EncryptionVaultUri</span></span>
<span data-ttu-id="ee560-180">A titkosítási tároló URI-azonosítójának beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="ee560-180">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="ee560-181">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="ee560-181">-HeadNodeSize</span></span>
<span data-ttu-id="ee560-182">A fej csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-182">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="ee560-183">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="ee560-183">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="ee560-184">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="ee560-184">-HiveMetastore</span></span>
<span data-ttu-id="ee560-185">A kaptár metaadatait tároló SQL-adatbázist adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-185">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="ee560-186">A Add-AzHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="ee560-186">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="ee560-187">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="ee560-187">-HttpCredential</span></span>
<span data-ttu-id="ee560-188">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="ee560-188">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="ee560-189">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="ee560-189">-KafkaClientGroupId</span></span>
<span data-ttu-id="ee560-190">Megkapja vagy beállítja a Kafka-REST-alapú hozzáférés ügyfélalkalmazás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="ee560-190">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="ee560-191">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="ee560-191">-KafkaClientGroupName</span></span>
<span data-ttu-id="ee560-192">Megkapja vagy beállítja az ügyfél csoportjának nevét a Kafka-Rest proxy eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="ee560-192">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="ee560-193">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="ee560-193">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="ee560-194">Megkapja vagy beállítja a Kafka-kezelési csomópont méretét.</span><span class="sxs-lookup"><span data-stu-id="ee560-194">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="ee560-195">-Hely</span><span class="sxs-lookup"><span data-stu-id="ee560-195">-Location</span></span>
<span data-ttu-id="ee560-196">A fürt helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-196">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="ee560-197">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ee560-197">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="ee560-198">A minimálisan támogatott TLS-verziót kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="ee560-198">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="ee560-199">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ee560-199">-ObjectId</span></span>
<span data-ttu-id="ee560-200">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="ee560-200">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="ee560-201">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="ee560-201">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ee560-202">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="ee560-202">-OozieMetastore</span></span>
<span data-ttu-id="ee560-203">Megadja a Oozie metaadatait tároló SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="ee560-203">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="ee560-204">A Add-AzHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="ee560-204">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="ee560-205">-OSType</span><span class="sxs-lookup"><span data-stu-id="ee560-205">-OSType</span></span>
<span data-ttu-id="ee560-206">A fürt operációs rendszerét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-206">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="ee560-207">A beállítások a következők: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="ee560-207">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="ee560-208">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="ee560-208">-RdpAccessExpiry</span></span>
<span data-ttu-id="ee560-209">Itt adhatja meg a fürthöz az RDP-hozzáféréssel való hozzáférés időpontját DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="ee560-209">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="ee560-210">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="ee560-210">-RdpCredential</span></span>
<span data-ttu-id="ee560-211">A fürt távoli asztali (RDP) hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-211">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="ee560-212">Ez csak Windows-fürtök esetén használható.</span><span class="sxs-lookup"><span data-stu-id="ee560-212">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="ee560-213">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee560-213">-ResourceGroupName</span></span>
<span data-ttu-id="ee560-214">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-214">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ee560-215">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="ee560-215">-ScriptActions</span></span>
<span data-ttu-id="ee560-216">Megadja, hogy milyen parancsfájl-műveletek legyenek futtathatók a fürtökön a fürtök létrehozása végén.</span><span class="sxs-lookup"><span data-stu-id="ee560-216">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="ee560-217">Másik lehetőségként használhatja a bővítmények AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="ee560-217">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="ee560-218">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="ee560-218">-SecurityProfile</span></span>
<span data-ttu-id="ee560-219">A biztonságos fürtök létrehozásához használt biztonsággal kapcsolatos tulajdonságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-219">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="ee560-220">A Add-AzHDInsightSecurityProfile parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="ee560-220">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="ee560-221">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="ee560-221">-SshCredential</span></span>
<span data-ttu-id="ee560-222">Itt adhatja meg az SSH-kapcsolatokhoz használt SSH-hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="ee560-222">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="ee560-223">Ez csak a Linux-fürtök esetében érhető el.</span><span class="sxs-lookup"><span data-stu-id="ee560-223">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="ee560-224">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ee560-224">-SshPublicKey</span></span>
<span data-ttu-id="ee560-225">Az SSH-kapcsolatokhoz használt nyilvános kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-225">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="ee560-226">Ez csak a Linux-fürtök esetében érhető el.</span><span class="sxs-lookup"><span data-stu-id="ee560-226">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="ee560-227">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ee560-227">-StorageAccountKey</span></span>
<span data-ttu-id="ee560-228">Megkapja vagy beállítja a tárterület-hozzáférés kulcsát a tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="ee560-228">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="ee560-229">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ee560-229">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="ee560-230">A távtárolású fiók felügyelt identitását kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="ee560-230">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="ee560-231">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ee560-231">-StorageAccountResourceId</span></span>
<span data-ttu-id="ee560-232">A tárolási fiók tárolási erőforrás-azonosítóját adja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="ee560-232">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="ee560-233">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ee560-233">-StorageAccountType</span></span>
<span data-ttu-id="ee560-234">Megkapja vagy beállítja a tárolási fiók típusát.</span><span class="sxs-lookup"><span data-stu-id="ee560-234">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="ee560-235">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="ee560-235">-StorageContainer</span></span>
<span data-ttu-id="ee560-236">Az alapértelmezett Azure tárterület-fiók StorageContainer kapja vagy adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-236">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="ee560-237">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="ee560-237">-StorageFileSystem</span></span>
<span data-ttu-id="ee560-238">Az alapértelmezett Azure Data Lake Storage Gen2-fiók fájlrendszerének beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="ee560-238">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="ee560-239">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="ee560-239">-StorageRootPath</span></span>
<span data-ttu-id="ee560-240">A fürt gyökerének elérési útját az alapértelmezett adattó-tároló fiókban kapja vagy adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-240">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="ee560-241">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ee560-241">-SubnetName</span></span>
<span data-ttu-id="ee560-242">A HDInsight-fürt alhálózati nevének beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="ee560-242">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="ee560-243">-Verzió</span><span class="sxs-lookup"><span data-stu-id="ee560-243">-Version</span></span>
<span data-ttu-id="ee560-244">A HDInsight-fürt HDI-változatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-244">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="ee560-245">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ee560-245">-VirtualNetworkId</span></span>
<span data-ttu-id="ee560-246">Annak a virtuális hálózatnak az AZONOSÍTÓját adja meg, amelybe a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="ee560-246">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="ee560-247">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="ee560-247">-WorkerNodeSize</span></span>
<span data-ttu-id="ee560-248">A munkavégző csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-248">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="ee560-249">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="ee560-249">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="ee560-250">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="ee560-250">-ZookeeperNodeSize</span></span>
<span data-ttu-id="ee560-251">A Zookeeper csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee560-251">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="ee560-252">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="ee560-252">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="ee560-253">Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="ee560-253">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="ee560-254">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee560-254">CommonParameters</span></span>
<span data-ttu-id="ee560-255">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee560-255">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee560-256">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ee560-256">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee560-257">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee560-257">INPUTS</span></span>

### <span data-ttu-id="ee560-258">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ee560-258">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ee560-259">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee560-259">OUTPUTS</span></span>

### <span data-ttu-id="ee560-260">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ee560-260">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="ee560-261">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee560-261">NOTES</span></span>
<span data-ttu-id="ee560-262">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="ee560-262">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="ee560-263">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee560-263">RELATED LINKS</span></span>

[<span data-ttu-id="ee560-264">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ee560-264">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

