---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468941"
---
# <span data-ttu-id="5d750-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5d750-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="5d750-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d750-102">SYNOPSIS</span></span>
<span data-ttu-id="5d750-103">Eltávolít egy identitást az ExpressRoutePort-ból.</span><span class="sxs-lookup"><span data-stu-id="5d750-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="5d750-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d750-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d750-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d750-105">DESCRIPTION</span></span>
<span data-ttu-id="5d750-106">A **Remove-AzExpressRoutePortIdentity** parancsmag eltávolítja az identitást egy helyi Azure ExpressRoutePort-objektumból.</span><span class="sxs-lookup"><span data-stu-id="5d750-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="5d750-107">Az **Remove-AzExpressRoutePort** segítségével távolítsa el az ExpressRoutePortból.</span><span class="sxs-lookup"><span data-stu-id="5d750-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="5d750-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d750-108">EXAMPLES</span></span>

### <span data-ttu-id="5d750-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="5d750-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="5d750-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d750-110">PARAMETERS</span></span>

### <span data-ttu-id="5d750-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d750-111">-DefaultProfile</span></span>
<span data-ttu-id="5d750-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d750-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d750-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5d750-113">-ExpressRoutePort</span></span>
<span data-ttu-id="5d750-114">Az ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5d750-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="5d750-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d750-115">-Confirm</span></span>
<span data-ttu-id="5d750-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d750-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d750-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d750-117">-WhatIf</span></span>
<span data-ttu-id="5d750-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d750-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d750-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d750-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d750-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d750-120">CommonParameters</span></span>
<span data-ttu-id="5d750-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d750-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d750-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d750-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="5d750-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d750-123">INPUTS</span></span>

### <span data-ttu-id="5d750-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5d750-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="5d750-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d750-125">OUTPUTS</span></span>

### <span data-ttu-id="5d750-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5d750-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="5d750-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d750-127">NOTES</span></span>

## <span data-ttu-id="5d750-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d750-128">RELATED LINKS</span></span>
[<span data-ttu-id="5d750-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5d750-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5d750-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5d750-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5d750-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5d750-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
