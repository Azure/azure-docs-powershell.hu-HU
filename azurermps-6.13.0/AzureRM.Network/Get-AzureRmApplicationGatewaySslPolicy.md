---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 97851183233993400205993f091c8c57f376fcaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679163"
---
# <span data-ttu-id="8e10c-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8e10c-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="8e10c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e10c-102">SYNOPSIS</span></span>
<span data-ttu-id="8e10c-103">Az alkalmazás-átjáró SSL-házirendjének lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="8e10c-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e10c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e10c-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e10c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e10c-105">DESCRIPTION</span></span>
<span data-ttu-id="8e10c-106">A **Get-AzureRmApplicationGatewaySslPolicy** parancsmag egy alkalmazás-átjáró SSL-házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8e10c-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="8e10c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8e10c-107">EXAMPLES</span></span>

### <span data-ttu-id="8e10c-108">1:</span><span class="sxs-lookup"><span data-stu-id="8e10c-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="8e10c-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8e10c-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="8e10c-110">A második parancs a $AppGW nevű változóban tárolt alkalmazás-átjárótól kapja meg az SSL-házirendet.</span><span class="sxs-lookup"><span data-stu-id="8e10c-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="8e10c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e10c-111">PARAMETERS</span></span>

### <span data-ttu-id="8e10c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e10c-112">-ApplicationGateway</span></span>
<span data-ttu-id="8e10c-113">Annak az SSL-házirendnek az alkalmazási átjáróját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="8e10c-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8e10c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e10c-114">-DefaultProfile</span></span>
<span data-ttu-id="8e10c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e10c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e10c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e10c-116">CommonParameters</span></span>
<span data-ttu-id="8e10c-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e10c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e10c-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e10c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e10c-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e10c-119">INPUTS</span></span>

### <span data-ttu-id="8e10c-120">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e10c-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="8e10c-121">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8e10c-121">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="8e10c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e10c-122">OUTPUTS</span></span>

### <span data-ttu-id="8e10c-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8e10c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="8e10c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e10c-124">NOTES</span></span>
* <span data-ttu-id="8e10c-125">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="8e10c-125">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8e10c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e10c-126">RELATED LINKS</span></span>

[<span data-ttu-id="8e10c-127">Új – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8e10c-127">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="8e10c-128">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8e10c-128">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


