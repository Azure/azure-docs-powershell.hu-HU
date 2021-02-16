---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: 3cbd73075445bdcf65efafb266476c522dc4b1ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153090"
---
# <span data-ttu-id="23625-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="23625-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="23625-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23625-102">SYNOPSIS</span></span>
<span data-ttu-id="23625-103">Új parancsfájl-műveletet küld egy Azure HDInsight-fürtnek.</span><span class="sxs-lookup"><span data-stu-id="23625-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="23625-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="23625-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23625-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="23625-105">DESCRIPTION</span></span>
<span data-ttu-id="23625-106">A **Submit-AzHDInsightScriptAction** parancsmag új parancsfájl-műveletet küld egy Azure HDInsight-fürtnek.</span><span class="sxs-lookup"><span data-stu-id="23625-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="23625-107">A *PersistOnSuccess* segítségével futtassa a parancsfájl-műveletet a fürt minden egyes méretezésekor, ha a parancsfájl-művelet kezdetben sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="23625-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="23625-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="23625-108">EXAMPLES</span></span>

### <span data-ttu-id="23625-109">1. példa: Új parancsfájl-művelet elküldése egy futó HDInsight-fürtnek</span><span class="sxs-lookup"><span data-stu-id="23625-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="23625-110">Ez a parancs parancsprogramot küld egy futó HDInsight-fürtnek.</span><span class="sxs-lookup"><span data-stu-id="23625-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="23625-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23625-111">PARAMETERS</span></span>

### <span data-ttu-id="23625-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="23625-112">-ApplicationName</span></span>
<span data-ttu-id="23625-113">A parancsfájl-művelet alkalmazásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="23625-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="23625-114">Ha *az ApplicationName* meg van adva, a *PersistOnSuccess* értéke Hamis, a csomópontoknak csak edgenode-et kell tartalmazni, a parancsfájl-műveletszámnak pedig 1-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="23625-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="23625-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="23625-115">-ClusterName</span></span>
<span data-ttu-id="23625-116">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="23625-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="23625-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23625-117">-DefaultProfile</span></span>
<span data-ttu-id="23625-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="23625-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23625-119">-Name</span><span class="sxs-lookup"><span data-stu-id="23625-119">-Name</span></span>
<span data-ttu-id="23625-120">A parancsfájl-művelet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="23625-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="23625-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="23625-121">-NodeTypes</span></span>
<span data-ttu-id="23625-122">Megadja, hogy milyen csomóponttípusokon futtassa a parancsfájl-műveletet.</span><span class="sxs-lookup"><span data-stu-id="23625-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="23625-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="23625-123">-Parameters</span></span>
<span data-ttu-id="23625-124">A parancsfájl-művelet paramétereit adja meg.</span><span class="sxs-lookup"><span data-stu-id="23625-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="23625-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="23625-125">-PersistOnSuccess</span></span>
<span data-ttu-id="23625-126">Azt jelzi, hogy a parancsfájl-műveletnek minden alkalommal futnia kell, amikor a fürt mérete fel van méretezve.</span><span class="sxs-lookup"><span data-stu-id="23625-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="23625-127">Ezt a kapcsoló paramétert figyelmen kívül hagyja a program, ha a parancsprogram-művelet kezdetben meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="23625-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="23625-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23625-128">-ResourceGroupName</span></span>
<span data-ttu-id="23625-129">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="23625-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="23625-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="23625-130">-Uri</span></span>
<span data-ttu-id="23625-131">A parancsfájl-művelet nyilvános URI-ját adja meg (PowerShell- vagy Bash-parancsfájl).</span><span class="sxs-lookup"><span data-stu-id="23625-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="23625-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23625-132">CommonParameters</span></span>
<span data-ttu-id="23625-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23625-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23625-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23625-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23625-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23625-135">INPUTS</span></span>

### <span data-ttu-id="23625-136">System.String</span><span class="sxs-lookup"><span data-stu-id="23625-136">System.String</span></span>

### <span data-ttu-id="23625-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="23625-137">System.Uri</span></span>

### <span data-ttu-id="23625-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span><span class="sxs-lookup"><span data-stu-id="23625-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="23625-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23625-139">OUTPUTS</span></span>

### <span data-ttu-id="23625-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="23625-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="23625-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="23625-141">NOTES</span></span>

## <span data-ttu-id="23625-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23625-142">RELATED LINKS</span></span>

[<span data-ttu-id="23625-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="23625-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


