---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: afc2400feb8694e74dd46731969429d6d7784369
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007269"
---
# <span data-ttu-id="d3d31-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="d3d31-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="d3d31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3d31-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d31-103">Egy url-címet ellenőriz.</span><span class="sxs-lookup"><span data-stu-id="d3d31-103">Validates a probe URL.</span></span>

## <span data-ttu-id="d3d31-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3d31-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3d31-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3d31-105">DESCRIPTION</span></span>
<span data-ttu-id="d3d31-106">A **Confirm-AzCdnEndpointProbeURL** parancsmag megerősíti, hogy a megadott url-cím használható-e a dinamikus webhely-gyorsításhoz.</span><span class="sxs-lookup"><span data-stu-id="d3d31-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="d3d31-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3d31-107">EXAMPLES</span></span>

### <span data-ttu-id="d3d31-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d3d31-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="d3d31-109">A "" url-cím ellenőrzése http://www.bing.com/images</span><span class="sxs-lookup"><span data-stu-id="d3d31-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="d3d31-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3d31-110">PARAMETERS</span></span>

### <span data-ttu-id="d3d31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d31-111">-DefaultProfile</span></span>
<span data-ttu-id="d3d31-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3d31-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3d31-113">-Az 10000000000</span><span class="sxs-lookup"><span data-stu-id="d3d31-113">-ProbeUrl</span></span>
<span data-ttu-id="d3d31-114">Érvényesíthető javasolt URL-cím.</span><span class="sxs-lookup"><span data-stu-id="d3d31-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="d3d31-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d31-115">CommonParameters</span></span>
<span data-ttu-id="d3d31-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d31-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d31-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3d31-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d31-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3d31-118">INPUTS</span></span>

### <span data-ttu-id="d3d31-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="d3d31-119">None</span></span>

## <span data-ttu-id="d3d31-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3d31-120">OUTPUTS</span></span>

### <span data-ttu-id="d3d31-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="d3d31-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="d3d31-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3d31-122">NOTES</span></span>

## <span data-ttu-id="d3d31-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3d31-123">RELATED LINKS</span></span>
