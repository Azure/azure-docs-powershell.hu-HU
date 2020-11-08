---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: b3697b0f5e657a95d131c928f4393f8a4f1e854c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185382"
---
# <span data-ttu-id="f502e-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="f502e-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="f502e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f502e-102">SYNOPSIS</span></span>
<span data-ttu-id="f502e-103">Azure-tárterületet ad hozzá egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="f502e-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="f502e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f502e-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f502e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f502e-105">DESCRIPTION</span></span>
<span data-ttu-id="f502e-106">Az **Add-AzHDInsightStorage** parancsmag az Azure Storage Account bejegyzését hozzáadja az New-AzHDInsightClusterConfig parancsmag által létrehozott Azure HDInsight Configuration objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="f502e-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f502e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f502e-107">EXAMPLES</span></span>

### <span data-ttu-id="f502e-108">1. példa: az Azure Storage kulcs felvétele a fürtkonfigurációs objektumba</span><span class="sxs-lookup"><span data-stu-id="f502e-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

<span data-ttu-id="f502e-109">Ez a parancs a blob-tároló fiók bejegyzését hozzáadja a-Hadoop-001 nevű HDInsight-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="f502e-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="f502e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f502e-110">PARAMETERS</span></span>

### <span data-ttu-id="f502e-111">-Config</span><span class="sxs-lookup"><span data-stu-id="f502e-111">-Config</span></span>
<span data-ttu-id="f502e-112">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f502e-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="f502e-113">Ezt az objektumot a **New-AzHDInsightClusterConfig** parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f502e-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="f502e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f502e-114">-DefaultProfile</span></span>
<span data-ttu-id="f502e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f502e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f502e-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f502e-116">-StorageAccountKey</span></span>
<span data-ttu-id="f502e-117">Az új fürthöz hozzáadni kívánt tárterülethez tartozó tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f502e-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="f502e-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f502e-118">-StorageAccountName</span></span>
<span data-ttu-id="f502e-119">Annak a tárterületnek a tárolási fiókjának a nevét adja meg, amelyet hozzá szeretne adni a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="f502e-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="f502e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f502e-120">CommonParameters</span></span>
<span data-ttu-id="f502e-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f502e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f502e-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f502e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f502e-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f502e-123">INPUTS</span></span>

### <span data-ttu-id="f502e-124">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f502e-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f502e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f502e-125">OUTPUTS</span></span>

### <span data-ttu-id="f502e-126">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f502e-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f502e-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f502e-127">NOTES</span></span>

## <span data-ttu-id="f502e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f502e-128">RELATED LINKS</span></span>

[<span data-ttu-id="f502e-129">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f502e-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


