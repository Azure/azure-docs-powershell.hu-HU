---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
ms.openlocfilehash: a0c534042df15d4ef999b47a5e468b1e13a8d14f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680550"
---
# <span data-ttu-id="ee682-101">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="ee682-101">Set-AzureRmHDInsightDefaultStorage</span></span>

## <span data-ttu-id="ee682-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee682-102">SYNOPSIS</span></span>
<span data-ttu-id="ee682-103">Beállítja az alapértelmezett tárolási fiók beállítását egy fürtkonfiguráció-objektumban.</span><span class="sxs-lookup"><span data-stu-id="ee682-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee682-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee682-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee682-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee682-105">DESCRIPTION</span></span>
<span data-ttu-id="ee682-106">A **set-AzureRmHDInsightDefaultStorage** parancsmag az New-AzureRmHDInsightClusterConfig parancsmag által létrehozott Azure HDInsight-fürtkonfigurációs objektum alapértelmezett tárolási fiók beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee682-106">The **Set-AzureRmHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ee682-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee682-107">EXAMPLES</span></span>

### <span data-ttu-id="ee682-108">Példa 1: a fürtkonfigurációs objektum alapértelmezett tárolási fiókjának beállítása</span><span class="sxs-lookup"><span data-stu-id="ee682-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Set-AzureRmHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="ee682-109">Ez a parancs beállítja a fürtkonfigurációs objektum alapértelmezett tárolási fiókját.</span><span class="sxs-lookup"><span data-stu-id="ee682-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="ee682-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee682-110">PARAMETERS</span></span>

### <span data-ttu-id="ee682-111">-Config</span><span class="sxs-lookup"><span data-stu-id="ee682-111">-Config</span></span>
<span data-ttu-id="ee682-112">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="ee682-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ee682-113">Ezt az objektumot a **New-AzureRmHDInsightClusterConfig** parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ee682-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="ee682-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ee682-114">-StorageAccountKey</span></span>
<span data-ttu-id="ee682-115">A HDInsight-fürtöt használó alapértelmezett Azure-tárterülethez tartozó fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee682-115">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="ee682-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ee682-116">-StorageAccountName</span></span>
<span data-ttu-id="ee682-117">Annak az alapértelmezett tárterület-fióknak a nevét adja meg, amelyet a HDInsight-fürt fog használni.</span><span class="sxs-lookup"><span data-stu-id="ee682-117">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="ee682-118">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ee682-118">-StorageAccountType</span></span>
<span data-ttu-id="ee682-119">Az alapértelmezett tárterület-fiók típusának megadása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="ee682-119">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="ee682-120">Alapértékek a AzureStorage</span><span class="sxs-lookup"><span data-stu-id="ee682-120">Defaults to AzureStorage</span></span>

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

### <span data-ttu-id="ee682-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee682-121">-DefaultProfile</span></span>
<span data-ttu-id="ee682-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee682-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee682-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee682-123">CommonParameters</span></span>
<span data-ttu-id="ee682-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee682-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee682-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee682-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee682-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee682-126">INPUTS</span></span>

### <span data-ttu-id="ee682-127">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ee682-127">AzureHDInsightConfig</span></span>
<span data-ttu-id="ee682-128">A "config" paraméter elfogadja a "AzureHDInsightConfig" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ee682-128">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="ee682-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee682-129">OUTPUTS</span></span>

### <span data-ttu-id="ee682-130">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ee682-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ee682-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee682-131">NOTES</span></span>

## <span data-ttu-id="ee682-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee682-132">RELATED LINKS</span></span>

