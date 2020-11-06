---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: a41ddb9ee845bce0687448d0745904b9cec9ba05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498819"
---
# <span data-ttu-id="5bc7c-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5bc7c-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="5bc7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bc7c-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc7c-103">A megadott erőforráscsoport engedélyezési szabályát távolítja el a szolgáltatási busz névteréről vagy egy várólistáról vagy témáról.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bc7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bc7c-104">SYNTAX</span></span>

### <span data-ttu-id="5bc7c-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5bc7c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc7c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5bc7c-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc7c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5bc7c-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bc7c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bc7c-108">DESCRIPTION</span></span>
<span data-ttu-id="5bc7c-109">A **Remove-AzureRmServiceBusAuthorizationRule** parancsmag eltávolítja a megadott erőforráscsoport szolgáltatási busz-névtérének és-várólistájának engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="5bc7c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5bc7c-110">EXAMPLES</span></span>

### <span data-ttu-id="5bc7c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5bc7c-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="5bc7c-112">Eltávolítja a `SBAuthoRule1` megadott erőforráscsoport névterének engedélyezési szabályát `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="5bc7c-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="5bc7c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5bc7c-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="5bc7c-114">A megadott erőforráscsoport várólistájának engedélyezési szabályát távolítja `SBAuthoRule1` `SBQueue` el.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="5bc7c-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="5bc7c-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="5bc7c-116">Eltávolítja a témakör engedélyezési szabályát `SBAuthoRule1` `SBTopic` a megadott erőforráscsoport közül.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="5bc7c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bc7c-117">PARAMETERS</span></span>

### <span data-ttu-id="5bc7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc7c-118">-DefaultProfile</span></span>
<span data-ttu-id="5bc7c-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc7c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5bc7c-120">-Force</span></span>
<span data-ttu-id="5bc7c-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5bc7c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bc7c-122">-InputObject</span></span>
<span data-ttu-id="5bc7c-123">ServiceBus AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="5bc7c-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc7c-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5bc7c-124">-Name</span></span>
<span data-ttu-id="5bc7c-125">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="5bc7c-125">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc7c-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5bc7c-126">-Namespace</span></span>
<span data-ttu-id="5bc7c-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="5bc7c-127">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc7c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bc7c-128">-PassThru</span></span>
<span data-ttu-id="5bc7c-129">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5bc7c-130">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5bc7c-131">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="5bc7c-131">-Queue</span></span>
<span data-ttu-id="5bc7c-132">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="5bc7c-132">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc7c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc7c-133">-ResourceGroupName</span></span>
<span data-ttu-id="5bc7c-134">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5bc7c-134">Resource Group Name</span></span>

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

### <span data-ttu-id="5bc7c-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="5bc7c-135">-Topic</span></span>
<span data-ttu-id="5bc7c-136">Téma neve</span><span class="sxs-lookup"><span data-stu-id="5bc7c-136">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc7c-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5bc7c-137">-Confirm</span></span>
<span data-ttu-id="5bc7c-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc7c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bc7c-139">-WhatIf</span></span>
<span data-ttu-id="5bc7c-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bc7c-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bc7c-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc7c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc7c-142">CommonParameters</span></span>
<span data-ttu-id="5bc7c-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bc7c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5bc7c-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bc7c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc7c-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bc7c-145">INPUTS</span></span>

### <span data-ttu-id="5bc7c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5bc7c-146">System.String</span></span>
<span data-ttu-id="5bc7c-147">Microsoft. Azure. Command. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5bc7c-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="5bc7c-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bc7c-148">OUTPUTS</span></span>

### <span data-ttu-id="5bc7c-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5bc7c-149">System.Boolean</span></span>


## <span data-ttu-id="5bc7c-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bc7c-150">NOTES</span></span>

## <span data-ttu-id="5bc7c-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bc7c-151">RELATED LINKS</span></span>
