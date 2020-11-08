---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194135"
---
# <span data-ttu-id="a93aa-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="a93aa-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="a93aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a93aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a93aa-103">Számlázási profilok beszerzése</span><span class="sxs-lookup"><span data-stu-id="a93aa-103">Get billing profiles.</span></span>

## <span data-ttu-id="a93aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a93aa-104">SYNTAX</span></span>

### <span data-ttu-id="a93aa-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a93aa-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a93aa-106">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="a93aa-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a93aa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a93aa-107">DESCRIPTION</span></span>
<span data-ttu-id="a93aa-108">A **Get-AzBillingProfile** parancsmag a megadott számlázási fiók alatti számlázási profilokat kapja.</span><span class="sxs-lookup"><span data-stu-id="a93aa-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="a93aa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a93aa-109">EXAMPLES</span></span>

### <span data-ttu-id="a93aa-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a93aa-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="a93aa-111">A megadott számlázási fiók alatti összes számlázási profil beszerzése.</span><span class="sxs-lookup"><span data-stu-id="a93aa-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="a93aa-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="a93aa-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="a93aa-113">A megadott nevű számlázási profil beszerzése.</span><span class="sxs-lookup"><span data-stu-id="a93aa-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="a93aa-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="a93aa-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="a93aa-115">A megadott számlázási fiók csoportban adja meg az összes számlázási profilt, és vegye fel az eredménybe a számla szakaszokat.</span><span class="sxs-lookup"><span data-stu-id="a93aa-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="a93aa-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="a93aa-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="a93aa-117">A megadott néven adja meg a számlázási profilt, és vegye fel a számla szakaszokat az eredménybe.</span><span class="sxs-lookup"><span data-stu-id="a93aa-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="a93aa-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a93aa-118">PARAMETERS</span></span>

### <span data-ttu-id="a93aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93aa-119">-DefaultProfile</span></span>
<span data-ttu-id="a93aa-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a93aa-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a93aa-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="a93aa-121">-BillingAccountName</span></span>
<span data-ttu-id="a93aa-122">Az adott számlázási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a93aa-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="a93aa-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="a93aa-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="a93aa-124">Vegye fel a számlák szakaszt a számlázási profil csoportban.</span><span class="sxs-lookup"><span data-stu-id="a93aa-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="a93aa-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a93aa-125">-Name</span></span>
<span data-ttu-id="a93aa-126">Egy adott számlázási profil neve.</span><span class="sxs-lookup"><span data-stu-id="a93aa-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="a93aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93aa-127">CommonParameters</span></span>
<span data-ttu-id="a93aa-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a93aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93aa-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a93aa-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93aa-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a93aa-130">INPUTS</span></span>

### <span data-ttu-id="a93aa-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="a93aa-131">None</span></span>

## <span data-ttu-id="a93aa-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a93aa-132">OUTPUTS</span></span>

### <span data-ttu-id="a93aa-133">Microsoft. Azure. commands. számlázás. modellek. PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="a93aa-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="a93aa-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a93aa-134">NOTES</span></span>

## <span data-ttu-id="a93aa-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a93aa-135">RELATED LINKS</span></span>
