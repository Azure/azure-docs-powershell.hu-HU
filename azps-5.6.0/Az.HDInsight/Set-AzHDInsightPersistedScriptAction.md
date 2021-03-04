---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 573bb9534107a4df020e21269b5bdb2ec12db125
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934937"
---
# <span data-ttu-id="5b291-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5b291-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="5b291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b291-102">SYNOPSIS</span></span>
<span data-ttu-id="5b291-103">Egy korábban végrehajtott parancsfájl-műveletet állandó parancsfájl-műveletként állít be.</span><span class="sxs-lookup"><span data-stu-id="5b291-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="5b291-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b291-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b291-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b291-105">DESCRIPTION</span></span>
<span data-ttu-id="5b291-106">A **Set-AzHDInsightPersistedScriptAction parancsmag** egy korábban végrehajtott parancsfájl-műveletet állandó parancsfájl-műveletként állít be.</span><span class="sxs-lookup"><span data-stu-id="5b291-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="5b291-107">A megadott parancsprogram-műveletnek korábban sikeresnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5b291-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="5b291-108">A parancsfájl-művelet minden alkalommal lefut, amikor az Azure HDInsight-fürt mérete fel lesz méretezve.</span><span class="sxs-lookup"><span data-stu-id="5b291-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="5b291-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b291-109">EXAMPLES</span></span>

### <span data-ttu-id="5b291-110">1. példa: A korábban sikeres parancsfájl-művelet állandóként való beállítása vagy a fürtméretarány beállítása</span><span class="sxs-lookup"><span data-stu-id="5b291-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="5b291-111">Ez a parancs egy korábban sikeres parancsfájl-műveletet állandó parancsfájl-műveletként állít be.</span><span class="sxs-lookup"><span data-stu-id="5b291-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="5b291-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b291-112">PARAMETERS</span></span>

### <span data-ttu-id="5b291-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5b291-113">-ClusterName</span></span>
<span data-ttu-id="5b291-114">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b291-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5b291-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b291-115">-DefaultProfile</span></span>
<span data-ttu-id="5b291-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5b291-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b291-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b291-117">-ResourceGroupName</span></span>
<span data-ttu-id="5b291-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b291-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5b291-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="5b291-119">-ScriptExecutionId</span></span>
<span data-ttu-id="5b291-120">Annak a parancsfájl-műveletnek a végrehajtási azonosítóját adja meg, amely állandóra előléptet.</span><span class="sxs-lookup"><span data-stu-id="5b291-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="5b291-121">Ennek a parancsfájl-műveletnek sikeresnek kell lennie ahhoz, hogy előléptetve legyen.</span><span class="sxs-lookup"><span data-stu-id="5b291-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="5b291-122">A parancsfájl-művelet végrehajtási azonosítóját a Get-AzHDInsightScriptActionHistory használatával találhatja meg.</span><span class="sxs-lookup"><span data-stu-id="5b291-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b291-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b291-123">CommonParameters</span></span>
<span data-ttu-id="5b291-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b291-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b291-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b291-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b291-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b291-126">INPUTS</span></span>

### <span data-ttu-id="5b291-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="5b291-127">None</span></span>

## <span data-ttu-id="5b291-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b291-128">OUTPUTS</span></span>

### <span data-ttu-id="5b291-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="5b291-129">System.Void</span></span>

## <span data-ttu-id="5b291-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b291-130">NOTES</span></span>

## <span data-ttu-id="5b291-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b291-131">RELATED LINKS</span></span>

[<span data-ttu-id="5b291-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5b291-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="5b291-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5b291-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


