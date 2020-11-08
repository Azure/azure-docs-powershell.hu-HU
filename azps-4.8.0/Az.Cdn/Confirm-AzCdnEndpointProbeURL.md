---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024179"
---
# <span data-ttu-id="89ceb-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="89ceb-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="89ceb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="89ceb-103">Ellenőrzi a szonda URL-címét.</span><span class="sxs-lookup"><span data-stu-id="89ceb-103">Validates a probe URL.</span></span>

## <span data-ttu-id="89ceb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89ceb-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89ceb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89ceb-105">DESCRIPTION</span></span>
<span data-ttu-id="89ceb-106">A **Confirm-AzCdnEndpointProbeURL** parancsmag igazolja, hogy a szonda URL-címe használható a dinamikus webhely-gyorsításhoz.</span><span class="sxs-lookup"><span data-stu-id="89ceb-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="89ceb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="89ceb-107">EXAMPLES</span></span>

### <span data-ttu-id="89ceb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="89ceb-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="89ceb-109">Hitelesíti a szonda URL-címét " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="89ceb-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="89ceb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89ceb-110">PARAMETERS</span></span>

### <span data-ttu-id="89ceb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ceb-111">-DefaultProfile</span></span>
<span data-ttu-id="89ceb-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89ceb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ceb-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="89ceb-113">-ProbeUrl</span></span>
<span data-ttu-id="89ceb-114">Az ellenőrzéshez javasolt szonda URL-neve</span><span class="sxs-lookup"><span data-stu-id="89ceb-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="89ceb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ceb-115">CommonParameters</span></span>
<span data-ttu-id="89ceb-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89ceb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ceb-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89ceb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ceb-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89ceb-118">INPUTS</span></span>

### <span data-ttu-id="89ceb-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="89ceb-119">None</span></span>

## <span data-ttu-id="89ceb-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89ceb-120">OUTPUTS</span></span>

### <span data-ttu-id="89ceb-121">Microsoft. Azure. Command. CDN. models. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="89ceb-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="89ceb-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89ceb-122">NOTES</span></span>

## <span data-ttu-id="89ceb-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89ceb-123">RELATED LINKS</span></span>
