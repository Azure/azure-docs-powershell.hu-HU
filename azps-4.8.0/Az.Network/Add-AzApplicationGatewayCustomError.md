---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: e3bac58fca1c405aeef3366cb3ec1ee1b01a0891
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181612"
---
# <span data-ttu-id="fc726-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="fc726-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="fc726-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc726-102">SYNOPSIS</span></span>
<span data-ttu-id="fc726-103">Egyéni hibaüzenetet ad az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="fc726-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="fc726-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc726-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc726-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc726-105">DESCRIPTION</span></span>
<span data-ttu-id="fc726-106">Az **Add-AzApplicationGatewayCustomError** parancsmag egyéni hibaüzenetet ad egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="fc726-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="fc726-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc726-107">EXAMPLES</span></span>

### <span data-ttu-id="fc726-108">1. példa: egyéni hiba hozzáadása az Application Gateway szintjéhez</span><span class="sxs-lookup"><span data-stu-id="fc726-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="fc726-109">Ez a parancs a 502-as http-állapotkód egyéni hibáját adja hozzá az Application Gateway $appgwhez, és visszaadja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="fc726-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="fc726-110">2. példa: egyéni hiba hozzáadása az alkalmazás átjárójának figyelő szintjéhez</span><span class="sxs-lookup"><span data-stu-id="fc726-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
 $resourceGroupName = "resourceGroupName"
 $AppGWName = "applicationGatewayName"
 $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
 $listenerName = "listenerName"
 $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $resourceGroupName
 $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
 $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
 Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="fc726-111">Ez a parancs a 502-as http-állapotkód egyéni hibáját felveszi az Application Gateway-$appgw a figyelő szinten, és visszaadja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="fc726-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="fc726-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc726-112">PARAMETERS</span></span>

### <span data-ttu-id="fc726-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc726-113">-ApplicationGateway</span></span>
<span data-ttu-id="fc726-114">Az Application Gateway</span><span class="sxs-lookup"><span data-stu-id="fc726-114">The Application Gateway</span></span>

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

### <span data-ttu-id="fc726-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="fc726-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="fc726-116">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="fc726-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="fc726-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc726-117">-DefaultProfile</span></span>
<span data-ttu-id="fc726-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc726-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc726-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="fc726-119">-StatusCode</span></span>
<span data-ttu-id="fc726-120">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="fc726-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="fc726-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc726-121">CommonParameters</span></span>
<span data-ttu-id="fc726-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc726-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc726-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc726-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc726-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc726-124">INPUTS</span></span>

### <span data-ttu-id="fc726-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc726-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc726-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc726-126">OUTPUTS</span></span>

### <span data-ttu-id="fc726-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="fc726-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="fc726-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc726-128">NOTES</span></span>

## <span data-ttu-id="fc726-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc726-129">RELATED LINKS</span></span>

[<span data-ttu-id="fc726-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="fc726-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="fc726-131">Új – AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="fc726-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="fc726-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="fc726-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="fc726-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="fc726-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
