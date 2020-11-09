---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302123"
---
# <span data-ttu-id="ebd02-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="ebd02-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="ebd02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebd02-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd02-103">Számlázási fiókok beszerzése</span><span class="sxs-lookup"><span data-stu-id="ebd02-103">Get billing accounts.</span></span>

## <span data-ttu-id="ebd02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebd02-104">SYNTAX</span></span>

### <span data-ttu-id="ebd02-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebd02-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebd02-106">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="ebd02-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebd02-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebd02-107">DESCRIPTION</span></span>
<span data-ttu-id="ebd02-108">A **Get-AzBillingAccount** parancsmag számlázási fiókokat kap, a felhasználónak hozzáférése van.</span><span class="sxs-lookup"><span data-stu-id="ebd02-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="ebd02-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ebd02-109">EXAMPLES</span></span>

### <span data-ttu-id="ebd02-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ebd02-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="ebd02-111">Az összes számlázási fiók beszerzése: a felhasználónak hozzáférése van.</span><span class="sxs-lookup"><span data-stu-id="ebd02-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="ebd02-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="ebd02-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="ebd02-113">A megadott nevű számlázási fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="ebd02-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="ebd02-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="ebd02-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="ebd02-115">Az összes számlázási fiók beszerzése: a felhasználó hozzáféréssel rendelkezik, és felveheti a címet az eredménybe.</span><span class="sxs-lookup"><span data-stu-id="ebd02-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="ebd02-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="ebd02-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="ebd02-117">Az összes számlázási fiók beszerzése: a felhasználó hozzáférhet az eredményhez, és felveszi a számlázási profilokat.</span><span class="sxs-lookup"><span data-stu-id="ebd02-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="ebd02-118">Példa 5</span><span class="sxs-lookup"><span data-stu-id="ebd02-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="ebd02-119">Az összes számlázási fiók beszerzése: a felhasználó hozzáféréssel rendelkezik, és belefoglalhatja a számlázási profilokat és a számla szakaszokat az eredményben.</span><span class="sxs-lookup"><span data-stu-id="ebd02-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="ebd02-120">6. példa</span><span class="sxs-lookup"><span data-stu-id="ebd02-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="ebd02-121">Adja meg a megadott nevű számlázási fiókot, és adja meg a cím, a számlázási profilok és a számla szakaszt az eredményben.</span><span class="sxs-lookup"><span data-stu-id="ebd02-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="ebd02-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebd02-122">PARAMETERS</span></span>

### <span data-ttu-id="ebd02-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd02-123">-DefaultProfile</span></span>
<span data-ttu-id="ebd02-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ebd02-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebd02-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="ebd02-125">-IncludeAddress</span></span>
<span data-ttu-id="ebd02-126">Adja meg a Számlázási fiók címét.</span><span class="sxs-lookup"><span data-stu-id="ebd02-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="ebd02-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="ebd02-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="ebd02-128">Adja meg a számlázási profilokat a Számlázási fiók csoportban.</span><span class="sxs-lookup"><span data-stu-id="ebd02-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="ebd02-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="ebd02-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="ebd02-130">Adja meg a számlázási profilokat az alatta lévő számlázási fiók és számlák szakaszban.</span><span class="sxs-lookup"><span data-stu-id="ebd02-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="ebd02-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ebd02-131">-Name</span></span>
<span data-ttu-id="ebd02-132">Egy adott számlázási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ebd02-132">Name of a specific billing account.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebd02-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="ebd02-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="ebd02-134">A számlázási entitások listája a Számlázási fiók csoportban, amelyet az előfizetés létrehozásakor a bemenetként használhat.</span><span class="sxs-lookup"><span data-stu-id="ebd02-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebd02-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd02-135">CommonParameters</span></span>
<span data-ttu-id="ebd02-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebd02-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd02-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebd02-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd02-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebd02-138">INPUTS</span></span>

### <span data-ttu-id="ebd02-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="ebd02-139">None</span></span>

## <span data-ttu-id="ebd02-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebd02-140">OUTPUTS</span></span>

### <span data-ttu-id="ebd02-141">Microsoft. Azure. commands. számlázás. modellek. PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="ebd02-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="ebd02-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebd02-142">NOTES</span></span>

## <span data-ttu-id="ebd02-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebd02-143">RELATED LINKS</span></span>
