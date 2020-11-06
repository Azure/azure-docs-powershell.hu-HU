---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 94a4b4dc41aa1ae7c2a7bb2596018382296f5f87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495856"
---
# <span data-ttu-id="569e4-101">Set-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="569e4-101">Set-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="569e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="569e4-102">SYNOPSIS</span></span>
<span data-ttu-id="569e4-103">Az alkalmazás-átjárók egyéni hibáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="569e4-103">Updates a custom error in an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="569e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="569e4-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="569e4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="569e4-105">DESCRIPTION</span></span>
<span data-ttu-id="569e4-106">A **set-AzureRmApplicationGatewayCustomError** parancsmag egy egyéni hibaüzenetet frissít egy alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="569e4-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="569e4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="569e4-107">EXAMPLES</span></span>

### <span data-ttu-id="569e4-108">Példa 1: az alkalmazás-átjáró egyéni hibáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="569e4-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="569e4-109">Ez a parancs frissíti a 502-as http-állapotkód egyéni hibáját az Application Gateway $appgw, és a frissített átjárót számítja ki.</span><span class="sxs-lookup"><span data-stu-id="569e4-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="569e4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="569e4-110">PARAMETERS</span></span>

### <span data-ttu-id="569e4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="569e4-111">-ApplicationGateway</span></span>
<span data-ttu-id="569e4-112">Az Application Gateway</span><span class="sxs-lookup"><span data-stu-id="569e4-112">The Application Gateway</span></span>

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

### <span data-ttu-id="569e4-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="569e4-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="569e4-114">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="569e4-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="569e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569e4-115">-DefaultProfile</span></span>
<span data-ttu-id="569e4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="569e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="569e4-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="569e4-117">-StatusCode</span></span>
<span data-ttu-id="569e4-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="569e4-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="569e4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569e4-119">CommonParameters</span></span>
<span data-ttu-id="569e4-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="569e4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569e4-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="569e4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569e4-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="569e4-122">INPUTS</span></span>

### <span data-ttu-id="569e4-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="569e4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="569e4-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="569e4-124">OUTPUTS</span></span>

### <span data-ttu-id="569e4-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="569e4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="569e4-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="569e4-126">NOTES</span></span>

## <span data-ttu-id="569e4-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="569e4-127">RELATED LINKS</span></span>
