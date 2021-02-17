---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147490"
---
# <span data-ttu-id="38f88-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="38f88-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="38f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38f88-102">SYNOPSIS</span></span>
<span data-ttu-id="38f88-103">Elfogadhatja vagy elutasíthatja egy adott közzétevő-azonosító (Publisher), az ajánlatazonosító(Termék) és a tervazonosító(Név) feltételeit.</span><span class="sxs-lookup"><span data-stu-id="38f88-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="38f88-104">Kérjük, Get-AzMarketplaceTerms fel a szerződési feltételeket.</span><span class="sxs-lookup"><span data-stu-id="38f88-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="38f88-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="38f88-105">SYNTAX</span></span>

### <span data-ttu-id="38f88-106">AgreementAcceptParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38f88-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38f88-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38f88-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38f88-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="38f88-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38f88-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38f88-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38f88-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="38f88-110">DESCRIPTION</span></span>
<span data-ttu-id="38f88-111">A **Set-AzMarketplaceTerms** parancsmag menti az adott közzétevőazonosító(Publisher), az ajánlatazonosító(Termék) és a tervazonosító(Név) rekord kifejezésobjektumát.</span><span class="sxs-lookup"><span data-stu-id="38f88-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="38f88-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="38f88-112">EXAMPLES</span></span>

### <span data-ttu-id="38f88-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="38f88-113">Example 1</span></span>
<span data-ttu-id="38f88-114">A piactér kiadói szerződésének lekérte</span><span class="sxs-lookup"><span data-stu-id="38f88-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="38f88-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="38f88-115">Example 2</span></span>
<span data-ttu-id="38f88-116">Állítsa be a kiadói szerződést "Elfogadás" beállításra.</span><span class="sxs-lookup"><span data-stu-id="38f88-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="38f88-117">A "Terms" paraméter értékének lekérte a Get-AzMarketplaceTerms parancsmagból</span><span class="sxs-lookup"><span data-stu-id="38f88-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="38f88-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38f88-118">PARAMETERS</span></span>

### <span data-ttu-id="38f88-119">-Elfogadás</span><span class="sxs-lookup"><span data-stu-id="38f88-119">-Accept</span></span>
<span data-ttu-id="38f88-120">Adja át ezt a feltételek elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="38f88-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f88-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f88-121">-DefaultProfile</span></span>
<span data-ttu-id="38f88-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38f88-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38f88-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38f88-123">-InputObject</span></span>
<span data-ttu-id="38f88-124">A Get-AzMarketplaceTerms kifejezésobjektuma.</span><span class="sxs-lookup"><span data-stu-id="38f88-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="38f88-125">Ez egy kötelező paraméter, ha az Elfogadható paraméter értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="38f88-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38f88-126">-Name</span><span class="sxs-lookup"><span data-stu-id="38f88-126">-Name</span></span>
<span data-ttu-id="38f88-127">Plan identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="38f88-127">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f88-128">-Product</span><span class="sxs-lookup"><span data-stu-id="38f88-128">-Product</span></span>
<span data-ttu-id="38f88-129">Offer identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="38f88-129">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f88-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="38f88-130">-Publisher</span></span>
<span data-ttu-id="38f88-131">Publisher identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="38f88-131">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f88-132">-Reject</span><span class="sxs-lookup"><span data-stu-id="38f88-132">-Reject</span></span>
<span data-ttu-id="38f88-133">Adja át ezt a feltételt a jogi feltételek elutasításához.</span><span class="sxs-lookup"><span data-stu-id="38f88-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f88-134">-Feltételek</span><span class="sxs-lookup"><span data-stu-id="38f88-134">-Terms</span></span>
<span data-ttu-id="38f88-135">A Get-AzMarketplaceTerms kifejezésobjektum.</span><span class="sxs-lookup"><span data-stu-id="38f88-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="38f88-136">Ez egy kötelező paraméter, ha az Elfogadható paraméter értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="38f88-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f88-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38f88-137">-Confirm</span></span>
<span data-ttu-id="38f88-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="38f88-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38f88-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f88-139">-WhatIf</span></span>
<span data-ttu-id="38f88-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="38f88-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38f88-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38f88-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38f88-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f88-142">CommonParameters</span></span>
<span data-ttu-id="38f88-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f88-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f88-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f88-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f88-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38f88-145">INPUTS</span></span>

### <span data-ttu-id="38f88-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="38f88-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="38f88-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38f88-147">OUTPUTS</span></span>

### <span data-ttu-id="38f88-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="38f88-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="38f88-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="38f88-149">NOTES</span></span>

## <span data-ttu-id="38f88-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38f88-150">RELATED LINKS</span></span>
