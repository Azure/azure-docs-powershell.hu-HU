---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 00e82a9bc0f1708edcf3498369e630bb3b3f7885
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841522"
---
# <span data-ttu-id="b436f-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b436f-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b436f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b436f-102">SYNOPSIS</span></span>
<span data-ttu-id="b436f-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="b436f-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="b436f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b436f-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b436f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b436f-105">DESCRIPTION</span></span>
<span data-ttu-id="b436f-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="b436f-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="b436f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b436f-107">EXAMPLES</span></span>

### <span data-ttu-id="b436f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b436f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b436f-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="b436f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b436f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b436f-110">PARAMETERS</span></span>

### <span data-ttu-id="b436f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b436f-111">-DefaultProfile</span></span>
<span data-ttu-id="b436f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b436f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b436f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b436f-113">-Name</span></span>
<span data-ttu-id="b436f-114">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="b436f-114">The name of the route filter rule</span></span>

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

### <span data-ttu-id="b436f-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b436f-115">-RouteFilter</span></span>
<span data-ttu-id="b436f-116">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b436f-116">The RouteFilter</span></span>

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

### <span data-ttu-id="b436f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b436f-117">CommonParameters</span></span>
<span data-ttu-id="b436f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b436f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b436f-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b436f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b436f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b436f-120">INPUTS</span></span>

### <span data-ttu-id="b436f-121">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b436f-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b436f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b436f-122">OUTPUTS</span></span>

### <span data-ttu-id="b436f-123">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="b436f-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="b436f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b436f-124">NOTES</span></span>

## <span data-ttu-id="b436f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b436f-125">RELATED LINKS</span></span>

