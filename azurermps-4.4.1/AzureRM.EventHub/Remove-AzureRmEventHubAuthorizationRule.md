---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505003"
---
# <span data-ttu-id="013d2-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="013d2-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="013d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="013d2-102">SYNOPSIS</span></span>
<span data-ttu-id="013d2-103">Eltávolítja a megadott esemény központi engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="013d2-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="013d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="013d2-104">SYNTAX</span></span>

### <span data-ttu-id="013d2-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="013d2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="013d2-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="013d2-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="013d2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="013d2-107">DESCRIPTION</span></span>
<span data-ttu-id="013d2-108">A Remove-AzureRmEventHubAuthorizationRule parancsmag eltávolítja és törli a megadott engedélyezési szabályt az esemény központból.</span><span class="sxs-lookup"><span data-stu-id="013d2-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="013d2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="013d2-109">EXAMPLES</span></span>

### <span data-ttu-id="013d2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="013d2-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="013d2-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="013d2-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="013d2-112">Eltávolítja az MyAuthRuleName-as engedélyezési szabályt \` \` az esemény központi \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="013d2-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="013d2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="013d2-113">PARAMETERS</span></span>

### <span data-ttu-id="013d2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="013d2-114">-ResourceGroupName</span></span>
<span data-ttu-id="013d2-115">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="013d2-115">Resource group name.</span></span>

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

### <span data-ttu-id="013d2-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="013d2-116">-Confirm</span></span>
<span data-ttu-id="013d2-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="013d2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="013d2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="013d2-118">-WhatIf</span></span>
<span data-ttu-id="013d2-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="013d2-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="013d2-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="013d2-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="013d2-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="013d2-121">-EventHub</span></span>
<span data-ttu-id="013d2-122">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="013d2-122">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="013d2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="013d2-123">-Force</span></span>
<span data-ttu-id="013d2-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="013d2-124">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="013d2-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="013d2-125">-Name</span></span>
<span data-ttu-id="013d2-126">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="013d2-126">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="013d2-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="013d2-127">-Namespace</span></span>
<span data-ttu-id="013d2-128">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="013d2-128">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="013d2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="013d2-129">-PassThru</span></span>
<span data-ttu-id="013d2-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="013d2-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="013d2-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="013d2-131">INPUTS</span></span>

### <span data-ttu-id="013d2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="013d2-132">System.String</span></span>

## <span data-ttu-id="013d2-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="013d2-133">OUTPUTS</span></span>

### <span data-ttu-id="013d2-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="013d2-134">System.Boolean</span></span>

## <span data-ttu-id="013d2-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="013d2-135">NOTES</span></span>

## <span data-ttu-id="013d2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="013d2-136">RELATED LINKS</span></span>

