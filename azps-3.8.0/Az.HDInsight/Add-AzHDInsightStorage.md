---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 43850e035a59674b06502db1486de0d90fe6e4ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847586"
---
# <span data-ttu-id="41029-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="41029-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="41029-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41029-102">SYNOPSIS</span></span>
<span data-ttu-id="41029-103">Azure-tárterületet ad hozzá egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="41029-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="41029-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41029-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41029-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41029-105">DESCRIPTION</span></span>
<span data-ttu-id="41029-106">Az **Add-AzHDInsightStorage** parancsmag az Azure Storage Account bejegyzését hozzáadja az New-AzHDInsightClusterConfig parancsmag által létrehozott Azure HDInsight Configuration objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="41029-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="41029-107">Példák</span><span class="sxs-lookup"><span data-stu-id="41029-107">EXAMPLES</span></span>

### <span data-ttu-id="41029-108">1. példa: az Azure Storage kulcs felvétele a fürtkonfigurációs objektumba</span><span class="sxs-lookup"><span data-stu-id="41029-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="41029-109">Ez a parancs a blob-tároló fiók bejegyzését hozzáadja a-Hadoop-001 nevű HDInsight-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="41029-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="41029-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41029-110">PARAMETERS</span></span>

### <span data-ttu-id="41029-111">-Config</span><span class="sxs-lookup"><span data-stu-id="41029-111">-Config</span></span>
<span data-ttu-id="41029-112">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="41029-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="41029-113">Ezt az objektumot a **New-AzHDInsightClusterConfig** parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="41029-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="41029-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41029-114">-DefaultProfile</span></span>
<span data-ttu-id="41029-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="41029-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41029-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="41029-116">-StorageAccountKey</span></span>
<span data-ttu-id="41029-117">Az új fürthöz hozzáadni kívánt tárterülethez tartozó tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41029-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="41029-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="41029-118">-StorageAccountName</span></span>
<span data-ttu-id="41029-119">Annak a tárterületnek a tárolási fiókjának a nevét adja meg, amelyet hozzá szeretne adni a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="41029-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="41029-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41029-120">CommonParameters</span></span>
<span data-ttu-id="41029-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41029-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41029-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41029-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41029-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41029-123">INPUTS</span></span>

### <span data-ttu-id="41029-124">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="41029-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="41029-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41029-125">OUTPUTS</span></span>

### <span data-ttu-id="41029-126">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="41029-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="41029-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41029-127">NOTES</span></span>

## <span data-ttu-id="41029-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41029-128">RELATED LINKS</span></span>

[<span data-ttu-id="41029-129">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="41029-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


