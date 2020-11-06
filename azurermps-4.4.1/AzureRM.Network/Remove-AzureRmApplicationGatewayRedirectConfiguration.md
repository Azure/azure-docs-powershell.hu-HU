---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: bd9ab62406d033eefe3fb3723d2a2ebf2f9dbb8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497068"
---
# <span data-ttu-id="b1b1b-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1b1b-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b1b1b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b1b-103">Átirányítási konfiguráció eltávolítása egy meglévő alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="b1b1b-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1b1b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1b1b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b1b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b1b-106">A **Remove-AzureRmApplicationGatewayRedirectConfiguration** parancsmag egy meglévő alkalmazás-átjáróból távolítja el az átirányítás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b1b1b-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="b1b1b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b1b1b-107">EXAMPLES</span></span>

### <span data-ttu-id="b1b1b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b1b1b-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="b1b1b-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b1b1b-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b1b1b-110">A második parancs eltávolítja a Redirect01 nevű átirányítás-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="b1b1b-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b1b1b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1b1b-111">PARAMETERS</span></span>

### <span data-ttu-id="b1b1b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1b1b-112">-ApplicationGateway</span></span>
<span data-ttu-id="b1b1b-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1b1b-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b1b1b-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1b1b-114">-Name</span></span>
<span data-ttu-id="b1b1b-115">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="b1b1b-115">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="b1b1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b1b-116">-DefaultProfile</span></span>
<span data-ttu-id="b1b1b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1b1b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1b1b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b1b-118">CommonParameters</span></span>
<span data-ttu-id="b1b1b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1b1b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b1b-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b1b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b1b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1b1b-121">INPUTS</span></span>

### <span data-ttu-id="b1b1b-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1b1b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1b1b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1b1b-123">OUTPUTS</span></span>

### <span data-ttu-id="b1b1b-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1b1b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1b1b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1b1b-125">NOTES</span></span>

## <span data-ttu-id="b1b1b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1b1b-126">RELATED LINKS</span></span>

