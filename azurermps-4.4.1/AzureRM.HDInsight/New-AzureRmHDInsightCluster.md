---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: bc89dff9fa6feecf38f0d9f81efb3bdc18c70641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680555"
---
# <span data-ttu-id="d389f-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d389f-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="d389f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d389f-102">SYNOPSIS</span></span>
<span data-ttu-id="d389f-103">Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="d389f-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d389f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d389f-104">SYNTAX</span></span>

### <span data-ttu-id="d389f-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d389f-105">Default (Default)</span></span>
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
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d389f-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="d389f-106">CertificateFilePath</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d389f-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="d389f-107">CertificateFileContents</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d389f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d389f-108">DESCRIPTION</span></span>
<span data-ttu-id="d389f-109">A New-AzureHDInsightCluster Azure HDInsight-fürtöt hoz létre a megadott paraméterekkel vagy a New-AzureRmHDInsightClusterConfig parancsmaggal létrehozott konfigurációs objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="d389f-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="d389f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d389f-110">EXAMPLES</span></span>

### <span data-ttu-id="d389f-111">--------------------------Példa 1: Azure HDInsight-ös fürt létrehozása--------------------------</span><span class="sxs-lookup"><span data-stu-id="d389f-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
<span data-ttu-id="d389f-112">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d389f-112">@{paragraph=PS C:\\\>}</span></span>









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

<span data-ttu-id="d389f-113">Ez a parancs létrehoz egy fürtöt az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="d389f-113">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="d389f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d389f-114">PARAMETERS</span></span>

### <span data-ttu-id="d389f-115">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="d389f-115">-AadTenantId</span></span>
<span data-ttu-id="d389f-116">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="d389f-116">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d389f-117">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d389f-117">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="d389f-118">A fürt további Azure-tárolási fiókjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-118">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="d389f-119">A Add-AzureRmHDInsightStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="d389f-119">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="d389f-120">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="d389f-120">-CertificateFileContents</span></span>
<span data-ttu-id="d389f-121">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-121">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d389f-122">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="d389f-122">-CertificateFilePath</span></span>
<span data-ttu-id="d389f-123">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="d389f-123">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="d389f-124">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="d389f-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d389f-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d389f-125">-CertificatePassword</span></span>
<span data-ttu-id="d389f-126">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="d389f-126">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="d389f-127">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="d389f-127">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d389f-128">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="d389f-128">-ClusterName</span></span>
<span data-ttu-id="d389f-129">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-129">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d389f-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="d389f-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="d389f-131">A fürthöz tartozó munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-131">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="d389f-132">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="d389f-132">-ClusterTier</span></span>
<span data-ttu-id="d389f-133">A HDInsight-szektorcsoport rétegének meghatározása</span><span class="sxs-lookup"><span data-stu-id="d389f-133">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="d389f-134">Alapértelmezés szerint ez a normál.</span><span class="sxs-lookup"><span data-stu-id="d389f-134">By default, this is Standard.</span></span>
<span data-ttu-id="d389f-135">A prémium szint csak Linux-fürtökkel használható, és lehetővé teszi néhány új funkció használatát.</span><span class="sxs-lookup"><span data-stu-id="d389f-135">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="d389f-136">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="d389f-136">-ClusterType</span></span>
<span data-ttu-id="d389f-137">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-137">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="d389f-138">A beállítások a következők: Hadoop, HBase, Storm, szikra</span><span class="sxs-lookup"><span data-stu-id="d389f-138">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="d389f-139">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="d389f-139">-ComponentVersion</span></span>
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

### <span data-ttu-id="d389f-140">-Config</span><span class="sxs-lookup"><span data-stu-id="d389f-140">-Config</span></span>
<span data-ttu-id="d389f-141">Azt a szektorcsoport-objektumot adja meg, amellyel a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="d389f-141">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="d389f-142">Ezt az objektumot az New-AzureRmHDInsightClusterConfig parancsmag segítségével hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="d389f-142">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="d389f-143">-Konfigurációk</span><span class="sxs-lookup"><span data-stu-id="d389f-143">-Configurations</span></span>
<span data-ttu-id="d389f-144">A HDInsight-fürt konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-144">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="d389f-145">A Add-AzureRmHDInsightConfigValues parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="d389f-145">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="d389f-146">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d389f-146">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="d389f-147">A HDInsight-fürtöt használó alapértelmezett Azure-tárterülethez tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-147">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="d389f-148">A Set-AzureRmHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="d389f-148">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="d389f-149">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d389f-149">-DefaultStorageAccountName</span></span>
<span data-ttu-id="d389f-150">Annak az alapértelmezett Azure-tárterületnek a nevét adja meg, amelyet a HDInsight-fürt használni fog.</span><span class="sxs-lookup"><span data-stu-id="d389f-150">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="d389f-151">A Set-AzureRmHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="d389f-151">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="d389f-152">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d389f-152">-DefaultStorageAccountType</span></span>
<span data-ttu-id="d389f-153">A HDInsight-fürtöt használó alapértelmezett tárterület-fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-153">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="d389f-154">A lehetséges értékek a AzureStorage és a AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="d389f-154">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="d389f-155">Az alapértelmezett érték a AzureStorage, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="d389f-155">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="d389f-156">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d389f-156">-DefaultStorageContainer</span></span>
<span data-ttu-id="d389f-157">Annak az alapértelmezett tárolónak a nevét adja meg, amely a HDInsight-fürtöt használó alapértelmezett Azure Storage fiókban található.</span><span class="sxs-lookup"><span data-stu-id="d389f-157">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="d389f-158">A Set-AzureRmHDInsightDefaultStorage parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="d389f-158">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="d389f-159">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="d389f-159">-DefaultStorageRootPath</span></span>
<span data-ttu-id="d389f-160">Megadja az elérési utat az adattó-tároló fiókban, amelyet a HDInsight-fürt alapértelmezett fájlrendszerként fog használni.</span><span class="sxs-lookup"><span data-stu-id="d389f-160">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="d389f-161">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="d389f-161">-EdgeNodeSize</span></span>
<span data-ttu-id="d389f-162">Az Edge csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-162">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="d389f-163">Használja a Get-AzureRmVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="d389f-163">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="d389f-164">Ez a paraméter csak a RServer-fürtök esetében érvényes.</span><span class="sxs-lookup"><span data-stu-id="d389f-164">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="d389f-165">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="d389f-165">-HeadNodeSize</span></span>
<span data-ttu-id="d389f-166">A fej csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-166">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="d389f-167">Használja a Get-AzureRmVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="d389f-167">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="d389f-168">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="d389f-168">-HiveMetastore</span></span>
<span data-ttu-id="d389f-169">A kaptár metaadatait tároló SQL-adatbázist adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-169">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="d389f-170">A Add-AzureRmHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="d389f-170">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="d389f-171">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d389f-171">-HttpCredential</span></span>
<span data-ttu-id="d389f-172">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="d389f-172">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="d389f-173">-Hely</span><span class="sxs-lookup"><span data-stu-id="d389f-173">-Location</span></span>
<span data-ttu-id="d389f-174">A fürt helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-174">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="d389f-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d389f-175">-ObjectId</span></span>
<span data-ttu-id="d389f-176">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="d389f-176">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="d389f-177">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="d389f-177">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d389f-178">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="d389f-178">-OozieMetastore</span></span>
<span data-ttu-id="d389f-179">Megadja a Oozie metaadatait tároló SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="d389f-179">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="d389f-180">A Add-AzureRmHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="d389f-180">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="d389f-181">-OSType</span><span class="sxs-lookup"><span data-stu-id="d389f-181">-OSType</span></span>
<span data-ttu-id="d389f-182">A fürt operációs rendszerét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-182">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="d389f-183">A beállítások a következők: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="d389f-183">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="d389f-184">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="d389f-184">-RdpAccessExpiry</span></span>
<span data-ttu-id="d389f-185">Itt adhatja meg a fürthöz az RDP-hozzáféréssel való hozzáférés időpontját DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="d389f-185">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="d389f-186">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="d389f-186">-RdpCredential</span></span>
<span data-ttu-id="d389f-187">A fürt távoli asztali (RDP) hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-187">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="d389f-188">Ez csak Windows-fürtök esetén használható.</span><span class="sxs-lookup"><span data-stu-id="d389f-188">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="d389f-189">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d389f-189">-ResourceGroupName</span></span>
<span data-ttu-id="d389f-190">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-190">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d389f-191">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="d389f-191">-ScriptActions</span></span>
<span data-ttu-id="d389f-192">Megadja, hogy milyen parancsfájl-műveletek legyenek futtathatók a fürtökön a fürtök létrehozása végén.</span><span class="sxs-lookup"><span data-stu-id="d389f-192">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="d389f-193">Másik lehetőségként használhatja a bővítmények AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="d389f-193">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="d389f-194">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="d389f-194">-SecurityProfile</span></span>
<span data-ttu-id="d389f-195">A biztonságos fürtök létrehozásához használt biztonsággal kapcsolatos tulajdonságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-195">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="d389f-196">A Add-AzureRmHDInsightSecurityProfile parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="d389f-196">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="d389f-197">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="d389f-197">-SshCredential</span></span>
<span data-ttu-id="d389f-198">Itt adhatja meg az SSH-kapcsolatokhoz használt SSH-hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="d389f-198">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="d389f-199">Ez csak a Linux-fürtök esetében érhető el.</span><span class="sxs-lookup"><span data-stu-id="d389f-199">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="d389f-200">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d389f-200">-SshPublicKey</span></span>
<span data-ttu-id="d389f-201">Az SSH-kapcsolatokhoz használt nyilvános kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-201">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="d389f-202">Ez csak a Linux-fürtök esetében érhető el.</span><span class="sxs-lookup"><span data-stu-id="d389f-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="d389f-203">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d389f-203">-SubnetName</span></span>
<span data-ttu-id="d389f-204">A fürt kiválasztott virtuális hálózatán belüli alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-204">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="d389f-205">-Verzió</span><span class="sxs-lookup"><span data-stu-id="d389f-205">-Version</span></span>
<span data-ttu-id="d389f-206">A HDInsight-fürt HDI-változatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-206">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="d389f-207">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d389f-207">-VirtualNetworkId</span></span>
<span data-ttu-id="d389f-208">Annak a virtuális hálózatnak az AZONOSÍTÓját adja meg, amelybe a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="d389f-208">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="d389f-209">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="d389f-209">-WorkerNodeSize</span></span>
<span data-ttu-id="d389f-210">A munkavégző csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-210">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="d389f-211">Használja a Get-AzureRmVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="d389f-211">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="d389f-212">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="d389f-212">-ZookeeperNodeSize</span></span>
<span data-ttu-id="d389f-213">A Zookeeper csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d389f-213">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="d389f-214">Használja a Get-AzureRmVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="d389f-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="d389f-215">Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="d389f-215">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="d389f-216">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d389f-216">-DefaultProfile</span></span>
<span data-ttu-id="d389f-217">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d389f-217">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d389f-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d389f-218">CommonParameters</span></span>
<span data-ttu-id="d389f-219">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d389f-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d389f-220">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d389f-220">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d389f-221">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d389f-221">INPUTS</span></span>

### <span data-ttu-id="d389f-222">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d389f-222">AzureHDInsightConfig</span></span>
<span data-ttu-id="d389f-223">A "config" paraméter elfogadja a "AzureHDInsightConfig" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d389f-223">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="d389f-224">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d389f-224">OUTPUTS</span></span>

### <span data-ttu-id="d389f-225">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d389f-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="d389f-226">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d389f-226">NOTES</span></span>
<span data-ttu-id="d389f-227">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="d389f-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="d389f-228">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d389f-228">RELATED LINKS</span></span>

[<span data-ttu-id="d389f-229">Új – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d389f-229">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

