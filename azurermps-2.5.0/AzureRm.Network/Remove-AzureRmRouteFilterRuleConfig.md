---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: d11de748c8c86c974b45ac2f171b5eb54b97ee6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849558"
---
# <span data-ttu-id="23d56-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="23d56-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="23d56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23d56-102">SYNOPSIS</span></span>
<span data-ttu-id="23d56-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="23d56-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23d56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23d56-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23d56-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23d56-105">DESCRIPTION</span></span>
<span data-ttu-id="23d56-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="23d56-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="23d56-107">Példák</span><span class="sxs-lookup"><span data-stu-id="23d56-107">EXAMPLES</span></span>

### <span data-ttu-id="23d56-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="23d56-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="23d56-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="23d56-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="23d56-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23d56-110">PARAMETERS</span></span>

### <span data-ttu-id="23d56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d56-111">-DefaultProfile</span></span>
<span data-ttu-id="23d56-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23d56-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23d56-113">-Force</span><span class="sxs-lookup"><span data-stu-id="23d56-113">-Force</span></span>
<span data-ttu-id="23d56-114">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="23d56-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="23d56-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23d56-115">-Name</span></span>
<span data-ttu-id="23d56-116">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="23d56-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="23d56-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="23d56-117">-RouteFilter</span></span>
<span data-ttu-id="23d56-118">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="23d56-118">The RouteFilter</span></span>

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

### <span data-ttu-id="23d56-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="23d56-119">-Confirm</span></span>
<span data-ttu-id="23d56-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23d56-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23d56-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d56-121">-WhatIf</span></span>
<span data-ttu-id="23d56-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="23d56-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23d56-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23d56-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23d56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d56-124">CommonParameters</span></span>
<span data-ttu-id="23d56-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23d56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d56-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d56-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d56-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23d56-127">INPUTS</span></span>

### <span data-ttu-id="23d56-128">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="23d56-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="23d56-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23d56-129">OUTPUTS</span></span>

### <span data-ttu-id="23d56-130">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="23d56-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="23d56-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23d56-131">NOTES</span></span>

## <span data-ttu-id="23d56-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23d56-132">RELATED LINKS</span></span>

