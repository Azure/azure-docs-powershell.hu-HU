---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 89e323bd8e8dedbaa3c7716a6c10119a6fb69365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495956"
---
# <span data-ttu-id="341aa-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="341aa-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="341aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="341aa-102">SYNOPSIS</span></span>
<span data-ttu-id="341aa-103">Egyéni hibák jelentkeznek az alkalmazás-átjárók http-figyelőben.</span><span class="sxs-lookup"><span data-stu-id="341aa-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="341aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="341aa-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="341aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="341aa-105">DESCRIPTION</span></span>
<span data-ttu-id="341aa-106">A **Get-AzureRmApplicationGatewayCustomError** parancsmag egyéni hibaüzeneteket kap egy alkalmazás-átjáró http-figyelője alapján.</span><span class="sxs-lookup"><span data-stu-id="341aa-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="341aa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="341aa-107">EXAMPLES</span></span>

### <span data-ttu-id="341aa-108">Példa 1: egyéni hiba beolvasása http-figyelőben</span><span class="sxs-lookup"><span data-stu-id="341aa-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="341aa-109">Ez a parancs a HTTP-figyelő $listener 01-es 502 verziójának egyéni hibáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="341aa-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="341aa-110">2. példa: beolvassa a http-figyelők minden egyéni hibájának listáját.</span><span class="sxs-lookup"><span data-stu-id="341aa-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="341aa-111">Ez a parancs a HTTP-figyelő $listener 01-es verziójában található összes egyéni hiba listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="341aa-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="341aa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="341aa-112">PARAMETERS</span></span>

### <span data-ttu-id="341aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="341aa-113">-DefaultProfile</span></span>
<span data-ttu-id="341aa-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="341aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="341aa-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="341aa-115">-HttpListener</span></span>
<span data-ttu-id="341aa-116">Az alkalmazás-átjáró http-figyelése</span><span class="sxs-lookup"><span data-stu-id="341aa-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="341aa-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="341aa-117">-StatusCode</span></span>
<span data-ttu-id="341aa-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="341aa-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341aa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="341aa-119">CommonParameters</span></span>
<span data-ttu-id="341aa-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="341aa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="341aa-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="341aa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="341aa-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="341aa-122">INPUTS</span></span>

### <span data-ttu-id="341aa-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="341aa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="341aa-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="341aa-124">OUTPUTS</span></span>

### <span data-ttu-id="341aa-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="341aa-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="341aa-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="341aa-126">NOTES</span></span>

## <span data-ttu-id="341aa-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="341aa-127">RELATED LINKS</span></span>
