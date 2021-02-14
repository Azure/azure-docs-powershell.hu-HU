---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167499"
---
# <span data-ttu-id="0a078-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="0a078-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="0a078-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a078-102">SYNOPSIS</span></span>
<span data-ttu-id="0a078-103">Olyan nem állandó fürtkonfigurációs objektumot hoz létre, amely leírja az Azure HDInsight-fürtkonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="0a078-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="0a078-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a078-104">SYNTAX</span></span>

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

## <span data-ttu-id="0a078-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a078-105">DESCRIPTION</span></span>
<span data-ttu-id="0a078-106">A **New-AzHDInsightClusterConfig** parancsmag létrehoz egy nem állandó objektumot, amely leírja az Azure HDInsight-fürtkonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="0a078-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="0a078-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a078-107">EXAMPLES</span></span>

### <span data-ttu-id="0a078-108">1. példa: Fürtkonfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a078-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="0a078-109">Ez a parancs fürtkonfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0a078-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="0a078-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a078-110">PARAMETERS</span></span>

### <span data-ttu-id="0a078-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="0a078-111">-AadTenantId</span></span>
<span data-ttu-id="0a078-112">Az Azure Data Lake Store elérésekor használt Azure AD bérlőazonosító.</span><span class="sxs-lookup"><span data-stu-id="0a078-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0a078-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0a078-113">-ApplicationId</span></span>
<span data-ttu-id="0a078-114">Beállítja vagy beállítja az Egyszerű szolgáltatásalkalmazás-azonosítót az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="0a078-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="0a078-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0a078-115">-AssignedIdentity</span></span>
<span data-ttu-id="0a078-116">Beállítja vagy beállítja a hozzárendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="0a078-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="0a078-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="0a078-117">-CertificateFileContents</span></span>
<span data-ttu-id="0a078-118">Megadja annak a tanúsítványnak a fájl tartalmát, amely az Azure Data Lake Store elérésekor használatos.</span><span class="sxs-lookup"><span data-stu-id="0a078-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0a078-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="0a078-119">-CertificateFilePath</span></span>
<span data-ttu-id="0a078-120">Megadja annak a tanúsítványnak a fájl elérési útját, amely a szolgáltatásnévként való hitelesítéshez használatos.</span><span class="sxs-lookup"><span data-stu-id="0a078-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="0a078-121">A fürt ezt fogja használni az Azure Data Lake Store elérésekor.</span><span class="sxs-lookup"><span data-stu-id="0a078-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0a078-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="0a078-122">-CertificatePassword</span></span>
<span data-ttu-id="0a078-123">Megadja annak a tanúsítványnak a jelszavát, amely a szolgáltatásnévként való hitelesítéshez használatos.</span><span class="sxs-lookup"><span data-stu-id="0a078-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="0a078-124">A fürt ezt fogja használni az Azure Data Lake Store elérésekor.</span><span class="sxs-lookup"><span data-stu-id="0a078-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0a078-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="0a078-125">-ClusterTier</span></span>
<span data-ttu-id="0a078-126">A HDInsight-fürtréteget adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a078-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="0a078-127">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="0a078-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a078-128">Normál</span><span class="sxs-lookup"><span data-stu-id="0a078-128">Standard</span></span>
- <span data-ttu-id="0a078-129">Prémium: Az alapértelmezett érték a Standard.</span><span class="sxs-lookup"><span data-stu-id="0a078-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="0a078-130">A prémium szint csak Linux-fürtökhöz használható, és lehetővé teszi egyes új funkciók használatát.</span><span class="sxs-lookup"><span data-stu-id="0a078-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="0a078-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="0a078-131">-ClusterType</span></span>
<span data-ttu-id="0a078-132">A létrehozni szükséges fürt típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0a078-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="0a078-133">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="0a078-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a078-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="0a078-134">Hadoop</span></span>
- <span data-ttu-id="0a078-135">HBase</span><span class="sxs-lookup"><span data-stu-id="0a078-135">HBase</span></span>
- <span data-ttu-id="0a078-136">Storm</span><span class="sxs-lookup"><span data-stu-id="0a078-136">Storm</span></span>
- <span data-ttu-id="0a078-137">Spark</span><span class="sxs-lookup"><span data-stu-id="0a078-137">Spark</span></span>
- <span data-ttu-id="0a078-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="0a078-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="0a078-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="0a078-139">Kafka</span></span>
- <span data-ttu-id="0a078-140">RServer</span><span class="sxs-lookup"><span data-stu-id="0a078-140">RServer</span></span>

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

### <span data-ttu-id="0a078-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a078-141">-DefaultProfile</span></span>
<span data-ttu-id="0a078-142">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a078-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a078-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="0a078-143">-EdgeNodeSize</span></span>
<span data-ttu-id="0a078-144">A virtuális gép mérete a peremcsomóponthoz.</span><span class="sxs-lookup"><span data-stu-id="0a078-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="0a078-145">A Get-AzVMSize a MEGFELELŐ VM-méretekért, és tekintse meg a HDInsight árazási lapját.</span><span class="sxs-lookup"><span data-stu-id="0a078-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="0a078-146">Ez a paraméter csak RServer-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="0a078-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="0a078-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0a078-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="0a078-148">Beállítja vagy beállítja a titkosítási algoritmust.</span><span class="sxs-lookup"><span data-stu-id="0a078-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="0a078-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="0a078-149">-EncryptionAtHost</span></span>
<span data-ttu-id="0a078-150">Beállítja vagy beállítja a jelölőt, amely jelzi, hogy engedélyezi-e a titkosítást a gazdaszámítógépen.</span><span class="sxs-lookup"><span data-stu-id="0a078-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="0a078-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="0a078-151">-EncryptionInTransit</span></span>
<span data-ttu-id="0a078-152">Beállítja vagy beállítja a jelölőt, amely jelzi, hogy engedélyezi-e a titkosítást az átvitel során.</span><span class="sxs-lookup"><span data-stu-id="0a078-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="0a078-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="0a078-153">-EncryptionKeyName</span></span>
<span data-ttu-id="0a078-154">Beállítja vagy beállítja a titkosítási kulcs nevét.</span><span class="sxs-lookup"><span data-stu-id="0a078-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="0a078-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="0a078-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="0a078-156">Beállítja vagy beállítja a titkosítási kulcs verzióját.</span><span class="sxs-lookup"><span data-stu-id="0a078-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="0a078-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="0a078-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="0a078-158">Beállítja vagy beállítja a titkosítási tároló uri-ját.</span><span class="sxs-lookup"><span data-stu-id="0a078-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="0a078-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="0a078-159">-HeadNodeSize</span></span>
<span data-ttu-id="0a078-160">A Head csomópont virtuális gépének mérete.</span><span class="sxs-lookup"><span data-stu-id="0a078-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="0a078-161">A Get-AzVMSize a MEGFELELŐ VM-méretekért, és tekintse meg a HDInsight árazási lapját.</span><span class="sxs-lookup"><span data-stu-id="0a078-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="0a078-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="0a078-162">-HiveMetastore</span></span>
<span data-ttu-id="0a078-163">A Hive-metaadatot tároló metaadatot tároló metaadatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a078-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="0a078-164">Másik lehetőségként használhatja a Add-AzHDInsightMetastore parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0a078-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="0a078-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0a078-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="0a078-166">A minimálisan támogatott TLS-verziót kapja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="0a078-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="0a078-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0a078-167">-ObjectId</span></span>
<span data-ttu-id="0a078-168">A fürtöt képviselő Azure AD-szolgáltatásnév Azure AD-objektumazonosítóját (GUID) adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a078-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="0a078-169">A fürt ezt fogja használni az Azure Data Lake Store elérésekor.</span><span class="sxs-lookup"><span data-stu-id="0a078-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0a078-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="0a078-170">-OozieMetastore</span></span>
<span data-ttu-id="0a078-171">Megadja az Oozie-metaadatokat tároló metaadatot tároló metatárat.</span><span class="sxs-lookup"><span data-stu-id="0a078-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="0a078-172">Használhatja az **Add-AzHDInsightMetastore** parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="0a078-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="0a078-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0a078-173">-StorageAccountKey</span></span>
<span data-ttu-id="0a078-174">Beállítja vagy beállítja a tárfiók hozzáférési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="0a078-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="0a078-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0a078-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="0a078-176">Beállítja vagy beállítja a tárfiók erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="0a078-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="0a078-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0a078-177">-StorageAccountType</span></span>
<span data-ttu-id="0a078-178">Beállítja vagy beállítja az alapértelmezett tárfiók típusát.</span><span class="sxs-lookup"><span data-stu-id="0a078-178">Gets or sets the type of the default storage account.</span></span>

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

### <span data-ttu-id="0a078-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="0a078-179">-WorkerNodeSize</span></span>
<span data-ttu-id="0a078-180">A Munkavégi csomópont virtuális gépének mérete.</span><span class="sxs-lookup"><span data-stu-id="0a078-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="0a078-181">A Get-AzVMSize a MEGFELELŐ VM-méretekért, és tekintse meg a HDInsight árazási lapját.</span><span class="sxs-lookup"><span data-stu-id="0a078-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="0a078-182">-ÁllatmemónisnodeSize</span><span class="sxs-lookup"><span data-stu-id="0a078-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="0a078-183">Az Állatkezelő csomópont virtuális gépének mérete.</span><span class="sxs-lookup"><span data-stu-id="0a078-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="0a078-184">A Get-AzVMSize a MEGFELELŐ VM-méretekért, és tekintse meg a HDInsight árazási lapját.</span><span class="sxs-lookup"><span data-stu-id="0a078-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="0a078-185">Ez a paraméter csak HBase vagy Storm fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="0a078-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="0a078-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a078-186">CommonParameters</span></span>
<span data-ttu-id="0a078-187">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a078-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a078-188">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a078-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a078-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a078-189">INPUTS</span></span>

### <span data-ttu-id="0a078-190">Nincs</span><span class="sxs-lookup"><span data-stu-id="0a078-190">None</span></span>

## <span data-ttu-id="0a078-191">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a078-191">OUTPUTS</span></span>

### <span data-ttu-id="0a078-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0a078-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="0a078-193">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a078-193">NOTES</span></span>

## <span data-ttu-id="0a078-194">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a078-194">RELATED LINKS</span></span>

[<span data-ttu-id="0a078-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="0a078-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


