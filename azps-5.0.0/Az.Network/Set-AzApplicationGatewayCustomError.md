---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194229"
---
# <span data-ttu-id="450b4-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="450b4-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="450b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="450b4-102">SYNOPSIS</span></span>
<span data-ttu-id="450b4-103">Az alkalmazás-átjárók egyéni hibáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="450b4-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="450b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="450b4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="450b4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="450b4-105">DESCRIPTION</span></span>
<span data-ttu-id="450b4-106">A **set-AzApplicationGatewayCustomError** parancsmag egy egyéni hibaüzenetet frissít egy alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="450b4-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="450b4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="450b4-107">EXAMPLES</span></span>

### <span data-ttu-id="450b4-108">Példa 1: az alkalmazás-átjáró egyéni hibáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="450b4-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="450b4-109">Ez a parancs frissíti a 502-as http-állapotkód egyéni hibáját az Application Gateway $appgw, és a frissített átjárót számítja ki.</span><span class="sxs-lookup"><span data-stu-id="450b4-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="450b4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="450b4-110">PARAMETERS</span></span>

### <span data-ttu-id="450b4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="450b4-111">-ApplicationGateway</span></span>
<span data-ttu-id="450b4-112">Az Application Gateway</span><span class="sxs-lookup"><span data-stu-id="450b4-112">The Application Gateway</span></span>

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

### <span data-ttu-id="450b4-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="450b4-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="450b4-114">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="450b4-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="450b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450b4-115">-DefaultProfile</span></span>
<span data-ttu-id="450b4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="450b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="450b4-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="450b4-117">-StatusCode</span></span>
<span data-ttu-id="450b4-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="450b4-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="450b4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450b4-119">CommonParameters</span></span>
<span data-ttu-id="450b4-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="450b4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450b4-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="450b4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450b4-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="450b4-122">INPUTS</span></span>

### <span data-ttu-id="450b4-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="450b4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="450b4-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="450b4-124">OUTPUTS</span></span>

### <span data-ttu-id="450b4-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="450b4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="450b4-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="450b4-126">NOTES</span></span>

## <span data-ttu-id="450b4-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="450b4-127">RELATED LINKS</span></span>

[<span data-ttu-id="450b4-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="450b4-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="450b4-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="450b4-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="450b4-130">Új – AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="450b4-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="450b4-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="450b4-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
