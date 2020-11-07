---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: a372654faa9c3f157c44e5f60ff2f4244cd16d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666350"
---
# <span data-ttu-id="326d8-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="326d8-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="326d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="326d8-102">SYNOPSIS</span></span>
<span data-ttu-id="326d8-103">Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="326d8-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="326d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="326d8-104">SYNTAX</span></span>

### <span data-ttu-id="326d8-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="326d8-105">Default (Default)</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="326d8-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="326d8-106">CertificateFilePath</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="326d8-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="326d8-107">CertificateFileContents</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="326d8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="326d8-108">DESCRIPTION</span></span>
<span data-ttu-id="326d8-109">A New-AzHDInsightCluster Azure HDInsight-fürtöt hoz létre a megadott paraméterekkel vagy a New-AzHDInsightClusterConfig parancsmaggal létrehozott konfigurációs objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="326d8-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="326d8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="326d8-110">EXAMPLES</span></span>

### <span data-ttu-id="326d8-111">Példa 1: Azure HDInsight-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="326d8-111">Example 1: Create an Azure HDInsight cluster</span></span>
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
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
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

<span data-ttu-id="326d8-112">Ez a parancs létrehoz egy fürtöt az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="326d8-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="326d8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="326d8-113">PARAMETERS</span></span>

### <span data-ttu-id="326d8-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="326d8-114">-AadTenantId</span></span>
<span data-ttu-id="326d8-115">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="326d8-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="326d8-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="326d8-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="326d8-117">A fürt további Azure-tárolási fiókjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="326d8-118">A Add-AzHDInsightStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="326d8-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="326d8-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="326d8-119">-CertificateFileContents</span></span>
<span data-ttu-id="326d8-120">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="326d8-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="326d8-121">-CertificateFilePath</span></span>
<span data-ttu-id="326d8-122">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="326d8-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="326d8-123">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="326d8-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="326d8-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="326d8-124">-CertificatePassword</span></span>
<span data-ttu-id="326d8-125">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="326d8-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="326d8-126">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="326d8-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="326d8-127">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="326d8-127">-ClusterName</span></span>
<span data-ttu-id="326d8-128">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-128">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="326d8-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="326d8-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="326d8-130">A fürthöz tartozó munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-130">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="326d8-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="326d8-131">-ClusterTier</span></span>
<span data-ttu-id="326d8-132">A HDInsight-szektorcsoport rétegének meghatározása</span><span class="sxs-lookup"><span data-stu-id="326d8-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="326d8-133">Alapértelmezés szerint ez a normál.</span><span class="sxs-lookup"><span data-stu-id="326d8-133">By default, this is Standard.</span></span>
<span data-ttu-id="326d8-134">A prémium szint csak Linux-fürtökkel használható, és lehetővé teszi néhány új funkció használatát.</span><span class="sxs-lookup"><span data-stu-id="326d8-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="326d8-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="326d8-135">-ClusterType</span></span>
<span data-ttu-id="326d8-136">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="326d8-137">A beállítások a következők: Hadoop, HBase, Storm, szikra</span><span class="sxs-lookup"><span data-stu-id="326d8-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="326d8-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="326d8-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="326d8-139">-Config</span><span class="sxs-lookup"><span data-stu-id="326d8-139">-Config</span></span>
<span data-ttu-id="326d8-140">Azt a szektorcsoport-objektumot adja meg, amellyel a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="326d8-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="326d8-141">Ezt az objektumot az New-AzHDInsightClusterConfig parancsmag segítségével hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="326d8-141">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="326d8-142">-Konfigurációk</span><span class="sxs-lookup"><span data-stu-id="326d8-142">-Configurations</span></span>
<span data-ttu-id="326d8-143">A HDInsight-fürt konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="326d8-144">A Add-AzHDInsightConfigValues parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="326d8-144">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="326d8-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326d8-145">-DefaultProfile</span></span>
<span data-ttu-id="326d8-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="326d8-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="326d8-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="326d8-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="326d8-148">A HDInsight-fürtöt használó alapértelmezett Azure-tárterülethez tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="326d8-149">A Set-AzHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="326d8-149">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="326d8-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="326d8-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="326d8-151">Annak az alapértelmezett Azure-tárterületnek a nevét adja meg, amelyet a HDInsight-fürt használni fog.</span><span class="sxs-lookup"><span data-stu-id="326d8-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="326d8-152">A Set-AzHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="326d8-152">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="326d8-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="326d8-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="326d8-154">A HDInsight-fürtöt használó alapértelmezett tárterület-fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="326d8-155">A lehetséges értékek a AzureStorage és a AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="326d8-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="326d8-156">Az alapértelmezett érték a AzureStorage, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="326d8-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="326d8-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="326d8-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="326d8-158">Annak az alapértelmezett tárolónak a nevét adja meg, amely a HDInsight-fürtöt használó alapértelmezett Azure Storage fiókban található.</span><span class="sxs-lookup"><span data-stu-id="326d8-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="326d8-159">A Set-AzHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="326d8-159">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="326d8-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="326d8-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="326d8-161">Megadja az elérési utat az adattó-tároló fiókban, amelyet a HDInsight-fürt alapértelmezett fájlrendszerként fog használni.</span><span class="sxs-lookup"><span data-stu-id="326d8-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="326d8-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="326d8-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="326d8-163">Itt adhatja meg a fürtben a munkavégző csomópont szerepkörrel rendelkező lemezek számát.</span><span class="sxs-lookup"><span data-stu-id="326d8-163">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="326d8-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="326d8-164">-EdgeNodeSize</span></span>
<span data-ttu-id="326d8-165">Az Edge csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="326d8-166">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="326d8-166">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="326d8-167">Ez a paraméter csak a RServer-fürtök esetében érvényes.</span><span class="sxs-lookup"><span data-stu-id="326d8-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="326d8-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="326d8-168">-HeadNodeSize</span></span>
<span data-ttu-id="326d8-169">A fej csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="326d8-170">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="326d8-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="326d8-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="326d8-171">-HiveMetastore</span></span>
<span data-ttu-id="326d8-172">A kaptár metaadatait tároló SQL-adatbázist adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="326d8-173">A Add-AzHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="326d8-173">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="326d8-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="326d8-174">-HttpCredential</span></span>
<span data-ttu-id="326d8-175">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="326d8-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="326d8-176">-Hely</span><span class="sxs-lookup"><span data-stu-id="326d8-176">-Location</span></span>
<span data-ttu-id="326d8-177">A fürt helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-177">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="326d8-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="326d8-178">-ObjectId</span></span>
<span data-ttu-id="326d8-179">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="326d8-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="326d8-180">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="326d8-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="326d8-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="326d8-181">-OozieMetastore</span></span>
<span data-ttu-id="326d8-182">Megadja a Oozie metaadatait tároló SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="326d8-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="326d8-183">A Add-AzHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="326d8-183">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="326d8-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="326d8-184">-OSType</span></span>
<span data-ttu-id="326d8-185">A fürt operációs rendszerét adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="326d8-186">A beállítások a következők: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="326d8-186">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="326d8-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="326d8-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="326d8-188">Itt adhatja meg a fürthöz az RDP-hozzáféréssel való hozzáférés időpontját DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="326d8-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="326d8-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="326d8-189">-RdpCredential</span></span>
<span data-ttu-id="326d8-190">A fürt távoli asztali (RDP) hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="326d8-191">Ez csak Windows-fürtök esetén használható.</span><span class="sxs-lookup"><span data-stu-id="326d8-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="326d8-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="326d8-192">-ResourceGroupName</span></span>
<span data-ttu-id="326d8-193">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-193">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="326d8-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="326d8-194">-ScriptActions</span></span>
<span data-ttu-id="326d8-195">Megadja, hogy milyen parancsfájl-műveletek legyenek futtathatók a fürtökön a fürtök létrehozása végén.</span><span class="sxs-lookup"><span data-stu-id="326d8-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="326d8-196">Másik lehetőségként használhatja a bővítmények AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="326d8-196">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="326d8-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="326d8-197">-SecurityProfile</span></span>
<span data-ttu-id="326d8-198">A biztonságos fürtök létrehozásához használt biztonsággal kapcsolatos tulajdonságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="326d8-199">A Add-AzHDInsightSecurityProfile parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="326d8-199">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="326d8-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="326d8-200">-SshCredential</span></span>
<span data-ttu-id="326d8-201">Itt adhatja meg az SSH-kapcsolatokhoz használt SSH-hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="326d8-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="326d8-202">Ez csak a Linux-fürtök esetében érhető el.</span><span class="sxs-lookup"><span data-stu-id="326d8-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="326d8-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="326d8-203">-SshPublicKey</span></span>
<span data-ttu-id="326d8-204">Az SSH-kapcsolatokhoz használt nyilvános kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="326d8-205">Ez csak a Linux-fürtök esetében érhető el.</span><span class="sxs-lookup"><span data-stu-id="326d8-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="326d8-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="326d8-206">-SubnetName</span></span>
<span data-ttu-id="326d8-207">A fürt kiválasztott virtuális hálózatán belüli alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="326d8-208">-Verzió</span><span class="sxs-lookup"><span data-stu-id="326d8-208">-Version</span></span>
<span data-ttu-id="326d8-209">A HDInsight-fürt HDI-változatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="326d8-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="326d8-210">-VirtualNetworkId</span></span>
<span data-ttu-id="326d8-211">Annak a virtuális hálózatnak az AZONOSÍTÓját adja meg, amelybe a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="326d8-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="326d8-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="326d8-212">-WorkerNodeSize</span></span>
<span data-ttu-id="326d8-213">A munkavégző csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="326d8-214">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="326d8-214">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="326d8-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="326d8-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="326d8-216">A Zookeeper csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="326d8-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="326d8-217">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="326d8-217">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="326d8-218">Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="326d8-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="326d8-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326d8-219">CommonParameters</span></span>
<span data-ttu-id="326d8-220">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="326d8-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326d8-221">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="326d8-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326d8-222">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="326d8-222">INPUTS</span></span>

### <span data-ttu-id="326d8-223">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="326d8-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="326d8-224">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="326d8-224">OUTPUTS</span></span>

### <span data-ttu-id="326d8-225">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="326d8-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="326d8-226">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="326d8-226">NOTES</span></span>
<span data-ttu-id="326d8-227">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="326d8-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="326d8-228">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="326d8-228">RELATED LINKS</span></span>

[<span data-ttu-id="326d8-229">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="326d8-229">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

