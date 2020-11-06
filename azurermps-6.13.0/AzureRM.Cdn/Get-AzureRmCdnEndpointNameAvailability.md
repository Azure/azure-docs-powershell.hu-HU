---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: c5db5d27edb537602638ff5654a6da3ac35813ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500256"
---
# <span data-ttu-id="56e38-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="56e38-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="56e38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56e38-102">SYNOPSIS</span></span>
<span data-ttu-id="56e38-103">A CDN-végpont elérhetőségi állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="56e38-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56e38-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56e38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="56e38-105">DESCRIPTION</span></span>
<span data-ttu-id="56e38-106">A **Get-AzureRmCdnEndpointNameAvailability** parancsmag az Azure Content Delivery Network (CDN) végpontjának elérhetőségi állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="56e38-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="56e38-107">Példák</span><span class="sxs-lookup"><span data-stu-id="56e38-107">EXAMPLES</span></span>

## <span data-ttu-id="56e38-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56e38-108">PARAMETERS</span></span>

### <span data-ttu-id="56e38-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e38-109">-DefaultProfile</span></span>
<span data-ttu-id="56e38-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="56e38-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e38-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="56e38-111">-EndpointName</span></span>
<span data-ttu-id="56e38-112">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56e38-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="56e38-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e38-113">CommonParameters</span></span>
<span data-ttu-id="56e38-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56e38-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e38-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e38-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e38-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56e38-116">INPUTS</span></span>

### <span data-ttu-id="56e38-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="56e38-117">None</span></span>

## <span data-ttu-id="56e38-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56e38-118">OUTPUTS</span></span>

### <span data-ttu-id="56e38-119">Microsoft. Azure. Command. CDN. models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="56e38-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="56e38-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56e38-120">NOTES</span></span>

## <span data-ttu-id="56e38-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56e38-121">RELATED LINKS</span></span>
