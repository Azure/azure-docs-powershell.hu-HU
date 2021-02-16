---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: dd0dfb633fd48f2f747d6f4c0eb3471745b40da1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168850"
---
# <span data-ttu-id="33859-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="33859-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="33859-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33859-102">SYNOPSIS</span></span>
<span data-ttu-id="33859-103">Eltávolítja egy témakör előfizetését a megadott Service Bus névtérből.</span><span class="sxs-lookup"><span data-stu-id="33859-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="33859-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33859-104">SYNTAX</span></span>

### <span data-ttu-id="33859-105">SubscriptionPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33859-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33859-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="33859-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33859-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="33859-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33859-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33859-108">DESCRIPTION</span></span>
<span data-ttu-id="33859-109">A **Remove-AzServiceBusSubscription** parancsmag eltávolítja az előfizetést egy témakörből a megadott Service Bus névtérből.</span><span class="sxs-lookup"><span data-stu-id="33859-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="33859-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33859-110">EXAMPLES</span></span>

### <span data-ttu-id="33859-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="33859-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="33859-112">Eltávolítja a szolgáltatásbusz névterében található témakörre `SB-TopicSubscription-Example1` `SB-Topic_exampl1` vonatkozó `SB-Example1` előfizetést.</span><span class="sxs-lookup"><span data-stu-id="33859-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="33859-113">2. példa: InputObject – Változó használatával:</span><span class="sxs-lookup"><span data-stu-id="33859-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="33859-114">3. példa: InputObject – Piping használata:</span><span class="sxs-lookup"><span data-stu-id="33859-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="33859-115">4. példa: ResourceId – Változó használatával:</span><span class="sxs-lookup"><span data-stu-id="33859-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="33859-116">5. példa: ResourceId – Karakterlánc-érték használata:</span><span class="sxs-lookup"><span data-stu-id="33859-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="33859-117">A -ResourceId paraméter ARM $resourceid/karakterláncában megadott előfizetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="33859-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="33859-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33859-118">PARAMETERS</span></span>

### <span data-ttu-id="33859-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33859-119">-AsJob</span></span>
<span data-ttu-id="33859-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="33859-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33859-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33859-121">-DefaultProfile</span></span>
<span data-ttu-id="33859-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33859-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33859-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33859-123">-InputObject</span></span>
<span data-ttu-id="33859-124">Service Bus Subscription Object</span><span class="sxs-lookup"><span data-stu-id="33859-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="33859-125">-Name</span><span class="sxs-lookup"><span data-stu-id="33859-125">-Name</span></span>
<span data-ttu-id="33859-126">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="33859-126">Subscription Name</span></span>

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

### <span data-ttu-id="33859-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="33859-127">-Namespace</span></span>
<span data-ttu-id="33859-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="33859-128">Namespace Name</span></span>

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

### <span data-ttu-id="33859-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33859-129">-PassThru</span></span>
<span data-ttu-id="33859-130">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="33859-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="33859-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33859-131">-ResourceGroupName</span></span>
<span data-ttu-id="33859-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="33859-132">The name of the resource group</span></span>

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

### <span data-ttu-id="33859-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33859-133">-ResourceId</span></span>
<span data-ttu-id="33859-134">Service Bus Subscription Resource Id</span><span class="sxs-lookup"><span data-stu-id="33859-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="33859-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="33859-135">-Topic</span></span>
<span data-ttu-id="33859-136">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="33859-136">Topic Name</span></span>

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

### <span data-ttu-id="33859-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33859-137">-Confirm</span></span>
<span data-ttu-id="33859-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="33859-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33859-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33859-139">-WhatIf</span></span>
<span data-ttu-id="33859-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="33859-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33859-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="33859-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33859-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33859-142">CommonParameters</span></span>
<span data-ttu-id="33859-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33859-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33859-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33859-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33859-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33859-145">INPUTS</span></span>

### <span data-ttu-id="33859-146">System.String</span><span class="sxs-lookup"><span data-stu-id="33859-146">System.String</span></span>

### <span data-ttu-id="33859-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="33859-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="33859-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33859-148">OUTPUTS</span></span>

### <span data-ttu-id="33859-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33859-149">System.Boolean</span></span>

## <span data-ttu-id="33859-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33859-150">NOTES</span></span>

## <span data-ttu-id="33859-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33859-151">RELATED LINKS</span></span>
