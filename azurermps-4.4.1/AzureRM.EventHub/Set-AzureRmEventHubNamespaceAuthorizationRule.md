---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505948"
---
# <span data-ttu-id="0c783-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0c783-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="0c783-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c783-102">SYNOPSIS</span></span>
<span data-ttu-id="0c783-103">Frissíti az engedélyezési szabályt a megadott esemény-hubok névtérben.</span><span class="sxs-lookup"><span data-stu-id="0c783-103">Updates the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c783-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c783-104">SYNTAX</span></span>

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0c783-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c783-105">DESCRIPTION</span></span>
<span data-ttu-id="0c783-106">Az Set-AzureRmEventHubNamespaceAuthorizationRule parancsmag a megadott esemény-hubok névtérben frissíti az engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="0c783-106">The Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet updates the authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="0c783-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0c783-107">EXAMPLES</span></span>

### <span data-ttu-id="0c783-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0c783-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="0c783-109">Frissíti az MyAuthRuleName engedélyezési szabályát \` \` .</span><span class="sxs-lookup"><span data-stu-id="0c783-109">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights.</span></span>

## <span data-ttu-id="0c783-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c783-110">PARAMETERS</span></span>

### <span data-ttu-id="0c783-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="0c783-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="0c783-112">Az engedélyezési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="0c783-112">The authorization rule name.</span></span>
<span data-ttu-id="0c783-113">Kötelező, ha-AuthruleObj nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="0c783-113">Required if -AuthruleObj is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c783-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="0c783-114">-AuthRuleObj</span></span>
<span data-ttu-id="0c783-115">Az esemény-hubok névtér-engedélyezési szabály objektuma.</span><span class="sxs-lookup"><span data-stu-id="0c783-115">The Event Hubs namespace authorization rule object.</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c783-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0c783-116">-NamespaceName</span></span>
<span data-ttu-id="0c783-117">Az esemény hubok névterének neve.</span><span class="sxs-lookup"><span data-stu-id="0c783-117">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="0c783-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c783-118">-ResourceGroupName</span></span>
<span data-ttu-id="0c783-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="0c783-119">Resource group name.</span></span>

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

### <span data-ttu-id="0c783-120">– Jogok</span><span class="sxs-lookup"><span data-stu-id="0c783-120">-Rights</span></span>
<span data-ttu-id="0c783-121">Kötelező, ha-AuthruleObj nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="0c783-121">Required if -AuthruleObj is not specified.</span></span>
<span data-ttu-id="0c783-122">Tartalomvédelmi például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="0c783-122">Rights; for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c783-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c783-123">-Confirm</span></span>
<span data-ttu-id="0c783-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c783-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c783-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c783-125">-WhatIf</span></span>
<span data-ttu-id="0c783-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0c783-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c783-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c783-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="0c783-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c783-128">INPUTS</span></span>

### <span data-ttu-id="0c783-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0c783-129">System.String</span></span>

## <span data-ttu-id="0c783-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c783-130">OUTPUTS</span></span>

### <span data-ttu-id="0c783-131">Microsoft. Azure. Command. EventHub. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0c783-131">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0c783-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c783-132">NOTES</span></span>

## <span data-ttu-id="0c783-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c783-133">RELATED LINKS</span></span>

