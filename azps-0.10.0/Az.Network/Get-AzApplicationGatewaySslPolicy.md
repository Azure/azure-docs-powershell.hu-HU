---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 98f824ec0d874f8977c6e29f51358856cb5d1ca1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841694"
---
# <span data-ttu-id="b6515-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="b6515-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="b6515-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6515-102">SYNOPSIS</span></span>
<span data-ttu-id="b6515-103">Az alkalmazás-átjáró SSL-házirendjének lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="b6515-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="b6515-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6515-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6515-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6515-105">DESCRIPTION</span></span>
<span data-ttu-id="b6515-106">A **Get-AzApplicationGatewaySslPolicy** parancsmag egy alkalmazás-átjáró SSL-házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b6515-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="b6515-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6515-107">EXAMPLES</span></span>

### <span data-ttu-id="b6515-108">1:</span><span class="sxs-lookup"><span data-stu-id="b6515-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="b6515-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b6515-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b6515-110">A második parancs a $AppGW nevű változóban tárolt alkalmazás-átjárótól kapja meg az SSL-házirendet.</span><span class="sxs-lookup"><span data-stu-id="b6515-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="b6515-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6515-111">PARAMETERS</span></span>

### <span data-ttu-id="b6515-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6515-112">-ApplicationGateway</span></span>
<span data-ttu-id="b6515-113">Annak az SSL-házirendnek az alkalmazási átjáróját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="b6515-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b6515-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6515-114">-DefaultProfile</span></span>
<span data-ttu-id="b6515-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6515-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6515-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6515-116">CommonParameters</span></span>
<span data-ttu-id="b6515-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6515-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6515-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6515-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6515-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6515-119">INPUTS</span></span>

### <span data-ttu-id="b6515-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b6515-120">System.String</span></span>

## <span data-ttu-id="b6515-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6515-121">OUTPUTS</span></span>

### <span data-ttu-id="b6515-122">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="b6515-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="b6515-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6515-123">NOTES</span></span>
* <span data-ttu-id="b6515-124">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="b6515-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b6515-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6515-125">RELATED LINKS</span></span>

[<span data-ttu-id="b6515-126">Új – AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="b6515-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="b6515-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="b6515-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


