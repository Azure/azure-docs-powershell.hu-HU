---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 1091a8433cd226982d3f2addf7e02b2414020fe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503039"
---
# <span data-ttu-id="c3525-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c3525-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="c3525-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3525-102">SYNOPSIS</span></span>
<span data-ttu-id="c3525-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="c3525-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3525-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3525-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3525-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3525-105">DESCRIPTION</span></span>
<span data-ttu-id="c3525-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="c3525-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c3525-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c3525-107">EXAMPLES</span></span>

### <span data-ttu-id="c3525-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c3525-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c3525-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="c3525-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c3525-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3525-110">PARAMETERS</span></span>

### <span data-ttu-id="c3525-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3525-111">-AsJob</span></span>
<span data-ttu-id="c3525-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c3525-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3525-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3525-113">-DefaultProfile</span></span>
<span data-ttu-id="c3525-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3525-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3525-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c3525-115">-Force</span></span>
<span data-ttu-id="c3525-116">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="c3525-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="c3525-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c3525-117">-RouteFilter</span></span>
<span data-ttu-id="c3525-118">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c3525-118">The RouteFilter</span></span>

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

### <span data-ttu-id="c3525-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3525-119">-Confirm</span></span>
<span data-ttu-id="c3525-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3525-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3525-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3525-121">-WhatIf</span></span>
<span data-ttu-id="c3525-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3525-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3525-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3525-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3525-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3525-124">CommonParameters</span></span>
<span data-ttu-id="c3525-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3525-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3525-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3525-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3525-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3525-127">INPUTS</span></span>

### <span data-ttu-id="c3525-128">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c3525-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c3525-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3525-129">OUTPUTS</span></span>

### <span data-ttu-id="c3525-130">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c3525-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c3525-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3525-131">NOTES</span></span>

## <span data-ttu-id="c3525-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3525-132">RELATED LINKS</span></span>

