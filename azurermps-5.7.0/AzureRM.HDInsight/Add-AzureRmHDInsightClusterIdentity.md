---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: e4e481a7ee26be966abda3d996575ab1bbd03b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495362"
---
# <span data-ttu-id="29098-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="29098-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="29098-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29098-102">SYNOPSIS</span></span>
<span data-ttu-id="29098-103">A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="29098-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29098-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29098-104">SYNTAX</span></span>

### <span data-ttu-id="29098-105">CertificateFilePath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29098-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29098-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="29098-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29098-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="29098-107">DESCRIPTION</span></span>
<span data-ttu-id="29098-108">Az **Add-AzureRmHDInsightClusterIdentity** parancsmag a New-AzureRmHDInsightClusterConfig parancsmag által létrehozott Azure HDInsight Configuration objektumhoz ad egy fürtöt.</span><span class="sxs-lookup"><span data-stu-id="29098-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="29098-109">Példák</span><span class="sxs-lookup"><span data-stu-id="29098-109">EXAMPLES</span></span>

### <span data-ttu-id="29098-110">1. példa: a fürtkonfigurációs adatok felvétele a fürtkonfigurációs objektumba</span><span class="sxs-lookup"><span data-stu-id="29098-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="29098-111">Ez a parancs a cluster Identity-adatokat hozzáadja a-Hadoop-001 nevű fürthöz, így a klaszter hozzáférhet az Azure Data Lake Store szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="29098-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="29098-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29098-112">PARAMETERS</span></span>

### <span data-ttu-id="29098-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="29098-113">-AadTenantId</span></span>
<span data-ttu-id="29098-114">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="29098-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29098-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="29098-115">-CertificateFileContents</span></span>
<span data-ttu-id="29098-116">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="29098-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29098-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="29098-117">-CertificateFilePath</span></span>
<span data-ttu-id="29098-118">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="29098-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="29098-119">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="29098-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: CertificateFilePath
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29098-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="29098-120">-CertificatePassword</span></span>
<span data-ttu-id="29098-121">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="29098-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="29098-122">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="29098-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29098-123">-Config</span><span class="sxs-lookup"><span data-stu-id="29098-123">-Config</span></span>
<span data-ttu-id="29098-124">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="29098-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="29098-125">Ezt az objektumot az New-AzureRmHDInsightClusterConfig parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="29098-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29098-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29098-126">-DefaultProfile</span></span>
<span data-ttu-id="29098-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="29098-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29098-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="29098-128">-ObjectId</span></span>
<span data-ttu-id="29098-129">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="29098-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="29098-130">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="29098-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29098-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29098-131">CommonParameters</span></span>
<span data-ttu-id="29098-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29098-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29098-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29098-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29098-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29098-134">INPUTS</span></span>

### <span data-ttu-id="29098-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="29098-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="29098-136">A "config" paraméter elfogadja a "AzureHDInsightConfig" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="29098-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

### <span data-ttu-id="29098-137">GUID</span><span class="sxs-lookup"><span data-stu-id="29098-137">Guid</span></span>
<span data-ttu-id="29098-138">A ' ObjectId ' paraméter a pipeline "GUID" típusú értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29098-138">Parameter 'ObjectId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="29098-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29098-139">OUTPUTS</span></span>

### <span data-ttu-id="29098-140">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="29098-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="29098-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29098-141">NOTES</span></span>

## <span data-ttu-id="29098-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29098-142">RELATED LINKS</span></span>

[<span data-ttu-id="29098-143">Új – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="29098-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


