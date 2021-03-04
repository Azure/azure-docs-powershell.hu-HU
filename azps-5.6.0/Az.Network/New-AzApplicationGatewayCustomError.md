---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 377145933832c587691ed30db08754ef1e6f1f64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928577"
---
# <span data-ttu-id="530de-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="530de-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="530de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="530de-102">SYNOPSIS</span></span>
<span data-ttu-id="530de-103">Egyéni hiba létrehozása http-állapotkóddal és egyéni hibalap URL-címével</span><span class="sxs-lookup"><span data-stu-id="530de-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="530de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="530de-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="530de-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="530de-105">DESCRIPTION</span></span>
<span data-ttu-id="530de-106">A **New-AzApplicationGatewayCustomError** parancsmag egyéni hibát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="530de-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="530de-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="530de-107">EXAMPLES</span></span>

### <span data-ttu-id="530de-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="530de-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="530de-109">Ez a parancs a http 403-as állapotkód egyéni hibaüzenetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="530de-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="530de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="530de-110">PARAMETERS</span></span>

### <span data-ttu-id="530de-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="530de-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="530de-112">Hibalap URL-címe az alkalmazás-átjáró ügyfélalkalmazásának hibaüzenetéhez.</span><span class="sxs-lookup"><span data-stu-id="530de-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="530de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="530de-113">-DefaultProfile</span></span>
<span data-ttu-id="530de-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="530de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="530de-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="530de-115">-StatusCode</span></span>
<span data-ttu-id="530de-116">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="530de-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="530de-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="530de-117">CommonParameters</span></span>
<span data-ttu-id="530de-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="530de-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="530de-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="530de-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="530de-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="530de-120">INPUTS</span></span>

### <span data-ttu-id="530de-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="530de-121">None</span></span>

## <span data-ttu-id="530de-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="530de-122">OUTPUTS</span></span>

### <span data-ttu-id="530de-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="530de-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="530de-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="530de-124">NOTES</span></span>

## <span data-ttu-id="530de-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="530de-125">RELATED LINKS</span></span>

[<span data-ttu-id="530de-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="530de-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="530de-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="530de-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="530de-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="530de-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="530de-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="530de-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
