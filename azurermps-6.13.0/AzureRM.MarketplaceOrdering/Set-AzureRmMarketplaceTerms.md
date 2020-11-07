---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 7932a733fcd672d8ee92e6452765745281ee0a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672244"
---
# <span data-ttu-id="208eb-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="208eb-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="208eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="208eb-102">SYNOPSIS</span></span>
<span data-ttu-id="208eb-103">Az adott közzétevői azonosító (közzétevő), az ajánlat azonosítója (szorzat) és a terv azonosítója (név) feltételeinek elfogadása vagy elvetése.</span><span class="sxs-lookup"><span data-stu-id="208eb-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="208eb-104">Kérjük, hogy a szerződési feltételeknek megfelelő Get-AzureRmMarketplaceTerms használatával töltse le a szerződési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="208eb-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="208eb-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="208eb-105">SYNTAX</span></span>

### <span data-ttu-id="208eb-106">AgreementAcceptParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="208eb-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="208eb-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="208eb-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="208eb-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="208eb-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="208eb-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="208eb-109">InputObjectRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="208eb-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="208eb-110">DESCRIPTION</span></span>
<span data-ttu-id="208eb-111">A **set-AzureRmMarketplaceTerms** parancsmag az adott közzétevői azonosító (közzétevő), az ajánlat azonosítója (szorzat) és a terv azonosítója (név) rekord tárgyát menti.</span><span class="sxs-lookup"><span data-stu-id="208eb-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="208eb-112">Példák</span><span class="sxs-lookup"><span data-stu-id="208eb-112">EXAMPLES</span></span>

### <span data-ttu-id="208eb-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="208eb-113">Example 1</span></span>
<span data-ttu-id="208eb-114">A Marketplace Publisher-szerződés beszerzése</span><span class="sxs-lookup"><span data-stu-id="208eb-114">Get the marketplace publisher agreement</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

### <span data-ttu-id="208eb-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="208eb-115">Example 2</span></span>
<span data-ttu-id="208eb-116">A Publisher-szerződés beállítása az "elfogadás" értékre</span><span class="sxs-lookup"><span data-stu-id="208eb-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="208eb-117">A ' get-AzureRmMarketplaceTerms ' parancsmag "terms" paramétere értékének beszerzése</span><span class="sxs-lookup"><span data-stu-id="208eb-117">Get the value for the 'Terms' parameter from the 'Get-AzureRmMarketplaceTerms' cmdlet</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```


## <span data-ttu-id="208eb-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="208eb-118">PARAMETERS</span></span>

### <span data-ttu-id="208eb-119">-Accept (elfogadás)</span><span class="sxs-lookup"><span data-stu-id="208eb-119">-Accept</span></span>
<span data-ttu-id="208eb-120">Adja át ezt a jogi fogalmak elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="208eb-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="208eb-121">-DefaultProfile</span></span>
<span data-ttu-id="208eb-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="208eb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="208eb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="208eb-123">-InputObject</span></span>
<span data-ttu-id="208eb-124">Get-AzureRmMarketplaceTerms parancsmagban visszaadott fogalmak objektum</span><span class="sxs-lookup"><span data-stu-id="208eb-124">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="208eb-125">Ez egy kötelező paraméter, ha az elfogadott paraméter igaz.</span><span class="sxs-lookup"><span data-stu-id="208eb-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="208eb-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="208eb-126">-Name</span></span>
<span data-ttu-id="208eb-127">A telepítendő kép terv azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="208eb-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="208eb-128">-Szorzat</span><span class="sxs-lookup"><span data-stu-id="208eb-128">-Product</span></span>
<span data-ttu-id="208eb-129">A telepített lemezkép azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="208eb-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="208eb-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="208eb-130">-Publisher</span></span>
<span data-ttu-id="208eb-131">A telepítendő lemezkép közzétevő azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="208eb-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="208eb-132">-Elutasítás</span><span class="sxs-lookup"><span data-stu-id="208eb-132">-Reject</span></span>
<span data-ttu-id="208eb-133">Adja át ezt a jogi fogalmak elutasításához.</span><span class="sxs-lookup"><span data-stu-id="208eb-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208eb-134">– A fogalmak</span><span class="sxs-lookup"><span data-stu-id="208eb-134">-Terms</span></span>
<span data-ttu-id="208eb-135">Get-AzureRmMarketplaceTerms parancsmagban visszaadott fogalmak objektum</span><span class="sxs-lookup"><span data-stu-id="208eb-135">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="208eb-136">Ez egy kötelező paraméter, ha az elfogadott paraméter igaz.</span><span class="sxs-lookup"><span data-stu-id="208eb-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="208eb-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="208eb-137">-Confirm</span></span>
<span data-ttu-id="208eb-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="208eb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="208eb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208eb-139">-WhatIf</span></span>
<span data-ttu-id="208eb-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="208eb-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="208eb-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="208eb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="208eb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208eb-142">CommonParameters</span></span>
<span data-ttu-id="208eb-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="208eb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208eb-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="208eb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208eb-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="208eb-145">INPUTS</span></span>

### <span data-ttu-id="208eb-146">Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="208eb-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="208eb-147">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="208eb-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="208eb-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="208eb-148">OUTPUTS</span></span>

### <span data-ttu-id="208eb-149">Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="208eb-149">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="208eb-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="208eb-150">NOTES</span></span>

## <span data-ttu-id="208eb-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="208eb-151">RELATED LINKS</span></span>
