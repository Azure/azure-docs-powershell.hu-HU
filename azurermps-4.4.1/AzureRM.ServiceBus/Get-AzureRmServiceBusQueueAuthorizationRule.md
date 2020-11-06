---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 5d3f9212fcaf55d6506723b6c29ed1da0d676bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494691"
---
# <span data-ttu-id="ddad6-101">Get-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ddad6-101">Get-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="ddad6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddad6-102">SYNOPSIS</span></span>
<span data-ttu-id="ddad6-103">Egy adott szolgáltatási busz várólistára vonatkozó meghatározott engedélyezési szabály leírását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ddad6-103">Gets the description of a specified authorization rule for a given Service Bus queue.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddad6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddad6-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddad6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddad6-105">DESCRIPTION</span></span>
<span data-ttu-id="ddad6-106">A **Get-AzureRmServiceBusQueueAuthorizationRule** parancsmag a megadott szolgáltatási busz várólistán megadott engedélyezési szabály leírását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ddad6-106">The **Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet gets the description of a specified authorization rule on the given Service Bus queue.</span></span>

## <span data-ttu-id="ddad6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ddad6-107">EXAMPLES</span></span>

### <span data-ttu-id="ddad6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ddad6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="ddad6-109">A megadott engedélyezési szabály leírását adja meg egy adott szolgáltatási busz várólistájában.</span><span class="sxs-lookup"><span data-stu-id="ddad6-109">Returns the specified authorization rule description for a given Service Bus queue.</span></span>

## <span data-ttu-id="ddad6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddad6-110">PARAMETERS</span></span>

### <span data-ttu-id="ddad6-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddad6-111">-ResourceGroup</span></span>
<span data-ttu-id="ddad6-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ddad6-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="ddad6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddad6-113">-DefaultProfile</span></span>
<span data-ttu-id="ddad6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddad6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddad6-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ddad6-115">-Name</span></span>
<span data-ttu-id="ddad6-116">EventHub AuthorizationRule név.</span><span class="sxs-lookup"><span data-stu-id="ddad6-116">EventHub AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="ddad6-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ddad6-117">-Namespace</span></span>
<span data-ttu-id="ddad6-118">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ddad6-118">Namespace Name.</span></span>

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

### <span data-ttu-id="ddad6-119">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="ddad6-119">-Queue</span></span>
<span data-ttu-id="ddad6-120">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="ddad6-120">Queue Name.</span></span>

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

### <span data-ttu-id="ddad6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddad6-121">CommonParameters</span></span>
<span data-ttu-id="ddad6-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddad6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddad6-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddad6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddad6-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddad6-124">INPUTS</span></span>

### <span data-ttu-id="ddad6-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddad6-125">-ResourceGroup</span></span>
 <span data-ttu-id="ddad6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ddad6-126">System.String</span></span>
 

### <span data-ttu-id="ddad6-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ddad6-127">-NamespaceName</span></span>
 <span data-ttu-id="ddad6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ddad6-128">System.String</span></span>
 

### <span data-ttu-id="ddad6-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="ddad6-129">-QueueName</span></span>
 <span data-ttu-id="ddad6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ddad6-130">System.String</span></span>
 

### <span data-ttu-id="ddad6-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="ddad6-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="ddad6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ddad6-132">System.String</span></span>

## <span data-ttu-id="ddad6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddad6-133">OUTPUTS</span></span>

### <span data-ttu-id="ddad6-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ddad6-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ddad6-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 típus: Microsoft. ServiceBus/AuthorizationRules név: SBAuthoRule1 hely: West US Tags: Rights: {figyelj, küldés}</span><span class="sxs-lookup"><span data-stu-id="ddad6-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="ddad6-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddad6-136">NOTES</span></span>

## <span data-ttu-id="ddad6-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddad6-137">RELATED LINKS</span></span>

