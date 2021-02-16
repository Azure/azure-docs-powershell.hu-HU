---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160635"
---
# <span data-ttu-id="430fa-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="430fa-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="430fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="430fa-102">SYNOPSIS</span></span>
<span data-ttu-id="430fa-103">Egyéni hiba frissítése egy alkalmazás átjáróban.</span><span class="sxs-lookup"><span data-stu-id="430fa-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="430fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="430fa-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="430fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="430fa-105">DESCRIPTION</span></span>
<span data-ttu-id="430fa-106">A **Set-AzApplicationGatewayCustomError** parancsmag frissíti az egyéni hibát egy alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="430fa-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="430fa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="430fa-107">EXAMPLES</span></span>

### <span data-ttu-id="430fa-108">1. példa: Egyéni hiba frissítése egy alkalmazás-átjáróban</span><span class="sxs-lookup"><span data-stu-id="430fa-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="430fa-109">Ez a parancs frissíti az 502-es http állapotkódot az alkalmazás átjárókezelő $appgw, és visszaadja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="430fa-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="430fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="430fa-110">PARAMETERS</span></span>

### <span data-ttu-id="430fa-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="430fa-111">-ApplicationGateway</span></span>
<span data-ttu-id="430fa-112">Az alkalmazás átjárója</span><span class="sxs-lookup"><span data-stu-id="430fa-112">The Application Gateway</span></span>

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

### <span data-ttu-id="430fa-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="430fa-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="430fa-114">Hibalap URL-címe az ügyfélalkalmazásnak az alkalmazás átjáróján.</span><span class="sxs-lookup"><span data-stu-id="430fa-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="430fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="430fa-115">-DefaultProfile</span></span>
<span data-ttu-id="430fa-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="430fa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="430fa-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="430fa-117">-StatusCode</span></span>
<span data-ttu-id="430fa-118">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="430fa-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="430fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="430fa-119">CommonParameters</span></span>
<span data-ttu-id="430fa-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="430fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="430fa-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="430fa-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="430fa-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="430fa-122">INPUTS</span></span>

### <span data-ttu-id="430fa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="430fa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="430fa-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="430fa-124">OUTPUTS</span></span>

### <span data-ttu-id="430fa-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="430fa-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="430fa-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="430fa-126">NOTES</span></span>

## <span data-ttu-id="430fa-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="430fa-127">RELATED LINKS</span></span>

[<span data-ttu-id="430fa-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="430fa-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="430fa-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="430fa-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="430fa-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="430fa-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="430fa-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="430fa-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
