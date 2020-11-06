---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: cc1f6b487d0faf58999a0326a77e01bea74d8c91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493638"
---
# <span data-ttu-id="8d111-101">Remove-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8d111-101">Remove-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="8d111-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d111-102">SYNOPSIS</span></span>
<span data-ttu-id="8d111-103">Eltávolít egy egyéni hibaüzenetet egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="8d111-103">Removes a custom error from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d111-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d111-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d111-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d111-105">DESCRIPTION</span></span>
<span data-ttu-id="8d111-106">A **Remove-AzureRmApplicationGatewayCustomError** parancsmag egy egyéni hibaüzenetet távolít el egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="8d111-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="8d111-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8d111-107">EXAMPLES</span></span>

### <span data-ttu-id="8d111-108">1. példa: az egyéni hiba eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="8d111-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="8d111-109">Ez a parancs eltávolítja a 502-as http-állapotkód egyéni hibáját az Application Gateway $appgwból, és visszaadja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="8d111-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="8d111-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d111-110">PARAMETERS</span></span>

### <span data-ttu-id="8d111-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d111-111">-ApplicationGateway</span></span>
<span data-ttu-id="8d111-112">Az Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8d111-112">The Application Gateway</span></span>

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

### <span data-ttu-id="8d111-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d111-113">-DefaultProfile</span></span>
<span data-ttu-id="8d111-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d111-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d111-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="8d111-115">-StatusCode</span></span>
<span data-ttu-id="8d111-116">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="8d111-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="8d111-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d111-117">CommonParameters</span></span>
<span data-ttu-id="8d111-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d111-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d111-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d111-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d111-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d111-120">INPUTS</span></span>

### <span data-ttu-id="8d111-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d111-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d111-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d111-122">OUTPUTS</span></span>

### <span data-ttu-id="8d111-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d111-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d111-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d111-124">NOTES</span></span>

## <span data-ttu-id="8d111-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d111-125">RELATED LINKS</span></span>
