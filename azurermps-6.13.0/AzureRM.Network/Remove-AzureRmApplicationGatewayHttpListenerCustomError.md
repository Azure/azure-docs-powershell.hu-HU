---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493634"
---
# <span data-ttu-id="dfa39-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dfa39-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="dfa39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfa39-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa39-103">Az alkalmazás-átjárók http-figyelőkből származó egyéni hibák eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="dfa39-103">Removes a custom error from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfa39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfa39-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfa39-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfa39-105">DESCRIPTION</span></span>
<span data-ttu-id="dfa39-106">A **Remove-AzureRmApplicationGatewayCustomError** parancsmag az alkalmazás-átjárók http-figyelőkből származó egyéni hibát távolít el.</span><span class="sxs-lookup"><span data-stu-id="dfa39-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="dfa39-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dfa39-107">EXAMPLES</span></span>

### <span data-ttu-id="dfa39-108">Példa 1: egyéni hiba eltávolítása http-figyelőből</span><span class="sxs-lookup"><span data-stu-id="dfa39-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="dfa39-109">Ez a parancs eltávolítja a 502-as HTTP-figyelő egyéni hibáját a http-figyelőből $listener 01-ből, és visszaadja a frissített figyelőt.</span><span class="sxs-lookup"><span data-stu-id="dfa39-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="dfa39-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfa39-110">PARAMETERS</span></span>

### <span data-ttu-id="dfa39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa39-111">-DefaultProfile</span></span>
<span data-ttu-id="dfa39-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfa39-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa39-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="dfa39-113">-HttpListener</span></span>
<span data-ttu-id="dfa39-114">Az alkalmazás-átjáró http-figyelése</span><span class="sxs-lookup"><span data-stu-id="dfa39-114">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa39-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="dfa39-115">-StatusCode</span></span>
<span data-ttu-id="dfa39-116">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="dfa39-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa39-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa39-117">CommonParameters</span></span>
<span data-ttu-id="dfa39-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfa39-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dfa39-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfa39-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa39-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfa39-120">INPUTS</span></span>

### <span data-ttu-id="dfa39-121">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dfa39-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="dfa39-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfa39-122">OUTPUTS</span></span>

### <span data-ttu-id="dfa39-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dfa39-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="dfa39-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfa39-124">NOTES</span></span>

## <span data-ttu-id="dfa39-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfa39-125">RELATED LINKS</span></span>
