---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: 6c5c11123ab39d92bb7b702542b007c8c075f9b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500924"
---
# <span data-ttu-id="7c7d2-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="7c7d2-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="7c7d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7d2-103">A CDN-végpont elérhetőségi állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="7c7d2-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c7d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c7d2-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c7d2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c7d2-105">DESCRIPTION</span></span>
<span data-ttu-id="7c7d2-106">A **Get-AzureRmCdnEndpointNameAvailability** parancsmag az Azure Content Delivery Network (CDN) végpontjának elérhetőségi állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="7c7d2-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7c7d2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7c7d2-107">EXAMPLES</span></span>

## <span data-ttu-id="7c7d2-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c7d2-108">PARAMETERS</span></span>

### <span data-ttu-id="7c7d2-109">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7c7d2-109">-EndpointName</span></span>
<span data-ttu-id="7c7d2-110">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c7d2-110">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="7c7d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7d2-111">-DefaultProfile</span></span>
<span data-ttu-id="7c7d2-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c7d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c7d2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7d2-113">CommonParameters</span></span>
<span data-ttu-id="7c7d2-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c7d2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7d2-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c7d2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7d2-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c7d2-116">INPUTS</span></span>

## <span data-ttu-id="7c7d2-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c7d2-117">OUTPUTS</span></span>

### <span data-ttu-id="7c7d2-118">Microsoft. Azure. Command. CDN. models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="7c7d2-118">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="7c7d2-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c7d2-119">NOTES</span></span>

## <span data-ttu-id="7c7d2-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c7d2-120">RELATED LINKS</span></span>

