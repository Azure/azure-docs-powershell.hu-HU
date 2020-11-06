---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: dc75d9895d5e56f7cd7915947ff8a63ac54f2a3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497324"
---
# <span data-ttu-id="4a386-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="4a386-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="4a386-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a386-102">SYNOPSIS</span></span>
<span data-ttu-id="4a386-103">Egy adott előfizetés speficied szabályát távolítja el.</span><span class="sxs-lookup"><span data-stu-id="4a386-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a386-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a386-104">SYNTAX</span></span>

### <span data-ttu-id="4a386-105">RulePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a386-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a386-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4a386-106">RuleResourceIdSet</span></span>
```
Remove-AzureRmServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a386-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a386-107">DESCRIPTION</span></span>
<span data-ttu-id="4a386-108">A **Remove-AzureRmServiceBusRule** parancsmag eltávolítja az adott témakörhöz tartozó előfizetés szabályát.</span><span class="sxs-lookup"><span data-stu-id="4a386-108">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="4a386-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4a386-109">EXAMPLES</span></span>

### <span data-ttu-id="4a386-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4a386-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="4a386-111">Eltávolítja a `SBRule` megadott témakör előfizetési szabályát `SBSubscription` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="4a386-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="4a386-112">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="4a386-112">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="4a386-113">A $inputobject for-InputObject paraméterrel megadott szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4a386-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="4a386-114">Példa 2,2-InputObject:</span><span class="sxs-lookup"><span data-stu-id="4a386-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusRule <params> | Remove-AzureRmServiceBusRule
```

### <span data-ttu-id="4a386-115">Példa 3,1-ResourceId – változó használata</span><span class="sxs-lookup"><span data-stu-id="4a386-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="4a386-116">Példa 3,1-ResourceId – karakterlánc-érték használata</span><span class="sxs-lookup"><span data-stu-id="4a386-116">Example 3.1 - ResourceId - Using string value</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="4a386-117">A $resourceid/string for-ResourceId paraméterrel megadott szabály eltávolítása a ARM azonosítóval</span><span class="sxs-lookup"><span data-stu-id="4a386-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="4a386-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a386-118">PARAMETERS</span></span>

### <span data-ttu-id="4a386-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a386-119">-AsJob</span></span>
<span data-ttu-id="4a386-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4a386-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a386-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a386-121">-DefaultProfile</span></span>
<span data-ttu-id="4a386-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a386-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a386-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4a386-123">-Force</span></span>
<span data-ttu-id="4a386-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a386-124">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a386-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a386-125">-InputObject</span></span>
<span data-ttu-id="4a386-126">A Service Bus Rule objektum</span><span class="sxs-lookup"><span data-stu-id="4a386-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a386-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a386-127">-Name</span></span>
<span data-ttu-id="4a386-128">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="4a386-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a386-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4a386-129">-Namespace</span></span>
<span data-ttu-id="4a386-130">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="4a386-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a386-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a386-131">-PassThru</span></span>
<span data-ttu-id="4a386-132">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="4a386-132">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a386-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a386-133">-ResourceGroupName</span></span>
<span data-ttu-id="4a386-134">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4a386-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a386-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a386-135">-ResourceId</span></span>
<span data-ttu-id="4a386-136">A Service Bus szabály erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4a386-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a386-137">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="4a386-137">-Subscription</span></span>
<span data-ttu-id="4a386-138">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="4a386-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a386-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="4a386-139">-Topic</span></span>
<span data-ttu-id="4a386-140">Téma neve</span><span class="sxs-lookup"><span data-stu-id="4a386-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a386-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a386-141">-Confirm</span></span>
<span data-ttu-id="4a386-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a386-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a386-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a386-143">-WhatIf</span></span>
<span data-ttu-id="4a386-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4a386-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a386-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a386-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a386-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a386-146">CommonParameters</span></span>
<span data-ttu-id="4a386-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a386-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a386-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a386-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a386-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a386-149">INPUTS</span></span>

### <span data-ttu-id="4a386-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4a386-150">System.String</span></span>

### <span data-ttu-id="4a386-151">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="4a386-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="4a386-152">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4a386-152">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4a386-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a386-153">OUTPUTS</span></span>

### <span data-ttu-id="4a386-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a386-154">System.Boolean</span></span>

## <span data-ttu-id="4a386-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a386-155">NOTES</span></span>

## <span data-ttu-id="4a386-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a386-156">RELATED LINKS</span></span>
