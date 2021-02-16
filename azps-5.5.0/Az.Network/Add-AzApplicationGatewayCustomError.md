---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: e3bac58fca1c405aeef3366cb3ec1ee1b01a0891
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152034"
---
# <span data-ttu-id="3e5bc-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3e5bc-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3e5bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="3e5bc-103">Egyéni hibát ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3e5bc-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="3e5bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e5bc-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e5bc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e5bc-105">DESCRIPTION</span></span>
<span data-ttu-id="3e5bc-106">Az **Add-AzApplicationGatewayCustomError** parancsmag egyéni hibát ad egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3e5bc-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="3e5bc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e5bc-107">EXAMPLES</span></span>

### <span data-ttu-id="3e5bc-108">1. példa: Egyéni hiba hozzáadása az alkalmazás átjárószinthez</span><span class="sxs-lookup"><span data-stu-id="3e5bc-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="3e5bc-109">Ez a parancs egyéni hibát ad hozzá az 502-es http állapotkódhoz az alkalmazás-$appgw, és visszaadja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="3e5bc-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="3e5bc-110">2. példa: Egyéni hiba hozzáadása az alkalmazás átjárót hallgatói szintjéhez</span><span class="sxs-lookup"><span data-stu-id="3e5bc-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
 $resourceGroupName = "resourceGroupName"
 $AppGWName = "applicationGatewayName"
 $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
 $listenerName = "listenerName"
 $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $resourceGroupName
 $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
 $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
 Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="3e5bc-111">Ez a parancs egyéni hibát ad hozzá az 502-es http állapotkódhoz az alkalmazás$appgw szinten, és visszaadja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="3e5bc-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="3e5bc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e5bc-112">PARAMETERS</span></span>

### <span data-ttu-id="3e5bc-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e5bc-113">-ApplicationGateway</span></span>
<span data-ttu-id="3e5bc-114">Az alkalmazás átjárója</span><span class="sxs-lookup"><span data-stu-id="3e5bc-114">The Application Gateway</span></span>

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

### <span data-ttu-id="3e5bc-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="3e5bc-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="3e5bc-116">Hibalap URL-címe az ügyfélalkalmazásnak az alkalmazás átjáróján.</span><span class="sxs-lookup"><span data-stu-id="3e5bc-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="3e5bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e5bc-117">-DefaultProfile</span></span>
<span data-ttu-id="3e5bc-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e5bc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e5bc-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="3e5bc-119">-StatusCode</span></span>
<span data-ttu-id="3e5bc-120">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="3e5bc-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="3e5bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e5bc-121">CommonParameters</span></span>
<span data-ttu-id="3e5bc-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e5bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e5bc-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e5bc-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e5bc-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e5bc-124">INPUTS</span></span>

### <span data-ttu-id="3e5bc-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e5bc-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e5bc-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e5bc-126">OUTPUTS</span></span>

### <span data-ttu-id="3e5bc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3e5bc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3e5bc-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e5bc-128">NOTES</span></span>

## <span data-ttu-id="3e5bc-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e5bc-129">RELATED LINKS</span></span>

[<span data-ttu-id="3e5bc-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3e5bc-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3e5bc-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3e5bc-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3e5bc-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3e5bc-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3e5bc-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3e5bc-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
