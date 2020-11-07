---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 6f93a66739fe1943182726e6998267d1e406f0a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837624"
---
# <span data-ttu-id="99266-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="99266-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="99266-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99266-102">SYNOPSIS</span></span>
<span data-ttu-id="99266-103">Az alkalmazás-átjáró SSL-házirendjének lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="99266-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="99266-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99266-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99266-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99266-105">DESCRIPTION</span></span>
<span data-ttu-id="99266-106">A **Get-AzApplicationGatewaySslPolicy** parancsmag egy alkalmazás-átjáró SSL-házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="99266-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="99266-107">Példák</span><span class="sxs-lookup"><span data-stu-id="99266-107">EXAMPLES</span></span>

### <span data-ttu-id="99266-108">1:</span><span class="sxs-lookup"><span data-stu-id="99266-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="99266-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="99266-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="99266-110">A második parancs a $AppGW nevű változóban tárolt alkalmazás-átjárótól kapja meg az SSL-házirendet.</span><span class="sxs-lookup"><span data-stu-id="99266-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="99266-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99266-111">PARAMETERS</span></span>

### <span data-ttu-id="99266-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99266-112">-ApplicationGateway</span></span>
<span data-ttu-id="99266-113">Annak az SSL-házirendnek az alkalmazási átjáróját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="99266-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="99266-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99266-114">-DefaultProfile</span></span>
<span data-ttu-id="99266-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99266-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99266-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99266-116">CommonParameters</span></span>
<span data-ttu-id="99266-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99266-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99266-118">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="99266-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99266-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99266-119">INPUTS</span></span>

### <span data-ttu-id="99266-120">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99266-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99266-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99266-121">OUTPUTS</span></span>

### <span data-ttu-id="99266-122">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="99266-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="99266-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99266-123">NOTES</span></span>
* <span data-ttu-id="99266-124">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="99266-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="99266-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99266-125">RELATED LINKS</span></span>

[<span data-ttu-id="99266-126">Új – AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="99266-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="99266-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="99266-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


