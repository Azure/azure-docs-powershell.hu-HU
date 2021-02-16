---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202964"
---
# <span data-ttu-id="ea141-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ea141-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ea141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea141-102">SYNOPSIS</span></span>
<span data-ttu-id="ea141-103">Egyéni hiba létrehozása http-állapotkóddal és egyéni hibalap URL-címével</span><span class="sxs-lookup"><span data-stu-id="ea141-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="ea141-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea141-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea141-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea141-105">DESCRIPTION</span></span>
<span data-ttu-id="ea141-106">A **New-AzApplicationGatewayCustomError** parancsmag egyéni hibát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ea141-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="ea141-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea141-107">EXAMPLES</span></span>

### <span data-ttu-id="ea141-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ea141-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="ea141-109">Ez a parancs a http 403-as állapotkód egyéni hibaüzenetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ea141-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="ea141-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea141-110">PARAMETERS</span></span>

### <span data-ttu-id="ea141-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="ea141-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="ea141-112">Hibalap URL-címe az ügyfélalkalmazásnak az alkalmazás átjáróján.</span><span class="sxs-lookup"><span data-stu-id="ea141-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ea141-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea141-113">-DefaultProfile</span></span>
<span data-ttu-id="ea141-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea141-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea141-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ea141-115">-StatusCode</span></span>
<span data-ttu-id="ea141-116">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="ea141-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ea141-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea141-117">CommonParameters</span></span>
<span data-ttu-id="ea141-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea141-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea141-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea141-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea141-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea141-120">INPUTS</span></span>

### <span data-ttu-id="ea141-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="ea141-121">None</span></span>

## <span data-ttu-id="ea141-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea141-122">OUTPUTS</span></span>

### <span data-ttu-id="ea141-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ea141-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ea141-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea141-124">NOTES</span></span>

## <span data-ttu-id="ea141-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea141-125">RELATED LINKS</span></span>

[<span data-ttu-id="ea141-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ea141-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ea141-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ea141-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ea141-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ea141-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ea141-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ea141-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
