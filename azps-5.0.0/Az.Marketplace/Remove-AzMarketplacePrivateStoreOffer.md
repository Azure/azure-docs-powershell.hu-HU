---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194346"
---
# <span data-ttu-id="d4a5b-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="d4a5b-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="d4a5b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a5b-103">Egy ajánlat eltávolítása a privát áruházból.</span><span class="sxs-lookup"><span data-stu-id="d4a5b-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="d4a5b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4a5b-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4a5b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4a5b-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a5b-106">A bérlői hatókörben létrehozott privát áruházból származó ajánlat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d4a5b-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="d4a5b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d4a5b-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a5b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d4a5b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="d4a5b-109">A bérlői hatókörben létrehozott privát áruházból származó ajánlat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d4a5b-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="d4a5b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4a5b-110">PARAMETERS</span></span>

### <span data-ttu-id="d4a5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a5b-111">-DefaultProfile</span></span>
<span data-ttu-id="d4a5b-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4a5b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a5b-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="d4a5b-113">-OfferId</span></span>
<span data-ttu-id="d4a5b-114">Szükséges Azure Marketplace privateStore ajánlat</span><span class="sxs-lookup"><span data-stu-id="d4a5b-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="d4a5b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4a5b-115">-PassThru</span></span>
<span data-ttu-id="d4a5b-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d4a5b-116">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a5b-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="d4a5b-117">-PrivateStoreId</span></span>
<span data-ttu-id="d4a5b-118">Szükséges Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="d4a5b-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="d4a5b-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4a5b-119">-Confirm</span></span>
<span data-ttu-id="d4a5b-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4a5b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a5b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a5b-121">-WhatIf</span></span>
<span data-ttu-id="d4a5b-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4a5b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4a5b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4a5b-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a5b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a5b-124">CommonParameters</span></span>
<span data-ttu-id="d4a5b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4a5b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a5b-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4a5b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a5b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4a5b-127">INPUTS</span></span>

### <span data-ttu-id="d4a5b-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="d4a5b-128">None</span></span>

## <span data-ttu-id="d4a5b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4a5b-129">OUTPUTS</span></span>

### <span data-ttu-id="d4a5b-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4a5b-130">System.Boolean</span></span>

## <span data-ttu-id="d4a5b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4a5b-131">NOTES</span></span>

## <span data-ttu-id="d4a5b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4a5b-132">RELATED LINKS</span></span>