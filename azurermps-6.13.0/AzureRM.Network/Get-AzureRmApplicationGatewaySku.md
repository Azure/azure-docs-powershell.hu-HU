---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 5d0409ae5be910f2e4480ac61f36d907e7736f0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501144"
---
# <span data-ttu-id="8fb63-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="8fb63-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="8fb63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fb63-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb63-103">Az alkalmazás-átjáró SKU-ának beolvasása</span><span class="sxs-lookup"><span data-stu-id="8fb63-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fb63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fb63-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fb63-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fb63-105">DESCRIPTION</span></span>
<span data-ttu-id="8fb63-106">A **Get-AzureRmApplicationGatewaySku** parancsmag az alkalmazás-átjárók készletezési egységét (SKU) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8fb63-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="8fb63-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8fb63-107">EXAMPLES</span></span>

### <span data-ttu-id="8fb63-108">Példa 1: alkalmazás-átjáró SKU beszerzése</span><span class="sxs-lookup"><span data-stu-id="8fb63-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="8fb63-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8fb63-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="8fb63-110">A második parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjáró SKU-értékét, és az eredményt az $SKU nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8fb63-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="8fb63-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fb63-111">PARAMETERS</span></span>

### <span data-ttu-id="8fb63-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8fb63-112">-ApplicationGateway</span></span>
<span data-ttu-id="8fb63-113">Az Application Gateway-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fb63-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="8fb63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb63-114">-DefaultProfile</span></span>
<span data-ttu-id="8fb63-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fb63-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fb63-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb63-116">CommonParameters</span></span>
<span data-ttu-id="8fb63-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fb63-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb63-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fb63-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb63-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fb63-119">INPUTS</span></span>

### <span data-ttu-id="8fb63-120">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8fb63-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="8fb63-121">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8fb63-121">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="8fb63-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fb63-122">OUTPUTS</span></span>

### <span data-ttu-id="8fb63-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="8fb63-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="8fb63-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fb63-124">NOTES</span></span>

## <span data-ttu-id="8fb63-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fb63-125">RELATED LINKS</span></span>

[<span data-ttu-id="8fb63-126">Új – AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="8fb63-126">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="8fb63-127">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="8fb63-127">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


