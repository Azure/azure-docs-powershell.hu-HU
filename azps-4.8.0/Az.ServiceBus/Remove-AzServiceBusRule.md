---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: a3fc0d37e48ddeba41b6870edfe1732eeecfaa14
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017610"
---
# <span data-ttu-id="94fc8-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="94fc8-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="94fc8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="94fc8-103">Egy adott előfizetés meghatározott szabályát távolítja el.</span><span class="sxs-lookup"><span data-stu-id="94fc8-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="94fc8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94fc8-104">SYNTAX</span></span>

### <span data-ttu-id="94fc8-105">RulePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94fc8-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94fc8-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="94fc8-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94fc8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="94fc8-107">DESCRIPTION</span></span>
<span data-ttu-id="94fc8-108">A **Remove-AzServiceBusRule** parancsmag eltávolítja az adott témakörhöz tartozó előfizetés szabályát.</span><span class="sxs-lookup"><span data-stu-id="94fc8-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="94fc8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="94fc8-109">EXAMPLES</span></span>

### <span data-ttu-id="94fc8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94fc8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="94fc8-111">Eltávolítja a `SBRule` megadott témakör előfizetési szabályát `SBSubscription` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="94fc8-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="94fc8-112">2. példa: InputObject-változó használata:</span><span class="sxs-lookup"><span data-stu-id="94fc8-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="94fc8-113">A $inputobject for-InputObject paraméterrel megadott szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="94fc8-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="94fc8-114">3. példa: InputObject csövek használata:</span><span class="sxs-lookup"><span data-stu-id="94fc8-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="94fc8-115">Példa 4: ResourceId változó használata</span><span class="sxs-lookup"><span data-stu-id="94fc8-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="94fc8-116">Példa 5: ResourceId – karakterlánc-érték használata</span><span class="sxs-lookup"><span data-stu-id="94fc8-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="94fc8-117">A $resourceid/string for-ResourceId paraméterrel megadott szabály eltávolítása a ARM azonosítóval</span><span class="sxs-lookup"><span data-stu-id="94fc8-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="94fc8-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94fc8-118">PARAMETERS</span></span>

### <span data-ttu-id="94fc8-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94fc8-119">-AsJob</span></span>
<span data-ttu-id="94fc8-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="94fc8-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94fc8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94fc8-121">-DefaultProfile</span></span>
<span data-ttu-id="94fc8-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94fc8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94fc8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="94fc8-123">-Force</span></span>
<span data-ttu-id="94fc8-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94fc8-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="94fc8-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94fc8-125">-InputObject</span></span>
<span data-ttu-id="94fc8-126">A Service Bus Rule objektum</span><span class="sxs-lookup"><span data-stu-id="94fc8-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="94fc8-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94fc8-127">-Name</span></span>
<span data-ttu-id="94fc8-128">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="94fc8-128">Rule Name</span></span>

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

### <span data-ttu-id="94fc8-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="94fc8-129">-Namespace</span></span>
<span data-ttu-id="94fc8-130">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="94fc8-130">Namespace Name</span></span>

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

### <span data-ttu-id="94fc8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94fc8-131">-PassThru</span></span>
<span data-ttu-id="94fc8-132">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="94fc8-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="94fc8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94fc8-133">-ResourceGroupName</span></span>
<span data-ttu-id="94fc8-134">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="94fc8-134">The name of the resource group</span></span>

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

### <span data-ttu-id="94fc8-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94fc8-135">-ResourceId</span></span>
<span data-ttu-id="94fc8-136">A Service Bus szabály erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="94fc8-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="94fc8-137">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="94fc8-137">-Subscription</span></span>
<span data-ttu-id="94fc8-138">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="94fc8-138">Subscription Name</span></span>

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

### <span data-ttu-id="94fc8-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="94fc8-139">-Topic</span></span>
<span data-ttu-id="94fc8-140">Téma neve</span><span class="sxs-lookup"><span data-stu-id="94fc8-140">Topic Name</span></span>

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

### <span data-ttu-id="94fc8-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94fc8-141">-Confirm</span></span>
<span data-ttu-id="94fc8-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94fc8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94fc8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94fc8-143">-WhatIf</span></span>
<span data-ttu-id="94fc8-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94fc8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94fc8-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94fc8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94fc8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94fc8-146">CommonParameters</span></span>
<span data-ttu-id="94fc8-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94fc8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94fc8-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94fc8-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94fc8-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94fc8-149">INPUTS</span></span>

### <span data-ttu-id="94fc8-150">System. String</span><span class="sxs-lookup"><span data-stu-id="94fc8-150">System.String</span></span>

### <span data-ttu-id="94fc8-151">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="94fc8-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="94fc8-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94fc8-152">OUTPUTS</span></span>

### <span data-ttu-id="94fc8-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94fc8-153">System.Boolean</span></span>

## <span data-ttu-id="94fc8-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94fc8-154">NOTES</span></span>

## <span data-ttu-id="94fc8-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94fc8-155">RELATED LINKS</span></span>
