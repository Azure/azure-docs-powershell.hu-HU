---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012040"
---
# <span data-ttu-id="f1379-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1379-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f1379-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1379-102">SYNOPSIS</span></span>
<span data-ttu-id="f1379-103">Eltávolít egy egyéni hibaüzenetet egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="f1379-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="f1379-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1379-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1379-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1379-105">DESCRIPTION</span></span>
<span data-ttu-id="f1379-106">A **Remove-AzApplicationGatewayCustomError** parancsmag egy egyéni hibaüzenetet távolít el egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="f1379-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="f1379-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1379-107">EXAMPLES</span></span>

### <span data-ttu-id="f1379-108">1. példa: az egyéni hiba eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="f1379-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="f1379-109">Ez a parancs eltávolítja a 502-as http-állapotkód egyéni hibáját az Application Gateway $appgwból, és visszaadja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="f1379-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="f1379-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1379-110">PARAMETERS</span></span>

### <span data-ttu-id="f1379-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1379-111">-ApplicationGateway</span></span>
<span data-ttu-id="f1379-112">Az Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f1379-112">The Application Gateway</span></span>

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

### <span data-ttu-id="f1379-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1379-113">-DefaultProfile</span></span>
<span data-ttu-id="f1379-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1379-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1379-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f1379-115">-StatusCode</span></span>
<span data-ttu-id="f1379-116">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="f1379-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f1379-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1379-117">CommonParameters</span></span>
<span data-ttu-id="f1379-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1379-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1379-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1379-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1379-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1379-120">INPUTS</span></span>

### <span data-ttu-id="f1379-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1379-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1379-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1379-122">OUTPUTS</span></span>

### <span data-ttu-id="f1379-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1379-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f1379-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1379-124">NOTES</span></span>

## <span data-ttu-id="f1379-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1379-125">RELATED LINKS</span></span>

[<span data-ttu-id="f1379-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1379-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f1379-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1379-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f1379-128">Új – AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1379-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f1379-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1379-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
