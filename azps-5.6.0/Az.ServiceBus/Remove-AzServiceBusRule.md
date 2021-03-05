---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: 673e67b9611cfab468c1c6f83393515bd4997e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015894"
---
# <span data-ttu-id="ba558-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="ba558-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="ba558-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba558-102">SYNOPSIS</span></span>
<span data-ttu-id="ba558-103">Egy adott előfizetés megadott szabályának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ba558-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="ba558-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba558-104">SYNTAX</span></span>

### <span data-ttu-id="ba558-105">RulePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba558-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba558-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ba558-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba558-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba558-107">DESCRIPTION</span></span>
<span data-ttu-id="ba558-108">A **Remove-AzServiceBusRule** parancsmag eltávolítja egy adott témakör előfizetésének szabályát.</span><span class="sxs-lookup"><span data-stu-id="ba558-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="ba558-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba558-109">EXAMPLES</span></span>

### <span data-ttu-id="ba558-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ba558-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="ba558-111">A megadott témakör `SBRule` előfizetési `SBSubscription` szabályának `SBTopic` eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ba558-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="ba558-112">2. példa: InputObject – Változó használata:</span><span class="sxs-lookup"><span data-stu-id="ba558-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="ba558-113">Az -InputObject paraméter $inputobject által biztosított szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ba558-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="ba558-114">3. példa: InputObject – Piping használata:</span><span class="sxs-lookup"><span data-stu-id="ba558-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="ba558-115">4. példa: ResourceId – Változó használata</span><span class="sxs-lookup"><span data-stu-id="ba558-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="ba558-116">5. példa: ResourceId – Karakterláncérték használata</span><span class="sxs-lookup"><span data-stu-id="ba558-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="ba558-117">Eltávolítja a ARM -ResourceId paraméter $resourceid/karakterláncában megadott szabályt</span><span class="sxs-lookup"><span data-stu-id="ba558-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="ba558-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba558-118">PARAMETERS</span></span>

### <span data-ttu-id="ba558-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba558-119">-AsJob</span></span>
<span data-ttu-id="ba558-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ba558-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba558-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba558-121">-DefaultProfile</span></span>
<span data-ttu-id="ba558-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba558-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba558-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ba558-123">-Force</span></span>
<span data-ttu-id="ba558-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba558-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ba558-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba558-125">-InputObject</span></span>
<span data-ttu-id="ba558-126">Service Bus Rule Object</span><span class="sxs-lookup"><span data-stu-id="ba558-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="ba558-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ba558-127">-Name</span></span>
<span data-ttu-id="ba558-128">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="ba558-128">Rule Name</span></span>

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

### <span data-ttu-id="ba558-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ba558-129">-Namespace</span></span>
<span data-ttu-id="ba558-130">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ba558-130">Namespace Name</span></span>

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

### <span data-ttu-id="ba558-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba558-131">-PassThru</span></span>
<span data-ttu-id="ba558-132">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="ba558-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ba558-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba558-133">-ResourceGroupName</span></span>
<span data-ttu-id="ba558-134">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ba558-134">The name of the resource group</span></span>

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

### <span data-ttu-id="ba558-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba558-135">-ResourceId</span></span>
<span data-ttu-id="ba558-136">Service Bus Rule Resource Id</span><span class="sxs-lookup"><span data-stu-id="ba558-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="ba558-137">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="ba558-137">-Subscription</span></span>
<span data-ttu-id="ba558-138">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="ba558-138">Subscription Name</span></span>

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

### <span data-ttu-id="ba558-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="ba558-139">-Topic</span></span>
<span data-ttu-id="ba558-140">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="ba558-140">Topic Name</span></span>

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

### <span data-ttu-id="ba558-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba558-141">-Confirm</span></span>
<span data-ttu-id="ba558-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ba558-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba558-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba558-143">-WhatIf</span></span>
<span data-ttu-id="ba558-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ba558-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba558-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba558-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba558-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba558-146">CommonParameters</span></span>
<span data-ttu-id="ba558-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba558-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba558-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba558-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba558-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba558-149">INPUTS</span></span>

### <span data-ttu-id="ba558-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ba558-150">System.String</span></span>

### <span data-ttu-id="ba558-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ba558-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="ba558-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba558-152">OUTPUTS</span></span>

### <span data-ttu-id="ba558-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba558-153">System.Boolean</span></span>

## <span data-ttu-id="ba558-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba558-154">NOTES</span></span>

## <span data-ttu-id="ba558-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba558-155">RELATED LINKS</span></span>
