---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 6ca7bc3e5d1af477c7d6750f674272ff64d54889
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157099"
---
# <span data-ttu-id="e1630-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e1630-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e1630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1630-102">SYNOPSIS</span></span>
<span data-ttu-id="e1630-103">Egy alkalmazás-átjáró háttércímkészletét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e1630-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="e1630-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1630-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1630-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1630-105">DESCRIPTION</span></span>
<span data-ttu-id="e1630-106">A **Get-AzApplicationGatewayBackendAddressPool** parancsmag egy vagy több háttércímkészlet-konfigurációt kap egy alkalmazás-átjárótól.</span><span class="sxs-lookup"><span data-stu-id="e1630-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="e1630-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1630-107">EXAMPLES</span></span>

### <span data-ttu-id="e1630-108">1. példa: Egy megadott háttérkiszolgáló-készlet lekérte</span><span class="sxs-lookup"><span data-stu-id="e1630-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="e1630-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="e1630-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e1630-110">A második parancs a Készlet01 nevű $AppGw a háttércímkészletet, és a $BackendPool tárolja.</span><span class="sxs-lookup"><span data-stu-id="e1630-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="e1630-111">2. példa: Háttérkiszolgáló-készlet listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="e1630-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="e1630-112">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="e1630-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e1630-113">A második parancs lekérte a $AppGw háttércímkészletek listáját, és a listát a $BackendPools változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e1630-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="e1630-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1630-114">PARAMETERS</span></span>

### <span data-ttu-id="e1630-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1630-115">-ApplicationGateway</span></span>
<span data-ttu-id="e1630-116">A **Get-AzApplicationGatewayBackendAddressPool** parancsmag egy háttércímkészletet kap egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e1630-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="e1630-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1630-117">-DefaultProfile</span></span>
<span data-ttu-id="e1630-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1630-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1630-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e1630-119">-Name</span></span>
<span data-ttu-id="e1630-120">A parancsmag háttércímkészletének a neve.</span><span class="sxs-lookup"><span data-stu-id="e1630-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e1630-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1630-121">CommonParameters</span></span>
<span data-ttu-id="e1630-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1630-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1630-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1630-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1630-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1630-124">INPUTS</span></span>

### <span data-ttu-id="e1630-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1630-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1630-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1630-126">OUTPUTS</span></span>

### <span data-ttu-id="e1630-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e1630-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e1630-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1630-128">NOTES</span></span>

## <span data-ttu-id="e1630-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1630-129">RELATED LINKS</span></span>

[<span data-ttu-id="e1630-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e1630-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e1630-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e1630-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e1630-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e1630-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e1630-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e1630-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


