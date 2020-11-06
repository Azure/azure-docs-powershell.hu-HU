---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/confirm-azurermcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
ms.openlocfilehash: d6cf25c352c89592112aaa0a60cf7ba14ff7acf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498395"
---
# <span data-ttu-id="e5762-101">Confirm-AzureRmCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="e5762-101">Confirm-AzureRmCdnEndpointProbeURL</span></span>

## <span data-ttu-id="e5762-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5762-102">SYNOPSIS</span></span>
<span data-ttu-id="e5762-103">Ellenőrzi a szonda URL-címét.</span><span class="sxs-lookup"><span data-stu-id="e5762-103">Validates a probe URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5762-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5762-104">SYNTAX</span></span>

```
Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5762-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5762-105">DESCRIPTION</span></span>
<span data-ttu-id="e5762-106">A **Confirm-AzureRmCdnEndpointProbeURL** parancsmag igazolja, hogy a szonda URL-címe használható a dinamikus webhely-gyorsításhoz.</span><span class="sxs-lookup"><span data-stu-id="e5762-106">The **Confirm-AzureRmCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="e5762-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e5762-107">EXAMPLES</span></span>

### <span data-ttu-id="e5762-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e5762-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="e5762-109">Hitelesíti a szonda URL-címét " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="e5762-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="e5762-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5762-110">PARAMETERS</span></span>

### <span data-ttu-id="e5762-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5762-111">-DefaultProfile</span></span>
<span data-ttu-id="e5762-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5762-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5762-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="e5762-113">-ProbeUrl</span></span>
<span data-ttu-id="e5762-114">Az ellenőrzéshez javasolt szonda URL-neve</span><span class="sxs-lookup"><span data-stu-id="e5762-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="e5762-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5762-115">CommonParameters</span></span>
<span data-ttu-id="e5762-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5762-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5762-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5762-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5762-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5762-118">INPUTS</span></span>

### <span data-ttu-id="e5762-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="e5762-119">None</span></span>

## <span data-ttu-id="e5762-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5762-120">OUTPUTS</span></span>

### <span data-ttu-id="e5762-121">Microsoft. Azure. Command. CDN. models. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="e5762-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="e5762-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5762-122">NOTES</span></span>

## <span data-ttu-id="e5762-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5762-123">RELATED LINKS</span></span>
