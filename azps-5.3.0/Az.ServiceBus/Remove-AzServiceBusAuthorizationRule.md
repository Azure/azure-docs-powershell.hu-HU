---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479639"
---
# <span data-ttu-id="70067-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="70067-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="70067-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70067-102">SYNOPSIS</span></span>
<span data-ttu-id="70067-103">Eltávolítja egy szolgáltatásbusz névterének vagy várólistájának vagy témájának engedélyezési szabályát a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="70067-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="70067-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="70067-104">SYNTAX</span></span>

### <span data-ttu-id="70067-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70067-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70067-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="70067-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70067-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="70067-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70067-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="70067-108">DESCRIPTION</span></span>
<span data-ttu-id="70067-109">A **Remove-AzServiceBusAuthorizationRule** parancsmag eltávolítja egy szolgáltatásbusz névterének vagy várólistájának vagy témájának engedélyezési szabályát a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="70067-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="70067-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="70067-110">EXAMPLES</span></span>

### <span data-ttu-id="70067-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="70067-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="70067-112">Eltávolítja a `SBAuthoRule1` névtér engedélyezési szabályát `SB-Example1` a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="70067-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="70067-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="70067-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="70067-114">Eltávolítja a `SBAuthoRule1` várólistára vonatkozó engedélyezési szabályt `SBQueue` a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="70067-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="70067-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="70067-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="70067-116">Eltávolítja a témakör engedélyezési `SBAuthoRule1` `SBTopic` szabályát a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="70067-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="70067-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70067-117">PARAMETERS</span></span>

### <span data-ttu-id="70067-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70067-118">-DefaultProfile</span></span>
<span data-ttu-id="70067-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70067-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70067-120">-Force</span><span class="sxs-lookup"><span data-stu-id="70067-120">-Force</span></span>
<span data-ttu-id="70067-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70067-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="70067-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70067-122">-InputObject</span></span>
<span data-ttu-id="70067-123">ServiceBus AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="70067-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70067-124">-Name</span><span class="sxs-lookup"><span data-stu-id="70067-124">-Name</span></span>
<span data-ttu-id="70067-125">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="70067-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="70067-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="70067-126">-Namespace</span></span>
<span data-ttu-id="70067-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="70067-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70067-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70067-128">-PassThru</span></span>
<span data-ttu-id="70067-129">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="70067-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="70067-130">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="70067-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="70067-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="70067-131">-Queue</span></span>
<span data-ttu-id="70067-132">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="70067-132">Queue Name</span></span>

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

### <span data-ttu-id="70067-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70067-133">-ResourceGroupName</span></span>
<span data-ttu-id="70067-134">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="70067-134">Resource Group Name</span></span>

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

### <span data-ttu-id="70067-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="70067-135">-Topic</span></span>
<span data-ttu-id="70067-136">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="70067-136">Topic Name</span></span>

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

### <span data-ttu-id="70067-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70067-137">-Confirm</span></span>
<span data-ttu-id="70067-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="70067-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70067-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70067-139">-WhatIf</span></span>
<span data-ttu-id="70067-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="70067-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70067-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70067-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70067-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70067-142">CommonParameters</span></span>
<span data-ttu-id="70067-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70067-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70067-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70067-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70067-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70067-145">INPUTS</span></span>

### <span data-ttu-id="70067-146">System.String</span><span class="sxs-lookup"><span data-stu-id="70067-146">System.String</span></span>

### <span data-ttu-id="70067-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="70067-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="70067-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70067-148">OUTPUTS</span></span>

### <span data-ttu-id="70067-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70067-149">System.Boolean</span></span>

## <span data-ttu-id="70067-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="70067-150">NOTES</span></span>

## <span data-ttu-id="70067-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70067-151">RELATED LINKS</span></span>
