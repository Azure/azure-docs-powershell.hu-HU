---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505012"
---
# <span data-ttu-id="16358-101">New-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="16358-101">New-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="16358-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16358-102">SYNOPSIS</span></span>
<span data-ttu-id="16358-103">Új engedélyezési szabály létrehozása a megadott névtéren</span><span class="sxs-lookup"><span data-stu-id="16358-103">Creates a new authorization rule on the specified namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16358-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16358-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="16358-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="16358-105">DESCRIPTION</span></span>
<span data-ttu-id="16358-106">A New-AzureRmEventHubNamespaceAuthorizationRule parancsmag új engedélyezési szabályt hoz létre a megadott esemény-hubok névtérben.</span><span class="sxs-lookup"><span data-stu-id="16358-106">The New-AzureRmEventHubNamespaceAuthorizationRule cmdlet creates a new authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="16358-107">Példák</span><span class="sxs-lookup"><span data-stu-id="16358-107">EXAMPLES</span></span>

### <span data-ttu-id="16358-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="16358-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="16358-109">Létrehozza az MyAuthRuleName a \` \` figyelési és küldési jogokkal, az esemény-hubok \` névtér \` -MyNamespaceName az erőforráscsoport- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="16358-109">Creates the authorization rule \`MyAuthRuleName\` with Listen and Send rights, for Event Hubs namespace \`MyNamespaceName\`, in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="16358-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16358-110">PARAMETERS</span></span>

### <span data-ttu-id="16358-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="16358-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="16358-112">Engedélyezési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="16358-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="16358-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="16358-113">-NamespaceName</span></span>
<span data-ttu-id="16358-114">Az esemény hubok névterének neve.</span><span class="sxs-lookup"><span data-stu-id="16358-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="16358-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16358-115">-ResourceGroupName</span></span>
<span data-ttu-id="16358-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="16358-116">Resource group name.</span></span>

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

### <span data-ttu-id="16358-117">– Jogok</span><span class="sxs-lookup"><span data-stu-id="16358-117">-Rights</span></span>
<span data-ttu-id="16358-118">Jogok; például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="16358-118">Rights;for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16358-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="16358-119">-Confirm</span></span>
<span data-ttu-id="16358-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="16358-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16358-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16358-121">-WhatIf</span></span>
<span data-ttu-id="16358-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="16358-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16358-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16358-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="16358-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16358-124">INPUTS</span></span>

### <span data-ttu-id="16358-125">System. String</span><span class="sxs-lookup"><span data-stu-id="16358-125">System.String</span></span>

## <span data-ttu-id="16358-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16358-126">OUTPUTS</span></span>

### <span data-ttu-id="16358-127">Microsoft. Azure. Command. EventHub. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="16358-127">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="16358-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16358-128">NOTES</span></span>

## <span data-ttu-id="16358-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16358-129">RELATED LINKS</span></span>

