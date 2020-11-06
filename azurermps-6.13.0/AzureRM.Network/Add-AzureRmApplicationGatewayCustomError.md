---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b56c358a208683e513844e36e561efa9e76cbede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493661"
---
# <span data-ttu-id="1c8de-101">Add-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1c8de-101">Add-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1c8de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c8de-102">SYNOPSIS</span></span>
<span data-ttu-id="1c8de-103">Egyéni hibaüzenetet ad az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="1c8de-103">Adds a custom error to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c8de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c8de-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c8de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c8de-105">DESCRIPTION</span></span>
<span data-ttu-id="1c8de-106">Az **Add-AzureRmApplicationGatewayCustomError** parancsmag egyéni hibaüzenetet ad egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="1c8de-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="1c8de-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1c8de-107">EXAMPLES</span></span>

### <span data-ttu-id="1c8de-108">1. példa: egyéni hiba hozzáadása az Application Gateway szintjéhez</span><span class="sxs-lookup"><span data-stu-id="1c8de-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="1c8de-109">Ez a parancs a 502-as http-állapotkód egyéni hibáját adja hozzá az Application Gateway $appgwhez, és visszaadja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="1c8de-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="1c8de-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c8de-110">PARAMETERS</span></span>

### <span data-ttu-id="1c8de-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c8de-111">-ApplicationGateway</span></span>
<span data-ttu-id="1c8de-112">Az Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1c8de-112">The Application Gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c8de-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="1c8de-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="1c8de-114">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="1c8de-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1c8de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c8de-115">-DefaultProfile</span></span>
<span data-ttu-id="1c8de-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c8de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8de-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1c8de-117">-StatusCode</span></span>
<span data-ttu-id="1c8de-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="1c8de-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1c8de-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c8de-119">CommonParameters</span></span>
<span data-ttu-id="1c8de-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c8de-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c8de-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c8de-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c8de-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c8de-122">INPUTS</span></span>

### <span data-ttu-id="1c8de-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c8de-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1c8de-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c8de-124">OUTPUTS</span></span>

### <span data-ttu-id="1c8de-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c8de-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1c8de-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c8de-126">NOTES</span></span>

## <span data-ttu-id="1c8de-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c8de-127">RELATED LINKS</span></span>
