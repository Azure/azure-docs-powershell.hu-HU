---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025207"
---
# <span data-ttu-id="e0838-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e0838-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e0838-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0838-102">SYNOPSIS</span></span>
<span data-ttu-id="e0838-103">Egyéni hibák jelentkeznek egy alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="e0838-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="e0838-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0838-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0838-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0838-105">DESCRIPTION</span></span>
<span data-ttu-id="e0838-106">A **Get-AzApplicationGatewayCustomError** parancsmag egyéni hibaüzeneteket kap egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="e0838-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="e0838-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e0838-107">EXAMPLES</span></span>

### <span data-ttu-id="e0838-108">Példa 1: egyéni hiba beolvasása egy alkalmazás-átjáróban</span><span class="sxs-lookup"><span data-stu-id="e0838-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="e0838-109">Ez a parancs a 502-ös http-állapotkód egyéni hibáját adja eredményül az Application Gateway $appgw.</span><span class="sxs-lookup"><span data-stu-id="e0838-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="e0838-110">2. példa: beolvassa az összes egyéni hiba listáját egy alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="e0838-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="e0838-111">Ez a parancs beolvassa és visszaadja az összes egyéni hiba listáját az Application Gateway $appgwból.</span><span class="sxs-lookup"><span data-stu-id="e0838-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="e0838-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0838-112">PARAMETERS</span></span>

### <span data-ttu-id="e0838-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0838-113">-ApplicationGateway</span></span>
<span data-ttu-id="e0838-114">Az Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e0838-114">The Application Gateway</span></span>

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

### <span data-ttu-id="e0838-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0838-115">-DefaultProfile</span></span>
<span data-ttu-id="e0838-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0838-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0838-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e0838-117">-StatusCode</span></span>
<span data-ttu-id="e0838-118">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="e0838-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e0838-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0838-119">CommonParameters</span></span>
<span data-ttu-id="e0838-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0838-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0838-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0838-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0838-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0838-122">INPUTS</span></span>

### <span data-ttu-id="e0838-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0838-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e0838-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0838-124">OUTPUTS</span></span>

### <span data-ttu-id="e0838-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e0838-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e0838-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0838-126">NOTES</span></span>

## <span data-ttu-id="e0838-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0838-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0838-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e0838-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e0838-129">Új – AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e0838-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e0838-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e0838-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e0838-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e0838-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
