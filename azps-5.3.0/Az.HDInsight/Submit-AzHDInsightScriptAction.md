---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: 3cbd73075445bdcf65efafb266476c522dc4b1ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469638"
---
# <span data-ttu-id="0b521-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="0b521-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="0b521-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b521-102">SYNOPSIS</span></span>
<span data-ttu-id="0b521-103">Új parancsfájl-műveletet küld egy Azure HDInsight-fürtnek.</span><span class="sxs-lookup"><span data-stu-id="0b521-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0b521-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b521-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b521-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b521-105">DESCRIPTION</span></span>
<span data-ttu-id="0b521-106">A **Submit-AzHDInsightScriptAction** parancsmag új parancsfájl-műveletet küld egy Azure HDInsight-fürtnek.</span><span class="sxs-lookup"><span data-stu-id="0b521-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="0b521-107">A *PersistOnSuccess* parancsprogramot használva futtassa a parancsfájl-műveletet a fürt minden egyes méretének méretezésekor, ha a parancsprogram-művelet kezdetben sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="0b521-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="0b521-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b521-108">EXAMPLES</span></span>

### <span data-ttu-id="0b521-109">1. példa: Új parancsfájl-művelet elküldése egy futó HDInsight-fürtnek</span><span class="sxs-lookup"><span data-stu-id="0b521-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="0b521-110">Ez a parancs parancsprogramot küld egy futó HDInsight-fürtnek.</span><span class="sxs-lookup"><span data-stu-id="0b521-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="0b521-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b521-111">PARAMETERS</span></span>

### <span data-ttu-id="0b521-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0b521-112">-ApplicationName</span></span>
<span data-ttu-id="0b521-113">A parancsfájl-művelet alkalmazásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b521-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="0b521-114">Ha *az ApplicationName* meg van adva, a *PersistOnSuccess* értéke Hamis, a csomópontoknak csak edgenode-et kell tartalmazni, a parancsfájl-műveletszámnak pedig 1-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="0b521-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b521-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0b521-115">-ClusterName</span></span>
<span data-ttu-id="0b521-116">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b521-116">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b521-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b521-117">-DefaultProfile</span></span>
<span data-ttu-id="0b521-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0b521-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b521-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0b521-119">-Name</span></span>
<span data-ttu-id="0b521-120">A parancsfájl-művelet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b521-120">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b521-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="0b521-121">-NodeTypes</span></span>
<span data-ttu-id="0b521-122">Megadja, hogy milyen csomóponttípusokon futtassa a parancsfájl-műveletet.</span><span class="sxs-lookup"><span data-stu-id="0b521-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b521-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="0b521-123">-Parameters</span></span>
<span data-ttu-id="0b521-124">A parancsfájl-művelet paramétereit adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b521-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b521-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="0b521-125">-PersistOnSuccess</span></span>
<span data-ttu-id="0b521-126">Azt jelzi, hogy a parancsfájl-műveletnek minden alkalommal futnia kell, amikor a fürt mérete fel van méretezve.</span><span class="sxs-lookup"><span data-stu-id="0b521-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="0b521-127">Ezt a kapcsoló paramétert figyelmen kívül hagyja a program, ha a parancsprogram-művelet kezdetben meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="0b521-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b521-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b521-128">-ResourceGroupName</span></span>
<span data-ttu-id="0b521-129">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b521-129">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b521-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="0b521-130">-Uri</span></span>
<span data-ttu-id="0b521-131">A parancsfájl-művelet nyilvános URI-ját adja meg (PowerShell- vagy Bash-parancsfájl).</span><span class="sxs-lookup"><span data-stu-id="0b521-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b521-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b521-132">CommonParameters</span></span>
<span data-ttu-id="0b521-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b521-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b521-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b521-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b521-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b521-135">INPUTS</span></span>

### <span data-ttu-id="0b521-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0b521-136">System.String</span></span>

### <span data-ttu-id="0b521-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="0b521-137">System.Uri</span></span>

### <span data-ttu-id="0b521-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span><span class="sxs-lookup"><span data-stu-id="0b521-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="0b521-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b521-139">OUTPUTS</span></span>

### <span data-ttu-id="0b521-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="0b521-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="0b521-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b521-141">NOTES</span></span>

## <span data-ttu-id="0b521-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b521-142">RELATED LINKS</span></span>

[<span data-ttu-id="0b521-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="0b521-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


