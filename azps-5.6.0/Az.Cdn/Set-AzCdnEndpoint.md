---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 4270f7c9781ef960cdbb20a8a067a3dc22255723
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941938"
---
# <span data-ttu-id="9e65e-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e65e-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="9e65e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e65e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e65e-103">Frissíti a CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="9e65e-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="9e65e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e65e-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e65e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e65e-105">DESCRIPTION</span></span>
<span data-ttu-id="9e65e-106">A **Set-AzCdnEndpoint** parancsmag frissíti az Azure Content Delivery Network (CDN) végpontot.</span><span class="sxs-lookup"><span data-stu-id="9e65e-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="9e65e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e65e-107">EXAMPLES</span></span>

## <span data-ttu-id="9e65e-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e65e-108">PARAMETERS</span></span>

### <span data-ttu-id="9e65e-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e65e-109">-CdnEndpoint</span></span>
<span data-ttu-id="9e65e-110">A parancsmag által frissülő végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e65e-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="9e65e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e65e-111">-DefaultProfile</span></span>
<span data-ttu-id="9e65e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9e65e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e65e-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e65e-113">-Confirm</span></span>
<span data-ttu-id="9e65e-114">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9e65e-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e65e-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e65e-115">-WhatIf</span></span>
<span data-ttu-id="9e65e-116">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9e65e-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e65e-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e65e-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e65e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e65e-118">CommonParameters</span></span>
<span data-ttu-id="9e65e-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e65e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e65e-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e65e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e65e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e65e-121">INPUTS</span></span>

### <span data-ttu-id="9e65e-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e65e-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9e65e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e65e-123">OUTPUTS</span></span>

### <span data-ttu-id="9e65e-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e65e-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9e65e-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e65e-125">NOTES</span></span>

## <span data-ttu-id="9e65e-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e65e-126">RELATED LINKS</span></span>

[<span data-ttu-id="9e65e-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e65e-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="9e65e-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e65e-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="9e65e-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e65e-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="9e65e-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e65e-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="9e65e-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e65e-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


