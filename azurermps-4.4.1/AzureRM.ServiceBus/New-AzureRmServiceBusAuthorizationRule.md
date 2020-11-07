---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: be2b841511669ffa2ac3ffd416fd86072edcfb52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679939"
---
# <span data-ttu-id="fcc5c-101">New-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fcc5c-101">New-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="fcc5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcc5c-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc5c-103">Új engedélyezési szabály létrehozása a megadott szolgáltatás-buszhoz megadott névtérhez, illetve a várólistához vagy a témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="fcc5c-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcc5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcc5c-104">SYNTAX</span></span>

### <span data-ttu-id="fcc5c-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fcc5c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcc5c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fcc5c-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcc5c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fcc5c-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcc5c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcc5c-108">DESCRIPTION</span></span>
<span data-ttu-id="fcc5c-109">A **New-AzureRmServiceBusAuthorizationRule** parancsmag új engedélyezési szabályt hoz létre a megadott szolgáltatási busz névteréhez, illetve a várólistához vagy a témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="fcc5c-109">The **New-AzureRmServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="fcc5c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fcc5c-110">EXAMPLES</span></span>

### <span data-ttu-id="fcc5c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fcc5c-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="fcc5c-112">`AuthoRule1`A névtér **figyelési** és **küldési** jogosultságait hozza létre `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="fcc5c-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="fcc5c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fcc5c-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="fcc5c-114">`AuthoRule1`A várólista **figyelési** és **küldési** jogainak létrehozása `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="fcc5c-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="fcc5c-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="fcc5c-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="fcc5c-116">`AuthoRule1`A cikk a téma **figyelése** és **küldése** című témakört hozza létre `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="fcc5c-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="fcc5c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcc5c-117">PARAMETERS</span></span>

### <span data-ttu-id="fcc5c-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fcc5c-118">-Confirm</span></span>
<span data-ttu-id="fcc5c-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fcc5c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcc5c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fcc5c-120">-Name</span></span>
<span data-ttu-id="fcc5c-121">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="fcc5c-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="fcc5c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fcc5c-122">-Namespace</span></span>
<span data-ttu-id="fcc5c-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="fcc5c-123">Namespace Name.</span></span>

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

### <span data-ttu-id="fcc5c-124">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="fcc5c-124">-Queue</span></span>
<span data-ttu-id="fcc5c-125">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="fcc5c-125">Queue Name.</span></span>

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

### <span data-ttu-id="fcc5c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc5c-126">-ResourceGroupName</span></span>
<span data-ttu-id="fcc5c-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fcc5c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcc5c-128">– Jogok</span><span class="sxs-lookup"><span data-stu-id="fcc5c-128">-Rights</span></span>
<span data-ttu-id="fcc5c-129">Jogok (például "Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="fcc5c-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="fcc5c-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="fcc5c-130">-Topic</span></span>
<span data-ttu-id="fcc5c-131">A téma neve</span><span class="sxs-lookup"><span data-stu-id="fcc5c-131">Topic Name.</span></span>

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

### <span data-ttu-id="fcc5c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcc5c-132">-WhatIf</span></span>
<span data-ttu-id="fcc5c-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fcc5c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcc5c-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fcc5c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcc5c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc5c-135">-DefaultProfile</span></span>
<span data-ttu-id="fcc5c-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcc5c-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcc5c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc5c-137">CommonParameters</span></span>
<span data-ttu-id="fcc5c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcc5c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc5c-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc5c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc5c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcc5c-140">INPUTS</span></span>

### <span data-ttu-id="fcc5c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fcc5c-141">System.String</span></span>
<span data-ttu-id="fcc5c-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="fcc5c-142">System.String[]</span></span>

## <span data-ttu-id="fcc5c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcc5c-143">OUTPUTS</span></span>

### <span data-ttu-id="fcc5c-144">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fcc5c-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="fcc5c-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcc5c-145">NOTES</span></span>

## <span data-ttu-id="fcc5c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcc5c-146">RELATED LINKS</span></span>

