---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503940"
---
# <span data-ttu-id="71a19-101">Set-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="71a19-101">Set-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="71a19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71a19-102">SYNOPSIS</span></span>
<span data-ttu-id="71a19-103">Frissíti a megadott engedélyezési szabály leírását a megadott szolgáltatási busz várólistájában.</span><span class="sxs-lookup"><span data-stu-id="71a19-103">Updates the specified authorization rule description for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71a19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71a19-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71a19-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71a19-105">DESCRIPTION</span></span>
<span data-ttu-id="71a19-106">A **set-AzureRmServiceBusQueueAuthorizationRule** parancsmag frissíti a megadott Service Bus-várólista megadott engedélyezési szabályának leírását.</span><span class="sxs-lookup"><span data-stu-id="71a19-106">The **Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus queue.</span></span>

## <span data-ttu-id="71a19-107">Példák</span><span class="sxs-lookup"><span data-stu-id="71a19-107">EXAMPLES</span></span>

### <span data-ttu-id="71a19-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="71a19-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="71a19-109">A várólista engedélyezési szabályának elérési jogát hozzáadja a **kezeléshez** `SBAuthoRule1` `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="71a19-109">Adds **Manage** to the access rights of the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="71a19-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71a19-110">PARAMETERS</span></span>

### <span data-ttu-id="71a19-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="71a19-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="71a19-112">Az engedélyezési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="71a19-112">The authorization rule name.</span></span> <span data-ttu-id="71a19-113">Kötelező, ha **-AuthruleObj** nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="71a19-113">Required if **-AuthruleObj** is not specified.</span></span>

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

### <span data-ttu-id="71a19-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="71a19-114">-AuthRuleObj</span></span>
<span data-ttu-id="71a19-115">A szolgáltatás busz várólista-engedélyezési szabály objektuma.</span><span class="sxs-lookup"><span data-stu-id="71a19-115">The Service Bus queue authorization rule object.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a19-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="71a19-116">-NamespaceName</span></span>
<span data-ttu-id="71a19-117">A szolgáltatás Buszjának névtér neve.</span><span class="sxs-lookup"><span data-stu-id="71a19-117">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="71a19-118">-QueueName</span><span class="sxs-lookup"><span data-stu-id="71a19-118">-QueueName</span></span>
<span data-ttu-id="71a19-119">A szolgáltatás Buszjának várólista neve.</span><span class="sxs-lookup"><span data-stu-id="71a19-119">The Service Bus queue name.</span></span>

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

### <span data-ttu-id="71a19-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71a19-120">-ResourceGroup</span></span>
<span data-ttu-id="71a19-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71a19-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="71a19-122">– Jogok</span><span class="sxs-lookup"><span data-stu-id="71a19-122">-Rights</span></span>
<span data-ttu-id="71a19-123">A jogok; például @ ("Figyelj", "Küldés", "kezelés").</span><span class="sxs-lookup"><span data-stu-id="71a19-123">The rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="71a19-124">Kötelező, ha a "AuthruleObj" nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="71a19-124">Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a19-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71a19-125">-Confirm</span></span>
<span data-ttu-id="71a19-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71a19-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a19-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a19-127">-WhatIf</span></span>
<span data-ttu-id="71a19-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71a19-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71a19-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71a19-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a19-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a19-130">CommonParameters</span></span>
<span data-ttu-id="71a19-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71a19-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a19-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71a19-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a19-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71a19-133">INPUTS</span></span>

### <span data-ttu-id="71a19-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71a19-134">-ResourceGroup</span></span>
 <span data-ttu-id="71a19-135">System. String</span><span class="sxs-lookup"><span data-stu-id="71a19-135">System.String</span></span>

### <span data-ttu-id="71a19-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="71a19-136">-NamespaceName</span></span>
 <span data-ttu-id="71a19-137">System. String</span><span class="sxs-lookup"><span data-stu-id="71a19-137">System.String</span></span>

### <span data-ttu-id="71a19-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="71a19-138">-QueueName</span></span>
 <span data-ttu-id="71a19-139">System. String</span><span class="sxs-lookup"><span data-stu-id="71a19-139">System.String</span></span>

### <span data-ttu-id="71a19-140">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="71a19-140">-AuthRuleObj</span></span>
 <span data-ttu-id="71a19-141">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="71a19-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="71a19-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71a19-142">OUTPUTS</span></span>

### <span data-ttu-id="71a19-143">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="71a19-143">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="71a19-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71a19-144">NOTES</span></span>

## <span data-ttu-id="71a19-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71a19-145">RELATED LINKS</span></span>

