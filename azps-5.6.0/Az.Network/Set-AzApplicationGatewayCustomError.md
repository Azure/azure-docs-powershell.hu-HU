---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 4c06b78062500ddb5c33353c00814a46e919bd8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936714"
---
# <span data-ttu-id="d1adb-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d1adb-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="d1adb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1adb-102">SYNOPSIS</span></span>
<span data-ttu-id="d1adb-103">Egyéni hiba frissítése egy alkalmazás átjáróban.</span><span class="sxs-lookup"><span data-stu-id="d1adb-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="d1adb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d1adb-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1adb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d1adb-105">DESCRIPTION</span></span>
<span data-ttu-id="d1adb-106">A **Set-AzApplicationGatewayCustomError** parancsmag frissíti az egyéni hibát egy alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="d1adb-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="d1adb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d1adb-107">EXAMPLES</span></span>

### <span data-ttu-id="d1adb-108">1. példa: Egyéni hiba frissítése egy alkalmazás-átjáróban</span><span class="sxs-lookup"><span data-stu-id="d1adb-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="d1adb-109">Ez a parancs frissíti az 502-es http állapotkódot az alkalmazás átjárókezelő $appgw, és visszaadja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="d1adb-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="d1adb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1adb-110">PARAMETERS</span></span>

### <span data-ttu-id="d1adb-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1adb-111">-ApplicationGateway</span></span>
<span data-ttu-id="d1adb-112">Az alkalmazás átjárója</span><span class="sxs-lookup"><span data-stu-id="d1adb-112">The Application Gateway</span></span>

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

### <span data-ttu-id="d1adb-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="d1adb-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="d1adb-114">Hibalap URL-címe az alkalmazás-átjáró ügyfélalkalmazásának hibaüzenetéhez.</span><span class="sxs-lookup"><span data-stu-id="d1adb-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="d1adb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1adb-115">-DefaultProfile</span></span>
<span data-ttu-id="d1adb-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1adb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1adb-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="d1adb-117">-StatusCode</span></span>
<span data-ttu-id="d1adb-118">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="d1adb-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="d1adb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1adb-119">CommonParameters</span></span>
<span data-ttu-id="d1adb-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1adb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1adb-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1adb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1adb-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1adb-122">INPUTS</span></span>

### <span data-ttu-id="d1adb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1adb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1adb-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1adb-124">OUTPUTS</span></span>

### <span data-ttu-id="d1adb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d1adb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="d1adb-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d1adb-126">NOTES</span></span>

## <span data-ttu-id="d1adb-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1adb-127">RELATED LINKS</span></span>

[<span data-ttu-id="d1adb-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d1adb-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="d1adb-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d1adb-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="d1adb-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d1adb-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="d1adb-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d1adb-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
