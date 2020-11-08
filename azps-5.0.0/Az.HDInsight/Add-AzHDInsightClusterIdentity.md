---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 4d791faf320285e5392eb9edd523447df02c1984
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185399"
---
# <span data-ttu-id="f944c-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="f944c-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="f944c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f944c-102">SYNOPSIS</span></span>
<span data-ttu-id="f944c-103">A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="f944c-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="f944c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f944c-104">SYNTAX</span></span>

### <span data-ttu-id="f944c-105">CertificateFilePath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f944c-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f944c-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f944c-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f944c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f944c-107">DESCRIPTION</span></span>
<span data-ttu-id="f944c-108">Az **Add-AzHDInsightClusterIdentity** parancsmag a New-AzHDInsightClusterConfig parancsmag által létrehozott Azure HDInsight Configuration objektumhoz ad egy fürtöt.</span><span class="sxs-lookup"><span data-stu-id="f944c-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f944c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f944c-109">EXAMPLES</span></span>

### <span data-ttu-id="f944c-110">1. példa: a fürtkonfigurációs adatok felvétele a fürtkonfigurációs objektumba</span><span class="sxs-lookup"><span data-stu-id="f944c-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
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

<span data-ttu-id="f944c-111">Ez a parancs a cluster Identity-adatokat hozzáadja a-Hadoop-001 nevű fürthöz, így a klaszter hozzáférhet az Azure Data Lake Store szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f944c-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="f944c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f944c-112">PARAMETERS</span></span>

### <span data-ttu-id="f944c-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="f944c-113">-AadTenantId</span></span>
<span data-ttu-id="f944c-114">Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.</span><span class="sxs-lookup"><span data-stu-id="f944c-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f944c-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f944c-115">-ApplicationId</span></span>
<span data-ttu-id="f944c-116">Az Azure-adattó elérésére szolgáló szolgáltatási Principal-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f944c-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="f944c-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f944c-117">-CertificateFileContents</span></span>
<span data-ttu-id="f944c-118">Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f944c-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f944c-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f944c-119">-CertificateFilePath</span></span>
<span data-ttu-id="f944c-120">Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.</span><span class="sxs-lookup"><span data-stu-id="f944c-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f944c-121">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f944c-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f944c-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f944c-122">-CertificatePassword</span></span>
<span data-ttu-id="f944c-123">Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.</span><span class="sxs-lookup"><span data-stu-id="f944c-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f944c-124">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f944c-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f944c-125">-Config</span><span class="sxs-lookup"><span data-stu-id="f944c-125">-Config</span></span>
<span data-ttu-id="f944c-126">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f944c-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="f944c-127">Ezt az objektumot az New-AzHDInsightClusterConfig parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f944c-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="f944c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f944c-128">-DefaultProfile</span></span>
<span data-ttu-id="f944c-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f944c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f944c-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f944c-130">-ObjectId</span></span>
<span data-ttu-id="f944c-131">Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.</span><span class="sxs-lookup"><span data-stu-id="f944c-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="f944c-132">A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f944c-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f944c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f944c-133">CommonParameters</span></span>
<span data-ttu-id="f944c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f944c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f944c-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f944c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f944c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f944c-136">INPUTS</span></span>

### <span data-ttu-id="f944c-137">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f944c-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="f944c-138">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f944c-138">System.Guid</span></span>

## <span data-ttu-id="f944c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f944c-139">OUTPUTS</span></span>

### <span data-ttu-id="f944c-140">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f944c-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f944c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f944c-141">NOTES</span></span>

## <span data-ttu-id="f944c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f944c-142">RELATED LINKS</span></span>

[<span data-ttu-id="f944c-143">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f944c-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


