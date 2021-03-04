---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: b4098481db78bf045abad04aee4e2e5076f71ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918778"
---
# <span data-ttu-id="551ee-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="551ee-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="551ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="551ee-102">SYNOPSIS</span></span>
<span data-ttu-id="551ee-103">Elfogadhatja vagy elutasíthatja egy adott közzétevő-azonosító(Publisher), az ajánlatazonosító(Termék) és a tervazonosító(Név) feltételeit.</span><span class="sxs-lookup"><span data-stu-id="551ee-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="551ee-104">Kérjük, Get-AzMarketplaceTerms fel a szerződési feltételeket.</span><span class="sxs-lookup"><span data-stu-id="551ee-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="551ee-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="551ee-105">SYNTAX</span></span>

### <span data-ttu-id="551ee-106">AgreementAcceptParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="551ee-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="551ee-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="551ee-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="551ee-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="551ee-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551ee-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="551ee-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="551ee-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="551ee-110">DESCRIPTION</span></span>
<span data-ttu-id="551ee-111">A **Set-AzMarketplaceTerms** parancsmag menti az adott közzétevőazonosító(Publisher), az ajánlatazonosító(Termék) és a tervazonosító(Név) rekord kifejezésobjektumát.</span><span class="sxs-lookup"><span data-stu-id="551ee-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="551ee-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="551ee-112">EXAMPLES</span></span>

### <span data-ttu-id="551ee-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="551ee-113">Example 1</span></span>
<span data-ttu-id="551ee-114">A piactér kiadói szerződésének lekérte</span><span class="sxs-lookup"><span data-stu-id="551ee-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="551ee-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="551ee-115">Example 2</span></span>
<span data-ttu-id="551ee-116">Állítsa be a kiadói szerződést "Elfogadás" beállításra.</span><span class="sxs-lookup"><span data-stu-id="551ee-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="551ee-117">A "Terms" paraméter értékének lekérte a Get-AzMarketplaceTerms parancsmagból</span><span class="sxs-lookup"><span data-stu-id="551ee-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="551ee-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="551ee-118">PARAMETERS</span></span>

### <span data-ttu-id="551ee-119">-Elfogadás</span><span class="sxs-lookup"><span data-stu-id="551ee-119">-Accept</span></span>
<span data-ttu-id="551ee-120">Adja át ezt a feltételek elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="551ee-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="551ee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551ee-121">-DefaultProfile</span></span>
<span data-ttu-id="551ee-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="551ee-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="551ee-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="551ee-123">-InputObject</span></span>
<span data-ttu-id="551ee-124">A visszaadott kifejezésobjektum Get-AzMarketplaceTerms parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="551ee-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="551ee-125">Ez egy kötelező paraméter, ha az Elfogadható paraméter értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="551ee-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="551ee-126">-Name</span><span class="sxs-lookup"><span data-stu-id="551ee-126">-Name</span></span>
<span data-ttu-id="551ee-127">Plan identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="551ee-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="551ee-128">-Product</span><span class="sxs-lookup"><span data-stu-id="551ee-128">-Product</span></span>
<span data-ttu-id="551ee-129">Offer identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="551ee-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="551ee-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="551ee-130">-Publisher</span></span>
<span data-ttu-id="551ee-131">Publisher identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="551ee-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="551ee-132">-Reject</span><span class="sxs-lookup"><span data-stu-id="551ee-132">-Reject</span></span>
<span data-ttu-id="551ee-133">Adja át ezt a feltételt a jogi feltételek elutasításához.</span><span class="sxs-lookup"><span data-stu-id="551ee-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="551ee-134">-Feltételek</span><span class="sxs-lookup"><span data-stu-id="551ee-134">-Terms</span></span>
<span data-ttu-id="551ee-135">A visszaadott kifejezésobjektum Get-AzMarketplaceTerms parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="551ee-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="551ee-136">Ez egy kötelező paraméter, ha az Elfogadható paraméter értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="551ee-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="551ee-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="551ee-137">-Confirm</span></span>
<span data-ttu-id="551ee-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="551ee-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="551ee-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="551ee-139">-WhatIf</span></span>
<span data-ttu-id="551ee-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="551ee-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="551ee-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="551ee-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="551ee-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551ee-142">CommonParameters</span></span>
<span data-ttu-id="551ee-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551ee-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551ee-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="551ee-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551ee-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="551ee-145">INPUTS</span></span>

### <span data-ttu-id="551ee-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="551ee-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="551ee-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="551ee-147">OUTPUTS</span></span>

### <span data-ttu-id="551ee-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="551ee-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="551ee-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="551ee-149">NOTES</span></span>

## <span data-ttu-id="551ee-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="551ee-150">RELATED LINKS</span></span>
