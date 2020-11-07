---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 8a0ce9d3e2c2a5272f6544b5c98ef763b9b288ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837886"
---
# <span data-ttu-id="7e787-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7e787-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="7e787-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e787-102">SYNOPSIS</span></span>
<span data-ttu-id="7e787-103">Az alkalmazás-átjárók http-figyelőkből származó egyéni hibák eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="7e787-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="7e787-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e787-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e787-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e787-105">DESCRIPTION</span></span>
<span data-ttu-id="7e787-106">A **Remove-AzApplicationGatewayCustomError** parancsmag az alkalmazás-átjárók http-figyelőkből származó egyéni hibát távolít el.</span><span class="sxs-lookup"><span data-stu-id="7e787-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="7e787-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7e787-107">EXAMPLES</span></span>

### <span data-ttu-id="7e787-108">Példa 1: egyéni hiba eltávolítása http-figyelőből</span><span class="sxs-lookup"><span data-stu-id="7e787-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="7e787-109">Ez a parancs eltávolítja a 502-as HTTP-figyelő egyéni hibáját a http-figyelőből $listener 01-ből, és visszaadja a frissített figyelőt.</span><span class="sxs-lookup"><span data-stu-id="7e787-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="7e787-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e787-110">PARAMETERS</span></span>

### <span data-ttu-id="7e787-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e787-111">-DefaultProfile</span></span>
<span data-ttu-id="7e787-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e787-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e787-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="7e787-113">-HttpListener</span></span>
<span data-ttu-id="7e787-114">Az alkalmazás-átjáró http-figyelése</span><span class="sxs-lookup"><span data-stu-id="7e787-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="7e787-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7e787-115">-StatusCode</span></span>
<span data-ttu-id="7e787-116">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="7e787-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7e787-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e787-117">CommonParameters</span></span>
<span data-ttu-id="7e787-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e787-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e787-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e787-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e787-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e787-120">INPUTS</span></span>

### <span data-ttu-id="7e787-121">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7e787-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7e787-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e787-122">OUTPUTS</span></span>

### <span data-ttu-id="7e787-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7e787-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7e787-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e787-124">NOTES</span></span>

## <span data-ttu-id="7e787-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e787-125">RELATED LINKS</span></span>

[<span data-ttu-id="7e787-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7e787-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="7e787-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7e787-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="7e787-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7e787-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
