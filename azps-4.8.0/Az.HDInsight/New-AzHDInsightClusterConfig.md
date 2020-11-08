---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024785"
---
# <span data-ttu-id="22aba-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="22aba-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="22aba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22aba-102">SYNOPSIS</span></span>
<span data-ttu-id="22aba-103">Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="22aba-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="22aba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22aba-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22aba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="22aba-105">DESCRIPTION</span></span>
<span data-ttu-id="22aba-106">A **New-AzHDInsightClusterConfig** parancsmag olyan nem állandó objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="22aba-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="22aba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="22aba-107">EXAMPLES</span></span>

### <span data-ttu-id="22aba-108">Példa 1: fürtkonfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="22aba-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
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

<span data-ttu-id="22aba-109">Ez a parancs létrehoz egy cluster Configuration objektumot.</span><span class="sxs-lookup"><span data-stu-id="22aba-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="22aba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22aba-110">PARAMETERS</span></span>

### <span data-ttu-id="22aba-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="22aba-111">-AadTenantId</span></span>
<span data-ttu-id="22aba-112">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="22aba-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="22aba-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="22aba-113">-ApplicationId</span></span>
<span data-ttu-id="22aba-114">Az Azure Data Lake elérési útjának beszerzése vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="22aba-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="22aba-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="22aba-115">-AssignedIdentity</span></span>
<span data-ttu-id="22aba-116">A hozzárendelt identitás beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="22aba-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="22aba-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="22aba-117">-CertificateFileContents</span></span>
<span data-ttu-id="22aba-118">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22aba-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22aba-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="22aba-119">-CertificateFilePath</span></span>
<span data-ttu-id="22aba-120">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="22aba-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="22aba-121">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="22aba-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="22aba-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="22aba-122">-CertificatePassword</span></span>
<span data-ttu-id="22aba-123">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="22aba-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="22aba-124">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="22aba-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="22aba-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="22aba-125">-ClusterTier</span></span>
<span data-ttu-id="22aba-126">A HDInsight-szektorcsoport rétegének meghatározása</span><span class="sxs-lookup"><span data-stu-id="22aba-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="22aba-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="22aba-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22aba-128">Standard</span><span class="sxs-lookup"><span data-stu-id="22aba-128">Standard</span></span>
- <span data-ttu-id="22aba-129">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="22aba-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="22aba-130">A prémium szint csak Linux-fürtökkel használható, és lehetővé teszi néhány új funkció használatát.</span><span class="sxs-lookup"><span data-stu-id="22aba-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="22aba-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="22aba-131">-ClusterType</span></span>
<span data-ttu-id="22aba-132">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22aba-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="22aba-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="22aba-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22aba-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="22aba-134">Hadoop</span></span>
- <span data-ttu-id="22aba-135">HBase</span><span class="sxs-lookup"><span data-stu-id="22aba-135">HBase</span></span>
- <span data-ttu-id="22aba-136">Vihar</span><span class="sxs-lookup"><span data-stu-id="22aba-136">Storm</span></span>
- <span data-ttu-id="22aba-137">Érdeklődést</span><span class="sxs-lookup"><span data-stu-id="22aba-137">Spark</span></span>
- <span data-ttu-id="22aba-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="22aba-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="22aba-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="22aba-139">Kafka</span></span>
- <span data-ttu-id="22aba-140">RServer</span><span class="sxs-lookup"><span data-stu-id="22aba-140">RServer</span></span>

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

### <span data-ttu-id="22aba-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22aba-141">-DefaultProfile</span></span>
<span data-ttu-id="22aba-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="22aba-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22aba-143">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="22aba-143">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="22aba-144">A HDInsight-fürtöt használó alapértelmezett Azure-tárterülethez tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22aba-144">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="22aba-145">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="22aba-145">-DefaultStorageAccountName</span></span>
<span data-ttu-id="22aba-146">Annak az alapértelmezett tárterület-fióknak a nevét adja meg, amelyet a HDInsight-fürt fog használni.</span><span class="sxs-lookup"><span data-stu-id="22aba-146">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="22aba-147">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="22aba-147">-DefaultStorageAccountType</span></span>
<span data-ttu-id="22aba-148">A HDInsight-fürtöt használó alapértelmezett tárterület-fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22aba-148">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="22aba-149">A lehetséges értékek a AzureStorage és a AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="22aba-149">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22aba-150">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="22aba-150">-EdgeNodeSize</span></span>
<span data-ttu-id="22aba-151">Az Edge csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22aba-151">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="22aba-152">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="22aba-152">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="22aba-153">Ez a paraméter csak a RServer-fürtök esetében érvényes.</span><span class="sxs-lookup"><span data-stu-id="22aba-153">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="22aba-154">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="22aba-154">-EncryptionAlgorithm</span></span>
<span data-ttu-id="22aba-155">A titkosítási algoritmust kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="22aba-155">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="22aba-156">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="22aba-156">-EncryptionAtHost</span></span>
<span data-ttu-id="22aba-157">Beilleszti vagy beállítja azt a jelölőt, amely azt jelzi, hogy engedélyezve van-e a titkosítás az állomáson.</span><span class="sxs-lookup"><span data-stu-id="22aba-157">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="22aba-158">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="22aba-158">-EncryptionInTransit</span></span>
<span data-ttu-id="22aba-159">Beilleszti vagy beállítja azt a jelölőt, amely azt jelzi, hogy engedélyezve van-e a titkosítás a továbbításban.</span><span class="sxs-lookup"><span data-stu-id="22aba-159">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="22aba-160">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="22aba-160">-EncryptionKeyName</span></span>
<span data-ttu-id="22aba-161">A titkosítási kulcs nevének beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="22aba-161">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="22aba-162">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="22aba-162">-EncryptionKeyVersion</span></span>
<span data-ttu-id="22aba-163">A titkosító kulcs verziójának beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="22aba-163">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="22aba-164">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="22aba-164">-EncryptionVaultUri</span></span>
<span data-ttu-id="22aba-165">A titkosítási tároló URI-azonosítójának beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="22aba-165">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="22aba-166">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="22aba-166">-HeadNodeSize</span></span>
<span data-ttu-id="22aba-167">A fej csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22aba-167">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="22aba-168">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="22aba-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="22aba-169">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="22aba-169">-HiveMetastore</span></span>
<span data-ttu-id="22aba-170">A kaptár metaadatait tároló metastore adja meg.</span><span class="sxs-lookup"><span data-stu-id="22aba-170">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="22aba-171">A Add-AzHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="22aba-171">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="22aba-172">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="22aba-172">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="22aba-173">A minimálisan támogatott TLS-verziót kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="22aba-173">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="22aba-174">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="22aba-174">-ObjectId</span></span>
<span data-ttu-id="22aba-175">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="22aba-175">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="22aba-176">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="22aba-176">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="22aba-177">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="22aba-177">-OozieMetastore</span></span>
<span data-ttu-id="22aba-178">A Oozie metaadatait tároló metastore adja meg.</span><span class="sxs-lookup"><span data-stu-id="22aba-178">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="22aba-179">Másik lehetőségként használhatja az **Add-AzHDInsightMetastore** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="22aba-179">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="22aba-180">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="22aba-180">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="22aba-181">Beilleszti vagy beállítja a kimenő hozzáférési típust a nyilvános hálózatra.</span><span class="sxs-lookup"><span data-stu-id="22aba-181">Gets or sets the outbound access type to the public network.</span></span>

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

### <span data-ttu-id="22aba-182">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="22aba-182">-PublicNetworkAccessType</span></span>
<span data-ttu-id="22aba-183">A nyilvános hálózat elérési típusának beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="22aba-183">Gets or sets the public network access type.</span></span>

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

### <span data-ttu-id="22aba-184">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="22aba-184">-WorkerNodeSize</span></span>
<span data-ttu-id="22aba-185">A munkavégző csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22aba-185">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="22aba-186">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="22aba-186">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="22aba-187">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="22aba-187">-ZookeeperNodeSize</span></span>
<span data-ttu-id="22aba-188">A Zookeeper csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22aba-188">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="22aba-189">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="22aba-189">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="22aba-190">Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="22aba-190">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="22aba-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22aba-191">CommonParameters</span></span>
<span data-ttu-id="22aba-192">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22aba-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22aba-193">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="22aba-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22aba-194">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22aba-194">INPUTS</span></span>

### <span data-ttu-id="22aba-195">Nincs</span><span class="sxs-lookup"><span data-stu-id="22aba-195">None</span></span>

## <span data-ttu-id="22aba-196">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22aba-196">OUTPUTS</span></span>

### <span data-ttu-id="22aba-197">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="22aba-197">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="22aba-198">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22aba-198">NOTES</span></span>

## <span data-ttu-id="22aba-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22aba-199">RELATED LINKS</span></span>

[<span data-ttu-id="22aba-200">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="22aba-200">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


