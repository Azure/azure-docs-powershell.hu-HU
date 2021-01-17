---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339762"
---
# <span data-ttu-id="e9fcc-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="e9fcc-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="e9fcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="e9fcc-103">Számlázási profilok lekérte.</span><span class="sxs-lookup"><span data-stu-id="e9fcc-103">Get billing profiles.</span></span>

## <span data-ttu-id="e9fcc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9fcc-104">SYNTAX</span></span>

### <span data-ttu-id="e9fcc-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9fcc-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9fcc-106">Single</span><span class="sxs-lookup"><span data-stu-id="e9fcc-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9fcc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="e9fcc-108">A **Get-AzBillingProfile** parancsmag a megadott számlázási fiókhoz veszi át a számlázási profilokat.</span><span class="sxs-lookup"><span data-stu-id="e9fcc-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="e9fcc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9fcc-109">EXAMPLES</span></span>

### <span data-ttu-id="e9fcc-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="e9fcc-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="e9fcc-111">Szerezze be az összes számlázási profilt a megadott számlázási fiókban.</span><span class="sxs-lookup"><span data-stu-id="e9fcc-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="e9fcc-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="e9fcc-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="e9fcc-113">Szerezze be a megadott nevű számlázási profilt.</span><span class="sxs-lookup"><span data-stu-id="e9fcc-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="e9fcc-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="e9fcc-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="e9fcc-115">Szerezze be a megadott számlázási fiókhoz tartozó összes számlázási profilt, és adja meg a számlaszakaszokat az eredményben.</span><span class="sxs-lookup"><span data-stu-id="e9fcc-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="e9fcc-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="e9fcc-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="e9fcc-117">Szerezze be a megadott nevű számlázási profilt, és adja meg a számlaszakaszokat az eredményben.</span><span class="sxs-lookup"><span data-stu-id="e9fcc-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="e9fcc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9fcc-118">PARAMETERS</span></span>

### <span data-ttu-id="e9fcc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9fcc-119">-DefaultProfile</span></span>
<span data-ttu-id="e9fcc-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e9fcc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9fcc-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="e9fcc-121">-BillingAccountName</span></span>
<span data-ttu-id="e9fcc-122">Az adott számlázási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e9fcc-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="e9fcc-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="e9fcc-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="e9fcc-124">A számlaszakaszokat foglalja bele a számlázási profilba.</span><span class="sxs-lookup"><span data-stu-id="e9fcc-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="e9fcc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e9fcc-125">-Name</span></span>
<span data-ttu-id="e9fcc-126">Egy adott számlázási profil neve.</span><span class="sxs-lookup"><span data-stu-id="e9fcc-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="e9fcc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9fcc-127">CommonParameters</span></span>
<span data-ttu-id="e9fcc-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9fcc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9fcc-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9fcc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9fcc-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9fcc-130">INPUTS</span></span>

### <span data-ttu-id="e9fcc-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="e9fcc-131">None</span></span>

## <span data-ttu-id="e9fcc-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9fcc-132">OUTPUTS</span></span>

### <span data-ttu-id="e9fcc-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="e9fcc-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="e9fcc-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9fcc-134">NOTES</span></span>

## <span data-ttu-id="e9fcc-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9fcc-135">RELATED LINKS</span></span>
