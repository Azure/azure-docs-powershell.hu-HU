---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194139"
---
# <span data-ttu-id="9575b-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="9575b-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="9575b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9575b-102">SYNOPSIS</span></span>
<span data-ttu-id="9575b-103">Lekérheti az előfizetés számlázási számláit.</span><span class="sxs-lookup"><span data-stu-id="9575b-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="9575b-104">Számlázási számlák és számlázási profil számlázási számláinak beszerzése</span><span class="sxs-lookup"><span data-stu-id="9575b-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="9575b-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9575b-105">SYNTAX</span></span>

### <span data-ttu-id="9575b-106">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9575b-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="9575b-107">Legújabb</span><span class="sxs-lookup"><span data-stu-id="9575b-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="9575b-108">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="9575b-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9575b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9575b-109">DESCRIPTION</span></span>
<span data-ttu-id="9575b-110">A **Get-AzBillingInvoice** parancsmag az előfizetés számlázási számláit kapja.</span><span class="sxs-lookup"><span data-stu-id="9575b-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="9575b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9575b-111">EXAMPLES</span></span>

### <span data-ttu-id="9575b-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9575b-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="9575b-113">Az előfizetés legújabb számlájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9575b-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="9575b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9575b-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="9575b-115">A megadott nevű előfizetés számlájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9575b-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="9575b-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="9575b-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="9575b-117">Az előfizetés összes elérhető számlájának beszerzése fordított időrendi sorrendben, az URL-cím letöltése nélkül, a legutóbbi számlával kezdve.</span><span class="sxs-lookup"><span data-stu-id="9575b-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="9575b-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="9575b-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="9575b-119">Az előfizetés legutóbbi 10 számlájának beszerzése, és az eredményben szerepel a letöltési URL-cím.</span><span class="sxs-lookup"><span data-stu-id="9575b-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="9575b-120">Példa 5</span><span class="sxs-lookup"><span data-stu-id="9575b-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="9575b-121">Adja meg az adott számlát név szerint, és vegye fel az eredmény letöltési URL-címét.</span><span class="sxs-lookup"><span data-stu-id="9575b-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="9575b-122">6. példa</span><span class="sxs-lookup"><span data-stu-id="9575b-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="9575b-123">Számlázási fiók nevével beolvashatja a számlákat, és az eredményben az egyes számlák letöltési URL-címét is megnyithatja.</span><span class="sxs-lookup"><span data-stu-id="9575b-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="9575b-124">7. példa</span><span class="sxs-lookup"><span data-stu-id="9575b-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="9575b-125">Adjon meg konkrét számlát a számla neve és a Számlázási fiók neve alapján, és vegye fel az eredményben az egyes számlák letöltési URL-címét.</span><span class="sxs-lookup"><span data-stu-id="9575b-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="9575b-126">8. példa</span><span class="sxs-lookup"><span data-stu-id="9575b-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="9575b-127">Számlázási fiók neve szerint töltse le a legújabb számlát, és az eredményben adja meg a számla letöltési URL-címét.</span><span class="sxs-lookup"><span data-stu-id="9575b-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="9575b-128">Példa 9</span><span class="sxs-lookup"><span data-stu-id="9575b-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="9575b-129">Az adott számlázási fiók és az adott számlázási profil legutóbbi 10 számlájának beszerzése, és az eredményben szerepel a letöltési URL-cím.</span><span class="sxs-lookup"><span data-stu-id="9575b-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="9575b-130">10. példa</span><span class="sxs-lookup"><span data-stu-id="9575b-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="9575b-131">Számlázási fiók nevének és számlázási profiljának neve, valamint a számla letöltési URL-címének beszerzése az eredményben.</span><span class="sxs-lookup"><span data-stu-id="9575b-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="9575b-132">10. példa</span><span class="sxs-lookup"><span data-stu-id="9575b-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="9575b-133">A számlák számlázási fiók neve és számlázási profil neve szerint perioStart a dátum és a periodEnd dátuma által megadott számlázási időszakra.</span><span class="sxs-lookup"><span data-stu-id="9575b-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="9575b-134">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9575b-134">PARAMETERS</span></span>

### <span data-ttu-id="9575b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9575b-135">-DefaultProfile</span></span>
<span data-ttu-id="9575b-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9575b-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9575b-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="9575b-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="9575b-138">A számlák letöltési URL-címének létrehozása.</span><span class="sxs-lookup"><span data-stu-id="9575b-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="9575b-139">-Legújabb</span><span class="sxs-lookup"><span data-stu-id="9575b-139">-Latest</span></span>
<span data-ttu-id="9575b-140">A legújabb számla beszerzése.</span><span class="sxs-lookup"><span data-stu-id="9575b-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="9575b-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9575b-141">-MaxCount</span></span>
<span data-ttu-id="9575b-142">A visszaadott rekordok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9575b-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="9575b-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9575b-143">-Name</span></span>
<span data-ttu-id="9575b-144">A beolvasott vagy a legutóbbiak szerint megadott számla neve</span><span class="sxs-lookup"><span data-stu-id="9575b-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="9575b-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="9575b-145">-BillingAccountName</span></span>
<span data-ttu-id="9575b-146">Egy adott számlázási fiók neve, amelyhez számlákat szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="9575b-146">Name of a specific billing account to get invoices for.</span></span>

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

### <span data-ttu-id="9575b-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="9575b-147">-BillingProfileName</span></span>
<span data-ttu-id="9575b-148">Annak a meghatározott számlázási profilnak a neve, amelyhez számlákat szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="9575b-148">Name of a specific billing profile to get invoices for.</span></span>

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

### <span data-ttu-id="9575b-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="9575b-149">-PeriodStartDate</span></span>
<span data-ttu-id="9575b-150">Számla kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="9575b-150">Start date for invoice.</span></span>

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

### <span data-ttu-id="9575b-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="9575b-151">-PeriodEndDate</span></span>
<span data-ttu-id="9575b-152">Számla befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="9575b-152">End date for invoice.</span></span>

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



### <span data-ttu-id="9575b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9575b-153">CommonParameters</span></span>
<span data-ttu-id="9575b-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9575b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9575b-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9575b-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9575b-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9575b-156">INPUTS</span></span>

### <span data-ttu-id="9575b-157">Nincs</span><span class="sxs-lookup"><span data-stu-id="9575b-157">None</span></span>

## <span data-ttu-id="9575b-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9575b-158">OUTPUTS</span></span>

### <span data-ttu-id="9575b-159">Microsoft. Azure. commands. számlázás. modellek. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="9575b-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="9575b-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9575b-160">NOTES</span></span>

## <span data-ttu-id="9575b-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9575b-161">RELATED LINKS</span></span>
