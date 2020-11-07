---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 0369d6bac19d2d2180c54f3c4244101df3a7bb42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838030"
---
# <span data-ttu-id="8dabf-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="8dabf-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="8dabf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8dabf-102">SYNOPSIS</span></span>
<span data-ttu-id="8dabf-103">Eltávolítja az előfizetést a megadott szolgáltatási busz névterből származó témára.</span><span class="sxs-lookup"><span data-stu-id="8dabf-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8dabf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8dabf-104">SYNTAX</span></span>

### <span data-ttu-id="8dabf-105">SubscriptionPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8dabf-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dabf-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8dabf-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dabf-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8dabf-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dabf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8dabf-108">DESCRIPTION</span></span>
<span data-ttu-id="8dabf-109">A **Remove-AzServiceBusSubscription** parancsmag eltávolítja az előfizetést a megadott szolgáltatási busz névtérből származó témára.</span><span class="sxs-lookup"><span data-stu-id="8dabf-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8dabf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8dabf-110">EXAMPLES</span></span>

### <span data-ttu-id="8dabf-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8dabf-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="8dabf-112">Eltávolítja az előfizetést `SB-TopicSubscription-Example1` a `SB-Topic_exampl1` megadott Service Bus névtérben lévő témakörre `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="8dabf-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="8dabf-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="8dabf-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="8dabf-114">Példa 2,2-InputObject:</span><span class="sxs-lookup"><span data-stu-id="8dabf-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="8dabf-115">Példa 3,1-ResourceId – változó használata:</span><span class="sxs-lookup"><span data-stu-id="8dabf-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="8dabf-116">Példa 3,2-ResourceId-karakterlánc-érték használatával:</span><span class="sxs-lookup"><span data-stu-id="8dabf-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="8dabf-117">A $resourceid/string for-ResourceId paraméterrel megadott ARM azonosítóval elkészített előfizetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8dabf-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="8dabf-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8dabf-118">PARAMETERS</span></span>

### <span data-ttu-id="8dabf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dabf-119">-AsJob</span></span>
<span data-ttu-id="8dabf-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8dabf-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dabf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dabf-121">-DefaultProfile</span></span>
<span data-ttu-id="8dabf-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8dabf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dabf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dabf-123">-InputObject</span></span>
<span data-ttu-id="8dabf-124">Service Bus előfizetés objektum</span><span class="sxs-lookup"><span data-stu-id="8dabf-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dabf-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8dabf-125">-Name</span></span>
<span data-ttu-id="8dabf-126">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="8dabf-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dabf-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8dabf-127">-Namespace</span></span>
<span data-ttu-id="8dabf-128">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="8dabf-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dabf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dabf-129">-PassThru</span></span>
<span data-ttu-id="8dabf-130">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="8dabf-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8dabf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dabf-131">-ResourceGroupName</span></span>
<span data-ttu-id="8dabf-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8dabf-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dabf-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dabf-133">-ResourceId</span></span>
<span data-ttu-id="8dabf-134">Szolgáltatás busz-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8dabf-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dabf-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="8dabf-135">-Topic</span></span>
<span data-ttu-id="8dabf-136">Téma neve</span><span class="sxs-lookup"><span data-stu-id="8dabf-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dabf-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8dabf-137">-Confirm</span></span>
<span data-ttu-id="8dabf-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8dabf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dabf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dabf-139">-WhatIf</span></span>
<span data-ttu-id="8dabf-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8dabf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dabf-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8dabf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dabf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dabf-142">CommonParameters</span></span>
<span data-ttu-id="8dabf-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8dabf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dabf-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dabf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dabf-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8dabf-145">INPUTS</span></span>

### <span data-ttu-id="8dabf-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8dabf-146">System.String</span></span>

### <span data-ttu-id="8dabf-147">Microsoft. Azure. Command. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="8dabf-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="8dabf-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8dabf-148">OUTPUTS</span></span>

### <span data-ttu-id="8dabf-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8dabf-149">System.Boolean</span></span>

## <span data-ttu-id="8dabf-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8dabf-150">NOTES</span></span>

## <span data-ttu-id="8dabf-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8dabf-151">RELATED LINKS</span></span>
