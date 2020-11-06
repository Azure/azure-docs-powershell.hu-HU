---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: f542783ce1edcebf0c0c4e70116423836ddff736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495030"
---
# <span data-ttu-id="d53e8-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d53e8-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="d53e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d53e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d53e8-103">Átirányítási konfiguráció eltávolítása egy meglévő alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="d53e8-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d53e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d53e8-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d53e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d53e8-105">DESCRIPTION</span></span>
<span data-ttu-id="d53e8-106">A **Remove-AzureRmApplicationGatewayRedirectConfiguration** parancsmag egy meglévő alkalmazás-átjáróból távolítja el az átirányítás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="d53e8-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="d53e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d53e8-107">EXAMPLES</span></span>

### <span data-ttu-id="d53e8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d53e8-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="d53e8-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d53e8-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d53e8-110">A második parancs eltávolítja a Redirect01 nevű átirányítás-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="d53e8-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d53e8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d53e8-111">PARAMETERS</span></span>

### <span data-ttu-id="d53e8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d53e8-112">-ApplicationGateway</span></span>
<span data-ttu-id="d53e8-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="d53e8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d53e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53e8-114">-DefaultProfile</span></span>
<span data-ttu-id="d53e8-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d53e8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d53e8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d53e8-116">-Name</span></span>
<span data-ttu-id="d53e8-117">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="d53e8-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="d53e8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53e8-118">CommonParameters</span></span>
<span data-ttu-id="d53e8-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d53e8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53e8-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d53e8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53e8-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d53e8-121">INPUTS</span></span>

### <span data-ttu-id="d53e8-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d53e8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="d53e8-123">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d53e8-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="d53e8-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d53e8-124">OUTPUTS</span></span>

### <span data-ttu-id="d53e8-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d53e8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d53e8-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d53e8-126">NOTES</span></span>

## <span data-ttu-id="d53e8-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d53e8-127">RELATED LINKS</span></span>
