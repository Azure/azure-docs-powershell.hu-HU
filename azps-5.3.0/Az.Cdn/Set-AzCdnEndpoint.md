---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480932"
---
# <span data-ttu-id="1d4b2-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d4b2-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="1d4b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d4b2-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4b2-103">Frissíti a CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="1d4b2-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="1d4b2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d4b2-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d4b2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d4b2-105">DESCRIPTION</span></span>
<span data-ttu-id="1d4b2-106">A **Set-AzCdnEndpoint** parancsmag frissíti az Azure Content Delivery Network (CDN) végpontot.</span><span class="sxs-lookup"><span data-stu-id="1d4b2-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="1d4b2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d4b2-107">EXAMPLES</span></span>

## <span data-ttu-id="1d4b2-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d4b2-108">PARAMETERS</span></span>

### <span data-ttu-id="1d4b2-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d4b2-109">-CdnEndpoint</span></span>
<span data-ttu-id="1d4b2-110">A parancsmag által frissülő végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d4b2-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d4b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4b2-111">-DefaultProfile</span></span>
<span data-ttu-id="1d4b2-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1d4b2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d4b2-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d4b2-113">-Confirm</span></span>
<span data-ttu-id="1d4b2-114">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1d4b2-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d4b2-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d4b2-115">-WhatIf</span></span>
<span data-ttu-id="1d4b2-116">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1d4b2-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d4b2-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d4b2-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d4b2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4b2-118">CommonParameters</span></span>
<span data-ttu-id="1d4b2-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d4b2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4b2-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d4b2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4b2-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d4b2-121">INPUTS</span></span>

### <span data-ttu-id="1d4b2-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d4b2-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="1d4b2-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d4b2-123">OUTPUTS</span></span>

### <span data-ttu-id="1d4b2-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d4b2-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="1d4b2-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d4b2-125">NOTES</span></span>

## <span data-ttu-id="1d4b2-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d4b2-126">RELATED LINKS</span></span>

[<span data-ttu-id="1d4b2-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d4b2-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="1d4b2-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d4b2-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="1d4b2-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d4b2-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="1d4b2-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d4b2-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="1d4b2-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d4b2-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


