---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195335"
---
# <span data-ttu-id="28639-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="28639-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="28639-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28639-102">SYNOPSIS</span></span>
<span data-ttu-id="28639-103">Egy egyéni hibaüzenetet frissít az alkalmazás-átjárók http-figyelőkben.</span><span class="sxs-lookup"><span data-stu-id="28639-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="28639-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28639-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28639-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="28639-105">DESCRIPTION</span></span>
<span data-ttu-id="28639-106">A **set-AzApplicationGatewayCustomError** parancsmag az alkalmazás-átjárók http-figyelők egyéni hibáit frissíti.</span><span class="sxs-lookup"><span data-stu-id="28639-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="28639-107">Példák</span><span class="sxs-lookup"><span data-stu-id="28639-107">EXAMPLES</span></span>

### <span data-ttu-id="28639-108">Példa 1: a http-figyelők egyéni hibáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="28639-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="28639-109">Ez a parancs frissíti a 502-as http-figyelőben az egyéni hibáját a http-$listener figyelőben, és a frissített figyelőt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="28639-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="28639-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28639-110">PARAMETERS</span></span>

### <span data-ttu-id="28639-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="28639-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="28639-112">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="28639-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="28639-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28639-113">-DefaultProfile</span></span>
<span data-ttu-id="28639-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28639-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28639-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="28639-115">-HttpListener</span></span>
<span data-ttu-id="28639-116">Az alkalmazás-átjáró http-figyelése</span><span class="sxs-lookup"><span data-stu-id="28639-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="28639-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="28639-117">-StatusCode</span></span>
<span data-ttu-id="28639-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="28639-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="28639-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28639-119">CommonParameters</span></span>
<span data-ttu-id="28639-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28639-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28639-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28639-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28639-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28639-122">INPUTS</span></span>

### <span data-ttu-id="28639-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="28639-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="28639-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28639-124">OUTPUTS</span></span>

### <span data-ttu-id="28639-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="28639-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="28639-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28639-126">NOTES</span></span>

## <span data-ttu-id="28639-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28639-127">RELATED LINKS</span></span>

[<span data-ttu-id="28639-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="28639-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="28639-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="28639-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="28639-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="28639-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)