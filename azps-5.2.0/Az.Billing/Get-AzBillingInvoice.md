---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339773"
---
# <span data-ttu-id="0faff-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="0faff-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="0faff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0faff-102">SYNOPSIS</span></span>
<span data-ttu-id="0faff-103">Lekérte az előfizetés számlázási számláit.</span><span class="sxs-lookup"><span data-stu-id="0faff-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="0faff-104">Számlázási fiók és számlázási profil számlázási számláinak lekérte</span><span class="sxs-lookup"><span data-stu-id="0faff-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="0faff-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0faff-105">SYNTAX</span></span>

### <span data-ttu-id="0faff-106">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0faff-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="0faff-107">Legújabb</span><span class="sxs-lookup"><span data-stu-id="0faff-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="0faff-108">Single</span><span class="sxs-lookup"><span data-stu-id="0faff-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0faff-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0faff-109">DESCRIPTION</span></span>
<span data-ttu-id="0faff-110">A **Get-AzBillingInvoice** parancsmag az előfizetés számlázási számláit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0faff-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="0faff-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0faff-111">EXAMPLES</span></span>

### <span data-ttu-id="0faff-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="0faff-113">Szerezze be az előfizetés legújabb számláját.</span><span class="sxs-lookup"><span data-stu-id="0faff-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="0faff-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="0faff-115">Szerezze be a megadott nevű előfizetés számláját.</span><span class="sxs-lookup"><span data-stu-id="0faff-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="0faff-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="0faff-117">Szerezze be az előfizetés összes elérhető számláját fordított időrendi sorrendben a legutóbbi számlával kezdve, az URL-cím letöltése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0faff-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="0faff-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="0faff-119">Szerezze be az előfizetés legutóbbi 10 számláját, és az eredményben foglalja bele a letöltési URL-címet.</span><span class="sxs-lookup"><span data-stu-id="0faff-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="0faff-120">5. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="0faff-121">Szerezze be az adott számlát név szerint, és töltse le az URL-címet az eredményben.</span><span class="sxs-lookup"><span data-stu-id="0faff-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="0faff-122">6. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="0faff-123">A számlákat a számlázási fiók nevével töltheti le, és az eredményben minden egyes számla letöltési URL-címét meg kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="0faff-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="0faff-124">7. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="0faff-125">Szerezze be a megfelelő számlát számlanévvel és számlázási fióknévvel, és az eredményben minden egyes számla letöltési URL-címét foglalja bele.</span><span class="sxs-lookup"><span data-stu-id="0faff-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="0faff-126">8. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="0faff-127">Töltse le a legújabb számlát a számlázási fiók nevével, és az eredményben tartalmazza a számla letöltési URL-címét.</span><span class="sxs-lookup"><span data-stu-id="0faff-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="0faff-128">9. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="0faff-129">Szerezze be az adott számlázási fiók és az adott számlázási profil legfrissebb 10 számláját, és az eredményben tartalmazza a letöltési URL-címet.</span><span class="sxs-lookup"><span data-stu-id="0faff-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="0faff-130">10. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="0faff-131">A legújabb számlát a számlázási fiók neve és a számlázási profil neve alapján töltheti le, és az eredményben szerepel a számla letöltési URL-címe.</span><span class="sxs-lookup"><span data-stu-id="0faff-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="0faff-132">10. példa</span><span class="sxs-lookup"><span data-stu-id="0faff-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="0faff-133">A számlakivonatokat a számlázási fiók neve és a számlázási profil neve alapján, a kezdő dátum és az időszakOn belül dátum szerint megadott számlázási időszakra vonatkozóan is leküldi.</span><span class="sxs-lookup"><span data-stu-id="0faff-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="0faff-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0faff-134">PARAMETERS</span></span>

### <span data-ttu-id="0faff-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0faff-135">-DefaultProfile</span></span>
<span data-ttu-id="0faff-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0faff-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0faff-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="0faff-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="0faff-138">Hozza létre a számlák letöltési URL-címét.</span><span class="sxs-lookup"><span data-stu-id="0faff-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="0faff-139">-Latest</span><span class="sxs-lookup"><span data-stu-id="0faff-139">-Latest</span></span>
<span data-ttu-id="0faff-140">Szerezze be a legújabb számlát.</span><span class="sxs-lookup"><span data-stu-id="0faff-140">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0faff-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0faff-141">-MaxCount</span></span>
<span data-ttu-id="0faff-142">Azt határozza meg, hogy legfeljebb hány rekordot kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="0faff-142">Determines the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0faff-143">-Name</span><span class="sxs-lookup"><span data-stu-id="0faff-143">-Name</span></span>
<span data-ttu-id="0faff-144">Egy behozni vagy a legutóbbi számla neve, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="0faff-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="0faff-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="0faff-145">-BillingAccountName</span></span>
<span data-ttu-id="0faff-146">Annak a számlázási fióknak a neve, amelyről számlát kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="0faff-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0faff-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="0faff-147">-BillingProfileName</span></span>
<span data-ttu-id="0faff-148">Annak a számlázási profilnak a neve, amelyről le kell kapnia a számlákat.</span><span class="sxs-lookup"><span data-stu-id="0faff-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0faff-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="0faff-149">-PeriodStartDate</span></span>
<span data-ttu-id="0faff-150">Számla kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="0faff-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0faff-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="0faff-151">-PeriodEndDate</span></span>
<span data-ttu-id="0faff-152">Számla záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="0faff-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="0faff-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0faff-153">CommonParameters</span></span>
<span data-ttu-id="0faff-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0faff-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0faff-155">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0faff-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0faff-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0faff-156">INPUTS</span></span>

### <span data-ttu-id="0faff-157">Nincs</span><span class="sxs-lookup"><span data-stu-id="0faff-157">None</span></span>

## <span data-ttu-id="0faff-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0faff-158">OUTPUTS</span></span>

### <span data-ttu-id="0faff-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span><span class="sxs-lookup"><span data-stu-id="0faff-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="0faff-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0faff-160">NOTES</span></span>

## <span data-ttu-id="0faff-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0faff-161">RELATED LINKS</span></span>
