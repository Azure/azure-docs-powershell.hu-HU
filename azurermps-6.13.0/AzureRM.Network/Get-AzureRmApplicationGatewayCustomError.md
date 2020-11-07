---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b2f748bca68bff772026237f3bb6205ca6bc1923
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680054"
---
# <span data-ttu-id="93ae3-101">Get-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="93ae3-101">Get-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="93ae3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="93ae3-103">Egyéni hibák jelentkeznek egy alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="93ae3-103">Gets custom error(s) from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93ae3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93ae3-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93ae3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93ae3-105">DESCRIPTION</span></span>
<span data-ttu-id="93ae3-106">A **Get-AzureRmApplicationGatewayCustomError** parancsmag egyéni hibaüzeneteket kap egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="93ae3-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="93ae3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="93ae3-107">EXAMPLES</span></span>

### <span data-ttu-id="93ae3-108">Példa 1: egyéni hiba beolvasása egy alkalmazás-átjáróban</span><span class="sxs-lookup"><span data-stu-id="93ae3-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="93ae3-109">Ez a parancs a 502-ös http-állapotkód egyéni hibáját adja eredményül az Application Gateway $appgw.</span><span class="sxs-lookup"><span data-stu-id="93ae3-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="93ae3-110">2. példa: beolvassa az összes egyéni hiba listáját egy alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="93ae3-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="93ae3-111">Ez a parancs beolvassa és visszaadja az összes egyéni hiba listáját az Application Gateway $appgwból.</span><span class="sxs-lookup"><span data-stu-id="93ae3-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="93ae3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93ae3-112">PARAMETERS</span></span>

### <span data-ttu-id="93ae3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93ae3-113">-ApplicationGateway</span></span>
<span data-ttu-id="93ae3-114">Az Application Gateway</span><span class="sxs-lookup"><span data-stu-id="93ae3-114">The Application Gateway</span></span>

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

### <span data-ttu-id="93ae3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ae3-115">-DefaultProfile</span></span>
<span data-ttu-id="93ae3-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93ae3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93ae3-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="93ae3-117">-StatusCode</span></span>
<span data-ttu-id="93ae3-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="93ae3-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="93ae3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ae3-119">CommonParameters</span></span>
<span data-ttu-id="93ae3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93ae3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ae3-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ae3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ae3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93ae3-122">INPUTS</span></span>

### <span data-ttu-id="93ae3-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93ae3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93ae3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93ae3-124">OUTPUTS</span></span>

### <span data-ttu-id="93ae3-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="93ae3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="93ae3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93ae3-126">NOTES</span></span>

## <span data-ttu-id="93ae3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93ae3-127">RELATED LINKS</span></span>
