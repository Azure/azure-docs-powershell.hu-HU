---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 990c9624d949fa695b815a9530125a90693816ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918697"
---
# <span data-ttu-id="c3d50-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3d50-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c3d50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3d50-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d50-103">Eltávolít egy egyéni hibát egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="c3d50-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="c3d50-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3d50-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3d50-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3d50-105">DESCRIPTION</span></span>
<span data-ttu-id="c3d50-106">A **Remove-AzApplicationGatewayCustomError** parancsmag eltávolít egy egyéni hibát egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="c3d50-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="c3d50-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3d50-107">EXAMPLES</span></span>

### <span data-ttu-id="c3d50-108">1. példa: Egyéni hiba eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="c3d50-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="c3d50-109">Ez a parancs eltávolítja az 502-es http állapotkód egyéni hibaüzenetét az alkalmazás-átjáró $appgw, és visszaadja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="c3d50-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="c3d50-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3d50-110">PARAMETERS</span></span>

### <span data-ttu-id="c3d50-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3d50-111">-ApplicationGateway</span></span>
<span data-ttu-id="c3d50-112">Az alkalmazás átjárója</span><span class="sxs-lookup"><span data-stu-id="c3d50-112">The Application Gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3d50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d50-113">-DefaultProfile</span></span>
<span data-ttu-id="c3d50-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3d50-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d50-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="c3d50-115">-StatusCode</span></span>
<span data-ttu-id="c3d50-116">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="c3d50-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c3d50-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d50-117">CommonParameters</span></span>
<span data-ttu-id="c3d50-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d50-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d50-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d50-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d50-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3d50-120">INPUTS</span></span>

### <span data-ttu-id="c3d50-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3d50-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3d50-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3d50-122">OUTPUTS</span></span>

### <span data-ttu-id="c3d50-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3d50-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c3d50-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3d50-124">NOTES</span></span>

## <span data-ttu-id="c3d50-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3d50-125">RELATED LINKS</span></span>

[<span data-ttu-id="c3d50-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3d50-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c3d50-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3d50-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c3d50-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3d50-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c3d50-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3d50-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
