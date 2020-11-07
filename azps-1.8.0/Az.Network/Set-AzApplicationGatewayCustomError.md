---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: a59646c6214b3c4372eef9def61f67fe4a5bd912
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670062"
---
# <span data-ttu-id="63489-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63489-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="63489-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63489-102">SYNOPSIS</span></span>
<span data-ttu-id="63489-103">Az alkalmazás-átjárók egyéni hibáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="63489-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="63489-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63489-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63489-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="63489-105">DESCRIPTION</span></span>
<span data-ttu-id="63489-106">A **set-AzApplicationGatewayCustomError** parancsmag egy egyéni hibaüzenetet frissít egy alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="63489-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="63489-107">Példák</span><span class="sxs-lookup"><span data-stu-id="63489-107">EXAMPLES</span></span>

### <span data-ttu-id="63489-108">Példa 1: az alkalmazás-átjáró egyéni hibáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="63489-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="63489-109">Ez a parancs frissíti a 502-as http-állapotkód egyéni hibáját az Application Gateway $appgw, és a frissített átjárót számítja ki.</span><span class="sxs-lookup"><span data-stu-id="63489-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="63489-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63489-110">PARAMETERS</span></span>

### <span data-ttu-id="63489-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63489-111">-ApplicationGateway</span></span>
<span data-ttu-id="63489-112">Az Application Gateway</span><span class="sxs-lookup"><span data-stu-id="63489-112">The Application Gateway</span></span>

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

### <span data-ttu-id="63489-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="63489-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="63489-114">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="63489-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="63489-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63489-115">-DefaultProfile</span></span>
<span data-ttu-id="63489-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63489-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63489-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="63489-117">-StatusCode</span></span>
<span data-ttu-id="63489-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="63489-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="63489-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63489-119">CommonParameters</span></span>
<span data-ttu-id="63489-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63489-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63489-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63489-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63489-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63489-122">INPUTS</span></span>

### <span data-ttu-id="63489-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63489-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63489-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63489-124">OUTPUTS</span></span>

### <span data-ttu-id="63489-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63489-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="63489-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63489-126">NOTES</span></span>

## <span data-ttu-id="63489-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63489-127">RELATED LINKS</span></span>

[<span data-ttu-id="63489-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63489-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="63489-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63489-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="63489-130">Új – AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63489-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="63489-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63489-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
