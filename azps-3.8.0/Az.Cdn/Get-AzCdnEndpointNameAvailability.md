---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010976"
---
# <span data-ttu-id="9f180-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9f180-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="9f180-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f180-102">SYNOPSIS</span></span>
<span data-ttu-id="9f180-103">A CDN-végpont elérhetőségi állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="9f180-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="9f180-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f180-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f180-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f180-105">DESCRIPTION</span></span>
<span data-ttu-id="9f180-106">A **Get-AzCdnEndpointNameAvailability** parancsmag az Azure Content Delivery Network (CDN) végpontjának elérhetőségi állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="9f180-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="9f180-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9f180-107">EXAMPLES</span></span>

## <span data-ttu-id="9f180-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f180-108">PARAMETERS</span></span>

### <span data-ttu-id="9f180-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f180-109">-DefaultProfile</span></span>
<span data-ttu-id="9f180-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9f180-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f180-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9f180-111">-EndpointName</span></span>
<span data-ttu-id="9f180-112">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f180-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="9f180-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f180-113">CommonParameters</span></span>
<span data-ttu-id="9f180-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f180-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f180-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9f180-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f180-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f180-116">INPUTS</span></span>

### <span data-ttu-id="9f180-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="9f180-117">None</span></span>

## <span data-ttu-id="9f180-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f180-118">OUTPUTS</span></span>

### <span data-ttu-id="9f180-119">Microsoft. Azure. Command. CDN. models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="9f180-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="9f180-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f180-120">NOTES</span></span>

## <span data-ttu-id="9f180-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f180-121">RELATED LINKS</span></span>
