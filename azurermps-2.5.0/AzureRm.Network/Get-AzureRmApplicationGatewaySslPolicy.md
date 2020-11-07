---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 237df37605581adeeb45fdfbb7bae6449128aa7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850733"
---
# <span data-ttu-id="3139f-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3139f-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="3139f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3139f-102">SYNOPSIS</span></span>
<span data-ttu-id="3139f-103">Az alkalmazás-átjáró SSL-házirendjének lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="3139f-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3139f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3139f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3139f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3139f-105">DESCRIPTION</span></span>
<span data-ttu-id="3139f-106">A **Get-AzureRmApplicationGatewaySslPolicy** parancsmag egy alkalmazás-átjáró SSL-házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3139f-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="3139f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3139f-107">EXAMPLES</span></span>

### <span data-ttu-id="3139f-108">1:</span><span class="sxs-lookup"><span data-stu-id="3139f-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="3139f-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3139f-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="3139f-110">A második parancs a $AppGW nevű változóban tárolt alkalmazás-átjárótól kapja meg az SSL-házirendet.</span><span class="sxs-lookup"><span data-stu-id="3139f-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="3139f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3139f-111">PARAMETERS</span></span>

### <span data-ttu-id="3139f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3139f-112">-ApplicationGateway</span></span>
<span data-ttu-id="3139f-113">Annak az SSL-házirendnek az alkalmazási átjáróját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="3139f-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3139f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3139f-114">-DefaultProfile</span></span>
<span data-ttu-id="3139f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3139f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3139f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3139f-116">CommonParameters</span></span>
<span data-ttu-id="3139f-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3139f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3139f-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3139f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3139f-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3139f-119">INPUTS</span></span>

### <span data-ttu-id="3139f-120">System. String</span><span class="sxs-lookup"><span data-stu-id="3139f-120">System.String</span></span>

## <span data-ttu-id="3139f-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3139f-121">OUTPUTS</span></span>

### <span data-ttu-id="3139f-122">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3139f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="3139f-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3139f-123">NOTES</span></span>
* <span data-ttu-id="3139f-124">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="3139f-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3139f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3139f-125">RELATED LINKS</span></span>

[<span data-ttu-id="3139f-126">Új – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3139f-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="3139f-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3139f-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


