---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightComponentVersion.md
ms.openlocfilehash: f464883eef8b37716585d4336d64dd6c032470da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496176"
---
# <span data-ttu-id="a0e94-101">Add-AzureRmHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="a0e94-101">Add-AzureRmHDInsightComponentVersion</span></span>

## <span data-ttu-id="a0e94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0e94-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e94-103">A fürtben futó szolgáltatás verziójának hozzáadása a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="a0e94-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0e94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0e94-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0e94-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0e94-105">DESCRIPTION</span></span>
<span data-ttu-id="a0e94-106">A Add-AzureRmHDInsightComponentVersion parancsmag a New-AzureRmHDInsightClusterConfig parancsmag által létrehozott Azure HDInsight Configuration objektumhoz ad egy verziót a fürtben futó szolgáltatásokhoz.</span><span class="sxs-lookup"><span data-stu-id="a0e94-106">The Add-AzureRmHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="a0e94-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0e94-107">EXAMPLES</span></span>

### <span data-ttu-id="a0e94-108">Példa 1: a szikra verziójának hozzáadása a fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="a0e94-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzureRmHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="a0e94-109">Ez a parancs hozzáadja a szikra verzióját a "saját szikra-001" nevű HDInsight-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="a0e94-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="a0e94-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0e94-110">PARAMETERS</span></span>

### <span data-ttu-id="a0e94-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="a0e94-111">-ComponentName</span></span>
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

### <span data-ttu-id="a0e94-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="a0e94-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="a0e94-113">-Config</span><span class="sxs-lookup"><span data-stu-id="a0e94-113">-Config</span></span>
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

### <span data-ttu-id="a0e94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e94-114">-DefaultProfile</span></span>
<span data-ttu-id="a0e94-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a0e94-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0e94-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0e94-116">-Confirm</span></span>
<span data-ttu-id="a0e94-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0e94-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e94-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e94-118">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e94-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e94-119">CommonParameters</span></span>
<span data-ttu-id="a0e94-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0e94-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e94-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0e94-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e94-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0e94-122">INPUTS</span></span>

### <span data-ttu-id="a0e94-123">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a0e94-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="a0e94-124">Paraméterek: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0e94-124">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="a0e94-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0e94-125">OUTPUTS</span></span>

### <span data-ttu-id="a0e94-126">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a0e94-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a0e94-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0e94-127">NOTES</span></span>

## <span data-ttu-id="a0e94-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0e94-128">RELATED LINKS</span></span>
