---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 8718d79abef18217a727916d36c09e19de2a2de4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837417"
---
# <span data-ttu-id="d2027-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d2027-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="d2027-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2027-102">SYNOPSIS</span></span>
<span data-ttu-id="d2027-103">Egyéni hibaüzenetet ad az alkalmazás-átjárók http-figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="d2027-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="d2027-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2027-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2027-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2027-105">DESCRIPTION</span></span>
<span data-ttu-id="d2027-106">Az **Add-AzApplicationGatewayCustomError** parancsmag egyéni hibaüzenetet ad az alkalmazás-átjárók http-figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="d2027-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="d2027-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d2027-107">EXAMPLES</span></span>

### <span data-ttu-id="d2027-108">1. példa: egyéni hiba hozzáadása a http-figyelők szintjéhez</span><span class="sxs-lookup"><span data-stu-id="d2027-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="d2027-109">Ez a parancs hozzáadja a 502-as http-állapotkód egyéni hibáját a http-figyelőhöz $listener 01, és visszaadja a frissített figyelőt.</span><span class="sxs-lookup"><span data-stu-id="d2027-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="d2027-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2027-110">PARAMETERS</span></span>

### <span data-ttu-id="d2027-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="d2027-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="d2027-112">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="d2027-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="d2027-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2027-113">-DefaultProfile</span></span>
<span data-ttu-id="d2027-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2027-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2027-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="d2027-115">-HttpListener</span></span>
<span data-ttu-id="d2027-116">Az alkalmazás-átjáró http-figyelése</span><span class="sxs-lookup"><span data-stu-id="d2027-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="d2027-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="d2027-117">-StatusCode</span></span>
<span data-ttu-id="d2027-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="d2027-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="d2027-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2027-119">CommonParameters</span></span>
<span data-ttu-id="d2027-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2027-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2027-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2027-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2027-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2027-122">INPUTS</span></span>

### <span data-ttu-id="d2027-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d2027-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d2027-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2027-124">OUTPUTS</span></span>

### <span data-ttu-id="d2027-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d2027-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="d2027-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2027-126">NOTES</span></span>

## <span data-ttu-id="d2027-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2027-127">RELATED LINKS</span></span>

[<span data-ttu-id="d2027-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d2027-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="d2027-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d2027-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="d2027-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d2027-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
