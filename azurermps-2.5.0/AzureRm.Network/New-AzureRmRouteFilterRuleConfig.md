---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 2309d49dcd91ddefbcbe0e40379a759d50d5ba2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850374"
---
# <span data-ttu-id="3406f-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3406f-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="3406f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3406f-102">SYNOPSIS</span></span>
<span data-ttu-id="3406f-103">Az útvonaltervezés szabályait hozza létre az útvonal-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="3406f-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3406f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3406f-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3406f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3406f-105">DESCRIPTION</span></span>
<span data-ttu-id="3406f-106">Az New-AzureRmRouteFilterRuleConfig parancsmag létrehoz egy útvonal-szűrési szabályt az Azure Route-szűrőhöz.</span><span class="sxs-lookup"><span data-stu-id="3406f-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="3406f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3406f-107">EXAMPLES</span></span>

### <span data-ttu-id="3406f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3406f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3406f-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="3406f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3406f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3406f-110">PARAMETERS</span></span>

### <span data-ttu-id="3406f-111">-Access</span><span class="sxs-lookup"><span data-stu-id="3406f-111">-Access</span></span>
<span data-ttu-id="3406f-112">Hozzáférés az útvonal-szűrő szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="3406f-112">Access for route filter rule.</span></span>
<span data-ttu-id="3406f-113">Az érvényes értékek: Allow vagy deny.</span><span class="sxs-lookup"><span data-stu-id="3406f-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3406f-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="3406f-114">-CommunityList</span></span>
<span data-ttu-id="3406f-115">Annak a közösségi értéknek a listája, amelyre az útvonal-szűrő szűrést fog kiszűrni</span><span class="sxs-lookup"><span data-stu-id="3406f-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3406f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3406f-116">-DefaultProfile</span></span>
<span data-ttu-id="3406f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3406f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3406f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3406f-118">-Force</span></span>
<span data-ttu-id="3406f-119">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="3406f-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3406f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3406f-120">-Name</span></span>
<span data-ttu-id="3406f-121">Az útvonal-szűrő szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3406f-121">Specifies a name for the route filter rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3406f-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="3406f-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="3406f-123">Az útvonal szűrési szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="3406f-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="3406f-124">Az érvényes értékek: Közösség</span><span class="sxs-lookup"><span data-stu-id="3406f-124">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3406f-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3406f-125">-Confirm</span></span>
<span data-ttu-id="3406f-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3406f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3406f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3406f-127">-WhatIf</span></span>
<span data-ttu-id="3406f-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3406f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3406f-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3406f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3406f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3406f-130">CommonParameters</span></span>
<span data-ttu-id="3406f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3406f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3406f-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3406f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3406f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3406f-133">INPUTS</span></span>

## <span data-ttu-id="3406f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3406f-134">OUTPUTS</span></span>

### <span data-ttu-id="3406f-135">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="3406f-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="3406f-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3406f-136">NOTES</span></span>
<span data-ttu-id="3406f-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="3406f-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3406f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3406f-138">RELATED LINKS</span></span>

[<span data-ttu-id="3406f-139">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3406f-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="3406f-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3406f-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="3406f-141">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3406f-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="3406f-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3406f-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

