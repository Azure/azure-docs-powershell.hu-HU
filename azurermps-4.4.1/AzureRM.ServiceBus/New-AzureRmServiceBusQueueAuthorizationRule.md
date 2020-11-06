---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 098c61be4eaf405d3c3a031601b48f20de1e234a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493357"
---
# <span data-ttu-id="24a38-101">New-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="24a38-101">New-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="24a38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24a38-102">SYNOPSIS</span></span>
<span data-ttu-id="24a38-103">Új engedélyezési szabály létrehozása a megadott szolgáltatás busz várólistájához.</span><span class="sxs-lookup"><span data-stu-id="24a38-103">Creates a new authorization rule for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24a38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24a38-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24a38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24a38-105">DESCRIPTION</span></span>
<span data-ttu-id="24a38-106">A **New-AzureRmServiceBusQueueAuthorizationRule** parancsmag új engedélyezési szabályt hoz létre a megadott szolgáltatási busz várólistához.</span><span class="sxs-lookup"><span data-stu-id="24a38-106">The **New-AzureRmServiceBusQueueAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus queue.</span></span>

## <span data-ttu-id="24a38-107">Példák</span><span class="sxs-lookup"><span data-stu-id="24a38-107">EXAMPLES</span></span>

### <span data-ttu-id="24a38-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24a38-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="24a38-109">Engedélyezési szabályt hoz létre `SBAuthoRule1` a várólistához való **figyelési és küldési** jogosultságokkal `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="24a38-109">Creates authorization rule `SBAuthoRule1` with **Listen and Send** rights for the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="24a38-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24a38-110">PARAMETERS</span></span>

### <span data-ttu-id="24a38-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24a38-111">-ResourceGroup</span></span>
<span data-ttu-id="24a38-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="24a38-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="24a38-113">– Jogok</span><span class="sxs-lookup"><span data-stu-id="24a38-113">-Rights</span></span>
<span data-ttu-id="24a38-114">Megadja a jogosultságokat; például</span><span class="sxs-lookup"><span data-stu-id="24a38-114">Specifies the rights; for example,</span></span>  
<span data-ttu-id="24a38-115">@ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="24a38-115">@("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="24a38-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24a38-116">-Confirm</span></span>
<span data-ttu-id="24a38-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24a38-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24a38-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24a38-118">-WhatIf</span></span>
<span data-ttu-id="24a38-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24a38-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24a38-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24a38-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24a38-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a38-121">-DefaultProfile</span></span>
<span data-ttu-id="24a38-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24a38-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24a38-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24a38-123">-Name</span></span>
<span data-ttu-id="24a38-124">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="24a38-124">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="24a38-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="24a38-125">-Namespace</span></span>
<span data-ttu-id="24a38-126">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="24a38-126">Namespace Name.</span></span>

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

### <span data-ttu-id="24a38-127">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="24a38-127">-Queue</span></span>
<span data-ttu-id="24a38-128">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="24a38-128">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a38-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a38-129">CommonParameters</span></span>
<span data-ttu-id="24a38-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24a38-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a38-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a38-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a38-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a38-132">INPUTS</span></span>

### <span data-ttu-id="24a38-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24a38-133">-ResourceGroup</span></span>
 <span data-ttu-id="24a38-134">System. String</span><span class="sxs-lookup"><span data-stu-id="24a38-134">System.String</span></span>
 

### <span data-ttu-id="24a38-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="24a38-135">-NamespaceName</span></span>
 <span data-ttu-id="24a38-136">System. String</span><span class="sxs-lookup"><span data-stu-id="24a38-136">System.String</span></span>
 

### <span data-ttu-id="24a38-137">-QueueName</span><span class="sxs-lookup"><span data-stu-id="24a38-137">-QueueName</span></span>
 <span data-ttu-id="24a38-138">System. String</span><span class="sxs-lookup"><span data-stu-id="24a38-138">System.String</span></span>
 

### <span data-ttu-id="24a38-139">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="24a38-139">-AuthorizationRuleName</span></span>
 <span data-ttu-id="24a38-140">System. String</span><span class="sxs-lookup"><span data-stu-id="24a38-140">System.String</span></span>

## <span data-ttu-id="24a38-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a38-141">OUTPUTS</span></span>

### <span data-ttu-id="24a38-142">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="24a38-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="24a38-143">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 típus: Microsoft. ServiceBus/AuthorizationRules név: SBAuthoRule1 hely: West US Tags: Rights: {figyelj, küldés}</span><span class="sxs-lookup"><span data-stu-id="24a38-143">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="24a38-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24a38-144">NOTES</span></span>

## <span data-ttu-id="24a38-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24a38-145">RELATED LINKS</span></span>

