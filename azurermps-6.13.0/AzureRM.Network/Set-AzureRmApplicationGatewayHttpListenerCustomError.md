---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: cb54299a1d3c06f9416ed574588a1bc77d9993a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671964"
---
# <span data-ttu-id="47f52-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="47f52-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="47f52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47f52-102">SYNOPSIS</span></span>
<span data-ttu-id="47f52-103">Egy egyéni hibaüzenetet frissít az alkalmazás-átjárók http-figyelőkben.</span><span class="sxs-lookup"><span data-stu-id="47f52-103">Updates a custom error in a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47f52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47f52-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47f52-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="47f52-105">DESCRIPTION</span></span>
<span data-ttu-id="47f52-106">A **set-AzureRmApplicationGatewayCustomError** parancsmag az alkalmazás-átjárók http-figyelők egyéni hibáit frissíti.</span><span class="sxs-lookup"><span data-stu-id="47f52-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="47f52-107">Példák</span><span class="sxs-lookup"><span data-stu-id="47f52-107">EXAMPLES</span></span>

### <span data-ttu-id="47f52-108">Példa 1: a http-figyelők egyéni hibáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="47f52-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="47f52-109">Ez a parancs frissíti a 502-as http-figyelőben az egyéni hibáját a http-$listener figyelőben, és a frissített figyelőt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="47f52-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="47f52-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47f52-110">PARAMETERS</span></span>

### <span data-ttu-id="47f52-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="47f52-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="47f52-112">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="47f52-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="47f52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f52-113">-DefaultProfile</span></span>
<span data-ttu-id="47f52-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47f52-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47f52-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="47f52-115">-HttpListener</span></span>
<span data-ttu-id="47f52-116">Az alkalmazás-átjáró http-figyelése</span><span class="sxs-lookup"><span data-stu-id="47f52-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="47f52-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="47f52-117">-StatusCode</span></span>
<span data-ttu-id="47f52-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="47f52-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="47f52-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f52-119">CommonParameters</span></span>
<span data-ttu-id="47f52-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47f52-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="47f52-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47f52-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f52-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47f52-122">INPUTS</span></span>

### <span data-ttu-id="47f52-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="47f52-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="47f52-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47f52-124">OUTPUTS</span></span>

### <span data-ttu-id="47f52-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="47f52-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="47f52-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47f52-126">NOTES</span></span>

## <span data-ttu-id="47f52-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47f52-127">RELATED LINKS</span></span>
