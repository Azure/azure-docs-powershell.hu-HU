---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 843bb68c5aebc18af60e1cc74915b269738059f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504887"
---
# <span data-ttu-id="a99a8-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a99a8-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="a99a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a99a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a99a8-103">Az adott közzétevői azonosító (közzétevő), az ajánlat azonosítója (szorzat) és a terv azonosítója (név) feltételeinek elfogadása vagy elvetése.</span><span class="sxs-lookup"><span data-stu-id="a99a8-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a99a8-104">Kérjük, hogy a szerződési feltételeknek megfelelő Get-AzureRmMarketplaceTerms használatával töltse le a szerződési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="a99a8-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a99a8-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a99a8-105">SYNTAX</span></span>

### <span data-ttu-id="a99a8-106">AgreementAcceptParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a99a8-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a99a8-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a99a8-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a99a8-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="a99a8-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a99a8-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="a99a8-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a99a8-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="a99a8-110">DESCRIPTION</span></span>
<span data-ttu-id="a99a8-111">A **set-AzureRmMarketplaceTerms** parancsmag az adott közzétevői azonosító (közzétevő), az ajánlat azonosítója (szorzat) és a terv azonosítója (név) rekord tárgyát menti.</span><span class="sxs-lookup"><span data-stu-id="a99a8-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="a99a8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a99a8-112">EXAMPLES</span></span>

### <span data-ttu-id="a99a8-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a99a8-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="a99a8-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a99a8-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="a99a8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a99a8-115">PARAMETERS</span></span>

### <span data-ttu-id="a99a8-116">-Accept (elfogadás)</span><span class="sxs-lookup"><span data-stu-id="a99a8-116">-Accept</span></span>
<span data-ttu-id="a99a8-117">Adja át ezt a jogi fogalmak elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="a99a8-117">Pass this to accept the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99a8-118">-DefaultProfile</span></span>
<span data-ttu-id="a99a8-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a99a8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a99a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a99a8-120">-InputObject</span></span>
<span data-ttu-id="a99a8-121">Get-AzureRmMarketplaceTerms parancsmagban visszaadott fogalmak objektum</span><span class="sxs-lookup"><span data-stu-id="a99a8-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="a99a8-122">Ez egy kötelező paraméter, ha az elfogadott paraméter igaz.</span><span class="sxs-lookup"><span data-stu-id="a99a8-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a99a8-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a99a8-123">-Name</span></span>
<span data-ttu-id="a99a8-124">A telepítendő kép terv azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="a99a8-124">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99a8-125">-Szorzat</span><span class="sxs-lookup"><span data-stu-id="a99a8-125">-Product</span></span>
<span data-ttu-id="a99a8-126">A telepített lemezkép azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="a99a8-126">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99a8-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a99a8-127">-Publisher</span></span>
<span data-ttu-id="a99a8-128">A telepítendő lemezkép közzétevő azonosító karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="a99a8-128">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99a8-129">-Elutasítás</span><span class="sxs-lookup"><span data-stu-id="a99a8-129">-Reject</span></span>
<span data-ttu-id="a99a8-130">Adja át ezt a jogi fogalmak elutasításához.</span><span class="sxs-lookup"><span data-stu-id="a99a8-130">Pass this to reject the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99a8-131">– A fogalmak</span><span class="sxs-lookup"><span data-stu-id="a99a8-131">-Terms</span></span>
<span data-ttu-id="a99a8-132">Get-AzureRmMarketplaceTerms parancsmagban visszaadott fogalmak objektum</span><span class="sxs-lookup"><span data-stu-id="a99a8-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="a99a8-133">Ez egy kötelező paraméter, ha az elfogadott paraméter igaz.</span><span class="sxs-lookup"><span data-stu-id="a99a8-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99a8-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a99a8-134">-Confirm</span></span>
<span data-ttu-id="a99a8-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a99a8-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99a8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a99a8-136">-WhatIf</span></span>
<span data-ttu-id="a99a8-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a99a8-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a99a8-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a99a8-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99a8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99a8-139">CommonParameters</span></span>
<span data-ttu-id="a99a8-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a99a8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99a8-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99a8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99a8-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a99a8-142">INPUTS</span></span>

### <span data-ttu-id="a99a8-143">Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a99a8-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="a99a8-144">Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a99a8-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a99a8-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a99a8-145">OUTPUTS</span></span>

### <span data-ttu-id="a99a8-146">Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a99a8-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="a99a8-147">Microsoft. Azure. Command. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a99a8-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a99a8-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a99a8-148">NOTES</span></span>

## <span data-ttu-id="a99a8-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a99a8-149">RELATED LINKS</span></span>

