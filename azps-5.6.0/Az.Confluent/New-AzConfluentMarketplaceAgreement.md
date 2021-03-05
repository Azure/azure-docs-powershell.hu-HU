---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: f8c293870fa4eeb6f0df8a543473c8a9bda314c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012582"
---
# <span data-ttu-id="0fdb7-101">New-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="0fdb7-101">New-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="0fdb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fdb7-102">SYNOPSIS</span></span>
<span data-ttu-id="0fdb7-103">Piactéri feltételek elfogadása.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-103">Accept marketplace terms.</span></span>

## <span data-ttu-id="0fdb7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0fdb7-104">SYNTAX</span></span>

```
New-AzConfluentMarketplaceAgreement [-SubscriptionId <String>] [-Accepted] [-LicenseTextLink <String>]
 [-Plan <String>] [-PrivacyPolicyLink <String>] [-Product <String>] [-Publisher <String>]
 [-RetrieveDatetime <DateTime>] [-Signature <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0fdb7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0fdb7-105">DESCRIPTION</span></span>
<span data-ttu-id="0fdb7-106">Piactéri feltételek elfogadása.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-106">Accept marketplace terms.</span></span>

## <span data-ttu-id="0fdb7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0fdb7-107">EXAMPLES</span></span>

### <span data-ttu-id="0fdb7-108">1. példa: Összefolyásos piactéri szerződés létrehozása előfizetés alapján</span><span class="sxs-lookup"><span data-stu-id="0fdb7-108">Example 1: Create confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> New-AzConfluentMarketplaceAgreement -Accepted

Name    Type
----    ----
default Microsoft.Confluent/agreement
```

<span data-ttu-id="0fdb7-109">Ez a parancs összefolyásos piactér-szerződést hoz létre egy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-109">This command create confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="0fdb7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fdb7-110">PARAMETERS</span></span>

### <span data-ttu-id="0fdb7-111">- Elfogadva</span><span class="sxs-lookup"><span data-stu-id="0fdb7-111">-Accepted</span></span>
<span data-ttu-id="0fdb7-112">Ha a feltételek bármelyik verzióját elfogadják, egyébként hamisak.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-112">If any version of the terms have been accepted, otherwise false.</span></span>

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

### <span data-ttu-id="0fdb7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fdb7-113">-DefaultProfile</span></span>
<span data-ttu-id="0fdb7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fdb7-115">-LicenseTextLink</span><span class="sxs-lookup"><span data-stu-id="0fdb7-115">-LicenseTextLink</span></span>
<span data-ttu-id="0fdb7-116">Hivatkozás HTML-kódra a Microsoft és a Publisher feltételeivel.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-116">Link to HTML with Microsoft and Publisher terms.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fdb7-117">-Plan</span><span class="sxs-lookup"><span data-stu-id="0fdb7-117">-Plan</span></span>
<span data-ttu-id="0fdb7-118">A terv azonosítójának karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-118">Plan identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fdb7-119">-PrivacyPolicyLink</span><span class="sxs-lookup"><span data-stu-id="0fdb7-119">-PrivacyPolicyLink</span></span>
<span data-ttu-id="0fdb7-120">A közzétevő adatvédelmi szabályzatának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-120">Link to the privacy policy of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fdb7-121">-Product</span><span class="sxs-lookup"><span data-stu-id="0fdb7-121">-Product</span></span>
<span data-ttu-id="0fdb7-122">Termékazonosító karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-122">Product identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fdb7-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0fdb7-123">-Publisher</span></span>
<span data-ttu-id="0fdb7-124">A Publisher azonosítójának karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-124">Publisher identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fdb7-125">-RetrieveDatetime</span><span class="sxs-lookup"><span data-stu-id="0fdb7-125">-RetrieveDatetime</span></span>
<span data-ttu-id="0fdb7-126">A feltételek elfogadott időszakának dátuma és időpontja AZ EGYEZMÉNYES VILÁGIDŐ szerint.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-126">Date and time in UTC of when the terms were accepted.</span></span>
<span data-ttu-id="0fdb7-127">Ez üres, ha az Elfogadás érték hamis.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-127">This is empty if Accepted is false.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fdb7-128">-Signature</span><span class="sxs-lookup"><span data-stu-id="0fdb7-128">-Signature</span></span>
<span data-ttu-id="0fdb7-129">Feltételek aláírása.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-129">Terms signature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fdb7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0fdb7-130">-SubscriptionId</span></span>
<span data-ttu-id="0fdb7-131">Microsoft Azure-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="0fdb7-131">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fdb7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fdb7-132">-Confirm</span></span>
<span data-ttu-id="0fdb7-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fdb7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fdb7-134">-WhatIf</span></span>
<span data-ttu-id="0fdb7-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fdb7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fdb7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fdb7-137">CommonParameters</span></span>
<span data-ttu-id="0fdb7-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fdb7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fdb7-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fdb7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fdb7-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fdb7-140">INPUTS</span></span>

## <span data-ttu-id="0fdb7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fdb7-141">OUTPUTS</span></span>

### <span data-ttu-id="0fdb7-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="0fdb7-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="0fdb7-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0fdb7-143">NOTES</span></span>

<span data-ttu-id="0fdb7-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0fdb7-144">ALIASES</span></span>

## <span data-ttu-id="0fdb7-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fdb7-145">RELATED LINKS</span></span>

