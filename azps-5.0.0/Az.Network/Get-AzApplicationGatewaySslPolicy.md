---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195688"
---
# <span data-ttu-id="c8dc8-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c8dc8-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c8dc8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="c8dc8-103">Az alkalmazás-átjáró SSL-házirendjének lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="c8dc8-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="c8dc8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8dc8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8dc8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="c8dc8-106">A **Get-AzApplicationGatewaySslPolicy** parancsmag egy alkalmazás-átjáró SSL-házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c8dc8-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="c8dc8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c8dc8-107">EXAMPLES</span></span>

### <span data-ttu-id="c8dc8-108">1:</span><span class="sxs-lookup"><span data-stu-id="c8dc8-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="c8dc8-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c8dc8-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c8dc8-110">A második parancs a $AppGW nevű változóban tárolt alkalmazás-átjárótól kapja meg az SSL-házirendet.</span><span class="sxs-lookup"><span data-stu-id="c8dc8-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="c8dc8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8dc8-111">PARAMETERS</span></span>

### <span data-ttu-id="c8dc8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8dc8-112">-ApplicationGateway</span></span>
<span data-ttu-id="c8dc8-113">Annak az SSL-házirendnek az alkalmazási átjáróját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="c8dc8-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c8dc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8dc8-114">-DefaultProfile</span></span>
<span data-ttu-id="c8dc8-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8dc8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8dc8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8dc8-116">CommonParameters</span></span>
<span data-ttu-id="c8dc8-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8dc8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8dc8-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c8dc8-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8dc8-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8dc8-119">INPUTS</span></span>

### <span data-ttu-id="c8dc8-120">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8dc8-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c8dc8-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8dc8-121">OUTPUTS</span></span>

### <span data-ttu-id="c8dc8-122">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c8dc8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c8dc8-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8dc8-123">NOTES</span></span>
* <span data-ttu-id="c8dc8-124">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="c8dc8-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c8dc8-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8dc8-125">RELATED LINKS</span></span>

[<span data-ttu-id="c8dc8-126">Új – AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c8dc8-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="c8dc8-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c8dc8-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


