---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 22904260488c716ffb702f47442dc8f4678ebe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505004"
---
# <span data-ttu-id="9ec67-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="9ec67-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="9ec67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ec67-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec67-103">Eltávolítja a megadott esemény hub-ot.</span><span class="sxs-lookup"><span data-stu-id="9ec67-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ec67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ec67-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9ec67-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ec67-105">DESCRIPTION</span></span>
<span data-ttu-id="9ec67-106">A Remove-AzureRmEventHub parancsmag eltávolítja és törli a megadott névtérből a megadott esemény középpontját.</span><span class="sxs-lookup"><span data-stu-id="9ec67-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="9ec67-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9ec67-107">EXAMPLES</span></span>

### <span data-ttu-id="9ec67-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ec67-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="9ec67-109">Eltávolítja az esemény-hub \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="9ec67-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="9ec67-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ec67-110">PARAMETERS</span></span>

### <span data-ttu-id="9ec67-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec67-111">-ResourceGroupName</span></span>
<span data-ttu-id="9ec67-112">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9ec67-112">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec67-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ec67-113">-Confirm</span></span>
<span data-ttu-id="9ec67-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9ec67-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec67-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ec67-115">-WhatIf</span></span>
<span data-ttu-id="9ec67-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ec67-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ec67-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ec67-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec67-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ec67-118">-Name</span></span>
<span data-ttu-id="9ec67-119">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="9ec67-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec67-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9ec67-120">-Namespace</span></span>
<span data-ttu-id="9ec67-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="9ec67-121">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="9ec67-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ec67-122">INPUTS</span></span>

### <span data-ttu-id="9ec67-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9ec67-123">System.String</span></span>

## <span data-ttu-id="9ec67-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ec67-124">OUTPUTS</span></span>

### <span data-ttu-id="9ec67-125">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="9ec67-125">System.Object</span></span>

## <span data-ttu-id="9ec67-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ec67-126">NOTES</span></span>

## <span data-ttu-id="9ec67-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ec67-127">RELATED LINKS</span></span>

