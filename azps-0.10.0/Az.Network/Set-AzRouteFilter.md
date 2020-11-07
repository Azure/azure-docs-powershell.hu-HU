---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 942669106e70bbb8c5b5b6f059fe934effe9b7fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843578"
---
# <span data-ttu-id="3ba91-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3ba91-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="3ba91-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ba91-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba91-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="3ba91-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="3ba91-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ba91-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ba91-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ba91-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba91-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="3ba91-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="3ba91-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3ba91-107">EXAMPLES</span></span>

### <span data-ttu-id="3ba91-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3ba91-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3ba91-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="3ba91-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3ba91-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ba91-110">PARAMETERS</span></span>

### <span data-ttu-id="3ba91-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ba91-111">-AsJob</span></span>
<span data-ttu-id="3ba91-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3ba91-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ba91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba91-113">-DefaultProfile</span></span>
<span data-ttu-id="3ba91-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ba91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ba91-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3ba91-115">-Force</span></span>
<span data-ttu-id="3ba91-116">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="3ba91-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="3ba91-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3ba91-117">-RouteFilter</span></span>
<span data-ttu-id="3ba91-118">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3ba91-118">The RouteFilter</span></span>

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

### <span data-ttu-id="3ba91-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ba91-119">-Confirm</span></span>
<span data-ttu-id="3ba91-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ba91-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ba91-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ba91-121">-WhatIf</span></span>
<span data-ttu-id="3ba91-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ba91-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ba91-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ba91-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ba91-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba91-124">CommonParameters</span></span>
<span data-ttu-id="3ba91-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ba91-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba91-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ba91-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba91-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ba91-127">INPUTS</span></span>

### <span data-ttu-id="3ba91-128">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3ba91-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="3ba91-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ba91-129">OUTPUTS</span></span>

### <span data-ttu-id="3ba91-130">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3ba91-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="3ba91-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ba91-131">NOTES</span></span>

## <span data-ttu-id="3ba91-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ba91-132">RELATED LINKS</span></span>

