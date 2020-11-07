---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a980edd1833b37b358f86d2e3ccb6a9efc8d836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673120"
---
# <span data-ttu-id="c978c-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c978c-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="c978c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c978c-102">SYNOPSIS</span></span>
<span data-ttu-id="c978c-103">A megadott engedélyezési szabály törlése az esemény-hubok névtérben.</span><span class="sxs-lookup"><span data-stu-id="c978c-103">Deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c978c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c978c-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c978c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c978c-105">DESCRIPTION</span></span>
<span data-ttu-id="c978c-106">A Remove-AzureRmEventHubNamespaceAuthorizationRule parancsmag eltávolítja és törli a megadott engedélyezési szabályt az adott esemény-hubok névtérben.</span><span class="sxs-lookup"><span data-stu-id="c978c-106">The Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet removes and deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

## <span data-ttu-id="c978c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c978c-107">EXAMPLES</span></span>

### <span data-ttu-id="c978c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c978c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="c978c-109">Eltávolítja az engedélyezési szabályt \` \` a MyAuthRuleName a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="c978c-109">Removes the authorization rule \`MyAuthRuleName\` from the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="c978c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c978c-110">PARAMETERS</span></span>

### <span data-ttu-id="c978c-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="c978c-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="c978c-112">Az esemény-hubok névtér-engedélyezési szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="c978c-112">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c978c-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c978c-113">-NamespaceName</span></span>
<span data-ttu-id="c978c-114">Az esemény hubok névterének neve.</span><span class="sxs-lookup"><span data-stu-id="c978c-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="c978c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c978c-115">-ResourceGroupName</span></span>
<span data-ttu-id="c978c-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c978c-116">Resource group name.</span></span>

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

### <span data-ttu-id="c978c-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c978c-117">-Confirm</span></span>
<span data-ttu-id="c978c-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c978c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c978c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c978c-119">-WhatIf</span></span>
<span data-ttu-id="c978c-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c978c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c978c-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c978c-121">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="c978c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c978c-122">INPUTS</span></span>

### <span data-ttu-id="c978c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c978c-123">System.String</span></span>

## <span data-ttu-id="c978c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c978c-124">OUTPUTS</span></span>

### <span data-ttu-id="c978c-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c978c-125">System.Boolean</span></span>

## <span data-ttu-id="c978c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c978c-126">NOTES</span></span>

## <span data-ttu-id="c978c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c978c-127">RELATED LINKS</span></span>

