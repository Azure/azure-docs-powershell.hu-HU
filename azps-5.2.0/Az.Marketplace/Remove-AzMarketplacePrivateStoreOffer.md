---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329874"
---
# <span data-ttu-id="6611f-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="6611f-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="6611f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6611f-102">SYNOPSIS</span></span>
<span data-ttu-id="6611f-103">Ajánlat eltávolítása a privát áruházból.</span><span class="sxs-lookup"><span data-stu-id="6611f-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="6611f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6611f-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6611f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6611f-105">DESCRIPTION</span></span>
<span data-ttu-id="6611f-106">Távolítsa el a bérlői webhelyen létrehozott privát áruház ajánlatát.</span><span class="sxs-lookup"><span data-stu-id="6611f-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="6611f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6611f-107">EXAMPLES</span></span>

### <span data-ttu-id="6611f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6611f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="6611f-109">Távolítsa el a bérlői webhelyen létrehozott privát áruház ajánlatát.</span><span class="sxs-lookup"><span data-stu-id="6611f-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="6611f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6611f-110">PARAMETERS</span></span>

### <span data-ttu-id="6611f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6611f-111">-DefaultProfile</span></span>
<span data-ttu-id="6611f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6611f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6611f-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="6611f-113">-OfferId</span></span>
<span data-ttu-id="6611f-114">Kötelező Azure Piactér privátStore-ajánlat</span><span class="sxs-lookup"><span data-stu-id="6611f-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="6611f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6611f-115">-PassThru</span></span>
<span data-ttu-id="6611f-116">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="6611f-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6611f-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="6611f-117">-PrivateStoreId</span></span>
<span data-ttu-id="6611f-118">Kötelező Azure Piactér privátStore</span><span class="sxs-lookup"><span data-stu-id="6611f-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="6611f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6611f-119">-Confirm</span></span>
<span data-ttu-id="6611f-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6611f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6611f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6611f-121">-WhatIf</span></span>
<span data-ttu-id="6611f-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6611f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6611f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6611f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6611f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6611f-124">CommonParameters</span></span>
<span data-ttu-id="6611f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6611f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6611f-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6611f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6611f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6611f-127">INPUTS</span></span>

### <span data-ttu-id="6611f-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="6611f-128">None</span></span>

## <span data-ttu-id="6611f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6611f-129">OUTPUTS</span></span>

### <span data-ttu-id="6611f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6611f-130">System.Boolean</span></span>

## <span data-ttu-id="6611f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6611f-131">NOTES</span></span>

## <span data-ttu-id="6611f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6611f-132">RELATED LINKS</span></span>
