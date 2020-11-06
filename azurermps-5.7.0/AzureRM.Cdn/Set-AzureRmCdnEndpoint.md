---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 13b5b219ec789ac54332caa366cfb0277f0bfacb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495468"
---
# <span data-ttu-id="343d0-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="343d0-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="343d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="343d0-102">SYNOPSIS</span></span>
<span data-ttu-id="343d0-103">Egy CDN-végpont frissítése</span><span class="sxs-lookup"><span data-stu-id="343d0-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="343d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="343d0-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="343d0-105">DESCRIPTION</span></span>
<span data-ttu-id="343d0-106">A **set-AzureRmCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját frissíti.</span><span class="sxs-lookup"><span data-stu-id="343d0-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="343d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="343d0-107">EXAMPLES</span></span>

## <span data-ttu-id="343d0-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="343d0-108">PARAMETERS</span></span>

### <span data-ttu-id="343d0-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="343d0-109">-CdnEndpoint</span></span>
<span data-ttu-id="343d0-110">A parancsmag által frissített végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="343d0-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="343d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343d0-111">-DefaultProfile</span></span>
<span data-ttu-id="343d0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="343d0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="343d0-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="343d0-113">-Confirm</span></span>
<span data-ttu-id="343d0-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="343d0-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343d0-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343d0-115">-WhatIf</span></span>
<span data-ttu-id="343d0-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="343d0-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="343d0-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="343d0-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343d0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343d0-118">CommonParameters</span></span>
<span data-ttu-id="343d0-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="343d0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343d0-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="343d0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343d0-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="343d0-121">INPUTS</span></span>

### <span data-ttu-id="343d0-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="343d0-122">PSEndpoint</span></span>
<span data-ttu-id="343d0-123">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="343d0-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="343d0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="343d0-124">OUTPUTS</span></span>

### <span data-ttu-id="343d0-125">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="343d0-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="343d0-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="343d0-126">NOTES</span></span>

## <span data-ttu-id="343d0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="343d0-127">RELATED LINKS</span></span>

[<span data-ttu-id="343d0-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="343d0-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="343d0-129">Új – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="343d0-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="343d0-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="343d0-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="343d0-131">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="343d0-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="343d0-132">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="343d0-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


