---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157074"
---
# <span data-ttu-id="14c27-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14c27-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="14c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c27-102">SYNOPSIS</span></span>
<span data-ttu-id="14c27-103">Egyéni hiba(oka)t kap egy alkalmazás átjárótól.</span><span class="sxs-lookup"><span data-stu-id="14c27-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="14c27-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="14c27-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14c27-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="14c27-105">DESCRIPTION</span></span>
<span data-ttu-id="14c27-106">A **Get-AzApplicationGatewayCustomError** parancsmag egyéni hiba(oka)t kap egy alkalmazás-átjárótól.</span><span class="sxs-lookup"><span data-stu-id="14c27-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="14c27-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="14c27-107">EXAMPLES</span></span>

### <span data-ttu-id="14c27-108">1. példa: Egyéni hibát kap egy alkalmazás-átjáróban</span><span class="sxs-lookup"><span data-stu-id="14c27-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="14c27-109">Ez a parancs az 502-es http-állapotkód egyéni hibaüzenetét kapja vissza az alkalmazás-átjárótól $appgw.</span><span class="sxs-lookup"><span data-stu-id="14c27-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="14c27-110">2. példa: Az összes egyéni hiba listájának lekérte egy alkalmazás-átjáróban</span><span class="sxs-lookup"><span data-stu-id="14c27-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="14c27-111">Ez a parancs be- és visszaadja az összes egyéni hiba listáját az $appgw.</span><span class="sxs-lookup"><span data-stu-id="14c27-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="14c27-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14c27-112">PARAMETERS</span></span>

### <span data-ttu-id="14c27-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14c27-113">-ApplicationGateway</span></span>
<span data-ttu-id="14c27-114">Az alkalmazás átjárója</span><span class="sxs-lookup"><span data-stu-id="14c27-114">The Application Gateway</span></span>

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

### <span data-ttu-id="14c27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c27-115">-DefaultProfile</span></span>
<span data-ttu-id="14c27-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14c27-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14c27-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="14c27-117">-StatusCode</span></span>
<span data-ttu-id="14c27-118">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="14c27-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="14c27-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c27-119">CommonParameters</span></span>
<span data-ttu-id="14c27-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14c27-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c27-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14c27-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c27-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14c27-122">INPUTS</span></span>

### <span data-ttu-id="14c27-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14c27-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14c27-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14c27-124">OUTPUTS</span></span>

### <span data-ttu-id="14c27-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14c27-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="14c27-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="14c27-126">NOTES</span></span>

## <span data-ttu-id="14c27-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14c27-127">RELATED LINKS</span></span>

[<span data-ttu-id="14c27-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14c27-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="14c27-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14c27-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="14c27-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14c27-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="14c27-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14c27-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
