---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 30f47cf6e345710da0e0d626929f65a33490e246
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013553"
---
# <span data-ttu-id="a30f3-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a30f3-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a30f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a30f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a30f3-103">Beolvassa az alkalmazás átjárójának HTTP-figyelését.</span><span class="sxs-lookup"><span data-stu-id="a30f3-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="a30f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a30f3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a30f3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a30f3-105">DESCRIPTION</span></span>
<span data-ttu-id="a30f3-106">A **Get-AzApplicationGatewayHttpListener** parancsmag az alkalmazás-ÁTJÁRÓk http-figyelését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a30f3-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="a30f3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a30f3-107">EXAMPLES</span></span>

### <span data-ttu-id="a30f3-108">Példa 1: speciális HTTP-figyelő beszerzése</span><span class="sxs-lookup"><span data-stu-id="a30f3-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="a30f3-109">Ez a parancs a Listener01 nevű HTTP-figyelőt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a30f3-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="a30f3-110">2. példa: a HTTP-figyelők listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a30f3-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="a30f3-111">Ez a parancs a HTTP-figyelők listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a30f3-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="a30f3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a30f3-112">PARAMETERS</span></span>

### <span data-ttu-id="a30f3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a30f3-113">-ApplicationGateway</span></span>
<span data-ttu-id="a30f3-114">A HTTP-figyelőt tartalmazó Application Gateway-objektum megadása.</span><span class="sxs-lookup"><span data-stu-id="a30f3-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="a30f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a30f3-115">-DefaultProfile</span></span>
<span data-ttu-id="a30f3-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a30f3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a30f3-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a30f3-117">-Name</span></span>
<span data-ttu-id="a30f3-118">Annak a HTTP-figyelőnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="a30f3-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a30f3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a30f3-119">CommonParameters</span></span>
<span data-ttu-id="a30f3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a30f3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a30f3-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a30f3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a30f3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a30f3-122">INPUTS</span></span>

### <span data-ttu-id="a30f3-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a30f3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a30f3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a30f3-124">OUTPUTS</span></span>

### <span data-ttu-id="a30f3-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a30f3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a30f3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a30f3-126">NOTES</span></span>

## <span data-ttu-id="a30f3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a30f3-127">RELATED LINKS</span></span>

[<span data-ttu-id="a30f3-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a30f3-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a30f3-129">Új – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a30f3-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a30f3-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a30f3-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a30f3-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a30f3-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


