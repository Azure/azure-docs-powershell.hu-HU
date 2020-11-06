---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 1f21022294b1bcf5c75a7cf49dcc009600dc4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501195"
---
# <span data-ttu-id="9c914-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="9c914-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="9c914-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c914-102">SYNOPSIS</span></span>
<span data-ttu-id="9c914-103">Lekérheti az előfizetés számlázási számláit.</span><span class="sxs-lookup"><span data-stu-id="9c914-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c914-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c914-104">SYNTAX</span></span>

### <span data-ttu-id="9c914-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c914-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c914-106">Legújabb</span><span class="sxs-lookup"><span data-stu-id="9c914-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c914-107">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="9c914-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c914-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c914-108">DESCRIPTION</span></span>
<span data-ttu-id="9c914-109">A **Get-AzureRmBillingInvoice** parancsmag az előfizetés számlázási számláit kapja.</span><span class="sxs-lookup"><span data-stu-id="9c914-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="9c914-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9c914-110">EXAMPLES</span></span>

### <span data-ttu-id="9c914-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9c914-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="9c914-112">Az előfizetés legújabb számlájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9c914-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="9c914-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="9c914-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="9c914-114">A megadott nevű előfizetés számlájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9c914-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="9c914-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="9c914-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="9c914-116">Az előfizetés összes elérhető számlájának beszerzése fordított időrendi sorrendben, az URL-cím letöltése nélkül, a legutóbbi számlával kezdve.</span><span class="sxs-lookup"><span data-stu-id="9c914-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="9c914-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="9c914-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="9c914-118">Az előfizetés legutóbbi 10 számlájának beszerzése, és az eredményben szerepel a letöltési URL-cím.</span><span class="sxs-lookup"><span data-stu-id="9c914-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="9c914-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c914-119">PARAMETERS</span></span>

### <span data-ttu-id="9c914-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c914-120">-DefaultProfile</span></span>
<span data-ttu-id="9c914-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9c914-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c914-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="9c914-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="9c914-123">A számlák letöltési URL-címének létrehozása.</span><span class="sxs-lookup"><span data-stu-id="9c914-123">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="9c914-124">-Legújabb</span><span class="sxs-lookup"><span data-stu-id="9c914-124">-Latest</span></span>
<span data-ttu-id="9c914-125">A legújabb számla beszerzése.</span><span class="sxs-lookup"><span data-stu-id="9c914-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="9c914-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9c914-126">-MaxCount</span></span>
<span data-ttu-id="9c914-127">A visszaadott rekordok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c914-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="9c914-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9c914-128">-Name</span></span>
<span data-ttu-id="9c914-129">A beolvasott vagy a legutóbbiak szerint megadott számla neve</span><span class="sxs-lookup"><span data-stu-id="9c914-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="9c914-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c914-130">CommonParameters</span></span>
<span data-ttu-id="9c914-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c914-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c914-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c914-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c914-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c914-133">INPUTS</span></span>

### <span data-ttu-id="9c914-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="9c914-134">None</span></span>

## <span data-ttu-id="9c914-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c914-135">OUTPUTS</span></span>

### <span data-ttu-id="9c914-136">Microsoft. Azure. commands. számlázás. modellek. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="9c914-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="9c914-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c914-137">NOTES</span></span>

## <span data-ttu-id="9c914-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c914-138">RELATED LINKS</span></span>
