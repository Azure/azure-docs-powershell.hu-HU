---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: bbc6c0119f0f8f424b508adc38b5de80cd097734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679936"
---
# <span data-ttu-id="5f2cd-101">Set-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5f2cd-101">Set-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="5f2cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f2cd-102">SYNOPSIS</span></span>
<span data-ttu-id="5f2cd-103">Frissíti a megadott engedélyezési szabály leírását a megadott buszjárattal kapcsolatos témakörben.</span><span class="sxs-lookup"><span data-stu-id="5f2cd-103">Updates the specified authorization rule description for the given Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f2cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f2cd-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f2cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f2cd-105">DESCRIPTION</span></span>
<span data-ttu-id="5f2cd-106">A **set-AzureRmServiceBusTopicAuthorizationRule** parancsmag frissíti a megadott szolgáltatási busz témakörben szereplő engedélyezési szabály leírását.</span><span class="sxs-lookup"><span data-stu-id="5f2cd-106">The **Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus topic.</span></span>

## <span data-ttu-id="5f2cd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5f2cd-107">EXAMPLES</span></span>

### <span data-ttu-id="5f2cd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5f2cd-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="5f2cd-109">A témakörben szereplő engedélyezési **szabály elérési jogát hozzáadja** `SBTopicAuthoRule1` `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="5f2cd-109">Adds **Manage** to the access rights of the authorization rule `SBTopicAuthoRule1` on topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="5f2cd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f2cd-110">PARAMETERS</span></span>

### <span data-ttu-id="5f2cd-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5f2cd-111">-ResourceGroup</span></span>
<span data-ttu-id="5f2cd-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5f2cd-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="5f2cd-113">– Jogok</span><span class="sxs-lookup"><span data-stu-id="5f2cd-113">-Rights</span></span>
<span data-ttu-id="5f2cd-114">Tartalomvédelmi például @ ("Figyelj", "Küldés", "kezelés").</span><span class="sxs-lookup"><span data-stu-id="5f2cd-114">Rights; for example, @("Listen","Send","Manage").</span></span> <span data-ttu-id="5f2cd-115">Kötelező, ha **-AuthruleObj** nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="5f2cd-115">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f2cd-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5f2cd-116">-Confirm</span></span>
<span data-ttu-id="5f2cd-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f2cd-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f2cd-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f2cd-118">-WhatIf</span></span>
<span data-ttu-id="5f2cd-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5f2cd-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f2cd-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f2cd-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f2cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f2cd-121">-DefaultProfile</span></span>
<span data-ttu-id="5f2cd-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f2cd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f2cd-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="5f2cd-123">-InputObj</span></span>
<span data-ttu-id="5f2cd-124">ServiceBus téma AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="5f2cd-124">ServiceBus Topic AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f2cd-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5f2cd-125">-Name</span></span>
<span data-ttu-id="5f2cd-126">AuthorizationRule neve – kötelező, ha a "AuthruleObj" nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="5f2cd-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f2cd-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5f2cd-127">-Namespace</span></span>
<span data-ttu-id="5f2cd-128">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="5f2cd-128">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f2cd-129">-Topic</span><span class="sxs-lookup"><span data-stu-id="5f2cd-129">-Topic</span></span>
<span data-ttu-id="5f2cd-130">A téma neve</span><span class="sxs-lookup"><span data-stu-id="5f2cd-130">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f2cd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f2cd-131">CommonParameters</span></span>
<span data-ttu-id="5f2cd-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f2cd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f2cd-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f2cd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f2cd-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f2cd-134">INPUTS</span></span>

### <span data-ttu-id="5f2cd-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5f2cd-135">-ResourceGroup</span></span>
 <span data-ttu-id="5f2cd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5f2cd-136">System.String</span></span>

### <span data-ttu-id="5f2cd-137">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5f2cd-137">-NamespaceName</span></span>
 <span data-ttu-id="5f2cd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5f2cd-138">System.String</span></span>

### <span data-ttu-id="5f2cd-139">-TopicName</span><span class="sxs-lookup"><span data-stu-id="5f2cd-139">-TopicName</span></span>
 <span data-ttu-id="5f2cd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5f2cd-140">System.String</span></span>

### <span data-ttu-id="5f2cd-141">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="5f2cd-141">-AuthRuleObj</span></span>
 <span data-ttu-id="5f2cd-142">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5f2cd-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5f2cd-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f2cd-143">OUTPUTS</span></span>

### <span data-ttu-id="5f2cd-144">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5f2cd-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="5f2cd-145">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/Authorization szabályok/SBTopicAuthoRule1 típusa: Microsoft. ServiceBus/AuthorizationRules név: SBTopicAuthoRule1 hely: West US Tags: Rights: {figyelj, küldés, kezelés}</span><span class="sxs-lookup"><span data-stu-id="5f2cd-145">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization Rules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send, Manage}</span></span>

## <span data-ttu-id="5f2cd-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f2cd-146">NOTES</span></span>

## <span data-ttu-id="5f2cd-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f2cd-147">RELATED LINKS</span></span>

