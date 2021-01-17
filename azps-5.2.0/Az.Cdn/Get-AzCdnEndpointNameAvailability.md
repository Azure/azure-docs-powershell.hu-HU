---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350274"
---
# <span data-ttu-id="41e67-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="41e67-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="41e67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41e67-102">SYNOPSIS</span></span>
<span data-ttu-id="41e67-103">A CDN-végpont elérhetőségi állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41e67-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="41e67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41e67-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41e67-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41e67-105">DESCRIPTION</span></span>
<span data-ttu-id="41e67-106">A **Get-AzCdnEndpointNameAvailability** parancsmag az Azure Content Delivery Network (CDN) végpont elérhetőségi állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41e67-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="41e67-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41e67-107">EXAMPLES</span></span>

## <span data-ttu-id="41e67-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41e67-108">PARAMETERS</span></span>

### <span data-ttu-id="41e67-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e67-109">-DefaultProfile</span></span>
<span data-ttu-id="41e67-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="41e67-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41e67-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="41e67-111">-EndpointName</span></span>
<span data-ttu-id="41e67-112">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41e67-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="41e67-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e67-113">CommonParameters</span></span>
<span data-ttu-id="41e67-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41e67-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e67-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41e67-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e67-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41e67-116">INPUTS</span></span>

### <span data-ttu-id="41e67-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="41e67-117">None</span></span>

## <span data-ttu-id="41e67-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41e67-118">OUTPUTS</span></span>

### <span data-ttu-id="41e67-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="41e67-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="41e67-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41e67-120">NOTES</span></span>

## <span data-ttu-id="41e67-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41e67-121">RELATED LINKS</span></span>
