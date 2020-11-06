---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
ms.openlocfilehash: f70403f70e116a0e6addc569942f927aca0dcf0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500039"
---
# <span data-ttu-id="23c34-101">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="23c34-101">Add-AzureRmHDInsightStorage</span></span>

## <span data-ttu-id="23c34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23c34-102">SYNOPSIS</span></span>
<span data-ttu-id="23c34-103">Azure-tárterületet ad hozzá egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="23c34-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23c34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23c34-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23c34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23c34-105">DESCRIPTION</span></span>
<span data-ttu-id="23c34-106">Az **Add-AzureRmHDInsightStorage** parancsmag az Azure Storage Account bejegyzését hozzáadja az New-AzureRmHDInsightClusterConfig parancsmag által létrehozott Azure HDInsight Configuration objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="23c34-106">The **Add-AzureRmHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="23c34-107">Példák</span><span class="sxs-lookup"><span data-stu-id="23c34-107">EXAMPLES</span></span>

### <span data-ttu-id="23c34-108">1. példa: az Azure Storage kulcs felvétele a fürtkonfigurációs objektumba</span><span class="sxs-lookup"><span data-stu-id="23c34-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzureRmStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="23c34-109">Ez a parancs a blob-tároló fiók bejegyzését hozzáadja a-Hadoop-001 nevű HDInsight-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="23c34-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="23c34-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23c34-110">PARAMETERS</span></span>

### <span data-ttu-id="23c34-111">-Config</span><span class="sxs-lookup"><span data-stu-id="23c34-111">-Config</span></span>
<span data-ttu-id="23c34-112">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="23c34-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="23c34-113">Ezt az objektumot a **New-AzureRmHDInsightClusterConfig** parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="23c34-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="23c34-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="23c34-114">-StorageAccountKey</span></span>
<span data-ttu-id="23c34-115">Az új fürthöz hozzáadni kívánt tárterülethez tartozó tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="23c34-115">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="23c34-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="23c34-116">-StorageAccountName</span></span>
<span data-ttu-id="23c34-117">Annak a tárterületnek a tárolási fiókjának a nevét adja meg, amelyet hozzá szeretne adni a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="23c34-117">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="23c34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c34-118">-DefaultProfile</span></span>
<span data-ttu-id="23c34-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23c34-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23c34-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c34-120">CommonParameters</span></span>
<span data-ttu-id="23c34-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23c34-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c34-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23c34-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c34-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23c34-123">INPUTS</span></span>

### <span data-ttu-id="23c34-124">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="23c34-124">AzureHDInsightConfig</span></span>
<span data-ttu-id="23c34-125">A "config" paraméter elfogadja a "AzureHDInsightConfig" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="23c34-125">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="23c34-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23c34-126">OUTPUTS</span></span>

### <span data-ttu-id="23c34-127">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="23c34-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="23c34-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23c34-128">NOTES</span></span>

## <span data-ttu-id="23c34-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23c34-129">RELATED LINKS</span></span>

[<span data-ttu-id="23c34-130">Új – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="23c34-130">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


