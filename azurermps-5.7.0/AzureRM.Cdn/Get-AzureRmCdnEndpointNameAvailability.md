---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: bf202a971497a9c43f7ed3731b7c53bc12e58d73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493233"
---
# <span data-ttu-id="f093d-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="f093d-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="f093d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f093d-102">SYNOPSIS</span></span>
<span data-ttu-id="f093d-103">A CDN-végpont elérhetőségi állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="f093d-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f093d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f093d-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f093d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f093d-105">DESCRIPTION</span></span>
<span data-ttu-id="f093d-106">A **Get-AzureRmCdnEndpointNameAvailability** parancsmag az Azure Content Delivery Network (CDN) végpontjának elérhetőségi állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="f093d-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f093d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f093d-107">EXAMPLES</span></span>

## <span data-ttu-id="f093d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f093d-108">PARAMETERS</span></span>

### <span data-ttu-id="f093d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f093d-109">-DefaultProfile</span></span>
<span data-ttu-id="f093d-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f093d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093d-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f093d-111">-EndpointName</span></span>
<span data-ttu-id="f093d-112">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f093d-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f093d-113">CommonParameters</span></span>
<span data-ttu-id="f093d-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f093d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f093d-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f093d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f093d-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f093d-116">INPUTS</span></span>

### <span data-ttu-id="f093d-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="f093d-117">None</span></span>
<span data-ttu-id="f093d-118">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f093d-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f093d-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f093d-119">OUTPUTS</span></span>

### <span data-ttu-id="f093d-120">Microsoft. Azure. Command. CDN. models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="f093d-120">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="f093d-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f093d-121">NOTES</span></span>

## <span data-ttu-id="f093d-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f093d-122">RELATED LINKS</span></span>

