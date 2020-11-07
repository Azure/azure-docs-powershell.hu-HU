---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 23cb65073f25f65a4e09f3b4a28891cff4e49c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680065"
---
# <span data-ttu-id="20c7d-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="20c7d-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="20c7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="20c7d-103">Egyéni hibaüzenetet ad az alkalmazás-átjárók http-figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="20c7d-103">Adds a custom error to a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20c7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20c7d-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20c7d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="20c7d-106">Az **Add-AzureRmApplicationGatewayCustomError** parancsmag egyéni hibaüzenetet ad az alkalmazás-átjárók http-figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="20c7d-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="20c7d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="20c7d-107">EXAMPLES</span></span>

### <span data-ttu-id="20c7d-108">1. példa: egyéni hiba hozzáadása a http-figyelők szintjéhez</span><span class="sxs-lookup"><span data-stu-id="20c7d-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="20c7d-109">Ez a parancs hozzáadja a 502-as http-állapotkód egyéni hibáját a http-figyelőhöz $listener 01, és visszaadja a frissített figyelőt.</span><span class="sxs-lookup"><span data-stu-id="20c7d-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="20c7d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20c7d-110">PARAMETERS</span></span>

### <span data-ttu-id="20c7d-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="20c7d-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="20c7d-112">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="20c7d-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="20c7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c7d-113">-DefaultProfile</span></span>
<span data-ttu-id="20c7d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20c7d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c7d-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="20c7d-115">-HttpListener</span></span>
<span data-ttu-id="20c7d-116">Az alkalmazás-átjáró http-figyelése</span><span class="sxs-lookup"><span data-stu-id="20c7d-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="20c7d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="20c7d-117">-StatusCode</span></span>
<span data-ttu-id="20c7d-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="20c7d-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="20c7d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c7d-119">CommonParameters</span></span>
<span data-ttu-id="20c7d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20c7d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="20c7d-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c7d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c7d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20c7d-122">INPUTS</span></span>

### <span data-ttu-id="20c7d-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="20c7d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="20c7d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20c7d-124">OUTPUTS</span></span>

### <span data-ttu-id="20c7d-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="20c7d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="20c7d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20c7d-126">NOTES</span></span>

## <span data-ttu-id="20c7d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20c7d-127">RELATED LINKS</span></span>
