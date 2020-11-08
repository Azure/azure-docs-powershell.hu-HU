---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195692"
---
# <span data-ttu-id="5a343-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5a343-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="5a343-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a343-102">SYNOPSIS</span></span>
<span data-ttu-id="5a343-103">Az alkalmazás-átjáró SKU-ának beolvasása</span><span class="sxs-lookup"><span data-stu-id="5a343-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="5a343-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a343-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a343-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a343-105">DESCRIPTION</span></span>
<span data-ttu-id="5a343-106">A **Get-AzApplicationGatewaySku** parancsmag az alkalmazás-átjárók készletezési egységét (SKU) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5a343-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="5a343-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5a343-107">EXAMPLES</span></span>

### <span data-ttu-id="5a343-108">Példa 1: alkalmazás-átjáró SKU beszerzése</span><span class="sxs-lookup"><span data-stu-id="5a343-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="5a343-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5a343-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5a343-110">A második parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjáró SKU-értékét, és az eredményt az $SKU nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5a343-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="5a343-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a343-111">PARAMETERS</span></span>

### <span data-ttu-id="5a343-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a343-112">-ApplicationGateway</span></span>
<span data-ttu-id="5a343-113">Az Application Gateway-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a343-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="5a343-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a343-114">-DefaultProfile</span></span>
<span data-ttu-id="5a343-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a343-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a343-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a343-116">CommonParameters</span></span>
<span data-ttu-id="5a343-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a343-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a343-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5a343-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a343-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a343-119">INPUTS</span></span>

### <span data-ttu-id="5a343-120">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a343-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5a343-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a343-121">OUTPUTS</span></span>

### <span data-ttu-id="5a343-122">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5a343-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="5a343-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a343-123">NOTES</span></span>

## <span data-ttu-id="5a343-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a343-124">RELATED LINKS</span></span>

[<span data-ttu-id="5a343-125">Új – AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5a343-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="5a343-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5a343-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)

