---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: d73fbe14e4b1d4c4ea34c7405ad7da5b7954ffd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503236"
---
# <span data-ttu-id="d60ee-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d60ee-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="d60ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d60ee-102">SYNOPSIS</span></span>
<span data-ttu-id="d60ee-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="d60ee-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d60ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d60ee-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d60ee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d60ee-105">DESCRIPTION</span></span>
<span data-ttu-id="d60ee-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="d60ee-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d60ee-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d60ee-107">EXAMPLES</span></span>

### <span data-ttu-id="d60ee-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d60ee-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d60ee-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="d60ee-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d60ee-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d60ee-110">PARAMETERS</span></span>

### <span data-ttu-id="d60ee-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d60ee-111">-Force</span></span>
<span data-ttu-id="d60ee-112">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="d60ee-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="d60ee-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d60ee-113">-Name</span></span>
<span data-ttu-id="d60ee-114">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="d60ee-114">The name of the route filter rule</span></span>

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

### <span data-ttu-id="d60ee-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d60ee-115">-RouteFilter</span></span>
<span data-ttu-id="d60ee-116">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d60ee-116">The RouteFilter</span></span>

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

### <span data-ttu-id="d60ee-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d60ee-117">-Confirm</span></span>
<span data-ttu-id="d60ee-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d60ee-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d60ee-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d60ee-119">-WhatIf</span></span>
<span data-ttu-id="d60ee-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d60ee-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d60ee-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d60ee-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d60ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d60ee-122">-DefaultProfile</span></span>
<span data-ttu-id="d60ee-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d60ee-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d60ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d60ee-124">CommonParameters</span></span>
<span data-ttu-id="d60ee-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d60ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d60ee-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d60ee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d60ee-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d60ee-127">INPUTS</span></span>

### <span data-ttu-id="d60ee-128">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d60ee-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d60ee-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d60ee-129">OUTPUTS</span></span>

### <span data-ttu-id="d60ee-130">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="d60ee-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="d60ee-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d60ee-131">NOTES</span></span>

## <span data-ttu-id="d60ee-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d60ee-132">RELATED LINKS</span></span>

