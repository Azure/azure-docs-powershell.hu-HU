---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: cce3e2f9deb1f5df5c85d4f0b289b97e9cd36820
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671399"
---
# <span data-ttu-id="81bc9-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="81bc9-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="81bc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="81bc9-103">Egy CDN-végpont frissítése</span><span class="sxs-lookup"><span data-stu-id="81bc9-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="81bc9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81bc9-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81bc9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81bc9-105">DESCRIPTION</span></span>
<span data-ttu-id="81bc9-106">A **set-AzCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját frissíti.</span><span class="sxs-lookup"><span data-stu-id="81bc9-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="81bc9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="81bc9-107">EXAMPLES</span></span>

## <span data-ttu-id="81bc9-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81bc9-108">PARAMETERS</span></span>

### <span data-ttu-id="81bc9-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="81bc9-109">-CdnEndpoint</span></span>
<span data-ttu-id="81bc9-110">A parancsmag által frissített végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="81bc9-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="81bc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bc9-111">-DefaultProfile</span></span>
<span data-ttu-id="81bc9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="81bc9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81bc9-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81bc9-113">-Confirm</span></span>
<span data-ttu-id="81bc9-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81bc9-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81bc9-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81bc9-115">-WhatIf</span></span>
<span data-ttu-id="81bc9-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81bc9-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81bc9-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81bc9-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81bc9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bc9-118">CommonParameters</span></span>
<span data-ttu-id="81bc9-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81bc9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bc9-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81bc9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bc9-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bc9-121">INPUTS</span></span>

### <span data-ttu-id="81bc9-122">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="81bc9-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="81bc9-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bc9-123">OUTPUTS</span></span>

### <span data-ttu-id="81bc9-124">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="81bc9-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="81bc9-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81bc9-125">NOTES</span></span>

## <span data-ttu-id="81bc9-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81bc9-126">RELATED LINKS</span></span>

[<span data-ttu-id="81bc9-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="81bc9-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="81bc9-128">Új – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="81bc9-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="81bc9-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="81bc9-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="81bc9-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="81bc9-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="81bc9-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="81bc9-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


