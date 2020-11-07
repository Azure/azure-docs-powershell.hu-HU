---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 3e5b928696fde62a9628a055191d0aabf94b5311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837516"
---
# <span data-ttu-id="ec585-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ec585-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ec585-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec585-102">SYNOPSIS</span></span>
<span data-ttu-id="ec585-103">Egyéni hibaüzenetet hoz létre a HTTP-állapotkódot és az egyéni hibaüzenetek URL-címét tartalmazó URL-címmel</span><span class="sxs-lookup"><span data-stu-id="ec585-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="ec585-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec585-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec585-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec585-105">DESCRIPTION</span></span>
<span data-ttu-id="ec585-106">A **New-AzApplicationGatewayCustomError** parancsmag egyéni hibaüzenetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ec585-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="ec585-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ec585-107">EXAMPLES</span></span>

### <span data-ttu-id="ec585-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ec585-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="ec585-109">Ezzel a paranccsal létrehozhatja az 403-as http-állapotkód egyéni hibáját.</span><span class="sxs-lookup"><span data-stu-id="ec585-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="ec585-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec585-110">PARAMETERS</span></span>

### <span data-ttu-id="ec585-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="ec585-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="ec585-112">Az Application Gateway-ügyfél hibájának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="ec585-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ec585-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec585-113">-DefaultProfile</span></span>
<span data-ttu-id="ec585-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec585-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec585-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ec585-115">-StatusCode</span></span>
<span data-ttu-id="ec585-116">Az alkalmazásobjektum-ügyfél hibájának állapotkód.</span><span class="sxs-lookup"><span data-stu-id="ec585-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ec585-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec585-117">CommonParameters</span></span>
<span data-ttu-id="ec585-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec585-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec585-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec585-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec585-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec585-120">INPUTS</span></span>

### <span data-ttu-id="ec585-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="ec585-121">None</span></span>

## <span data-ttu-id="ec585-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec585-122">OUTPUTS</span></span>

### <span data-ttu-id="ec585-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ec585-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ec585-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec585-124">NOTES</span></span>

## <span data-ttu-id="ec585-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec585-125">RELATED LINKS</span></span>

[<span data-ttu-id="ec585-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ec585-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ec585-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ec585-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ec585-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ec585-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ec585-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ec585-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
