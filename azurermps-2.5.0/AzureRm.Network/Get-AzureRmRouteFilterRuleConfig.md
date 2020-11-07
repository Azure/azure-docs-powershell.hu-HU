---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: f3b641e3e9229706f3010e7db95480423b06361c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848777"
---
# <span data-ttu-id="27d39-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27d39-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="27d39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27d39-102">SYNOPSIS</span></span>
<span data-ttu-id="27d39-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="27d39-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27d39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27d39-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27d39-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="27d39-105">DESCRIPTION</span></span>
<span data-ttu-id="27d39-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="27d39-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="27d39-107">Példák</span><span class="sxs-lookup"><span data-stu-id="27d39-107">EXAMPLES</span></span>

### <span data-ttu-id="27d39-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="27d39-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="27d39-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="27d39-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="27d39-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27d39-110">PARAMETERS</span></span>

### <span data-ttu-id="27d39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d39-111">-DefaultProfile</span></span>
<span data-ttu-id="27d39-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27d39-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27d39-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27d39-113">-Name</span></span>
<span data-ttu-id="27d39-114">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="27d39-114">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d39-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="27d39-115">-RouteFilter</span></span>
<span data-ttu-id="27d39-116">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="27d39-116">The RouteFilter</span></span>

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

### <span data-ttu-id="27d39-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d39-117">CommonParameters</span></span>
<span data-ttu-id="27d39-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27d39-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d39-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27d39-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d39-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27d39-120">INPUTS</span></span>

### <span data-ttu-id="27d39-121">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="27d39-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="27d39-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27d39-122">OUTPUTS</span></span>

### <span data-ttu-id="27d39-123">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="27d39-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="27d39-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27d39-124">NOTES</span></span>

## <span data-ttu-id="27d39-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27d39-125">RELATED LINKS</span></span>

