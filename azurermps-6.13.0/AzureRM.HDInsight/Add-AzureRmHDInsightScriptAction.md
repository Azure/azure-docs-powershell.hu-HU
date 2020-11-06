---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 359ec8ed28478b41b304f52fbd5a6c6fa2f1665a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496171"
---
# <span data-ttu-id="36a6f-101">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="36a6f-101">Add-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="36a6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="36a6f-103">Parancsfájl-műveleteket ad egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="36a6f-103">Adds a script action to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36a6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36a6f-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36a6f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36a6f-105">DESCRIPTION</span></span>
<span data-ttu-id="36a6f-106">Az **Add-AzureRmHDInsightScriptAction** parancsmag parancsfájl-műveleteket ad az New-AzureRmHDInsightClusterConfig parancsmag által létrehozott HDInsight-konfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="36a6f-106">The **Add-AzureRmHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="36a6f-107">A parancsfájl-műveletek funkciókat nyújtanak a további szoftverek telepítéséhez, illetve a Hadoop-fürtökön futó alkalmazások konfigurációjának módosításához Windows PowerShell-vagy bash-parancsfájlok (Windows-vagy Linux-fürtök esetén) segítségével.</span><span class="sxs-lookup"><span data-stu-id="36a6f-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="36a6f-108">Parancsfájl-műveletek akkor futnak a fürtcsomópontok során, ha a HDInsight-fürtöket telepítik, és a fürt a fürtök teljes HDInsight-konfigurációját követően futnak.</span><span class="sxs-lookup"><span data-stu-id="36a6f-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="36a6f-109">A parancsfájl-műveletek a rendszeradminisztrátori fiók jogosultságai csoportban futnak, és teljes hozzáférési jogosultságokat biztosítanak a fürtcsomópontok számára.</span><span class="sxs-lookup"><span data-stu-id="36a6f-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="36a6f-110">Az egyes fürtöket megadhatja az adott sorrendben futtatandó parancsfájl-műveletek listájával.</span><span class="sxs-lookup"><span data-stu-id="36a6f-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="36a6f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="36a6f-111">EXAMPLES</span></span>

### <span data-ttu-id="36a6f-112">1. példa: parancsfájl-művelet hozzáadása a fürtkonfigurációs objektumhoz</span><span class="sxs-lookup"><span data-stu-id="36a6f-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
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

<span data-ttu-id="36a6f-113">A parancs hozzáadja az Ön-Hadoop-001-fürthöz tartozó, a fürtök létrehozásakor futtatandó parancsfájl-műveleteket.</span><span class="sxs-lookup"><span data-stu-id="36a6f-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="36a6f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36a6f-114">PARAMETERS</span></span>

### <span data-ttu-id="36a6f-115">-Config</span><span class="sxs-lookup"><span data-stu-id="36a6f-115">-Config</span></span>
<span data-ttu-id="36a6f-116">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="36a6f-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="36a6f-117">Ezt az objektumot a **New-AzureRmHDInsightClusterConfig** parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="36a6f-117">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="36a6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a6f-118">-DefaultProfile</span></span>
<span data-ttu-id="36a6f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="36a6f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36a6f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36a6f-120">-Name</span></span>
<span data-ttu-id="36a6f-121">A parancsfájl-műveletek nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36a6f-121">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="36a6f-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="36a6f-122">-NodeType</span></span>
<span data-ttu-id="36a6f-123">Annak a csomópontnak a típusa, amelyen a parancsfájl-műveletek futtathatók.</span><span class="sxs-lookup"><span data-stu-id="36a6f-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="36a6f-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="36a6f-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36a6f-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="36a6f-125">HeadNode</span></span>
- <span data-ttu-id="36a6f-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="36a6f-126">WorkerNode</span></span>
- <span data-ttu-id="36a6f-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="36a6f-127">ZookeeperNode</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a6f-128">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="36a6f-128">-Parameters</span></span>
<span data-ttu-id="36a6f-129">A parancsfájl-műveletek paramétereit adja meg.</span><span class="sxs-lookup"><span data-stu-id="36a6f-129">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a6f-130">-URI</span><span class="sxs-lookup"><span data-stu-id="36a6f-130">-Uri</span></span>
<span data-ttu-id="36a6f-131">A parancsfájl-műveletek (PowerShell-vagy bash-parancsfájlok) nyilvános URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36a6f-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a6f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a6f-132">CommonParameters</span></span>
<span data-ttu-id="36a6f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36a6f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a6f-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36a6f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a6f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36a6f-135">INPUTS</span></span>

### <span data-ttu-id="36a6f-136">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="36a6f-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="36a6f-137">Paraméterek: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36a6f-137">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="36a6f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36a6f-138">OUTPUTS</span></span>

### <span data-ttu-id="36a6f-139">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="36a6f-139">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="36a6f-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36a6f-140">NOTES</span></span>

## <span data-ttu-id="36a6f-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36a6f-141">RELATED LINKS</span></span>

[<span data-ttu-id="36a6f-142">Új – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="36a6f-142">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


