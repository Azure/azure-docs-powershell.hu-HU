---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: f5b2a3f66a1972edbf6d3e475f5f30fc9530929f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494791"
---
# <span data-ttu-id="aec87-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aec87-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="aec87-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aec87-102">SYNOPSIS</span></span>
<span data-ttu-id="aec87-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="aec87-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aec87-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aec87-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec87-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aec87-105">DESCRIPTION</span></span>
<span data-ttu-id="aec87-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="aec87-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="aec87-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aec87-107">EXAMPLES</span></span>

### <span data-ttu-id="aec87-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aec87-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="aec87-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="aec87-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="aec87-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aec87-110">PARAMETERS</span></span>

### <span data-ttu-id="aec87-111">-Access</span><span class="sxs-lookup"><span data-stu-id="aec87-111">-Access</span></span>
<span data-ttu-id="aec87-112">A szabály hozzáférési típusa.</span><span class="sxs-lookup"><span data-stu-id="aec87-112">The access type of the rule.</span></span>
<span data-ttu-id="aec87-113">A lehetséges értékek a következők: "Allow", "deny"</span><span class="sxs-lookup"><span data-stu-id="aec87-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="aec87-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="aec87-114">-CommunityList</span></span>
<span data-ttu-id="aec87-115">Annak a közösségi értéknek a listája, amelyre az útvonal-szűrő szűrést fog kiszűrni</span><span class="sxs-lookup"><span data-stu-id="aec87-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="aec87-116">-Force</span><span class="sxs-lookup"><span data-stu-id="aec87-116">-Force</span></span>
<span data-ttu-id="aec87-117">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="aec87-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="aec87-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aec87-118">-Name</span></span>
<span data-ttu-id="aec87-119">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="aec87-119">The name of the route filter rule</span></span>

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

### <span data-ttu-id="aec87-120">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="aec87-120">-RouteFilter</span></span>
<span data-ttu-id="aec87-121">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="aec87-121">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aec87-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="aec87-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="aec87-123">Az útvonal-szűrő szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="aec87-123">The route filter rule type of the rule.</span></span>
<span data-ttu-id="aec87-124">Lehetséges értékek: "Közösség"</span><span class="sxs-lookup"><span data-stu-id="aec87-124">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="aec87-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aec87-125">-Confirm</span></span>
<span data-ttu-id="aec87-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aec87-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec87-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec87-127">-WhatIf</span></span>
<span data-ttu-id="aec87-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aec87-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aec87-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aec87-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec87-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec87-130">-DefaultProfile</span></span>
<span data-ttu-id="aec87-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aec87-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aec87-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec87-132">CommonParameters</span></span>
<span data-ttu-id="aec87-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aec87-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec87-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec87-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec87-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aec87-135">INPUTS</span></span>

### <span data-ttu-id="aec87-136">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aec87-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="aec87-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aec87-137">OUTPUTS</span></span>

### <span data-ttu-id="aec87-138">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aec87-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="aec87-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aec87-139">NOTES</span></span>

## <span data-ttu-id="aec87-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aec87-140">RELATED LINKS</span></span>

