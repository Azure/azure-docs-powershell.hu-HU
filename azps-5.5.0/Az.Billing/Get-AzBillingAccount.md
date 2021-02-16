---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149250"
---
# <span data-ttu-id="fba5f-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="fba5f-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="fba5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fba5f-102">SYNOPSIS</span></span>
<span data-ttu-id="fba5f-103">Számlázási fiókok lekérte.</span><span class="sxs-lookup"><span data-stu-id="fba5f-103">Get billing accounts.</span></span>

## <span data-ttu-id="fba5f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fba5f-104">SYNTAX</span></span>

### <span data-ttu-id="fba5f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fba5f-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fba5f-106">Single</span><span class="sxs-lookup"><span data-stu-id="fba5f-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fba5f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fba5f-107">DESCRIPTION</span></span>
<span data-ttu-id="fba5f-108">A **Get-AzBillingAccount** parancsmag számlázási fiókokat kap, és a felhasználó rendelkezik hozzáféréssel.</span><span class="sxs-lookup"><span data-stu-id="fba5f-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="fba5f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fba5f-109">EXAMPLES</span></span>

### <span data-ttu-id="fba5f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="fba5f-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="fba5f-111">Szerezze be az összes számlázási fiókot, amelyhez a felhasználó hozzáfér.</span><span class="sxs-lookup"><span data-stu-id="fba5f-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="fba5f-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="fba5f-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="fba5f-113">Szerezze be a megadott nevű számlázási fiókot.</span><span class="sxs-lookup"><span data-stu-id="fba5f-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="fba5f-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="fba5f-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="fba5f-115">Szerezze be az összes számlázási fiókot, amelyekhez a felhasználó hozzáfér, és az eredményben szerepeltetve tartalmazza a címet.</span><span class="sxs-lookup"><span data-stu-id="fba5f-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="fba5f-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="fba5f-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="fba5f-117">Szerezze be az összes olyan számlázási fiókot, amelyhez a felhasználó hozzáfér, és az eredményben szerepelteti a számlázási profilokat.</span><span class="sxs-lookup"><span data-stu-id="fba5f-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="fba5f-118">5. példa</span><span class="sxs-lookup"><span data-stu-id="fba5f-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="fba5f-119">Szerezze be az összes számlázási fiókot, amelyhez a felhasználó hozzáfér, és az eredményben foglalja bele a számlázási profilokat és a számlaszakaszokat.</span><span class="sxs-lookup"><span data-stu-id="fba5f-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="fba5f-120">6. példa</span><span class="sxs-lookup"><span data-stu-id="fba5f-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="fba5f-121">Szerezze be a megadott nevű számlázási fiókot, és az eredményben adja meg a címet, a számlázási profilokat és a számlaszakaszokat.</span><span class="sxs-lookup"><span data-stu-id="fba5f-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="fba5f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fba5f-122">PARAMETERS</span></span>

### <span data-ttu-id="fba5f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba5f-123">-DefaultProfile</span></span>
<span data-ttu-id="fba5f-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fba5f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fba5f-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="fba5f-125">-IncludeAddress</span></span>
<span data-ttu-id="fba5f-126">Tartalmazza a számlázási fiók címét.</span><span class="sxs-lookup"><span data-stu-id="fba5f-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="fba5f-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="fba5f-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="fba5f-128">A számlázási fiókba foglalja bele a számlázási profilokat.</span><span class="sxs-lookup"><span data-stu-id="fba5f-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="fba5f-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="fba5f-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="fba5f-130">A számlázási profilokat a számlázási fiók és a számlák szakaszba foglalja bele.</span><span class="sxs-lookup"><span data-stu-id="fba5f-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="fba5f-131">-Name</span><span class="sxs-lookup"><span data-stu-id="fba5f-131">-Name</span></span>
<span data-ttu-id="fba5f-132">Egy adott számlázási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="fba5f-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="fba5f-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="fba5f-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="fba5f-134">A számlázási fiókban sorolja fel azokat a számlázási entitásokat, amelyek bemenetként használhatók az előfizetés létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="fba5f-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

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

### <span data-ttu-id="fba5f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba5f-135">CommonParameters</span></span>
<span data-ttu-id="fba5f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba5f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba5f-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fba5f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba5f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fba5f-138">INPUTS</span></span>

### <span data-ttu-id="fba5f-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="fba5f-139">None</span></span>

## <span data-ttu-id="fba5f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fba5f-140">OUTPUTS</span></span>

### <span data-ttu-id="fba5f-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="fba5f-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="fba5f-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fba5f-142">NOTES</span></span>

## <span data-ttu-id="fba5f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fba5f-143">RELATED LINKS</span></span>
