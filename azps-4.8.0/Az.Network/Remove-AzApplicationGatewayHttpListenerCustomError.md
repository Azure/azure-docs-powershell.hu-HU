---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025162"
---
# <span data-ttu-id="f8e28-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f8e28-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="f8e28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8e28-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e28-103">Az alkalmazás-átjárók http-figyelőkből származó egyéni hibák eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f8e28-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="f8e28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8e28-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8e28-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8e28-105">DESCRIPTION</span></span>
<span data-ttu-id="f8e28-106">A **Remove-AzApplicationGatewayCustomError** parancsmag az alkalmazás-átjárók http-figyelőkből származó egyéni hibát távolít el.</span><span class="sxs-lookup"><span data-stu-id="f8e28-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="f8e28-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f8e28-107">EXAMPLES</span></span>

### <span data-ttu-id="f8e28-108">Példa 1: egyéni hiba eltávolítása http-figyelőből</span><span class="sxs-lookup"><span data-stu-id="f8e28-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="f8e28-109">Ez a parancs eltávolítja a 502-as HTTP-figyelő egyéni hibáját a http-figyelőből $listener 01-ből, és visszaadja a frissített figyelőt.</span><span class="sxs-lookup"><span data-stu-id="f8e28-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="f8e28-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8e28-110">PARAMETERS</span></span>

### <span data-ttu-id="f8e28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e28-111">-DefaultProfile</span></span>
<span data-ttu-id="f8e28-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8e28-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8e28-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f8e28-113">-HttpListener</span></span>
<span data-ttu-id="f8e28-114">Az alkalmazás-átjáró http-figyelése</span><span class="sxs-lookup"><span data-stu-id="f8e28-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="f8e28-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f8e28-115">-StatusCode</span></span>
<span data-ttu-id="f8e28-116">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="f8e28-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f8e28-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e28-117">CommonParameters</span></span>
<span data-ttu-id="f8e28-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8e28-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e28-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e28-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e28-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8e28-120">INPUTS</span></span>

### <span data-ttu-id="f8e28-121">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f8e28-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f8e28-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8e28-122">OUTPUTS</span></span>

### <span data-ttu-id="f8e28-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f8e28-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f8e28-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8e28-124">NOTES</span></span>

## <span data-ttu-id="f8e28-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8e28-125">RELATED LINKS</span></span>

[<span data-ttu-id="f8e28-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f8e28-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f8e28-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f8e28-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f8e28-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f8e28-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
