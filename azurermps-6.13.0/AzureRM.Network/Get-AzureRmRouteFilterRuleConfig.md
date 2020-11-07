---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 96122c68317166f078d40be8cee9d0124c4d713e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672598"
---
# <span data-ttu-id="374e2-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="374e2-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="374e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="374e2-102">SYNOPSIS</span></span>
<span data-ttu-id="374e2-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="374e2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="374e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="374e2-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="374e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="374e2-105">DESCRIPTION</span></span>
<span data-ttu-id="374e2-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="374e2-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="374e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="374e2-107">EXAMPLES</span></span>

### <span data-ttu-id="374e2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="374e2-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="374e2-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="374e2-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="374e2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="374e2-110">PARAMETERS</span></span>

### <span data-ttu-id="374e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="374e2-111">-DefaultProfile</span></span>
<span data-ttu-id="374e2-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="374e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="374e2-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="374e2-113">-Name</span></span>
<span data-ttu-id="374e2-114">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="374e2-114">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374e2-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="374e2-115">-RouteFilter</span></span>
<span data-ttu-id="374e2-116">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="374e2-116">The RouteFilter</span></span>

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

### <span data-ttu-id="374e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="374e2-117">CommonParameters</span></span>
<span data-ttu-id="374e2-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="374e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="374e2-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="374e2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="374e2-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="374e2-120">INPUTS</span></span>

### <span data-ttu-id="374e2-121">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="374e2-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="374e2-122">Paraméterek: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="374e2-122">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="374e2-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="374e2-123">OUTPUTS</span></span>

### <span data-ttu-id="374e2-124">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="374e2-124">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="374e2-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="374e2-125">NOTES</span></span>

## <span data-ttu-id="374e2-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="374e2-126">RELATED LINKS</span></span>
