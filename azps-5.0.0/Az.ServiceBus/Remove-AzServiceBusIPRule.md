---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 90c832d36017aa02a05d972a7b6e26fffd93937e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188170"
---
# <span data-ttu-id="a86b8-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="a86b8-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="a86b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a86b8-102">SYNOPSIS</span></span>
<span data-ttu-id="a86b8-103">Egyetlen IP-szabály eltávolítása a megadott névtér NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a86b8-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="a86b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a86b8-104">SYNTAX</span></span>

### <span data-ttu-id="a86b8-105">IPRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a86b8-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a86b8-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a86b8-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a86b8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a86b8-107">DESCRIPTION</span></span>
<span data-ttu-id="a86b8-108">Egyetlen IP-szabály eltávolítása a megadott névtér NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a86b8-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="a86b8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a86b8-109">EXAMPLES</span></span>

### <span data-ttu-id="a86b8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a86b8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="a86b8-111">A megadott névtér NetworkRuleSet IpMask eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a86b8-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="a86b8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a86b8-112">PARAMETERS</span></span>

### <span data-ttu-id="a86b8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a86b8-113">-AsJob</span></span>
<span data-ttu-id="a86b8-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a86b8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a86b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86b8-115">-DefaultProfile</span></span>
<span data-ttu-id="a86b8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a86b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a86b8-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="a86b8-117">-IpMask</span></span>
<span data-ttu-id="a86b8-118">Alhálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a86b8-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a86b8-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="a86b8-119">-IpRuleObject</span></span>
<span data-ttu-id="a86b8-120">IPRule konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="a86b8-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a86b8-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a86b8-121">-Name</span></span>
<span data-ttu-id="a86b8-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a86b8-122">Namespace Name</span></span>

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

### <span data-ttu-id="a86b8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a86b8-123">-PassThru</span></span>
<span data-ttu-id="a86b8-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a86b8-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a86b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a86b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="a86b8-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a86b8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a86b8-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a86b8-127">-Confirm</span></span>
<span data-ttu-id="a86b8-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a86b8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a86b8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a86b8-129">-WhatIf</span></span>
<span data-ttu-id="a86b8-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a86b8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a86b8-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a86b8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a86b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86b8-132">CommonParameters</span></span>
<span data-ttu-id="a86b8-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a86b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a86b8-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a86b8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86b8-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a86b8-135">INPUTS</span></span>

### <span data-ttu-id="a86b8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a86b8-136">System.String</span></span>

### <span data-ttu-id="a86b8-137">Microsoft. Azure. Command. ServiceBus. models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="a86b8-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="a86b8-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a86b8-138">OUTPUTS</span></span>

### <span data-ttu-id="a86b8-139">Microsoft. Azure. Command. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a86b8-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="a86b8-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a86b8-140">NOTES</span></span>

## <span data-ttu-id="a86b8-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a86b8-141">RELATED LINKS</span></span>