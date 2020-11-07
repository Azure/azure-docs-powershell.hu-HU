---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 38dc23c2bebe3c608833e55bcb4ffb2d687f9041
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847545"
---
# <span data-ttu-id="16d9d-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="16d9d-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="16d9d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="16d9d-103">Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="16d9d-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="16d9d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16d9d-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [[-DefaultStorageAccountType] <StorageType>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>] [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>]
 [[-EdgeNodeSize] <String>] [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>] [[-ClusterTier] <Tier>]
 [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>] [[-CertificateFileContents] <Byte[]>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16d9d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="16d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="16d9d-106">A **New-AzHDInsightClusterConfig** parancsmag olyan nem állandó objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="16d9d-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="16d9d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="16d9d-107">EXAMPLES</span></span>

### <span data-ttu-id="16d9d-108">Példa 1: fürtkonfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="16d9d-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="16d9d-109">Ez a parancs létrehoz egy cluster Configuration objektumot.</span><span class="sxs-lookup"><span data-stu-id="16d9d-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="16d9d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16d9d-110">PARAMETERS</span></span>

### <span data-ttu-id="16d9d-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="16d9d-111">-AadTenantId</span></span>
<span data-ttu-id="16d9d-112">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="16d9d-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="16d9d-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="16d9d-113">-ApplicationId</span></span>
<span data-ttu-id="16d9d-114">Az Azure Data Lake elérési útjának beszerzése vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="16d9d-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="16d9d-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="16d9d-115">-CertificateFileContents</span></span>
<span data-ttu-id="16d9d-116">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d9d-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="16d9d-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="16d9d-117">-CertificateFilePath</span></span>
<span data-ttu-id="16d9d-118">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="16d9d-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="16d9d-119">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="16d9d-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="16d9d-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="16d9d-120">-CertificatePassword</span></span>
<span data-ttu-id="16d9d-121">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="16d9d-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="16d9d-122">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="16d9d-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="16d9d-123">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="16d9d-123">-ClusterTier</span></span>
<span data-ttu-id="16d9d-124">A HDInsight-szektorcsoport rétegének meghatározása</span><span class="sxs-lookup"><span data-stu-id="16d9d-124">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="16d9d-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="16d9d-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16d9d-126">Standard</span><span class="sxs-lookup"><span data-stu-id="16d9d-126">Standard</span></span>
- <span data-ttu-id="16d9d-127">Prémium: az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="16d9d-127">Premium The default value is Standard.</span></span>
<span data-ttu-id="16d9d-128">A prémium szint csak Linux-fürtökkel használható, és lehetővé teszi néhány új funkció használatát.</span><span class="sxs-lookup"><span data-stu-id="16d9d-128">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="16d9d-129">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="16d9d-129">-ClusterType</span></span>
<span data-ttu-id="16d9d-130">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d9d-130">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="16d9d-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="16d9d-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16d9d-132">Hadoop</span><span class="sxs-lookup"><span data-stu-id="16d9d-132">Hadoop</span></span>
- <span data-ttu-id="16d9d-133">HBase</span><span class="sxs-lookup"><span data-stu-id="16d9d-133">HBase</span></span>
- <span data-ttu-id="16d9d-134">Vihar</span><span class="sxs-lookup"><span data-stu-id="16d9d-134">Storm</span></span>
- <span data-ttu-id="16d9d-135">Érdeklődést</span><span class="sxs-lookup"><span data-stu-id="16d9d-135">Spark</span></span>
- <span data-ttu-id="16d9d-136">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="16d9d-136">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="16d9d-137">Kafka</span><span class="sxs-lookup"><span data-stu-id="16d9d-137">Kafka</span></span>
- <span data-ttu-id="16d9d-138">RServer</span><span class="sxs-lookup"><span data-stu-id="16d9d-138">RServer</span></span>

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

### <span data-ttu-id="16d9d-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d9d-139">-DefaultProfile</span></span>
<span data-ttu-id="16d9d-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="16d9d-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16d9d-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="16d9d-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="16d9d-142">A HDInsight-fürtöt használó alapértelmezett Azure-tárterülethez tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d9d-142">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="16d9d-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="16d9d-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="16d9d-144">Annak az alapértelmezett tárterület-fióknak a nevét adja meg, amelyet a HDInsight-fürt fog használni.</span><span class="sxs-lookup"><span data-stu-id="16d9d-144">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="16d9d-145">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="16d9d-145">-DefaultStorageAccountType</span></span>
<span data-ttu-id="16d9d-146">A HDInsight-fürtöt használó alapértelmezett tárterület-fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d9d-146">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="16d9d-147">A lehetséges értékek a AzureStorage és a AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="16d9d-147">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="16d9d-148">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="16d9d-148">-EdgeNodeSize</span></span>
<span data-ttu-id="16d9d-149">Az Edge csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d9d-149">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="16d9d-150">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="16d9d-150">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="16d9d-151">Ez a paraméter csak a RServer-fürtök esetében érvényes.</span><span class="sxs-lookup"><span data-stu-id="16d9d-151">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="16d9d-152">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="16d9d-152">-HeadNodeSize</span></span>
<span data-ttu-id="16d9d-153">A fej csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d9d-153">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="16d9d-154">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="16d9d-154">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="16d9d-155">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="16d9d-155">-HiveMetastore</span></span>
<span data-ttu-id="16d9d-156">A kaptár metaadatait tároló metastore adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d9d-156">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="16d9d-157">A Add-AzHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="16d9d-157">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="16d9d-158">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="16d9d-158">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="16d9d-159">A minimálisan támogatott TLS-verziót kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="16d9d-159">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="16d9d-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="16d9d-160">-ObjectId</span></span>
<span data-ttu-id="16d9d-161">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="16d9d-161">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="16d9d-162">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="16d9d-162">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="16d9d-163">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="16d9d-163">-OozieMetastore</span></span>
<span data-ttu-id="16d9d-164">A Oozie metaadatait tároló metastore adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d9d-164">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="16d9d-165">Másik lehetőségként használhatja az **Add-AzHDInsightMetastore** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="16d9d-165">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="16d9d-166">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="16d9d-166">-WorkerNodeSize</span></span>
<span data-ttu-id="16d9d-167">A munkavégző csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d9d-167">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="16d9d-168">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="16d9d-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="16d9d-169">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="16d9d-169">-ZookeeperNodeSize</span></span>
<span data-ttu-id="16d9d-170">A Zookeeper csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16d9d-170">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="16d9d-171">Használja a Get-AzVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="16d9d-171">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="16d9d-172">Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="16d9d-172">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="16d9d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d9d-173">CommonParameters</span></span>
<span data-ttu-id="16d9d-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16d9d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d9d-175">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="16d9d-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d9d-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16d9d-176">INPUTS</span></span>

### <span data-ttu-id="16d9d-177">Nincs</span><span class="sxs-lookup"><span data-stu-id="16d9d-177">None</span></span>

## <span data-ttu-id="16d9d-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16d9d-178">OUTPUTS</span></span>

### <span data-ttu-id="16d9d-179">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="16d9d-179">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="16d9d-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16d9d-180">NOTES</span></span>

## <span data-ttu-id="16d9d-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16d9d-181">RELATED LINKS</span></span>

[<span data-ttu-id="16d9d-182">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="16d9d-182">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


