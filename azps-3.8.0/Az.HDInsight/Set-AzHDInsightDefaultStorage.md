---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: e4ecdb86d3c8b055f76303af5c3b86fc9813e167
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846054"
---
# <span data-ttu-id="85e34-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="85e34-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="85e34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85e34-102">SYNOPSIS</span></span>
<span data-ttu-id="85e34-103">Beállítja az alapértelmezett tárolási fiók beállítását egy fürtkonfiguráció-objektumban.</span><span class="sxs-lookup"><span data-stu-id="85e34-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="85e34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85e34-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85e34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85e34-105">DESCRIPTION</span></span>
<span data-ttu-id="85e34-106">A **set-AzHDInsightDefaultStorage** parancsmag az New-AzHDInsightClusterConfig parancsmag által létrehozott Azure HDInsight-fürtkonfigurációs objektum alapértelmezett tárolási fiók beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e34-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="85e34-107">Példák</span><span class="sxs-lookup"><span data-stu-id="85e34-107">EXAMPLES</span></span>

### <span data-ttu-id="85e34-108">Példa 1: a fürtkonfigurációs objektum alapértelmezett tárolási fiókjának beállítása</span><span class="sxs-lookup"><span data-stu-id="85e34-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="85e34-109">Ez a parancs beállítja a fürtkonfigurációs objektum alapértelmezett tárolási fiókját.</span><span class="sxs-lookup"><span data-stu-id="85e34-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="85e34-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85e34-110">PARAMETERS</span></span>

### <span data-ttu-id="85e34-111">-Config</span><span class="sxs-lookup"><span data-stu-id="85e34-111">-Config</span></span>
<span data-ttu-id="85e34-112">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="85e34-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="85e34-113">Ezt az objektumot a **New-AzHDInsightClusterConfig** parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="85e34-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="85e34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e34-114">-DefaultProfile</span></span>
<span data-ttu-id="85e34-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="85e34-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85e34-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="85e34-116">-StorageAccountKey</span></span>
<span data-ttu-id="85e34-117">A HDInsight-fürtöt használó alapértelmezett Azure-tárterülethez tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="85e34-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e34-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="85e34-118">-StorageAccountName</span></span>
<span data-ttu-id="85e34-119">Annak az alapértelmezett tárterület-fióknak a nevét adja meg, amelyet a HDInsight-fürt fog használni.</span><span class="sxs-lookup"><span data-stu-id="85e34-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="85e34-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="85e34-120">-StorageAccountType</span></span>
<span data-ttu-id="85e34-121">Az alapértelmezett tárterület-fiók típusának megadása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="85e34-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="85e34-122">Alapértékek a AzureStorage</span><span class="sxs-lookup"><span data-stu-id="85e34-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e34-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e34-123">CommonParameters</span></span>
<span data-ttu-id="85e34-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85e34-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e34-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e34-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e34-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85e34-126">INPUTS</span></span>

### <span data-ttu-id="85e34-127">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="85e34-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="85e34-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85e34-128">OUTPUTS</span></span>

### <span data-ttu-id="85e34-129">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="85e34-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="85e34-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85e34-130">NOTES</span></span>

## <span data-ttu-id="85e34-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85e34-131">RELATED LINKS</span></span>
