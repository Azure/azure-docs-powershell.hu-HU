---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 381143b356202a7b6b76e173b233f2fffe87f6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504980"
---
# <span data-ttu-id="a576d-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a576d-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="a576d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a576d-102">SYNOPSIS</span></span>
<span data-ttu-id="a576d-103">Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a576d-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a576d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a576d-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a576d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a576d-105">DESCRIPTION</span></span>
<span data-ttu-id="a576d-106">A **New-AzureRmHDInsightClusterConfig** parancsmag olyan nem állandó objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a576d-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="a576d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a576d-107">EXAMPLES</span></span>

### <span data-ttu-id="a576d-108">Példa 1: fürtkonfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a576d-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="a576d-109">Ez a parancs létrehoz egy cluster Configuration objektumot.</span><span class="sxs-lookup"><span data-stu-id="a576d-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="a576d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a576d-110">PARAMETERS</span></span>

### <span data-ttu-id="a576d-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="a576d-111">-AadTenantId</span></span>
<span data-ttu-id="a576d-112">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="a576d-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a576d-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="a576d-113">-CertificateFileContents</span></span>
<span data-ttu-id="a576d-114">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a576d-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a576d-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a576d-115">-CertificateFilePath</span></span>
<span data-ttu-id="a576d-116">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="a576d-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a576d-117">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="a576d-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a576d-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a576d-118">-CertificatePassword</span></span>
<span data-ttu-id="a576d-119">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="a576d-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a576d-120">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="a576d-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a576d-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="a576d-121">-ClusterTier</span></span>
<span data-ttu-id="a576d-122">A HDInsight-szektorcsoport rétegének meghatározása</span><span class="sxs-lookup"><span data-stu-id="a576d-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="a576d-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a576d-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a576d-124">Standard</span><span class="sxs-lookup"><span data-stu-id="a576d-124">Standard</span></span>
- <span data-ttu-id="a576d-125">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="a576d-125">Premium</span></span>

<span data-ttu-id="a576d-126">Az alapértelmezett érték a standard.</span><span class="sxs-lookup"><span data-stu-id="a576d-126">The default value is Standard.</span></span>
<span data-ttu-id="a576d-127">A prémium szint csak Linux-fürtökkel használható, és lehetővé teszi néhány új funkció használatát.</span><span class="sxs-lookup"><span data-stu-id="a576d-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="a576d-128">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="a576d-128">-ClusterType</span></span>
<span data-ttu-id="a576d-129">A létrehozandó fürt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a576d-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="a576d-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a576d-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a576d-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="a576d-131">Hadoop</span></span>
- <span data-ttu-id="a576d-132">HBase</span><span class="sxs-lookup"><span data-stu-id="a576d-132">HBase</span></span>
- <span data-ttu-id="a576d-133">Vihar</span><span class="sxs-lookup"><span data-stu-id="a576d-133">Storm</span></span>
- <span data-ttu-id="a576d-134">Érdeklődést</span><span class="sxs-lookup"><span data-stu-id="a576d-134">Spark</span></span>

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

### <span data-ttu-id="a576d-135">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a576d-135">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="a576d-136">A HDInsight-fürtöt használó alapértelmezett Azure-tárterülethez tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a576d-136">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="a576d-137">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a576d-137">-DefaultStorageAccountName</span></span>
<span data-ttu-id="a576d-138">Annak az alapértelmezett tárterület-fióknak a nevét adja meg, amelyet a HDInsight-fürt fog használni.</span><span class="sxs-lookup"><span data-stu-id="a576d-138">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="a576d-139">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a576d-139">-DefaultStorageAccountType</span></span>
<span data-ttu-id="a576d-140">A HDInsight-fürtöt használó alapértelmezett tárterület-fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a576d-140">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="a576d-141">A lehetséges értékek a AzureStorage és a AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="a576d-141">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="a576d-142">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="a576d-142">-EdgeNodeSize</span></span>
<span data-ttu-id="a576d-143">Az Edge csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a576d-143">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="a576d-144">Használja a Get-AzureRmVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="a576d-144">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="a576d-145">Ez a paraméter csak a RServer-fürtök esetében érvényes.</span><span class="sxs-lookup"><span data-stu-id="a576d-145">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="a576d-146">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="a576d-146">-HeadNodeSize</span></span>
<span data-ttu-id="a576d-147">A fej csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a576d-147">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="a576d-148">Használja a Get-AzureRMVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="a576d-148">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="a576d-149">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="a576d-149">-HiveMetastore</span></span>
<span data-ttu-id="a576d-150">A kaptár metaadatait tároló metastore adja meg.</span><span class="sxs-lookup"><span data-stu-id="a576d-150">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="a576d-151">A Add-AzureRmHDInsightMetastore parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="a576d-151">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="a576d-152">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a576d-152">-ObjectId</span></span>
<span data-ttu-id="a576d-153">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="a576d-153">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="a576d-154">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="a576d-154">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a576d-155">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="a576d-155">-OozieMetastore</span></span>
<span data-ttu-id="a576d-156">A Oozie metaadatait tároló metastore adja meg.</span><span class="sxs-lookup"><span data-stu-id="a576d-156">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="a576d-157">Másik lehetőségként használhatja az **Add-AzureRmHDInsightMetastore** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a576d-157">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="a576d-158">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="a576d-158">-WorkerNodeSize</span></span>
<span data-ttu-id="a576d-159">A munkavégző csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a576d-159">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="a576d-160">Használja a Get-AzureRMVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="a576d-160">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="a576d-161">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="a576d-161">-ZookeeperNodeSize</span></span>
<span data-ttu-id="a576d-162">A Zookeeper csomópont virtuális számítógépének méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a576d-162">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="a576d-163">Használja a Get-AzureRMVMSizet az elfogadható VM-méretekhez, és tekintse meg a HDInsight díjszabási lapját.</span><span class="sxs-lookup"><span data-stu-id="a576d-163">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="a576d-164">Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="a576d-164">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="a576d-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a576d-165">-DefaultProfile</span></span>
<span data-ttu-id="a576d-166">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a576d-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a576d-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a576d-167">CommonParameters</span></span>
<span data-ttu-id="a576d-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a576d-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a576d-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a576d-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a576d-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a576d-170">INPUTS</span></span>

## <span data-ttu-id="a576d-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a576d-171">OUTPUTS</span></span>

### <span data-ttu-id="a576d-172">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a576d-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a576d-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a576d-173">NOTES</span></span>

## <span data-ttu-id="a576d-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a576d-174">RELATED LINKS</span></span>

[<span data-ttu-id="a576d-175">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="a576d-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


