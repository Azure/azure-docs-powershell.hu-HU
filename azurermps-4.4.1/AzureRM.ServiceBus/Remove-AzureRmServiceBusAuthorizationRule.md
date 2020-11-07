---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 7722ee1a84aee6ef16642a84ac9f72f259d9772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672408"
---
# <span data-ttu-id="1ad42-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ad42-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="1ad42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ad42-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad42-103">A megadott erőforráscsoport engedélyezési szabályát távolítja el a szolgáltatási busz névteréről vagy egy várólistáról vagy témáról.</span><span class="sxs-lookup"><span data-stu-id="1ad42-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ad42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ad42-104">SYNTAX</span></span>

### <span data-ttu-id="1ad42-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ad42-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1ad42-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ad42-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Queue] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1ad42-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ad42-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Topic] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1ad42-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ad42-108">DESCRIPTION</span></span>
<span data-ttu-id="1ad42-109">A **Remove-AzureRmServiceBusAuthorizationRule** parancsmag eltávolítja a megadott erőforráscsoport szolgáltatási busz-névtérének és-várólistájának engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="1ad42-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="1ad42-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1ad42-110">EXAMPLES</span></span>

### <span data-ttu-id="1ad42-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1ad42-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```
<span data-ttu-id="1ad42-112">Eltávolítja a `SBAuthoRule1` megadott erőforráscsoport névterének engedélyezési szabályát `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="1ad42-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="1ad42-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1ad42-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```
<span data-ttu-id="1ad42-114">A megadott erőforráscsoport várólistájának engedélyezési szabályát távolítja `SBAuthoRule1` `SBQueue` el.</span><span class="sxs-lookup"><span data-stu-id="1ad42-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="1ad42-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="1ad42-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```
<span data-ttu-id="1ad42-116">Eltávolítja a témakör engedélyezési szabályát `SBAuthoRule1` `SBTopic` a megadott erőforráscsoport közül.</span><span class="sxs-lookup"><span data-stu-id="1ad42-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="1ad42-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ad42-117">PARAMETERS</span></span>

### <span data-ttu-id="1ad42-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ad42-118">-Confirm</span></span>
<span data-ttu-id="1ad42-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ad42-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad42-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1ad42-120">-Force</span></span>
<span data-ttu-id="1ad42-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ad42-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1ad42-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ad42-122">-Name</span></span>
<span data-ttu-id="1ad42-123">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="1ad42-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="1ad42-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1ad42-124">-Namespace</span></span>
<span data-ttu-id="1ad42-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="1ad42-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad42-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ad42-126">-PassThru</span></span>
<span data-ttu-id="1ad42-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1ad42-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1ad42-128">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="1ad42-128">-Queue</span></span>
<span data-ttu-id="1ad42-129">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="1ad42-129">Queue Name.</span></span>

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

### <span data-ttu-id="1ad42-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad42-130">-ResourceGroupName</span></span>
<span data-ttu-id="1ad42-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1ad42-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="1ad42-132">-Topic</span><span class="sxs-lookup"><span data-stu-id="1ad42-132">-Topic</span></span>
<span data-ttu-id="1ad42-133">A téma neve</span><span class="sxs-lookup"><span data-stu-id="1ad42-133">Topic Name.</span></span>

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

### <span data-ttu-id="1ad42-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad42-134">-WhatIf</span></span>
<span data-ttu-id="1ad42-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ad42-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad42-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ad42-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="1ad42-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ad42-137">INPUTS</span></span>

### <span data-ttu-id="1ad42-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1ad42-138">System.String</span></span>


## <span data-ttu-id="1ad42-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ad42-139">OUTPUTS</span></span>

### <span data-ttu-id="1ad42-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ad42-140">System.Boolean</span></span>


## <span data-ttu-id="1ad42-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ad42-141">NOTES</span></span>

## <span data-ttu-id="1ad42-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ad42-142">RELATED LINKS</span></span>

