---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 62edcb426fe62f834b876b0dd4e2006712f81348
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838044"
---
# <span data-ttu-id="12a04-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="12a04-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="12a04-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12a04-102">SYNOPSIS</span></span>
<span data-ttu-id="12a04-103">Új engedélyezési szabály létrehozása a megadott szolgáltatás-buszhoz megadott névtérhez, illetve a várólistához vagy a témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="12a04-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="12a04-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12a04-104">SYNTAX</span></span>

### <span data-ttu-id="12a04-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12a04-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12a04-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="12a04-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12a04-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="12a04-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12a04-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="12a04-108">DESCRIPTION</span></span>
<span data-ttu-id="12a04-109">A **New-AzServiceBusAuthorizationRule** parancsmag új engedélyezési szabályt hoz létre a megadott szolgáltatási busz névteréhez, illetve a várólistához vagy a témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="12a04-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="12a04-110">Példák</span><span class="sxs-lookup"><span data-stu-id="12a04-110">EXAMPLES</span></span>

### <span data-ttu-id="12a04-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="12a04-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="12a04-112">`AuthoRule1`A névtér **figyelési** és **küldési** jogosultságait hozza létre `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="12a04-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="12a04-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="12a04-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="12a04-114">`AuthoRule1`A várólista **figyelési** és **küldési** jogainak létrehozása `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="12a04-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="12a04-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="12a04-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="12a04-116">`AuthoRule1`A cikk a téma **figyelése** és **küldése** című témakört hozza létre `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="12a04-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="12a04-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12a04-117">PARAMETERS</span></span>

### <span data-ttu-id="12a04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a04-118">-DefaultProfile</span></span>
<span data-ttu-id="12a04-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12a04-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12a04-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12a04-120">-Name</span></span>
<span data-ttu-id="12a04-121">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="12a04-121">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a04-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="12a04-122">-Namespace</span></span>
<span data-ttu-id="12a04-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="12a04-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a04-124">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="12a04-124">-Queue</span></span>
<span data-ttu-id="12a04-125">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="12a04-125">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a04-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a04-126">-ResourceGroupName</span></span>
<span data-ttu-id="12a04-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="12a04-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a04-128">– Jogok</span><span class="sxs-lookup"><span data-stu-id="12a04-128">-Rights</span></span>
<span data-ttu-id="12a04-129">Jogok (például "Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="12a04-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a04-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="12a04-130">-Topic</span></span>
<span data-ttu-id="12a04-131">Téma neve</span><span class="sxs-lookup"><span data-stu-id="12a04-131">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a04-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="12a04-132">-Confirm</span></span>
<span data-ttu-id="12a04-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="12a04-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a04-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12a04-134">-WhatIf</span></span>
<span data-ttu-id="12a04-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="12a04-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12a04-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12a04-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a04-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a04-137">CommonParameters</span></span>
<span data-ttu-id="12a04-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12a04-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a04-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a04-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a04-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12a04-140">INPUTS</span></span>

### <span data-ttu-id="12a04-141">System. String</span><span class="sxs-lookup"><span data-stu-id="12a04-141">System.String</span></span>

### <span data-ttu-id="12a04-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="12a04-142">System.String[]</span></span>

## <span data-ttu-id="12a04-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12a04-143">OUTPUTS</span></span>

### <span data-ttu-id="12a04-144">Microsoft. Azure. Command. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="12a04-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="12a04-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12a04-145">NOTES</span></span>

## <span data-ttu-id="12a04-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12a04-146">RELATED LINKS</span></span>
