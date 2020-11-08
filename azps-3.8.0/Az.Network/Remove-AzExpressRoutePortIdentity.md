---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014050"
---
# <span data-ttu-id="19b2f-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="19b2f-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="19b2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="19b2f-103">Identitás eltávolítása egy ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="19b2f-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="19b2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19b2f-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19b2f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="19b2f-106">A **Remove-AzExpressRoutePortIdentity** parancsmag eltávolítja az identitást egy helyi Azure ExpressRoutePort-objektumból.</span><span class="sxs-lookup"><span data-stu-id="19b2f-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="19b2f-107">Távolítsa el a AzExpressRoutePort a ExpressRoutePort **-** ből.</span><span class="sxs-lookup"><span data-stu-id="19b2f-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="19b2f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="19b2f-108">EXAMPLES</span></span>

### <span data-ttu-id="19b2f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19b2f-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="19b2f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19b2f-110">PARAMETERS</span></span>

### <span data-ttu-id="19b2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b2f-111">-DefaultProfile</span></span>
<span data-ttu-id="19b2f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19b2f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19b2f-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="19b2f-113">-ExpressRoutePort</span></span>
<span data-ttu-id="19b2f-114">A ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="19b2f-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="19b2f-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19b2f-115">-Confirm</span></span>
<span data-ttu-id="19b2f-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19b2f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19b2f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19b2f-117">-WhatIf</span></span>
<span data-ttu-id="19b2f-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19b2f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19b2f-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19b2f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19b2f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b2f-120">CommonParameters</span></span>
<span data-ttu-id="19b2f-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19b2f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b2f-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b2f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="19b2f-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19b2f-123">INPUTS</span></span>

### <span data-ttu-id="19b2f-124">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="19b2f-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="19b2f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19b2f-125">OUTPUTS</span></span>

### <span data-ttu-id="19b2f-126">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="19b2f-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="19b2f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19b2f-127">NOTES</span></span>

## <span data-ttu-id="19b2f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19b2f-128">RELATED LINKS</span></span>
[<span data-ttu-id="19b2f-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="19b2f-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="19b2f-130">Új – AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="19b2f-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="19b2f-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="19b2f-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
