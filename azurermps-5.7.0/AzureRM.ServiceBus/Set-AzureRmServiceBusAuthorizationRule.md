---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 3d5c1b6b80ff4d2b046b8a4b23adf7407f680e6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500399"
---
# <span data-ttu-id="d4f19-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4f19-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="d4f19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4f19-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f19-103">Frissíti a megadott engedélyezési szabály leírását a megadott szolgáltatási busz névterében vagy a várólistában.</span><span class="sxs-lookup"><span data-stu-id="d4f19-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4f19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4f19-104">SYNTAX</span></span>

### <span data-ttu-id="d4f19-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4f19-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f19-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4f19-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f19-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4f19-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f19-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4f19-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4f19-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4f19-109">DESCRIPTION</span></span>
<span data-ttu-id="d4f19-110">A **set-AzureRmServiceBusAuthorizationRule** parancsmag frissíti a megadott engedélyezési szabály leírását a megadott szolgáltatási busz névterében vagy a várólistában vagy a témakörben.</span><span class="sxs-lookup"><span data-stu-id="d4f19-110">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="d4f19-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d4f19-111">EXAMPLES</span></span>

### <span data-ttu-id="d4f19-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d4f19-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="d4f19-113">Eltávolítja a **Manage** (névtér) engedélyezési szabályának hozzáférési jogát `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="d4f19-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="d4f19-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="d4f19-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="d4f19-115">Eltávolítja a **kezelés** lehetőséget az engedélyezési szabálynak a várólistában való elérési jogáról `AuthoRule1` `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="d4f19-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="d4f19-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="d4f19-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="d4f19-117">Eltávolítja a **kezelés** lehetőséget a témakör engedélyezési szabályának hozzáférési jogaiból `AuthoRule1` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="d4f19-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="d4f19-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4f19-118">PARAMETERS</span></span>

### <span data-ttu-id="d4f19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f19-119">-DefaultProfile</span></span>
<span data-ttu-id="d4f19-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4f19-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4f19-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4f19-121">-InputObject</span></span>
<span data-ttu-id="d4f19-122">ServiceBus AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="d4f19-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f19-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4f19-123">-Name</span></span>
<span data-ttu-id="d4f19-124">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="d4f19-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="d4f19-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d4f19-125">-Namespace</span></span>
<span data-ttu-id="d4f19-126">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="d4f19-126">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f19-127">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="d4f19-127">-Queue</span></span>
<span data-ttu-id="d4f19-128">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="d4f19-128">Queue Name</span></span>

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

### <span data-ttu-id="d4f19-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f19-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4f19-130">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d4f19-130">Resource Group Name</span></span>

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

### <span data-ttu-id="d4f19-131">– Jogok</span><span class="sxs-lookup"><span data-stu-id="d4f19-131">-Rights</span></span>
<span data-ttu-id="d4f19-132">Jogok, például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="d4f19-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f19-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="d4f19-133">-Topic</span></span>
<span data-ttu-id="d4f19-134">Téma neve</span><span class="sxs-lookup"><span data-stu-id="d4f19-134">Topic Name</span></span>

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

### <span data-ttu-id="d4f19-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4f19-135">-Confirm</span></span>
<span data-ttu-id="d4f19-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4f19-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4f19-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4f19-137">-WhatIf</span></span>
<span data-ttu-id="d4f19-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4f19-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4f19-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4f19-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4f19-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f19-140">CommonParameters</span></span>
<span data-ttu-id="d4f19-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4f19-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d4f19-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4f19-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f19-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4f19-143">INPUTS</span></span>

### <span data-ttu-id="d4f19-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d4f19-144">System.String</span></span>
<span data-ttu-id="d4f19-145">Microsoft. Azure. Command. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes System. string []</span><span class="sxs-lookup"><span data-stu-id="d4f19-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="d4f19-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4f19-146">OUTPUTS</span></span>

### <span data-ttu-id="d4f19-147">Microsoft. Azure. Command. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d4f19-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="d4f19-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4f19-148">NOTES</span></span>

## <span data-ttu-id="d4f19-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4f19-149">RELATED LINKS</span></span>
