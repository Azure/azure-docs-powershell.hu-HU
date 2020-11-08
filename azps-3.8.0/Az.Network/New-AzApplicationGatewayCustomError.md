---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014835"
---
# <span data-ttu-id="f6e63-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f6e63-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f6e63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6e63-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e63-103">Egyéni hibaüzenetet hoz létre a HTTP-állapotkódot és az egyéni hibaüzenetek URL-címét tartalmazó URL-címmel</span><span class="sxs-lookup"><span data-stu-id="f6e63-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="f6e63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6e63-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6e63-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6e63-105">DESCRIPTION</span></span>
<span data-ttu-id="f6e63-106">A **New-AzApplicationGatewayCustomError** parancsmag egyéni hibaüzenetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f6e63-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="f6e63-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f6e63-107">EXAMPLES</span></span>

### <span data-ttu-id="f6e63-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f6e63-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="f6e63-109">Ezzel a paranccsal létrehozhatja az 403-as http-állapotkód egyéni hibáját.</span><span class="sxs-lookup"><span data-stu-id="f6e63-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="f6e63-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6e63-110">PARAMETERS</span></span>

### <span data-ttu-id="f6e63-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f6e63-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f6e63-112">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="f6e63-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f6e63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e63-113">-DefaultProfile</span></span>
<span data-ttu-id="f6e63-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6e63-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6e63-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f6e63-115">-StatusCode</span></span>
<span data-ttu-id="f6e63-116">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="f6e63-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f6e63-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e63-117">CommonParameters</span></span>
<span data-ttu-id="f6e63-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6e63-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e63-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6e63-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e63-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6e63-120">INPUTS</span></span>

### <span data-ttu-id="f6e63-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="f6e63-121">None</span></span>

## <span data-ttu-id="f6e63-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6e63-122">OUTPUTS</span></span>

### <span data-ttu-id="f6e63-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f6e63-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f6e63-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6e63-124">NOTES</span></span>

## <span data-ttu-id="f6e63-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6e63-125">RELATED LINKS</span></span>

[<span data-ttu-id="f6e63-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f6e63-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f6e63-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f6e63-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f6e63-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f6e63-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f6e63-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f6e63-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
