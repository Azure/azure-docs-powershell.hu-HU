---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 866bd8c8189ca727b3893f09370bcca1136e827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504568"
---
# <span data-ttu-id="e9591-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="e9591-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="e9591-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9591-102">SYNOPSIS</span></span>
<span data-ttu-id="e9591-103">Új parancsfájl-művelet elküldhet egy Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="e9591-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9591-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9591-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9591-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9591-105">DESCRIPTION</span></span>
<span data-ttu-id="e9591-106">A **Submit-AzureRmHDInsightScriptAction** parancsmag új parancsfájl-műveleteket továbbít az Azure HDInsight-fürtökhöz.</span><span class="sxs-lookup"><span data-stu-id="e9591-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="e9591-107">A *PersistOnSuccess* használatával a parancsfájl-művelet minden alkalommal futtatható a fürt skálázásakor, amíg a parancsfájl művelete eredetileg sikeres.</span><span class="sxs-lookup"><span data-stu-id="e9591-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="e9591-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e9591-108">EXAMPLES</span></span>

### <span data-ttu-id="e9591-109">1. példa: új parancsfájl-művelet elterjesztése futó HDInsight-fürtön</span><span class="sxs-lookup"><span data-stu-id="e9591-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="e9591-110">Ez a parancs parancsfájl-műveleteket futtat egy futó HDInsight-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e9591-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="e9591-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9591-111">PARAMETERS</span></span>

### <span data-ttu-id="e9591-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="e9591-112">-ApplicationName</span></span>
<span data-ttu-id="e9591-113">A parancsfájl alkalmazásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9591-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="e9591-114">Ha a *ApplicationName* érték van megadva, akkor a *PersistOnSuccess* false értékre kell állítani, a csomópontoknak csak edgenode kell lenniük, és a parancsfájl-műveletek száma egyenlő 1-gyel fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="e9591-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9591-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="e9591-115">-ClusterName</span></span>
<span data-ttu-id="e9591-116">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9591-116">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9591-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9591-117">-DefaultProfile</span></span>
<span data-ttu-id="e9591-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e9591-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9591-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e9591-119">-Name</span></span>
<span data-ttu-id="e9591-120">A parancsfájl-műveletek nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9591-120">Specifies the name of the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9591-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="e9591-121">-NodeTypes</span></span>
<span data-ttu-id="e9591-122">Itt adhatja meg a parancsfájl-műveletek futtatásához használt csomópont-típusokat.</span><span class="sxs-lookup"><span data-stu-id="e9591-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9591-123">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="e9591-123">-Parameters</span></span>
<span data-ttu-id="e9591-124">A parancsfájl-műveletek paramétereit adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9591-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9591-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="e9591-125">-PersistOnSuccess</span></span>
<span data-ttu-id="e9591-126">Azt jelzi, hogy a parancsfájl-műveletek futtatásakor minden alkalommal futtatnia kell a parancsfájlt.</span><span class="sxs-lookup"><span data-stu-id="e9591-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="e9591-127">Ezt a kapcsolót a program figyelmen kívül hagyja, ha a parancsfájl-művelet eredetileg nem működik.</span><span class="sxs-lookup"><span data-stu-id="e9591-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9591-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9591-128">-ResourceGroupName</span></span>
<span data-ttu-id="e9591-129">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9591-129">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9591-130">-URI</span><span class="sxs-lookup"><span data-stu-id="e9591-130">-Uri</span></span>
<span data-ttu-id="e9591-131">A parancsfájl-műveletek (PowerShell-vagy bash-parancsfájlok) nyilvános URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9591-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9591-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9591-132">CommonParameters</span></span>
<span data-ttu-id="e9591-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9591-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9591-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9591-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9591-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9591-135">INPUTS</span></span>

### <span data-ttu-id="e9591-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="e9591-136">None</span></span>
<span data-ttu-id="e9591-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e9591-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9591-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9591-138">OUTPUTS</span></span>

### <span data-ttu-id="e9591-139">Microsoft. Azure. Command. HDInsight. models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="e9591-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="e9591-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9591-140">NOTES</span></span>

## <span data-ttu-id="e9591-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9591-141">RELATED LINKS</span></span>

[<span data-ttu-id="e9591-142">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="e9591-142">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


