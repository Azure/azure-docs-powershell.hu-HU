---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: cfa99107875940854b9ad9c74061ec717a16c51e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835982"
---
# <span data-ttu-id="fd76c-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="fd76c-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="fd76c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd76c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd76c-103">Állandó parancsfájl-művelet eltávolítása egy HDInsight-fürtről.</span><span class="sxs-lookup"><span data-stu-id="fd76c-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="fd76c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd76c-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd76c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd76c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd76c-106">A **Remove-AzHDInsightPersistedScriptAction** parancsmag egy állandó parancsfájl-műveletet távolít el a megadott Azure HDInsight-fürtök listájából, amely állandó parancsfájl-műveletekből áll.</span><span class="sxs-lookup"><span data-stu-id="fd76c-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="fd76c-107">Az eltávolított parancsfájl már nem fog megjelenni a fürt skálázásakor.</span><span class="sxs-lookup"><span data-stu-id="fd76c-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="fd76c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fd76c-108">EXAMPLES</span></span>

### <span data-ttu-id="fd76c-109">1. példa: parancsfájl-művelet eltávolítása a kitartott parancsfájl-műveletek listájáról a fürtökön</span><span class="sxs-lookup"><span data-stu-id="fd76c-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="fd76c-110">A parancs eltávolítja a Scriptaction nevű parancsfájl-műveletet a megadott fürt állandó parancsfájl-műveleteinek listájából.</span><span class="sxs-lookup"><span data-stu-id="fd76c-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="fd76c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd76c-111">PARAMETERS</span></span>

### <span data-ttu-id="fd76c-112">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="fd76c-112">-ClusterName</span></span>
<span data-ttu-id="fd76c-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd76c-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="fd76c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd76c-114">-DefaultProfile</span></span>
<span data-ttu-id="fd76c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fd76c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd76c-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd76c-116">-Name</span></span>
<span data-ttu-id="fd76c-117">Itt adhatja meg az eltávolítani kívánt állandó parancsfájl nevét.</span><span class="sxs-lookup"><span data-stu-id="fd76c-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="fd76c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd76c-118">-ResourceGroupName</span></span>
<span data-ttu-id="fd76c-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd76c-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fd76c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd76c-120">CommonParameters</span></span>
<span data-ttu-id="fd76c-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd76c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd76c-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd76c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd76c-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd76c-123">INPUTS</span></span>

### <span data-ttu-id="fd76c-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="fd76c-124">None</span></span>

## <span data-ttu-id="fd76c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd76c-125">OUTPUTS</span></span>

### <span data-ttu-id="fd76c-126">System. Void</span><span class="sxs-lookup"><span data-stu-id="fd76c-126">System.Void</span></span>

## <span data-ttu-id="fd76c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd76c-127">NOTES</span></span>

## <span data-ttu-id="fd76c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd76c-128">RELATED LINKS</span></span>

[<span data-ttu-id="fd76c-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="fd76c-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="fd76c-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="fd76c-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


