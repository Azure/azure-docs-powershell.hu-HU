---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3085479125219450368322ddb64fee4c06cdce2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679087"
---
# <span data-ttu-id="60e02-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="60e02-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="60e02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60e02-102">SYNOPSIS</span></span>
<span data-ttu-id="60e02-103">Új esemény-hubok engedélyezési szabályának létrehozása a névtérhez vagy a eventhub.</span><span class="sxs-lookup"><span data-stu-id="60e02-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60e02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60e02-104">SYNTAX</span></span>

### <span data-ttu-id="60e02-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60e02-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 -Rights <String[]> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="60e02-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="60e02-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> -Rights <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="60e02-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="60e02-107">DESCRIPTION</span></span>
<span data-ttu-id="60e02-108">Az New-AzureRmEventHubAuthorizationRule parancsmag új esemény-hubok engedélyezési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="60e02-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="60e02-109">Példák</span><span class="sxs-lookup"><span data-stu-id="60e02-109">EXAMPLES</span></span>

### <span data-ttu-id="60e02-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="60e02-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="60e02-111">Létrehoz egy engedélyezési szabályt \` \` , amely megadhatja a MyAuthRuleName, amely figyeli és elküldi a jogosultságokat a névtér \` MyNamespaceName \` , az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="60e02-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="60e02-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="60e02-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="60e02-113">Létrehoz egy engedélyezési szabályt \` \` , amely megadhatja a MyAuthRuleName, amely figyeli és elküldi a jogosultságokat az esemény központi \` MyEventHubName a \` MyNamespaceName névtér- \` \` , az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="60e02-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="60e02-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60e02-114">PARAMETERS</span></span>

### <span data-ttu-id="60e02-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60e02-115">-ResourceGroupName</span></span>
<span data-ttu-id="60e02-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="60e02-116">Resource group name.</span></span>

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

### <span data-ttu-id="60e02-117">– Jogok</span><span class="sxs-lookup"><span data-stu-id="60e02-117">-Rights</span></span>
<span data-ttu-id="60e02-118">Tartalomvédelmi például @ ("Figyelj", "Küldés", "kezelés").</span><span class="sxs-lookup"><span data-stu-id="60e02-118">Rights; for example @("Listen","Send","Manage").</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60e02-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60e02-119">-Confirm</span></span>
<span data-ttu-id="60e02-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60e02-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e02-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e02-121">-WhatIf</span></span>
<span data-ttu-id="60e02-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60e02-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60e02-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60e02-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60e02-124">-EventHub</span><span class="sxs-lookup"><span data-stu-id="60e02-124">-EventHub</span></span>
<span data-ttu-id="60e02-125">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="60e02-125">EventHub Name.</span></span>

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

### <span data-ttu-id="60e02-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60e02-126">-Name</span></span>
<span data-ttu-id="60e02-127">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="60e02-127">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="60e02-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="60e02-128">-Namespace</span></span>
<span data-ttu-id="60e02-129">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="60e02-129">Namespace Name.</span></span>

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

## <span data-ttu-id="60e02-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60e02-130">INPUTS</span></span>

### <span data-ttu-id="60e02-131">System. String</span><span class="sxs-lookup"><span data-stu-id="60e02-131">System.String</span></span>

## <span data-ttu-id="60e02-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60e02-132">OUTPUTS</span></span>

### <span data-ttu-id="60e02-133">Microsoft. Azure. Command. EventHub. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="60e02-133">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="60e02-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60e02-134">NOTES</span></span>

## <span data-ttu-id="60e02-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60e02-135">RELATED LINKS</span></span>

