---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 56f0c3ec3a69819ad7faa28b10d33a3cf751c48f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494801"
---
# <span data-ttu-id="fe0a8-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe0a8-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="fe0a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0a8-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="fe0a8-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe0a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe0a8-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe0a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe0a8-105">DESCRIPTION</span></span>
<span data-ttu-id="fe0a8-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="fe0a8-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="fe0a8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fe0a8-107">EXAMPLES</span></span>

### <span data-ttu-id="fe0a8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fe0a8-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fe0a8-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="fe0a8-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="fe0a8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe0a8-110">PARAMETERS</span></span>

### <span data-ttu-id="fe0a8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fe0a8-111">-Force</span></span>
<span data-ttu-id="fe0a8-112">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="fe0a8-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="fe0a8-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe0a8-113">-RouteFilter</span></span>
<span data-ttu-id="fe0a8-114">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe0a8-114">The RouteFilter</span></span>

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

### <span data-ttu-id="fe0a8-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe0a8-115">-Confirm</span></span>
<span data-ttu-id="fe0a8-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe0a8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0a8-117">-WhatIf</span></span>
<span data-ttu-id="fe0a8-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe0a8-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe0a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0a8-120">-DefaultProfile</span></span>
<span data-ttu-id="fe0a8-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe0a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0a8-122">CommonParameters</span></span>
<span data-ttu-id="fe0a8-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe0a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0a8-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe0a8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0a8-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe0a8-125">INPUTS</span></span>

### <span data-ttu-id="fe0a8-126">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe0a8-126">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="fe0a8-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe0a8-127">OUTPUTS</span></span>

### <span data-ttu-id="fe0a8-128">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe0a8-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="fe0a8-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe0a8-129">NOTES</span></span>

## <span data-ttu-id="fe0a8-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe0a8-130">RELATED LINKS</span></span>

