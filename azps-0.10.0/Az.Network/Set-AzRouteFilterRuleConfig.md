---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 8ab95789b73623716edc818c8092c8c0cd58c534
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843574"
---
# <span data-ttu-id="afe3e-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="afe3e-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="afe3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="afe3e-102">SYNOPSIS</span></span>
<span data-ttu-id="afe3e-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="afe3e-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="afe3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="afe3e-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afe3e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="afe3e-105">DESCRIPTION</span></span>
<span data-ttu-id="afe3e-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="afe3e-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="afe3e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="afe3e-107">EXAMPLES</span></span>

### <span data-ttu-id="afe3e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="afe3e-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="afe3e-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="afe3e-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="afe3e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="afe3e-110">PARAMETERS</span></span>

### <span data-ttu-id="afe3e-111">-Access</span><span class="sxs-lookup"><span data-stu-id="afe3e-111">-Access</span></span>
<span data-ttu-id="afe3e-112">A szabály hozzáférési típusa.</span><span class="sxs-lookup"><span data-stu-id="afe3e-112">The access type of the rule.</span></span>
<span data-ttu-id="afe3e-113">A lehetséges értékek a következők: "Allow", "deny"</span><span class="sxs-lookup"><span data-stu-id="afe3e-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="afe3e-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="afe3e-114">-CommunityList</span></span>
<span data-ttu-id="afe3e-115">Annak a közösségi értéknek a listája, amelyre az útvonal-szűrő szűrést fog kiszűrni</span><span class="sxs-lookup"><span data-stu-id="afe3e-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="afe3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe3e-116">-DefaultProfile</span></span>
<span data-ttu-id="afe3e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afe3e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afe3e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="afe3e-118">-Force</span></span>
<span data-ttu-id="afe3e-119">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="afe3e-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="afe3e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="afe3e-120">-Name</span></span>
<span data-ttu-id="afe3e-121">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="afe3e-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="afe3e-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="afe3e-122">-RouteFilter</span></span>
<span data-ttu-id="afe3e-123">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="afe3e-123">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afe3e-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="afe3e-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="afe3e-125">Az útvonal-szűrő szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="afe3e-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="afe3e-126">Lehetséges értékek: "Közösség"</span><span class="sxs-lookup"><span data-stu-id="afe3e-126">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="afe3e-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="afe3e-127">-Confirm</span></span>
<span data-ttu-id="afe3e-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="afe3e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afe3e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afe3e-129">-WhatIf</span></span>
<span data-ttu-id="afe3e-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="afe3e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afe3e-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="afe3e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afe3e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe3e-132">CommonParameters</span></span>
<span data-ttu-id="afe3e-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="afe3e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe3e-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afe3e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe3e-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="afe3e-135">INPUTS</span></span>

### <span data-ttu-id="afe3e-136">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="afe3e-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="afe3e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afe3e-137">OUTPUTS</span></span>

### <span data-ttu-id="afe3e-138">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="afe3e-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="afe3e-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="afe3e-139">NOTES</span></span>

## <span data-ttu-id="afe3e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afe3e-140">RELATED LINKS</span></span>

