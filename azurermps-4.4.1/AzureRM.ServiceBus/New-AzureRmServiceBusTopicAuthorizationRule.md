---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 603eb1363e15b58a324f7131dd986a7c84371a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672409"
---
# <span data-ttu-id="e5b88-101">New-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e5b88-101">New-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="e5b88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5b88-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b88-103">Új engedélyezési szabály létrehozása a megadott szolgáltatás buszhoz című témakörben.</span><span class="sxs-lookup"><span data-stu-id="e5b88-103">Creates a new authorization rule for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5b88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5b88-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5b88-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5b88-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b88-106">A **New-AzureRmServiceBusTopicAuthorizationRule** parancsmag új engedélyezési szabályt hoz létre a megadott buszjárati témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="e5b88-106">The **New-AzureRmServiceBusTopicAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus topic.</span></span>

## <span data-ttu-id="e5b88-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e5b88-107">EXAMPLES</span></span>

### <span data-ttu-id="e5b88-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e5b88-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="e5b88-109">Engedélyezési szabályt hoz létre `SBTopicAuthoRule1` , amelyben a téma **figyelése** és **küldése** jogosultsággal rendelkezik `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="e5b88-109">Creates authorization rule `SBTopicAuthoRule1` with **Listen** and **Send** rights for the topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="e5b88-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5b88-110">PARAMETERS</span></span>

### <span data-ttu-id="e5b88-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5b88-111">-ResourceGroup</span></span>
<span data-ttu-id="e5b88-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e5b88-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="e5b88-113">– Jogok</span><span class="sxs-lookup"><span data-stu-id="e5b88-113">-Rights</span></span>
<span data-ttu-id="e5b88-114">A jogok; például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="e5b88-114">The rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b88-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5b88-115">-Confirm</span></span>
<span data-ttu-id="e5b88-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5b88-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5b88-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5b88-117">-WhatIf</span></span>
<span data-ttu-id="e5b88-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5b88-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5b88-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5b88-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5b88-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b88-120">-DefaultProfile</span></span>
<span data-ttu-id="e5b88-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5b88-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5b88-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5b88-122">-Name</span></span>
<span data-ttu-id="e5b88-123">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="e5b88-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b88-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e5b88-124">-Namespace</span></span>
<span data-ttu-id="e5b88-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="e5b88-125">Namespace Name.</span></span>

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

### <span data-ttu-id="e5b88-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="e5b88-126">-Topic</span></span>
<span data-ttu-id="e5b88-127">A téma neve</span><span class="sxs-lookup"><span data-stu-id="e5b88-127">Topic Name.</span></span>

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

### <span data-ttu-id="e5b88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b88-128">CommonParameters</span></span>
<span data-ttu-id="e5b88-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5b88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b88-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5b88-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b88-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5b88-131">INPUTS</span></span>

### <span data-ttu-id="e5b88-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5b88-132">-ResourceGroup</span></span>
 <span data-ttu-id="e5b88-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e5b88-133">System.String</span></span>
 

### <span data-ttu-id="e5b88-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e5b88-134">-NamespaceName</span></span>
 <span data-ttu-id="e5b88-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e5b88-135">System.String</span></span>
 

### <span data-ttu-id="e5b88-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="e5b88-136">-TopicName</span></span>
 <span data-ttu-id="e5b88-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e5b88-137">System.String</span></span>
 

### <span data-ttu-id="e5b88-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e5b88-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="e5b88-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e5b88-139">System.String</span></span>

## <span data-ttu-id="e5b88-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5b88-140">OUTPUTS</span></span>

### <span data-ttu-id="e5b88-141">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e5b88-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="e5b88-142">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 típus: Microsoft. ServiceBus/AuthorizationRules név: SBTopicAuthoRule1 hely: West US Tags: Rights: {figyelj, küldés}</span><span class="sxs-lookup"><span data-stu-id="e5b88-142">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="e5b88-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5b88-143">NOTES</span></span>

## <span data-ttu-id="e5b88-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5b88-144">RELATED LINKS</span></span>

