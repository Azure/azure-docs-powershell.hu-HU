---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 63d90b646b639d7978dfbf734256976f423a3092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919497"
---
# <span data-ttu-id="a0b1d-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a0b1d-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="a0b1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b1d-103">Egyéni hiba frissítése egy alkalmazás-átjáró http- hallgatója esetén.</span><span class="sxs-lookup"><span data-stu-id="a0b1d-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="a0b1d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a0b1d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0b1d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a0b1d-105">DESCRIPTION</span></span>
<span data-ttu-id="a0b1d-106">A **Set-AzApplicationGatewayCustomError** parancsmag egyéni hibát jelez egy alkalmazásátjáró http-füzetében.</span><span class="sxs-lookup"><span data-stu-id="a0b1d-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="a0b1d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a0b1d-107">EXAMPLES</span></span>

### <span data-ttu-id="a0b1d-108">1. példa: Egyéni hiba frissítése egy http-hallgatótól</span><span class="sxs-lookup"><span data-stu-id="a0b1d-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="a0b1d-109">Ez a parancs frissíti az 502-es http-állapotkódot a http$listener 01 kódban, és visszaadja a frissített hallgatót.</span><span class="sxs-lookup"><span data-stu-id="a0b1d-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="a0b1d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0b1d-110">PARAMETERS</span></span>

### <span data-ttu-id="a0b1d-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="a0b1d-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="a0b1d-112">Hibalap URL-címe az alkalmazás-átjáró ügyfélalkalmazásának hibaüzenetéhez.</span><span class="sxs-lookup"><span data-stu-id="a0b1d-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a0b1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b1d-113">-DefaultProfile</span></span>
<span data-ttu-id="a0b1d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0b1d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0b1d-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="a0b1d-115">-HttpListener</span></span>
<span data-ttu-id="a0b1d-116">The Application Gateway Http Listener</span><span class="sxs-lookup"><span data-stu-id="a0b1d-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="a0b1d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a0b1d-117">-StatusCode</span></span>
<span data-ttu-id="a0b1d-118">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="a0b1d-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a0b1d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b1d-119">CommonParameters</span></span>
<span data-ttu-id="a0b1d-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b1d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b1d-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b1d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b1d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0b1d-122">INPUTS</span></span>

### <span data-ttu-id="a0b1d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a0b1d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a0b1d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0b1d-124">OUTPUTS</span></span>

### <span data-ttu-id="a0b1d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a0b1d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a0b1d-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a0b1d-126">NOTES</span></span>

## <span data-ttu-id="a0b1d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0b1d-127">RELATED LINKS</span></span>

[<span data-ttu-id="a0b1d-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a0b1d-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="a0b1d-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a0b1d-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="a0b1d-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a0b1d-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
