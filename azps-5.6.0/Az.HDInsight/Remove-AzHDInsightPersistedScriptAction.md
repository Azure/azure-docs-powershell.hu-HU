---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a7c5c9c2008839d4e90dd5f393fbe4acea0f78a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925561"
---
# <span data-ttu-id="43ed3-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="43ed3-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="43ed3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="43ed3-103">Egy megőrzött parancsfájl-műveletet eltávolít egy HDInsight-fürtből.</span><span class="sxs-lookup"><span data-stu-id="43ed3-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="43ed3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43ed3-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43ed3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43ed3-105">DESCRIPTION</span></span>
<span data-ttu-id="43ed3-106">Az **Remove-AzHDInsightPersistedScriptAction parancsmag** eltávolít egy megőrzött parancsfájlműveletet a megadott Azure HDInsight-fürt állandó parancsfájlműveleteinek listájából.</span><span class="sxs-lookup"><span data-stu-id="43ed3-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="43ed3-107">Az eltávolított parancsfájl a továbbiakban nem lesz végrehajtva a fürt méretének felskálakor.</span><span class="sxs-lookup"><span data-stu-id="43ed3-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="43ed3-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43ed3-108">EXAMPLES</span></span>

### <span data-ttu-id="43ed3-109">1. példa: Parancsfájl-művelet eltávolítása a fürtön megőrzött parancsfájlműveletek listájából</span><span class="sxs-lookup"><span data-stu-id="43ed3-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="43ed3-110">Ez a parancs eltávolítja a Scriptaction nevű parancsfájlműveletet a megadott fürt megőrzött parancsfájlműveletei listájából.</span><span class="sxs-lookup"><span data-stu-id="43ed3-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="43ed3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43ed3-111">PARAMETERS</span></span>

### <span data-ttu-id="43ed3-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="43ed3-112">-ClusterName</span></span>
<span data-ttu-id="43ed3-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43ed3-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="43ed3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ed3-114">-DefaultProfile</span></span>
<span data-ttu-id="43ed3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43ed3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43ed3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="43ed3-116">-Name</span></span>
<span data-ttu-id="43ed3-117">Az eltávolítható megőrzött parancsfájl-művelet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43ed3-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="43ed3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ed3-118">-ResourceGroupName</span></span>
<span data-ttu-id="43ed3-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43ed3-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="43ed3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ed3-120">CommonParameters</span></span>
<span data-ttu-id="43ed3-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ed3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ed3-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43ed3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ed3-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43ed3-123">INPUTS</span></span>

### <span data-ttu-id="43ed3-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="43ed3-124">None</span></span>

## <span data-ttu-id="43ed3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43ed3-125">OUTPUTS</span></span>

### <span data-ttu-id="43ed3-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="43ed3-126">System.Void</span></span>

## <span data-ttu-id="43ed3-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43ed3-127">NOTES</span></span>

## <span data-ttu-id="43ed3-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43ed3-128">RELATED LINKS</span></span>

[<span data-ttu-id="43ed3-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="43ed3-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="43ed3-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="43ed3-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


