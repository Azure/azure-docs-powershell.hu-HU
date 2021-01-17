---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 06a783d0faf32dc2a3a35b448b1316ef50ba3326
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467737"
---
# <span data-ttu-id="3c3d3-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="3c3d3-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="3c3d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c3d3-102">SYNOPSIS</span></span>
<span data-ttu-id="3c3d3-103">Egy fürtkonfigurációs objektum alapértelmezett tárfiók-beállítását állítja be.</span><span class="sxs-lookup"><span data-stu-id="3c3d3-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="3c3d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c3d3-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountResourceId] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c3d3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c3d3-105">DESCRIPTION</span></span>
<span data-ttu-id="3c3d3-106">A **Set-AzHDInsightDefaultStorage** parancsmag beállítja az alapértelmezett tárfiók-beállítást az Azure HDInsight-fürtkonfigurációs objektumban, amelyet a New-AzHDInsightClusterConfig parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3c3d3-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="3c3d3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c3d3-107">EXAMPLES</span></span>

### <span data-ttu-id="3c3d3-108">1. példa: A fürtkonfigurációs objektum alapértelmezett tárfiókjának beállítása</span><span class="sxs-lookup"><span data-stu-id="3c3d3-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
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
                -StorageAccountResourceId $storageAccountResourceId `
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

<span data-ttu-id="3c3d3-109">Ez a parancs beállítja egy fürtkonfigurációs objektum alapértelmezett tárfiókját.</span><span class="sxs-lookup"><span data-stu-id="3c3d3-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="3c3d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c3d3-110">PARAMETERS</span></span>

### <span data-ttu-id="3c3d3-111">-Config</span><span class="sxs-lookup"><span data-stu-id="3c3d3-111">-Config</span></span>
<span data-ttu-id="3c3d3-112">Ez a parancsmag által módosított HDInsight-fürtkonfigurációs objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c3d3-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3c3d3-113">Ezt az objektumot a **New-AzHDInsightClusterConfig** parancsmag hozta létre.</span><span class="sxs-lookup"><span data-stu-id="3c3d3-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="3c3d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c3d3-114">-DefaultProfile</span></span>
<span data-ttu-id="3c3d3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3c3d3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c3d3-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3c3d3-116">-StorageAccountKey</span></span>
<span data-ttu-id="3c3d3-117">A HDInsight-fürt által használt alapértelmezett Azure Storage-fiók fiókkulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c3d3-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="3c3d3-118">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3c3d3-118">-StorageAccountResourceId</span></span>
<span data-ttu-id="3c3d3-119">Az új fürthöz hozzáadható tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="3c3d3-119">The storage account name for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="3c3d3-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3c3d3-120">-StorageAccountType</span></span>
<span data-ttu-id="3c3d3-121">Beállítja vagy beállítja az alapértelmezett tárfiók típusát.</span><span class="sxs-lookup"><span data-stu-id="3c3d3-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="3c3d3-122">Alapértékek az AzureStorage-ban</span><span class="sxs-lookup"><span data-stu-id="3c3d3-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c3d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c3d3-123">CommonParameters</span></span>
<span data-ttu-id="3c3d3-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c3d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c3d3-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c3d3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c3d3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c3d3-126">INPUTS</span></span>

### <span data-ttu-id="3c3d3-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3c3d3-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3c3d3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c3d3-128">OUTPUTS</span></span>

### <span data-ttu-id="3c3d3-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3c3d3-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3c3d3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c3d3-130">NOTES</span></span>

## <span data-ttu-id="3c3d3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c3d3-131">RELATED LINKS</span></span>
