---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: 6755bb08174a34fe91c5e11373719607f87ad711
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356928"
---
# <span data-ttu-id="303f6-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="303f6-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="303f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="303f6-102">SYNOPSIS</span></span>
<span data-ttu-id="303f6-103">A fürtben futó szolgáltatások verziójának hozzáadása fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="303f6-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="303f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="303f6-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="303f6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="303f6-105">DESCRIPTION</span></span>
<span data-ttu-id="303f6-106">A Add-AzHDInsightComponentVersion parancsmag hozzáadja egy fürtben futó szolgáltatás verzióját a New-AzHDInsightClusterConfig Által létrehozott Azure HDInsight konfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="303f6-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="303f6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="303f6-107">EXAMPLES</span></span>

### <span data-ttu-id="303f6-108">1. példa: A Spark-verzió hozzáadása a fürt konfigurációs objektumához.</span><span class="sxs-lookup"><span data-stu-id="303f6-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = Get-AzStorageAccountKey `
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
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightClusterConfig `
            | Add-AzHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="303f6-109">Ez a parancs hozzáadja a Spark verzióját a "saját értékgörbéje 001" nevű HDInsight-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="303f6-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="303f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="303f6-110">PARAMETERS</span></span>

### <span data-ttu-id="303f6-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="303f6-111">-ComponentName</span></span>
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

### <span data-ttu-id="303f6-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="303f6-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="303f6-113">-Config</span><span class="sxs-lookup"><span data-stu-id="303f6-113">-Config</span></span>
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

### <span data-ttu-id="303f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303f6-114">-DefaultProfile</span></span>
<span data-ttu-id="303f6-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="303f6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="303f6-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="303f6-116">-Confirm</span></span>
<span data-ttu-id="303f6-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="303f6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="303f6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="303f6-118">-WhatIf</span></span>
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

### <span data-ttu-id="303f6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303f6-119">CommonParameters</span></span>
<span data-ttu-id="303f6-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="303f6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303f6-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="303f6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303f6-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="303f6-122">INPUTS</span></span>

### <span data-ttu-id="303f6-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="303f6-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="303f6-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="303f6-124">OUTPUTS</span></span>

### <span data-ttu-id="303f6-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="303f6-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="303f6-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="303f6-126">NOTES</span></span>

## <span data-ttu-id="303f6-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="303f6-127">RELATED LINKS</span></span>
