---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: d02dce12425015ed12e082f0bb3ba52c5b9b77c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491912"
---
# <span data-ttu-id="f2c3e-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="f2c3e-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="f2c3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c3e-103">A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2c3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2c3e-104">SYNTAX</span></span>

### <span data-ttu-id="f2c3e-105">CertificateFilePath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2c3e-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2c3e-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f2c3e-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2c3e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2c3e-107">DESCRIPTION</span></span>
<span data-ttu-id="f2c3e-108">Az **Add-AzureRmHDInsightClusterIdentity** parancsmag a New-AzureRmHDInsightClusterConfig parancsmag által létrehozott Azure HDInsight Configuration objektumhoz ad egy fürtöt.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f2c3e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f2c3e-109">EXAMPLES</span></span>

### <span data-ttu-id="f2c3e-110">1. példa: a fürtkonfigurációs adatok felvétele a fürtkonfigurációs objektumba</span><span class="sxs-lookup"><span data-stu-id="f2c3e-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
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

<span data-ttu-id="f2c3e-111">Ez a parancs a cluster Identity-adatokat hozzáadja a-Hadoop-001 nevű fürthöz, így a klaszter hozzáférhet az Azure Data Lake Store szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="f2c3e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2c3e-112">PARAMETERS</span></span>

### <span data-ttu-id="f2c3e-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="f2c3e-113">-AadTenantId</span></span>
<span data-ttu-id="f2c3e-114">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c3e-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f2c3e-115">-CertificateFileContents</span></span>
<span data-ttu-id="f2c3e-116">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c3e-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f2c3e-117">-CertificateFilePath</span></span>
<span data-ttu-id="f2c3e-118">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f2c3e-119">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c3e-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f2c3e-120">-CertificatePassword</span></span>
<span data-ttu-id="f2c3e-121">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f2c3e-122">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2c3e-123">-Config</span><span class="sxs-lookup"><span data-stu-id="f2c3e-123">-Config</span></span>
<span data-ttu-id="f2c3e-124">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="f2c3e-125">Ezt az objektumot az New-AzureRmHDInsightClusterConfig parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c3e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c3e-126">-DefaultProfile</span></span>
<span data-ttu-id="f2c3e-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f2c3e-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2c3e-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f2c3e-128">-ObjectId</span></span>
<span data-ttu-id="f2c3e-129">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="f2c3e-130">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f2c3e-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c3e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c3e-131">CommonParameters</span></span>
<span data-ttu-id="f2c3e-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2c3e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c3e-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2c3e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c3e-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2c3e-134">INPUTS</span></span>

### <span data-ttu-id="f2c3e-135">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f2c3e-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="f2c3e-136">Paraméterek: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2c3e-136">Parameters: Config (ByValue)</span></span>

### <span data-ttu-id="f2c3e-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f2c3e-137">System.Guid</span></span>
<span data-ttu-id="f2c3e-138">Paraméterek: ObjectId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2c3e-138">Parameters: ObjectId (ByValue)</span></span>

## <span data-ttu-id="f2c3e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2c3e-139">OUTPUTS</span></span>

### <span data-ttu-id="f2c3e-140">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f2c3e-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f2c3e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2c3e-141">NOTES</span></span>

## <span data-ttu-id="f2c3e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2c3e-142">RELATED LINKS</span></span>

[<span data-ttu-id="f2c3e-143">Új – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f2c3e-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


