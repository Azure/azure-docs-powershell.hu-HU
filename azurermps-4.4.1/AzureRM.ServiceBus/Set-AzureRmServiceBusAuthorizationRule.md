---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 9e4612f8b688181ca54c7fa8414d28e3a444b446
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503952"
---
# <span data-ttu-id="cb0b2-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb0b2-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="cb0b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0b2-103">Frissíti a megadott engedélyezési szabály leírását a megadott szolgáltatási busz névterében vagy a várólistában.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb0b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb0b2-104">SYNTAX</span></span>

### <span data-ttu-id="cb0b2-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb0b2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb0b2-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb0b2-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb0b2-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb0b2-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb0b2-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb0b2-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb0b2-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="cb0b2-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb0b2-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb0b2-110">DESCRIPTION</span></span>
<span data-ttu-id="cb0b2-111">A **set-AzureRmServiceBusAuthorizationRule** parancsmag frissíti a megadott engedélyezési szabály leírását a megadott szolgáltatási busz névterében vagy a várólistában vagy a témakörben.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-111">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="cb0b2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="cb0b2-112">EXAMPLES</span></span>

### <span data-ttu-id="cb0b2-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cb0b2-113">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="cb0b2-114">Eltávolítja a **Manage** (névtér) engedélyezési szabályának hozzáférési jogát `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="cb0b2-114">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="cb0b2-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="cb0b2-115">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="cb0b2-116">Eltávolítja a **kezelés** lehetőséget az engedélyezési szabálynak a várólistában való elérési jogáról `AuthoRule1` `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="cb0b2-116">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="cb0b2-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="cb0b2-117">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="cb0b2-118">Eltávolítja a **kezelés** lehetőséget a témakör engedélyezési szabályának hozzáférési jogaiból `AuthoRule1` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="cb0b2-118">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="cb0b2-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb0b2-119">PARAMETERS</span></span>

### <span data-ttu-id="cb0b2-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb0b2-120">-Confirm</span></span>
<span data-ttu-id="cb0b2-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb0b2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb0b2-122">-InputObject</span></span>
<span data-ttu-id="cb0b2-123">ServiceBus AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="cb0b2-123">ServiceBus AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b2-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb0b2-124">-Name</span></span>
<span data-ttu-id="cb0b2-125">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="cb0b2-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="cb0b2-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cb0b2-126">-Namespace</span></span>
<span data-ttu-id="cb0b2-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="cb0b2-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b2-128">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="cb0b2-128">-Queue</span></span>
<span data-ttu-id="cb0b2-129">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="cb0b2-129">Queue Name.</span></span>

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

### <span data-ttu-id="cb0b2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb0b2-130">-ResourceGroupName</span></span>
<span data-ttu-id="cb0b2-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="cb0b2-132">– Jogok</span><span class="sxs-lookup"><span data-stu-id="cb0b2-132">-Rights</span></span>
<span data-ttu-id="cb0b2-133">Jogok, például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="cb0b2-133">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b2-134">-Topic</span><span class="sxs-lookup"><span data-stu-id="cb0b2-134">-Topic</span></span>
<span data-ttu-id="cb0b2-135">A téma neve</span><span class="sxs-lookup"><span data-stu-id="cb0b2-135">Topic Name.</span></span>

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

### <span data-ttu-id="cb0b2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb0b2-136">-WhatIf</span></span>
<span data-ttu-id="cb0b2-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb0b2-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb0b2-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0b2-139">-DefaultProfile</span></span>
<span data-ttu-id="cb0b2-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb0b2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0b2-141">CommonParameters</span></span>
<span data-ttu-id="cb0b2-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb0b2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0b2-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb0b2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0b2-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb0b2-144">INPUTS</span></span>

### <span data-ttu-id="cb0b2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cb0b2-145">System.String</span></span>
<span data-ttu-id="cb0b2-146">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes System. string []</span><span class="sxs-lookup"><span data-stu-id="cb0b2-146">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes System.String[]</span></span>

## <span data-ttu-id="cb0b2-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb0b2-147">OUTPUTS</span></span>

### <span data-ttu-id="cb0b2-148">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cb0b2-148">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="cb0b2-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb0b2-149">NOTES</span></span>

## <span data-ttu-id="cb0b2-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb0b2-150">RELATED LINKS</span></span>

