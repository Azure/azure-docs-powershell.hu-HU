---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: ba979a12584d526ba7e3a36d13c44b51704b44f6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848754"
---
# <span data-ttu-id="72b19-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="72b19-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="72b19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72b19-102">SYNOPSIS</span></span>
<span data-ttu-id="72b19-103">Átirányítási konfiguráció eltávolítása egy meglévő alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="72b19-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72b19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72b19-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72b19-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72b19-105">DESCRIPTION</span></span>
<span data-ttu-id="72b19-106">A **Remove-AzureRmApplicationGatewayRedirectConfiguration** parancsmag egy meglévő alkalmazás-átjáróból távolítja el az átirányítás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="72b19-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="72b19-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72b19-107">EXAMPLES</span></span>

### <span data-ttu-id="72b19-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="72b19-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="72b19-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="72b19-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="72b19-110">A második parancs eltávolítja a Redirect01 nevű átirányítás-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="72b19-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="72b19-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72b19-111">PARAMETERS</span></span>

### <span data-ttu-id="72b19-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72b19-112">-ApplicationGateway</span></span>
<span data-ttu-id="72b19-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="72b19-113">The applicationGateway</span></span>

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

### <span data-ttu-id="72b19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b19-114">-DefaultProfile</span></span>
<span data-ttu-id="72b19-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72b19-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72b19-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72b19-116">-Name</span></span>
<span data-ttu-id="72b19-117">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="72b19-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="72b19-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b19-118">CommonParameters</span></span>
<span data-ttu-id="72b19-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72b19-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b19-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72b19-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b19-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72b19-121">INPUTS</span></span>

### <span data-ttu-id="72b19-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72b19-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="72b19-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72b19-123">OUTPUTS</span></span>

### <span data-ttu-id="72b19-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72b19-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="72b19-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72b19-125">NOTES</span></span>

## <span data-ttu-id="72b19-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72b19-126">RELATED LINKS</span></span>

