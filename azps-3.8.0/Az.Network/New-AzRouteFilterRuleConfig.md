---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013248"
---
# <span data-ttu-id="21eb0-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21eb0-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="21eb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="21eb0-103">Az útvonaltervezés szabályait hozza létre az útvonal-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="21eb0-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="21eb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21eb0-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21eb0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="21eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="21eb0-106">Az New-AzRouteFilterRuleConfig parancsmag létrehoz egy útvonal-szűrési szabályt az Azure Route-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="21eb0-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="21eb0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="21eb0-107">EXAMPLES</span></span>

### <span data-ttu-id="21eb0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="21eb0-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="21eb0-109">A parancs új útvonal-szűrési szabályt hoz létre, és az 1 $rule változóban tárolja azt.</span><span class="sxs-lookup"><span data-stu-id="21eb0-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="21eb0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21eb0-110">PARAMETERS</span></span>

### <span data-ttu-id="21eb0-111">-Access</span><span class="sxs-lookup"><span data-stu-id="21eb0-111">-Access</span></span>
<span data-ttu-id="21eb0-112">Hozzáférés az útvonal-szűrő szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="21eb0-112">Access for route filter rule.</span></span>
<span data-ttu-id="21eb0-113">Az érvényes értékek: Allow vagy deny.</span><span class="sxs-lookup"><span data-stu-id="21eb0-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21eb0-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="21eb0-114">-CommunityList</span></span>
<span data-ttu-id="21eb0-115">Annak a közösségi értéknek a listája, amelyre az útvonal-szűrő szűrést fog kiszűrni</span><span class="sxs-lookup"><span data-stu-id="21eb0-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21eb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21eb0-116">-DefaultProfile</span></span>
<span data-ttu-id="21eb0-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21eb0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21eb0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="21eb0-118">-Force</span></span>
<span data-ttu-id="21eb0-119">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21eb0-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="21eb0-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="21eb0-120">-Name</span></span>
<span data-ttu-id="21eb0-121">Az útvonal-szűrő szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="21eb0-121">Specifies a name for the route filter rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21eb0-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="21eb0-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="21eb0-123">Az útvonal szűrési szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="21eb0-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="21eb0-124">Az érvényes értékek: Közösség</span><span class="sxs-lookup"><span data-stu-id="21eb0-124">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21eb0-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21eb0-125">-Confirm</span></span>
<span data-ttu-id="21eb0-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21eb0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21eb0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21eb0-127">-WhatIf</span></span>
<span data-ttu-id="21eb0-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21eb0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21eb0-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21eb0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21eb0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21eb0-130">CommonParameters</span></span>
<span data-ttu-id="21eb0-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21eb0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21eb0-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21eb0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21eb0-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21eb0-133">INPUTS</span></span>

### <span data-ttu-id="21eb0-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="21eb0-134">None</span></span>

## <span data-ttu-id="21eb0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21eb0-135">OUTPUTS</span></span>

### <span data-ttu-id="21eb0-136">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="21eb0-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="21eb0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21eb0-137">NOTES</span></span>
<span data-ttu-id="21eb0-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="21eb0-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="21eb0-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21eb0-139">RELATED LINKS</span></span>

[<span data-ttu-id="21eb0-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21eb0-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="21eb0-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21eb0-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="21eb0-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21eb0-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="21eb0-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21eb0-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="21eb0-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="21eb0-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="21eb0-145">Új – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="21eb0-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="21eb0-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="21eb0-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="21eb0-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="21eb0-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
