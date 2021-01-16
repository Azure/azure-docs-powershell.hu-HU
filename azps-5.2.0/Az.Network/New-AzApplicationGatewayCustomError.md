---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340337"
---
# <span data-ttu-id="05da3-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="05da3-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="05da3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05da3-102">SYNOPSIS</span></span>
<span data-ttu-id="05da3-103">Egyéni hiba létrehozása http-állapotkóddal és egyéni hibalap URL-címével</span><span class="sxs-lookup"><span data-stu-id="05da3-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="05da3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="05da3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05da3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="05da3-105">DESCRIPTION</span></span>
<span data-ttu-id="05da3-106">A **New-AzApplicationGatewayCustomError** parancsmag egyéni hibát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="05da3-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="05da3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="05da3-107">EXAMPLES</span></span>

### <span data-ttu-id="05da3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="05da3-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="05da3-109">Ez a parancs a http 403-as állapotkód egyéni hibaüzenetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="05da3-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="05da3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05da3-110">PARAMETERS</span></span>

### <span data-ttu-id="05da3-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="05da3-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="05da3-112">Hibalap URL-címe az alkalmazás-átjáró ügyfélalkalmazásának hibaüzenetéhez.</span><span class="sxs-lookup"><span data-stu-id="05da3-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="05da3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05da3-113">-DefaultProfile</span></span>
<span data-ttu-id="05da3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05da3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05da3-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="05da3-115">-StatusCode</span></span>
<span data-ttu-id="05da3-116">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="05da3-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="05da3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05da3-117">CommonParameters</span></span>
<span data-ttu-id="05da3-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05da3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05da3-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05da3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05da3-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05da3-120">INPUTS</span></span>

### <span data-ttu-id="05da3-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="05da3-121">None</span></span>

## <span data-ttu-id="05da3-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05da3-122">OUTPUTS</span></span>

### <span data-ttu-id="05da3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="05da3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="05da3-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="05da3-124">NOTES</span></span>

## <span data-ttu-id="05da3-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05da3-125">RELATED LINKS</span></span>

[<span data-ttu-id="05da3-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="05da3-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="05da3-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="05da3-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="05da3-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="05da3-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="05da3-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="05da3-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
