---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: bcb0d59c564087e02cd152c1ae76f38c91f33e80
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843773"
---
# <span data-ttu-id="7c954-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c954-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="7c954-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c954-102">SYNOPSIS</span></span>
<span data-ttu-id="7c954-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="7c954-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="7c954-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c954-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c954-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c954-105">DESCRIPTION</span></span>
<span data-ttu-id="7c954-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="7c954-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7c954-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7c954-107">EXAMPLES</span></span>

### <span data-ttu-id="7c954-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7c954-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7c954-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="7c954-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="7c954-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c954-110">PARAMETERS</span></span>

### <span data-ttu-id="7c954-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c954-111">-DefaultProfile</span></span>
<span data-ttu-id="7c954-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c954-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c954-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7c954-113">-Force</span></span>
<span data-ttu-id="7c954-114">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="7c954-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="7c954-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c954-115">-Name</span></span>
<span data-ttu-id="7c954-116">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="7c954-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="7c954-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7c954-117">-RouteFilter</span></span>
<span data-ttu-id="7c954-118">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7c954-118">The RouteFilter</span></span>

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

### <span data-ttu-id="7c954-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7c954-119">-Confirm</span></span>
<span data-ttu-id="7c954-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c954-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c954-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c954-121">-WhatIf</span></span>
<span data-ttu-id="7c954-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7c954-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c954-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c954-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c954-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c954-124">CommonParameters</span></span>
<span data-ttu-id="7c954-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c954-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c954-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c954-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c954-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c954-127">INPUTS</span></span>

### <span data-ttu-id="7c954-128">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7c954-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7c954-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c954-129">OUTPUTS</span></span>

### <span data-ttu-id="7c954-130">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="7c954-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="7c954-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c954-131">NOTES</span></span>

## <span data-ttu-id="7c954-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c954-132">RELATED LINKS</span></span>

