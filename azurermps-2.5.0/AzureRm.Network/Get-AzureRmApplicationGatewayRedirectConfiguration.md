---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 286afc05e9b7c825f183aabe7a78c965c790cb02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850745"
---
# <span data-ttu-id="aab0f-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="aab0f-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="aab0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aab0f-102">SYNOPSIS</span></span>
<span data-ttu-id="aab0f-103">Meglévő átirányítási konfigurációt kap egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="aab0f-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aab0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aab0f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aab0f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aab0f-105">DESCRIPTION</span></span>
<span data-ttu-id="aab0f-106">A **Get-AzureRmApplicationGatewayRedirectConfiguration** parancsmag egy meglévő átirányítási konfigurációt kap egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="aab0f-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="aab0f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aab0f-107">EXAMPLES</span></span>

### <span data-ttu-id="aab0f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aab0f-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="aab0f-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="aab0f-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="aab0f-110">A második parancs a Redirect01 nevű átirányítási konfigurációt a $AppGW nevű változóban tárolt alkalmazás-átjáróról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aab0f-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="aab0f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aab0f-111">PARAMETERS</span></span>

### <span data-ttu-id="aab0f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aab0f-112">-ApplicationGateway</span></span>
<span data-ttu-id="aab0f-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="aab0f-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aab0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab0f-114">-DefaultProfile</span></span>
<span data-ttu-id="aab0f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aab0f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aab0f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aab0f-116">-Name</span></span>
<span data-ttu-id="aab0f-117">A kérés útválasztási szabályának neve</span><span class="sxs-lookup"><span data-stu-id="aab0f-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="aab0f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab0f-118">CommonParameters</span></span>
<span data-ttu-id="aab0f-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aab0f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab0f-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab0f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab0f-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aab0f-121">INPUTS</span></span>

### <span data-ttu-id="aab0f-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aab0f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="aab0f-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aab0f-123">OUTPUTS</span></span>

### <span data-ttu-id="aab0f-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="aab0f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="aab0f-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. commands. Network, Version = 4.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="aab0f-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="aab0f-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aab0f-126">NOTES</span></span>

## <span data-ttu-id="aab0f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aab0f-127">RELATED LINKS</span></span>

