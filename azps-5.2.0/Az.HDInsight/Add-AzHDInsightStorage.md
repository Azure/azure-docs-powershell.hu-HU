---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: b3697b0f5e657a95d131c928f4393f8a4f1e854c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339989"
---
# <span data-ttu-id="e03b8-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="e03b8-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="e03b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e03b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e03b8-103">Hozzáad egy Azure-tárterületkulcsot egy fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="e03b8-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="e03b8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e03b8-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e03b8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e03b8-105">DESCRIPTION</span></span>
<span data-ttu-id="e03b8-106">Az **Add-AzHDInsightStorage** parancsmag hozzáad egy Azure Storage-fiókbejegyzést a New-AzHDInsightClusterConfig által létrehozott Azure HDInsight konfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="e03b8-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="e03b8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e03b8-107">EXAMPLES</span></span>

### <span data-ttu-id="e03b8-108">1. példa: Azure-tárkulcs hozzáadása a fürtkonfigurációs objektumhoz</span><span class="sxs-lookup"><span data-stu-id="e03b8-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="e03b8-109">Ez a parancs hozzáad egy blobtároló-fiókbejegyzést a "your-hadoop-001" NEVŰ HDInsight-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="e03b8-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="e03b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e03b8-110">PARAMETERS</span></span>

### <span data-ttu-id="e03b8-111">-Config</span><span class="sxs-lookup"><span data-stu-id="e03b8-111">-Config</span></span>
<span data-ttu-id="e03b8-112">Ez a parancsmag által módosított HDInsight-fürtkonfigurációs objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e03b8-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="e03b8-113">Ezt az objektumot a **New-AzHDInsightClusterConfig** parancsmag hozta létre.</span><span class="sxs-lookup"><span data-stu-id="e03b8-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="e03b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e03b8-114">-DefaultProfile</span></span>
<span data-ttu-id="e03b8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e03b8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e03b8-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e03b8-116">-StorageAccountKey</span></span>
<span data-ttu-id="e03b8-117">Az új fürthöz hozzáadható tárfiók tárfiókkulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e03b8-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="e03b8-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e03b8-118">-StorageAccountName</span></span>
<span data-ttu-id="e03b8-119">Annak a tárfióknak a nevét adja meg, amelybe fel kell venni a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e03b8-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="e03b8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e03b8-120">CommonParameters</span></span>
<span data-ttu-id="e03b8-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e03b8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e03b8-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e03b8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e03b8-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e03b8-123">INPUTS</span></span>

### <span data-ttu-id="e03b8-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e03b8-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e03b8-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e03b8-125">OUTPUTS</span></span>

### <span data-ttu-id="e03b8-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e03b8-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e03b8-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e03b8-127">NOTES</span></span>

## <span data-ttu-id="e03b8-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e03b8-128">RELATED LINKS</span></span>

[<span data-ttu-id="e03b8-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e03b8-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


