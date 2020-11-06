---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 38b1c4e29ed82ac3bddcff9565a216bd6db23411
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500095"
---
# <span data-ttu-id="2ba01-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="2ba01-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="2ba01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ba01-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba01-103">Lekérheti az előfizetés számlázási számláit.</span><span class="sxs-lookup"><span data-stu-id="2ba01-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ba01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ba01-104">SYNTAX</span></span>

### <span data-ttu-id="2ba01-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ba01-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ba01-106">Legújabb</span><span class="sxs-lookup"><span data-stu-id="2ba01-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ba01-107">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="2ba01-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ba01-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ba01-108">DESCRIPTION</span></span>
<span data-ttu-id="2ba01-109">A **Get-AzureRmBillingInvoice** parancsmag az előfizetés számlázási számláit kapja.</span><span class="sxs-lookup"><span data-stu-id="2ba01-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="2ba01-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2ba01-110">EXAMPLES</span></span>

### <span data-ttu-id="2ba01-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2ba01-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="2ba01-112">Az előfizetés legújabb számlájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2ba01-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="2ba01-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2ba01-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="2ba01-114">A megadott nevű előfizetés számlájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2ba01-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="2ba01-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="2ba01-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="2ba01-116">Az előfizetés összes elérhető számlájának beszerzése fordított időrendi sorrendben, az URL-cím letöltése nélkül, a legutóbbi számlával kezdve.</span><span class="sxs-lookup"><span data-stu-id="2ba01-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="2ba01-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="2ba01-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="2ba01-118">Az előfizetés legutóbbi 10 számlájának beszerzése, és az eredményben szerepel a letöltési URL-cím.</span><span class="sxs-lookup"><span data-stu-id="2ba01-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="2ba01-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ba01-119">PARAMETERS</span></span>

### <span data-ttu-id="2ba01-120">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="2ba01-120">-GenerateDownloadUrl</span></span>
<span data-ttu-id="2ba01-121">A számlák letöltési URL-címének létrehozása.</span><span class="sxs-lookup"><span data-stu-id="2ba01-121">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="2ba01-122">-Legújabb</span><span class="sxs-lookup"><span data-stu-id="2ba01-122">-Latest</span></span>
<span data-ttu-id="2ba01-123">A legújabb számla beszerzése.</span><span class="sxs-lookup"><span data-stu-id="2ba01-123">Get the latest invoice.</span></span>

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

### <span data-ttu-id="2ba01-124">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2ba01-124">-MaxCount</span></span>
<span data-ttu-id="2ba01-125">A visszaadott rekordok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ba01-125">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="2ba01-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ba01-126">-Name</span></span>
<span data-ttu-id="2ba01-127">A beolvasott vagy a legutóbbiak szerint megadott számla neve</span><span class="sxs-lookup"><span data-stu-id="2ba01-127">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="2ba01-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba01-128">-DefaultProfile</span></span>
<span data-ttu-id="2ba01-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ba01-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ba01-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba01-130">CommonParameters</span></span>
<span data-ttu-id="2ba01-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ba01-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba01-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ba01-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba01-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ba01-133">INPUTS</span></span>

### <span data-ttu-id="2ba01-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="2ba01-134">None</span></span>

## <span data-ttu-id="2ba01-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ba01-135">OUTPUTS</span></span>

### <span data-ttu-id="2ba01-136">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. számlázás. models. számla, Microsoft. Azure. commands. számlázás, verzió = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2ba01-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Billing.Models.Invoice, Microsoft.Azure.Commands.Billing, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2ba01-137">Microsoft. Azure. Management. számlázás. modellek. számla</span><span class="sxs-lookup"><span data-stu-id="2ba01-137">Microsoft.Azure.Management.Billing.Models.Invoice</span></span>

## <span data-ttu-id="2ba01-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ba01-138">NOTES</span></span>

## <span data-ttu-id="2ba01-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ba01-139">RELATED LINKS</span></span>

