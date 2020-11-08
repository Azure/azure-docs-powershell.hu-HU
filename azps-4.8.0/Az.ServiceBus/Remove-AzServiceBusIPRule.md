---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 90c832d36017aa02a05d972a7b6e26fffd93937e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183962"
---
# <span data-ttu-id="aab64-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="aab64-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="aab64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aab64-102">SYNOPSIS</span></span>
<span data-ttu-id="aab64-103">Egyetlen IP-szabály eltávolítása a megadott névtér NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="aab64-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="aab64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aab64-104">SYNTAX</span></span>

### <span data-ttu-id="aab64-105">IPRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aab64-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aab64-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aab64-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aab64-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aab64-107">DESCRIPTION</span></span>
<span data-ttu-id="aab64-108">Egyetlen IP-szabály eltávolítása a megadott névtér NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="aab64-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="aab64-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aab64-109">EXAMPLES</span></span>

### <span data-ttu-id="aab64-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aab64-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="aab64-111">A megadott névtér NetworkRuleSet IpMask eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aab64-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="aab64-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aab64-112">PARAMETERS</span></span>

### <span data-ttu-id="aab64-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aab64-113">-AsJob</span></span>
<span data-ttu-id="aab64-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="aab64-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aab64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab64-115">-DefaultProfile</span></span>
<span data-ttu-id="aab64-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aab64-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aab64-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="aab64-117">-IpMask</span></span>
<span data-ttu-id="aab64-118">Alhálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="aab64-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="aab64-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="aab64-119">-IpRuleObject</span></span>
<span data-ttu-id="aab64-120">IPRule konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="aab64-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="aab64-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aab64-121">-Name</span></span>
<span data-ttu-id="aab64-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="aab64-122">Namespace Name</span></span>

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

### <span data-ttu-id="aab64-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aab64-123">-PassThru</span></span>
<span data-ttu-id="aab64-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="aab64-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="aab64-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab64-125">-ResourceGroupName</span></span>
<span data-ttu-id="aab64-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="aab64-126">Resource Group Name</span></span>

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

### <span data-ttu-id="aab64-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aab64-127">-Confirm</span></span>
<span data-ttu-id="aab64-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aab64-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab64-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab64-129">-WhatIf</span></span>
<span data-ttu-id="aab64-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aab64-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aab64-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aab64-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aab64-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab64-132">CommonParameters</span></span>
<span data-ttu-id="aab64-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aab64-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aab64-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab64-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab64-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aab64-135">INPUTS</span></span>

### <span data-ttu-id="aab64-136">System. String</span><span class="sxs-lookup"><span data-stu-id="aab64-136">System.String</span></span>

### <span data-ttu-id="aab64-137">Microsoft. Azure. Command. ServiceBus. models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="aab64-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="aab64-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aab64-138">OUTPUTS</span></span>

### <span data-ttu-id="aab64-139">Microsoft. Azure. Command. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="aab64-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="aab64-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aab64-140">NOTES</span></span>

## <span data-ttu-id="aab64-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aab64-141">RELATED LINKS</span></span>
