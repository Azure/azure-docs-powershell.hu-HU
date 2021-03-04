---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 22644dca713ef234aec8be17c324faaf90eebf20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941650"
---
# <span data-ttu-id="5836b-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5836b-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="5836b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5836b-102">SYNOPSIS</span></span>
<span data-ttu-id="5836b-103">Eltávolít egy identitást az ExpressRoutePort-ból.</span><span class="sxs-lookup"><span data-stu-id="5836b-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="5836b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5836b-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5836b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5836b-105">DESCRIPTION</span></span>
<span data-ttu-id="5836b-106">A **Remove-AzExpressRoutePortIdentity** parancsmag eltávolítja az identitást egy helyi Azure ExpressRoutePort-objektumból.</span><span class="sxs-lookup"><span data-stu-id="5836b-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="5836b-107">Az **Remove-AzExpressRoutePort** segítségével távolítsa el az ExpressRoutePortból.</span><span class="sxs-lookup"><span data-stu-id="5836b-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="5836b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5836b-108">EXAMPLES</span></span>

### <span data-ttu-id="5836b-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="5836b-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="5836b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5836b-110">PARAMETERS</span></span>

### <span data-ttu-id="5836b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5836b-111">-DefaultProfile</span></span>
<span data-ttu-id="5836b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5836b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5836b-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5836b-113">-ExpressRoutePort</span></span>
<span data-ttu-id="5836b-114">Az ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5836b-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="5836b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5836b-115">-Confirm</span></span>
<span data-ttu-id="5836b-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5836b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5836b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5836b-117">-WhatIf</span></span>
<span data-ttu-id="5836b-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5836b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5836b-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5836b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5836b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5836b-120">CommonParameters</span></span>
<span data-ttu-id="5836b-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5836b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5836b-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5836b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="5836b-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5836b-123">INPUTS</span></span>

### <span data-ttu-id="5836b-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5836b-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="5836b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5836b-125">OUTPUTS</span></span>

### <span data-ttu-id="5836b-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5836b-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="5836b-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5836b-127">NOTES</span></span>

## <span data-ttu-id="5836b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5836b-128">RELATED LINKS</span></span>
[<span data-ttu-id="5836b-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5836b-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5836b-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5836b-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5836b-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5836b-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
