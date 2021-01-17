---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480964"
---
# <span data-ttu-id="79d1c-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="79d1c-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="79d1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="79d1c-103">Egy url-címet ellenőriz.</span><span class="sxs-lookup"><span data-stu-id="79d1c-103">Validates a probe URL.</span></span>

## <span data-ttu-id="79d1c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79d1c-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79d1c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79d1c-105">DESCRIPTION</span></span>
<span data-ttu-id="79d1c-106">A **Confirm-AzCdnEndpointProbeURL** parancsmag megerősíti, hogy a megadott url-cím használható-e a dinamikus webhely-gyorsításhoz.</span><span class="sxs-lookup"><span data-stu-id="79d1c-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="79d1c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79d1c-107">EXAMPLES</span></span>

### <span data-ttu-id="79d1c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="79d1c-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="79d1c-109">A "" url-cím ellenőrzése http://www.bing.com/images</span><span class="sxs-lookup"><span data-stu-id="79d1c-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="79d1c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79d1c-110">PARAMETERS</span></span>

### <span data-ttu-id="79d1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d1c-111">-DefaultProfile</span></span>
<span data-ttu-id="79d1c-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79d1c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79d1c-113">-A116655666</span><span class="sxs-lookup"><span data-stu-id="79d1c-113">-ProbeUrl</span></span>
<span data-ttu-id="79d1c-114">Érvényesíthető javasolt URL-név.</span><span class="sxs-lookup"><span data-stu-id="79d1c-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="79d1c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d1c-115">CommonParameters</span></span>
<span data-ttu-id="79d1c-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79d1c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d1c-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79d1c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d1c-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79d1c-118">INPUTS</span></span>

### <span data-ttu-id="79d1c-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="79d1c-119">None</span></span>

## <span data-ttu-id="79d1c-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79d1c-120">OUTPUTS</span></span>

### <span data-ttu-id="79d1c-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="79d1c-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="79d1c-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79d1c-122">NOTES</span></span>

## <span data-ttu-id="79d1c-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79d1c-123">RELATED LINKS</span></span>
