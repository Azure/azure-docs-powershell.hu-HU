---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195606"
---
# <span data-ttu-id="f4df9-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f4df9-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="f4df9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4df9-102">SYNOPSIS</span></span>
<span data-ttu-id="f4df9-103">Egyéni hibaüzenetet ad az alkalmazás-átjárók http-figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f4df9-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="f4df9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4df9-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4df9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4df9-105">DESCRIPTION</span></span>
<span data-ttu-id="f4df9-106">Az **Add-AzApplicationGatewayCustomError** parancsmag egyéni hibaüzenetet ad az alkalmazás-átjárók http-figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f4df9-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="f4df9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4df9-107">EXAMPLES</span></span>

### <span data-ttu-id="f4df9-108">1. példa: egyéni hiba hozzáadása a http-figyelők szintjéhez</span><span class="sxs-lookup"><span data-stu-id="f4df9-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f4df9-109">Ez a parancs hozzáadja a 502-as http-állapotkód egyéni hibáját a http-figyelőhöz $listener 01, és visszaadja a frissített figyelőt.</span><span class="sxs-lookup"><span data-stu-id="f4df9-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="f4df9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4df9-110">PARAMETERS</span></span>

### <span data-ttu-id="f4df9-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f4df9-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f4df9-112">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="f4df9-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f4df9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4df9-113">-DefaultProfile</span></span>
<span data-ttu-id="f4df9-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4df9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4df9-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f4df9-115">-HttpListener</span></span>
<span data-ttu-id="f4df9-116">Az alkalmazás-átjáró http-figyelése</span><span class="sxs-lookup"><span data-stu-id="f4df9-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4df9-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f4df9-117">-StatusCode</span></span>
<span data-ttu-id="f4df9-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="f4df9-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f4df9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4df9-119">CommonParameters</span></span>
<span data-ttu-id="f4df9-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4df9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4df9-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4df9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4df9-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4df9-122">INPUTS</span></span>

### <span data-ttu-id="f4df9-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f4df9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f4df9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4df9-124">OUTPUTS</span></span>

### <span data-ttu-id="f4df9-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f4df9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f4df9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4df9-126">NOTES</span></span>

## <span data-ttu-id="f4df9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4df9-127">RELATED LINKS</span></span>

[<span data-ttu-id="f4df9-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f4df9-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f4df9-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f4df9-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f4df9-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f4df9-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
