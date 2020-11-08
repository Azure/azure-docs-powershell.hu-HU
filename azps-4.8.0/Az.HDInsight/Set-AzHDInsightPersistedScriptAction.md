---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: bff21d969a88282f3ba3c1d79d1f717c3c169265
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025328"
---
# <span data-ttu-id="1c6f0-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="1c6f0-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="1c6f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c6f0-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6f0-103">Egy korábban futtatott parancsfájlt egy állandó parancsfájl-műveletre állítja be.</span><span class="sxs-lookup"><span data-stu-id="1c6f0-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="1c6f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c6f0-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c6f0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c6f0-105">DESCRIPTION</span></span>
<span data-ttu-id="1c6f0-106">A **set-AzHDInsightPersistedScriptAction** parancsmag egy korábban végrehajtott parancsfájlt állít be egy állandó parancsfájl-műveletre.</span><span class="sxs-lookup"><span data-stu-id="1c6f0-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="1c6f0-107">A megadott parancsfájl-műveletnek korábban sikerültnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1c6f0-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="1c6f0-108">A parancsfájl-műveletek akkor futnak, amikor az Azure HDInsight-fürtöt átméretezi.</span><span class="sxs-lookup"><span data-stu-id="1c6f0-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="1c6f0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1c6f0-109">EXAMPLES</span></span>

### <span data-ttu-id="1c6f0-110">1. példa: a korábban sikeres parancsfájl beállítása állandó, vagy a fürtök léptékének beállítása</span><span class="sxs-lookup"><span data-stu-id="1c6f0-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="1c6f0-111">Ez a parancs egy korábban sikeres parancsfájlt állít be állandó parancsfájlként.</span><span class="sxs-lookup"><span data-stu-id="1c6f0-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="1c6f0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c6f0-112">PARAMETERS</span></span>

### <span data-ttu-id="1c6f0-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="1c6f0-113">-ClusterName</span></span>
<span data-ttu-id="1c6f0-114">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c6f0-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="1c6f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6f0-115">-DefaultProfile</span></span>
<span data-ttu-id="1c6f0-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1c6f0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c6f0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c6f0-117">-ResourceGroupName</span></span>
<span data-ttu-id="1c6f0-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c6f0-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1c6f0-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="1c6f0-119">-ScriptExecutionId</span></span>
<span data-ttu-id="1c6f0-120">Annak a parancsfájl-végrehajtásnak a végrehajtási AZONOSÍTÓját adja meg, amely elősegíti a kimaradt állapotot.</span><span class="sxs-lookup"><span data-stu-id="1c6f0-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="1c6f0-121">Ehhez a parancsfájl-művelethez sikeresnek kell lennie ahhoz, hogy előléptetni lehessen.</span><span class="sxs-lookup"><span data-stu-id="1c6f0-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="1c6f0-122">A parancsfájl-végrehajtás AZONOSÍTÓját a Get-AzHDInsightScriptActionHistory használatával találja.</span><span class="sxs-lookup"><span data-stu-id="1c6f0-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="1c6f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6f0-123">CommonParameters</span></span>
<span data-ttu-id="1c6f0-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c6f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6f0-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c6f0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6f0-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c6f0-126">INPUTS</span></span>

### <span data-ttu-id="1c6f0-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="1c6f0-127">None</span></span>

## <span data-ttu-id="1c6f0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c6f0-128">OUTPUTS</span></span>

### <span data-ttu-id="1c6f0-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="1c6f0-129">System.Void</span></span>

## <span data-ttu-id="1c6f0-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c6f0-130">NOTES</span></span>

## <span data-ttu-id="1c6f0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c6f0-131">RELATED LINKS</span></span>

[<span data-ttu-id="1c6f0-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="1c6f0-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="1c6f0-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="1c6f0-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


