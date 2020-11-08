---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2b1906d07b3e08b1761469b4a9d6d8d565e0fd8c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012440"
---
# <span data-ttu-id="91396-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="91396-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="91396-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91396-102">SYNOPSIS</span></span>
<span data-ttu-id="91396-103">Lekérheti az előfizetés számlázási számláit.</span><span class="sxs-lookup"><span data-stu-id="91396-103">Get billing invoices of the subscription.</span></span>

## <span data-ttu-id="91396-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91396-104">SYNTAX</span></span>

### <span data-ttu-id="91396-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91396-105">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91396-106">Legújabb</span><span class="sxs-lookup"><span data-stu-id="91396-106">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91396-107">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="91396-107">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91396-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="91396-108">DESCRIPTION</span></span>
<span data-ttu-id="91396-109">A **Get-AzBillingInvoice** parancsmag az előfizetés számlázási számláit kapja.</span><span class="sxs-lookup"><span data-stu-id="91396-109">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="91396-110">Példák</span><span class="sxs-lookup"><span data-stu-id="91396-110">EXAMPLES</span></span>

### <span data-ttu-id="91396-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91396-111">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="91396-112">Az előfizetés legújabb számlájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="91396-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="91396-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="91396-113">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="91396-114">A megadott nevű előfizetés számlájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="91396-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="91396-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="91396-115">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="91396-116">Az előfizetés összes elérhető számlájának beszerzése fordított időrendi sorrendben, az URL-cím letöltése nélkül, a legutóbbi számlával kezdve.</span><span class="sxs-lookup"><span data-stu-id="91396-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="91396-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="91396-117">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="91396-118">Az előfizetés legutóbbi 10 számlájának beszerzése, és az eredményben szerepel a letöltési URL-cím.</span><span class="sxs-lookup"><span data-stu-id="91396-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="91396-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91396-119">PARAMETERS</span></span>

### <span data-ttu-id="91396-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91396-120">-DefaultProfile</span></span>
<span data-ttu-id="91396-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="91396-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91396-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="91396-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="91396-123">A számlák letöltési URL-címének létrehozása.</span><span class="sxs-lookup"><span data-stu-id="91396-123">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91396-124">-Legújabb</span><span class="sxs-lookup"><span data-stu-id="91396-124">-Latest</span></span>
<span data-ttu-id="91396-125">A legújabb számla beszerzése.</span><span class="sxs-lookup"><span data-stu-id="91396-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="91396-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="91396-126">-MaxCount</span></span>
<span data-ttu-id="91396-127">A visszaadott rekordok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91396-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="91396-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91396-128">-Name</span></span>
<span data-ttu-id="91396-129">A beolvasott vagy a legutóbbiak szerint megadott számla neve</span><span class="sxs-lookup"><span data-stu-id="91396-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="91396-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91396-130">CommonParameters</span></span>
<span data-ttu-id="91396-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91396-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91396-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91396-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91396-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91396-133">INPUTS</span></span>

### <span data-ttu-id="91396-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="91396-134">None</span></span>

## <span data-ttu-id="91396-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91396-135">OUTPUTS</span></span>

### <span data-ttu-id="91396-136">Microsoft. Azure. commands. számlázás. modellek. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="91396-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="91396-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91396-137">NOTES</span></span>

## <span data-ttu-id="91396-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91396-138">RELATED LINKS</span></span>
