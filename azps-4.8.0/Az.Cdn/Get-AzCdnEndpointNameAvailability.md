---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181208"
---
# <span data-ttu-id="385d0-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="385d0-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="385d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="385d0-102">SYNOPSIS</span></span>
<span data-ttu-id="385d0-103">A CDN-végpont elérhetőségi állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="385d0-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="385d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="385d0-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="385d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="385d0-105">DESCRIPTION</span></span>
<span data-ttu-id="385d0-106">A **Get-AzCdnEndpointNameAvailability** parancsmag az Azure Content Delivery Network (CDN) végpontjának elérhetőségi állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="385d0-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="385d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="385d0-107">EXAMPLES</span></span>

## <span data-ttu-id="385d0-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="385d0-108">PARAMETERS</span></span>

### <span data-ttu-id="385d0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385d0-109">-DefaultProfile</span></span>
<span data-ttu-id="385d0-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="385d0-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="385d0-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="385d0-111">-EndpointName</span></span>
<span data-ttu-id="385d0-112">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="385d0-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="385d0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385d0-113">CommonParameters</span></span>
<span data-ttu-id="385d0-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="385d0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385d0-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="385d0-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385d0-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="385d0-116">INPUTS</span></span>

### <span data-ttu-id="385d0-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="385d0-117">None</span></span>

## <span data-ttu-id="385d0-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="385d0-118">OUTPUTS</span></span>

### <span data-ttu-id="385d0-119">Microsoft. Azure. Command. CDN. models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="385d0-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="385d0-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="385d0-120">NOTES</span></span>

## <span data-ttu-id="385d0-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="385d0-121">RELATED LINKS</span></span>
