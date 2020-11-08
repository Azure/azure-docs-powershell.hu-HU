---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184089"
---
# <span data-ttu-id="3035d-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="3035d-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="3035d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3035d-102">SYNOPSIS</span></span>
<span data-ttu-id="3035d-103">Identitás eltávolítása egy ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3035d-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="3035d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3035d-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3035d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3035d-105">DESCRIPTION</span></span>
<span data-ttu-id="3035d-106">A **Remove-AzExpressRoutePortIdentity** parancsmag eltávolítja az identitást egy helyi Azure ExpressRoutePort-objektumból.</span><span class="sxs-lookup"><span data-stu-id="3035d-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="3035d-107">Távolítsa el a AzExpressRoutePort a ExpressRoutePort **-** ből.</span><span class="sxs-lookup"><span data-stu-id="3035d-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="3035d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3035d-108">EXAMPLES</span></span>

### <span data-ttu-id="3035d-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3035d-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="3035d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3035d-110">PARAMETERS</span></span>

### <span data-ttu-id="3035d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3035d-111">-DefaultProfile</span></span>
<span data-ttu-id="3035d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3035d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3035d-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3035d-113">-ExpressRoutePort</span></span>
<span data-ttu-id="3035d-114">A ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3035d-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3035d-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3035d-115">-Confirm</span></span>
<span data-ttu-id="3035d-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3035d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3035d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3035d-117">-WhatIf</span></span>
<span data-ttu-id="3035d-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3035d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3035d-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3035d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3035d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3035d-120">CommonParameters</span></span>
<span data-ttu-id="3035d-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3035d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3035d-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3035d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="3035d-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3035d-123">INPUTS</span></span>

### <span data-ttu-id="3035d-124">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3035d-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="3035d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3035d-125">OUTPUTS</span></span>

### <span data-ttu-id="3035d-126">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3035d-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="3035d-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3035d-127">NOTES</span></span>

## <span data-ttu-id="3035d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3035d-128">RELATED LINKS</span></span>
[<span data-ttu-id="3035d-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="3035d-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="3035d-130">Új – AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="3035d-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="3035d-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="3035d-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
