---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187841"
---
# <span data-ttu-id="62833-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="62833-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="62833-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62833-102">SYNOPSIS</span></span>
<span data-ttu-id="62833-103">Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="62833-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="62833-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62833-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62833-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62833-105">DESCRIPTION</span></span>
<span data-ttu-id="62833-106">A **New-AzHDInsightClusterConfig** parancsmag olyan nem állandó objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="62833-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="62833-107">Példák</span><span class="sxs-lookup"><span data-stu-id="62833-107">EXAMPLES</span></span>

### <span data-ttu-id="62833-108">Példa 1: fürtkonfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="62833-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="62833-109">Ez a parancs létrehoz egy cluster Configuration objektumot.</span><span class="sxs-lookup"><span data-stu-id="62833-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="62833-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62833-110">PARAMETERS</span></span>

### <span data-ttu-id="62833-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="62833-111">-AadTenantId</span></span>
<span data-ttu-id="62833-112">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="62833-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="62833-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="62833-113">-ApplicationId</span></span>
<span data-ttu-id="62833-114">Az Azure Data Lake elérési útjának beszerzése vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="62833-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="62833-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="62833-115">-AssignedIdentity</span></span>
<span data-ttu-id="62833-116">A hozzárendelt identitás beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="62833-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="62833-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="62833-117">-CertificateFileContents</span></span>
<span data-ttu-id="62833-118">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="62833-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="62833-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="62833-119">-CertificateFilePath</span></span>
<span data-ttu-id="62833-120">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="62833-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="62833-121">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="62833-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="62833-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="62833-122">-CertificatePassword</span></span>
<span data-ttu-id="62833-123">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="62833-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="62833-124">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="62833-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="62833-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="62833-125">-ClusterTier</span></span>
<span data-ttu-id="62833-126">A HDInsight-szektorcsoport rétegének meghatározása</span><span class="sxs-lookup"><span data-stu-id="62833-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="62833-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="62833-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62833-128">Standard</span><span class="sxs-lookup"><span data-stu-id="62833-128">Standard</span></span>
- <span data-ttu-id="62833-129">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="62833-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="62833-130">A prémium szint csak Linux-fürtökkel használható, és lehetővé teszi néhány új funkció használatát.</span><span class="sxs-lookup"><span data-stu-id="62833-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="62833-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="62833-131">-ClusterType</span></span>
<span data-ttu-id="62833-132">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="62833-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="62833-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="62833-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62833-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="62833-134">Hadoop</span></span>
- <span data-ttu-id="62833-135">HBase</span><span class="sxs-lookup"><span data-stu-id="62833-135">HBase</span></span>
- <span data-ttu-id="62833-136">Vihar</span><span class="sxs-lookup"><span data-stu-id="62833-136">Storm</span></span>
- <span data-ttu-id="62833-137">Érdeklődést</span><span class="sxs-lookup"><span data-stu-id="62833-137">Spark</span></span>
- <span data-ttu-id="62833-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="62833-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="62833-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="62833-139">Kafka</span></span>
- <span data-ttu-id="62833-140">RServer</span><span class="sxs-lookup"><span data-stu-id="62833-140">RServer</span></span>

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

### <span data-ttu-id="62833-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62833-141">-DefaultProfile</span></span>
<span data-ttu-id="62833-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="62833-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62833-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="62833-143">-EdgeNodeSize</span></span>
<span data-ttu-id="62833-144">Az Edge csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62833-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="62833-145">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="62833-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="62833-146">Ez a paraméter csak a RServer-fürtök esetében érvényes.</span><span class="sxs-lookup"><span data-stu-id="62833-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="62833-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="62833-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="62833-148">A titkosítási algoritmust kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="62833-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="62833-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="62833-149">-EncryptionAtHost</span></span>
<span data-ttu-id="62833-150">Beilleszti vagy beállítja azt a jelölőt, amely azt jelzi, hogy engedélyezve van-e a titkosítás az állomáson.</span><span class="sxs-lookup"><span data-stu-id="62833-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="62833-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="62833-151">-EncryptionInTransit</span></span>
<span data-ttu-id="62833-152">Beilleszti vagy beállítja azt a jelölőt, amely azt jelzi, hogy engedélyezve van-e a titkosítás a továbbításban.</span><span class="sxs-lookup"><span data-stu-id="62833-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="62833-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="62833-153">-EncryptionKeyName</span></span>
<span data-ttu-id="62833-154">A titkosítási kulcs nevének beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="62833-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="62833-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="62833-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="62833-156">A titkosító kulcs verziójának beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="62833-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="62833-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="62833-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="62833-158">A titkosítási tároló URI-azonosítójának beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="62833-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="62833-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="62833-159">-HeadNodeSize</span></span>
<span data-ttu-id="62833-160">A fej csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62833-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="62833-161">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="62833-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="62833-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="62833-162">-HiveMetastore</span></span>
<span data-ttu-id="62833-163">A kaptár metaadatait tároló metastore adja meg.</span><span class="sxs-lookup"><span data-stu-id="62833-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="62833-164">A Add-AzHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="62833-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="62833-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="62833-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="62833-166">A minimálisan támogatott TLS-verziót kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="62833-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="62833-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="62833-167">-ObjectId</span></span>
<span data-ttu-id="62833-168">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="62833-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="62833-169">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="62833-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="62833-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="62833-170">-OozieMetastore</span></span>
<span data-ttu-id="62833-171">A Oozie metaadatait tároló metastore adja meg.</span><span class="sxs-lookup"><span data-stu-id="62833-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="62833-172">Másik lehetőségként használhatja az **Add-AzHDInsightMetastore** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="62833-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="62833-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="62833-173">-StorageAccountKey</span></span>
<span data-ttu-id="62833-174">A Storage Account Access kulcs beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="62833-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="62833-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="62833-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="62833-176">A tárolási fiók erőforrás-azonosítóját kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="62833-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="62833-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="62833-177">-StorageAccountType</span></span>
<span data-ttu-id="62833-178">Az alapértelmezett tárterület-fiók típusának megadása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="62833-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62833-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="62833-179">-WorkerNodeSize</span></span>
<span data-ttu-id="62833-180">A munkavégző csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62833-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="62833-181">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="62833-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="62833-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="62833-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="62833-183">A Zookeeper csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62833-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="62833-184">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="62833-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="62833-185">Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="62833-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="62833-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62833-186">CommonParameters</span></span>
<span data-ttu-id="62833-187">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62833-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62833-188">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="62833-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62833-189">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62833-189">INPUTS</span></span>

### <span data-ttu-id="62833-190">Nincs</span><span class="sxs-lookup"><span data-stu-id="62833-190">None</span></span>

## <span data-ttu-id="62833-191">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62833-191">OUTPUTS</span></span>

### <span data-ttu-id="62833-192">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="62833-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="62833-193">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62833-193">NOTES</span></span>

## <span data-ttu-id="62833-194">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62833-194">RELATED LINKS</span></span>

[<span data-ttu-id="62833-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="62833-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


