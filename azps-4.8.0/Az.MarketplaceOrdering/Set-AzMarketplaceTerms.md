---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183513"
---
# <span data-ttu-id="f7bca-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="f7bca-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="f7bca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7bca-102">SYNOPSIS</span></span>
<span data-ttu-id="f7bca-103">Az adott közzétevői azonosító (közzétevő), az ajánlat azonosítója (szorzat) és a terv azonosítója (név) feltételeinek elfogadása vagy elvetése.</span><span class="sxs-lookup"><span data-stu-id="f7bca-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="f7bca-104">Kérjük, hogy a szerződési feltételeknek megfelelő Get-AzMarketplaceTerms használatával töltse le a szerződési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="f7bca-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="f7bca-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7bca-105">SYNTAX</span></span>

### <span data-ttu-id="f7bca-106">AgreementAcceptParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7bca-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7bca-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7bca-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7bca-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7bca-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7bca-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7bca-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7bca-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7bca-110">DESCRIPTION</span></span>
<span data-ttu-id="f7bca-111">A **set-AzMarketplaceTerms** parancsmag az adott közzétevői azonosító (közzétevő), az ajánlat azonosítója (szorzat) és a terv azonosítója (név) rekord tárgyát menti.</span><span class="sxs-lookup"><span data-stu-id="f7bca-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="f7bca-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f7bca-112">EXAMPLES</span></span>

### <span data-ttu-id="f7bca-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f7bca-113">Example 1</span></span>
<span data-ttu-id="f7bca-114">A Marketplace Publisher-szerződés beszerzése</span><span class="sxs-lookup"><span data-stu-id="f7bca-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="f7bca-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="f7bca-115">Example 2</span></span>
<span data-ttu-id="f7bca-116">A Publisher-szerződés beállítása az "elfogadás" értékre</span><span class="sxs-lookup"><span data-stu-id="f7bca-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="f7bca-117">A ' get-AzMarketplaceTerms ' parancsmag "terms" paramétere értékének beszerzése</span><span class="sxs-lookup"><span data-stu-id="f7bca-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="f7bca-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7bca-118">PARAMETERS</span></span>

### <span data-ttu-id="f7bca-119">-Accept (elfogadás)</span><span class="sxs-lookup"><span data-stu-id="f7bca-119">-Accept</span></span>
<span data-ttu-id="f7bca-120">Adja át ezt a jogi fogalmak elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="f7bca-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="f7bca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7bca-121">-DefaultProfile</span></span>
<span data-ttu-id="f7bca-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7bca-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7bca-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7bca-123">-InputObject</span></span>
<span data-ttu-id="f7bca-124">Get-AzMarketplaceTerms parancsmagban visszaadott fogalmak objektum</span><span class="sxs-lookup"><span data-stu-id="f7bca-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="f7bca-125">Ez egy kötelező paraméter, ha az elfogadható paraméter értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="f7bca-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="f7bca-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7bca-126">-Name</span></span>
<span data-ttu-id="f7bca-127">A telepítendő kép terv azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="f7bca-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="f7bca-128">-Szorzat</span><span class="sxs-lookup"><span data-stu-id="f7bca-128">-Product</span></span>
<span data-ttu-id="f7bca-129">A telepített lemezkép azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="f7bca-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="f7bca-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f7bca-130">-Publisher</span></span>
<span data-ttu-id="f7bca-131">A telepítendő lemezkép közzétevő azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="f7bca-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="f7bca-132">-Elutasítás</span><span class="sxs-lookup"><span data-stu-id="f7bca-132">-Reject</span></span>
<span data-ttu-id="f7bca-133">Adja át ezt a jogi fogalmak elutasításához.</span><span class="sxs-lookup"><span data-stu-id="f7bca-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="f7bca-134">– A fogalmak</span><span class="sxs-lookup"><span data-stu-id="f7bca-134">-Terms</span></span>
<span data-ttu-id="f7bca-135">Get-AzMarketplaceTerms parancsmagban visszaadott fogalmak objektum</span><span class="sxs-lookup"><span data-stu-id="f7bca-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="f7bca-136">Ez egy kötelező paraméter, ha az elfogadható paraméter értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="f7bca-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="f7bca-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7bca-137">-Confirm</span></span>
<span data-ttu-id="f7bca-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7bca-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7bca-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7bca-139">-WhatIf</span></span>
<span data-ttu-id="f7bca-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7bca-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7bca-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7bca-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7bca-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7bca-142">CommonParameters</span></span>
<span data-ttu-id="f7bca-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7bca-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7bca-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7bca-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7bca-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7bca-145">INPUTS</span></span>

### <span data-ttu-id="f7bca-146">Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="f7bca-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="f7bca-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7bca-147">OUTPUTS</span></span>

### <span data-ttu-id="f7bca-148">Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="f7bca-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="f7bca-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7bca-149">NOTES</span></span>

## <span data-ttu-id="f7bca-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7bca-150">RELATED LINKS</span></span>
