---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: b8b2b9f6bb8a082647a14285a907465e8e12348f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497327"
---
# <span data-ttu-id="2c50a-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="2c50a-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="2c50a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c50a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c50a-103">Eltávolítja az előfizetést a megadott szolgáltatási busz névterből származó témára.</span><span class="sxs-lookup"><span data-stu-id="2c50a-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c50a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c50a-104">SYNTAX</span></span>

### <span data-ttu-id="2c50a-105">SubscriptionPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c50a-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c50a-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2c50a-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzureRmServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c50a-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2c50a-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzureRmServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c50a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c50a-108">DESCRIPTION</span></span>
<span data-ttu-id="2c50a-109">A **Remove-AzureRmServiceBusSubscription** parancsmag eltávolítja az előfizetést a megadott szolgáltatási busz névtérből származó témára.</span><span class="sxs-lookup"><span data-stu-id="2c50a-109">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2c50a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2c50a-110">EXAMPLES</span></span>

### <span data-ttu-id="2c50a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2c50a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="2c50a-112">Eltávolítja az előfizetést `SB-TopicSubscription-Example1` a `SB-Topic_exampl1` megadott Service Bus névtérben lévő témakörre `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="2c50a-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="2c50a-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="2c50a-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusSubscription <params>
PS C:\> Remove-AzureRmServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="2c50a-114">Példa 2,2-InputObject:</span><span class="sxs-lookup"><span data-stu-id="2c50a-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzureRmServiceBusSubscription <params> |Remove-AzureRmServiceBusSubscription
```

### <span data-ttu-id="2c50a-115">Példa 3,1-ResourceId – változó használata:</span><span class="sxs-lookup"><span data-stu-id="2c50a-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusSubscription <params>
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="2c50a-116">Példa 3,2-ResourceId-karakterlánc-érték használatával:</span><span class="sxs-lookup"><span data-stu-id="2c50a-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="2c50a-117">A $resourceid/string for-ResourceId paraméterrel megadott ARM azonosítóval elkészített előfizetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2c50a-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="2c50a-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c50a-118">PARAMETERS</span></span>

### <span data-ttu-id="2c50a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c50a-119">-AsJob</span></span>
<span data-ttu-id="2c50a-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2c50a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c50a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c50a-121">-DefaultProfile</span></span>
<span data-ttu-id="2c50a-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c50a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c50a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c50a-123">-InputObject</span></span>
<span data-ttu-id="2c50a-124">Service Bus előfizetés objektum</span><span class="sxs-lookup"><span data-stu-id="2c50a-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="2c50a-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c50a-125">-Name</span></span>
<span data-ttu-id="2c50a-126">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="2c50a-126">Subscription Name</span></span>

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

### <span data-ttu-id="2c50a-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2c50a-127">-Namespace</span></span>
<span data-ttu-id="2c50a-128">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="2c50a-128">Namespace Name</span></span>

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

### <span data-ttu-id="2c50a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c50a-129">-PassThru</span></span>
<span data-ttu-id="2c50a-130">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="2c50a-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2c50a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c50a-131">-ResourceGroupName</span></span>
<span data-ttu-id="2c50a-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2c50a-132">The name of the resource group</span></span>

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

### <span data-ttu-id="2c50a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c50a-133">-ResourceId</span></span>
<span data-ttu-id="2c50a-134">Szolgáltatás busz-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2c50a-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="2c50a-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="2c50a-135">-Topic</span></span>
<span data-ttu-id="2c50a-136">Téma neve</span><span class="sxs-lookup"><span data-stu-id="2c50a-136">Topic Name</span></span>

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

### <span data-ttu-id="2c50a-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c50a-137">-Confirm</span></span>
<span data-ttu-id="2c50a-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c50a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c50a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c50a-139">-WhatIf</span></span>
<span data-ttu-id="2c50a-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c50a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c50a-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c50a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c50a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c50a-142">CommonParameters</span></span>
<span data-ttu-id="2c50a-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c50a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c50a-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c50a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c50a-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c50a-145">INPUTS</span></span>

### <span data-ttu-id="2c50a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2c50a-146">System.String</span></span>

### <span data-ttu-id="2c50a-147">Microsoft. Azure. Command. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="2c50a-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>
<span data-ttu-id="2c50a-148">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2c50a-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2c50a-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c50a-149">OUTPUTS</span></span>

### <span data-ttu-id="2c50a-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c50a-150">System.Boolean</span></span>

## <span data-ttu-id="2c50a-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c50a-151">NOTES</span></span>

## <span data-ttu-id="2c50a-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c50a-152">RELATED LINKS</span></span>
