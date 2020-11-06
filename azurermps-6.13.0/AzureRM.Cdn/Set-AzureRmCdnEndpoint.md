---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 3705cd0b20927c4b10360b7e02d507227ef2ec53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498364"
---
# <span data-ttu-id="bc995-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc995-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="bc995-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc995-102">SYNOPSIS</span></span>
<span data-ttu-id="bc995-103">Egy CDN-végpont frissítése</span><span class="sxs-lookup"><span data-stu-id="bc995-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc995-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc995-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc995-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc995-105">DESCRIPTION</span></span>
<span data-ttu-id="bc995-106">A **set-AzureRmCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját frissíti.</span><span class="sxs-lookup"><span data-stu-id="bc995-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bc995-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc995-107">EXAMPLES</span></span>

## <span data-ttu-id="bc995-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc995-108">PARAMETERS</span></span>

### <span data-ttu-id="bc995-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc995-109">-CdnEndpoint</span></span>
<span data-ttu-id="bc995-110">A parancsmag által frissített végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc995-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="bc995-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc995-111">-DefaultProfile</span></span>
<span data-ttu-id="bc995-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bc995-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc995-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc995-113">-Confirm</span></span>
<span data-ttu-id="bc995-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc995-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc995-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc995-115">-WhatIf</span></span>
<span data-ttu-id="bc995-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc995-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc995-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc995-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc995-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc995-118">CommonParameters</span></span>
<span data-ttu-id="bc995-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc995-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc995-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc995-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc995-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc995-121">INPUTS</span></span>

### <span data-ttu-id="bc995-122">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc995-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="bc995-123">Paraméterek: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc995-123">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="bc995-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc995-124">OUTPUTS</span></span>

### <span data-ttu-id="bc995-125">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc995-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="bc995-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc995-126">NOTES</span></span>

## <span data-ttu-id="bc995-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc995-127">RELATED LINKS</span></span>

[<span data-ttu-id="bc995-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc995-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bc995-129">Új – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc995-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bc995-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc995-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bc995-131">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc995-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bc995-132">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc995-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


