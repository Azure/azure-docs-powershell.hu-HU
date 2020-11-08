---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013552"
---
# <span data-ttu-id="3483d-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="3483d-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="3483d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3483d-102">SYNOPSIS</span></span>
<span data-ttu-id="3483d-103">Egyéni hibák jelentkeznek az alkalmazás-átjárók http-figyelőben.</span><span class="sxs-lookup"><span data-stu-id="3483d-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="3483d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3483d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3483d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3483d-105">DESCRIPTION</span></span>
<span data-ttu-id="3483d-106">A **Get-AzApplicationGatewayCustomError** parancsmag egyéni hibaüzeneteket kap egy alkalmazás-átjáró http-figyelője alapján.</span><span class="sxs-lookup"><span data-stu-id="3483d-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="3483d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3483d-107">EXAMPLES</span></span>

### <span data-ttu-id="3483d-108">Példa 1: egyéni hiba beolvasása http-figyelőben</span><span class="sxs-lookup"><span data-stu-id="3483d-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="3483d-109">Ez a parancs a HTTP-figyelő $listener 01-es 502 verziójának egyéni hibáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3483d-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="3483d-110">2. példa: beolvassa a http-figyelők minden egyéni hibájának listáját.</span><span class="sxs-lookup"><span data-stu-id="3483d-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="3483d-111">Ez a parancs a HTTP-figyelő $listener 01-es verziójában található összes egyéni hiba listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3483d-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="3483d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3483d-112">PARAMETERS</span></span>

### <span data-ttu-id="3483d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3483d-113">-DefaultProfile</span></span>
<span data-ttu-id="3483d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3483d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3483d-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="3483d-115">-HttpListener</span></span>
<span data-ttu-id="3483d-116">Az alkalmazás-átjáró http-figyelése</span><span class="sxs-lookup"><span data-stu-id="3483d-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="3483d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="3483d-117">-StatusCode</span></span>
<span data-ttu-id="3483d-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="3483d-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3483d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3483d-119">CommonParameters</span></span>
<span data-ttu-id="3483d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3483d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3483d-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3483d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3483d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3483d-122">INPUTS</span></span>

### <span data-ttu-id="3483d-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3483d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3483d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3483d-124">OUTPUTS</span></span>

### <span data-ttu-id="3483d-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3483d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3483d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3483d-126">NOTES</span></span>

## <span data-ttu-id="3483d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3483d-127">RELATED LINKS</span></span>

[<span data-ttu-id="3483d-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="3483d-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="3483d-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="3483d-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="3483d-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="3483d-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
