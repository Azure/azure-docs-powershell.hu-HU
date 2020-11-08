---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195666"
---
# <span data-ttu-id="c3485-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3485-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c3485-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3485-102">SYNOPSIS</span></span>
<span data-ttu-id="c3485-103">Egyéni hibaüzenetet hoz létre a HTTP-állapotkódot és az egyéni hibaüzenetek URL-címét tartalmazó URL-címmel</span><span class="sxs-lookup"><span data-stu-id="c3485-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="c3485-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3485-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3485-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3485-105">DESCRIPTION</span></span>
<span data-ttu-id="c3485-106">A **New-AzApplicationGatewayCustomError** parancsmag egyéni hibaüzenetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c3485-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="c3485-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c3485-107">EXAMPLES</span></span>

### <span data-ttu-id="c3485-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c3485-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="c3485-109">Ezzel a paranccsal létrehozhatja az 403-as http-állapotkód egyéni hibáját.</span><span class="sxs-lookup"><span data-stu-id="c3485-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="c3485-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3485-110">PARAMETERS</span></span>

### <span data-ttu-id="c3485-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="c3485-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="c3485-112">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="c3485-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c3485-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3485-113">-DefaultProfile</span></span>
<span data-ttu-id="c3485-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3485-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3485-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="c3485-115">-StatusCode</span></span>
<span data-ttu-id="c3485-116">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="c3485-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c3485-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3485-117">CommonParameters</span></span>
<span data-ttu-id="c3485-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3485-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3485-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3485-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3485-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3485-120">INPUTS</span></span>

### <span data-ttu-id="c3485-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="c3485-121">None</span></span>

## <span data-ttu-id="c3485-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3485-122">OUTPUTS</span></span>

### <span data-ttu-id="c3485-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3485-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c3485-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3485-124">NOTES</span></span>

## <span data-ttu-id="c3485-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3485-125">RELATED LINKS</span></span>

[<span data-ttu-id="c3485-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3485-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c3485-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3485-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c3485-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3485-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c3485-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3485-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
