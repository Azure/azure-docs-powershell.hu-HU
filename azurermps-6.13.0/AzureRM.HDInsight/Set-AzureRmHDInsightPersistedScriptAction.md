---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 07f501be4ac775a9d80c43173e13fccf3057cc26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493693"
---
# <span data-ttu-id="76b25-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="76b25-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="76b25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76b25-102">SYNOPSIS</span></span>
<span data-ttu-id="76b25-103">Egy korábban futtatott parancsfájlt egy állandó parancsfájl-műveletre állítja be.</span><span class="sxs-lookup"><span data-stu-id="76b25-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76b25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76b25-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76b25-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76b25-105">DESCRIPTION</span></span>
<span data-ttu-id="76b25-106">A **set-AzureRmHDInsightPersistedScriptAction** parancsmag egy korábban végrehajtott parancsfájlt állít be egy állandó parancsfájl-műveletre.</span><span class="sxs-lookup"><span data-stu-id="76b25-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="76b25-107">A megadott parancsfájl-műveletnek korábban sikerültnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="76b25-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="76b25-108">A parancsfájl-műveletek akkor futnak, amikor az Azure HDInsight-fürtöt átméretezi.</span><span class="sxs-lookup"><span data-stu-id="76b25-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="76b25-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76b25-109">EXAMPLES</span></span>

### <span data-ttu-id="76b25-110">1. példa: a korábban sikeres parancsfájl beállítása állandó, vagy a fürtök léptékének beállítása</span><span class="sxs-lookup"><span data-stu-id="76b25-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="76b25-111">Ez a parancs egy korábban sikeres parancsfájlt állít be állandó parancsfájlként.</span><span class="sxs-lookup"><span data-stu-id="76b25-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="76b25-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76b25-112">PARAMETERS</span></span>

### <span data-ttu-id="76b25-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="76b25-113">-ClusterName</span></span>
<span data-ttu-id="76b25-114">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76b25-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="76b25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b25-115">-DefaultProfile</span></span>
<span data-ttu-id="76b25-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="76b25-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76b25-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b25-117">-ResourceGroupName</span></span>
<span data-ttu-id="76b25-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76b25-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="76b25-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="76b25-119">-ScriptExecutionId</span></span>
<span data-ttu-id="76b25-120">Annak a parancsfájl-végrehajtásnak a végrehajtási AZONOSÍTÓját adja meg, amely elősegíti a kimaradt állapotot.</span><span class="sxs-lookup"><span data-stu-id="76b25-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="76b25-121">Ehhez a parancsfájl-művelethez sikeresnek kell lennie ahhoz, hogy előléptetni lehessen.</span><span class="sxs-lookup"><span data-stu-id="76b25-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="76b25-122">A parancsfájl-végrehajtás AZONOSÍTÓját a Get-AzureRmHDInsightScriptActionHistory használatával találja.</span><span class="sxs-lookup"><span data-stu-id="76b25-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="76b25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b25-123">CommonParameters</span></span>
<span data-ttu-id="76b25-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76b25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b25-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76b25-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b25-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76b25-126">INPUTS</span></span>

### <span data-ttu-id="76b25-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="76b25-127">None</span></span>

## <span data-ttu-id="76b25-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76b25-128">OUTPUTS</span></span>

### <span data-ttu-id="76b25-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="76b25-129">System.Void</span></span>

## <span data-ttu-id="76b25-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76b25-130">NOTES</span></span>

## <span data-ttu-id="76b25-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76b25-131">RELATED LINKS</span></span>

[<span data-ttu-id="76b25-132">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="76b25-132">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="76b25-133">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="76b25-133">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


