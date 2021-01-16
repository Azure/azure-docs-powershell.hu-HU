---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 4d791faf320285e5392eb9edd523447df02c1984
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335982"
---
# <span data-ttu-id="94029-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="94029-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="94029-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94029-102">SYNOPSIS</span></span>
<span data-ttu-id="94029-103">Fürtidentitás hozzáadása fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="94029-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="94029-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94029-104">SYNTAX</span></span>

### <span data-ttu-id="94029-105">CertificateFilePath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94029-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94029-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="94029-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94029-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94029-107">DESCRIPTION</span></span>
<span data-ttu-id="94029-108">Az **Add-AzHDInsightClusterIdentity** parancsmag hozzáad egy fürt identitást a New-AzHDInsightClusterConfig által létrehozott Azure HDInsight konfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="94029-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="94029-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94029-109">EXAMPLES</span></span>

### <span data-ttu-id="94029-110">1. példa: Fürtidentitás-adatok hozzáadása a fürtkonfigurációs objektumhoz</span><span class="sxs-lookup"><span data-stu-id="94029-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $applicationId = "<Azure AD Service Principal Application ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -Application $applicationId
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="94029-111">Ez a parancs hozzáadja a fürt identitásával kapcsolatos adatokat a -hadoop-001 nevű fürthöz, így a fürt hozzáférhet az Azure Data Lake Store-hoz.</span><span class="sxs-lookup"><span data-stu-id="94029-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="94029-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94029-112">PARAMETERS</span></span>

### <span data-ttu-id="94029-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="94029-113">-AadTenantId</span></span>
<span data-ttu-id="94029-114">Az Azure Data Lake Store elérésekor használt Azure AD bérlőazonosító.</span><span class="sxs-lookup"><span data-stu-id="94029-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="94029-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="94029-115">-ApplicationId</span></span>
<span data-ttu-id="94029-116">Az Azure Data Lake eléréséhez szükséges egyszerű szolgáltatásalkalmazás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="94029-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="94029-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="94029-117">-CertificateFileContents</span></span>
<span data-ttu-id="94029-118">Megadja annak a tanúsítványnak a fájl tartalmát, amely az Azure Data Lake Store elérésekor használatos.</span><span class="sxs-lookup"><span data-stu-id="94029-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="94029-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="94029-119">-CertificateFilePath</span></span>
<span data-ttu-id="94029-120">Megadja annak a tanúsítványnak a fájl elérési útját, amely a szolgáltatásnévként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="94029-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="94029-121">A fürt ezt fogja használni az Azure Data Lake Store elérésekor.</span><span class="sxs-lookup"><span data-stu-id="94029-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="94029-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="94029-122">-CertificatePassword</span></span>
<span data-ttu-id="94029-123">Megadja annak a tanúsítványnak a jelszavát, amely a szolgáltatásnévként való hitelesítéshez használatos.</span><span class="sxs-lookup"><span data-stu-id="94029-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="94029-124">A fürt ezt fogja használni az Azure Data Lake Store elérésekor.</span><span class="sxs-lookup"><span data-stu-id="94029-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="94029-125">-Config</span><span class="sxs-lookup"><span data-stu-id="94029-125">-Config</span></span>
<span data-ttu-id="94029-126">Ez a parancsmag által módosított HDInsight-fürtkonfigurációs objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="94029-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="94029-127">Ezt az objektumot a New-AzHDInsightClusterConfig hozta létre.</span><span class="sxs-lookup"><span data-stu-id="94029-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="94029-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94029-128">-DefaultProfile</span></span>
<span data-ttu-id="94029-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="94029-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94029-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="94029-130">-ObjectId</span></span>
<span data-ttu-id="94029-131">A fürtöt képviselő Azure AD-szolgáltatásnév Azure AD-objektumazonosítóját (GUID azonosítóját) adja meg.</span><span class="sxs-lookup"><span data-stu-id="94029-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="94029-132">A fürt ezt fogja használni az Azure Data Lake Store elérésekor.</span><span class="sxs-lookup"><span data-stu-id="94029-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="94029-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94029-133">CommonParameters</span></span>
<span data-ttu-id="94029-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94029-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94029-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94029-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94029-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94029-136">INPUTS</span></span>

### <span data-ttu-id="94029-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="94029-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="94029-138">System.Guid</span><span class="sxs-lookup"><span data-stu-id="94029-138">System.Guid</span></span>

## <span data-ttu-id="94029-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94029-139">OUTPUTS</span></span>

### <span data-ttu-id="94029-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="94029-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="94029-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94029-141">NOTES</span></span>

## <span data-ttu-id="94029-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94029-142">RELATED LINKS</span></span>

[<span data-ttu-id="94029-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="94029-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


