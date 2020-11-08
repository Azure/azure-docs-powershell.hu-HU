---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194127"
---
# <span data-ttu-id="779e7-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="779e7-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="779e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="779e7-102">SYNOPSIS</span></span>
<span data-ttu-id="779e7-103">A számla szakaszainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="779e7-103">Get invoice sections.</span></span>

## <span data-ttu-id="779e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="779e7-104">SYNTAX</span></span>

### <span data-ttu-id="779e7-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="779e7-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="779e7-106">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="779e7-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="779e7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="779e7-107">DESCRIPTION</span></span>
<span data-ttu-id="779e7-108">A **Get-AzInvoiceSection** parancsmag a megadott számlázási profil alatt kapja meg a számla szakaszokat.</span><span class="sxs-lookup"><span data-stu-id="779e7-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="779e7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="779e7-109">EXAMPLES</span></span>

### <span data-ttu-id="779e7-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="779e7-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="779e7-111">A megadott számlázási profil alá tartozó összes számla szakasz beolvasása</span><span class="sxs-lookup"><span data-stu-id="779e7-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="779e7-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="779e7-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="779e7-113">A számla szakasz beolvasása a megadott névvel</span><span class="sxs-lookup"><span data-stu-id="779e7-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="779e7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="779e7-114">PARAMETERS</span></span>

### <span data-ttu-id="779e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="779e7-115">-DefaultProfile</span></span>
<span data-ttu-id="779e7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="779e7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="779e7-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="779e7-117">-BillingAccountName</span></span>
<span data-ttu-id="779e7-118">Az adott számlázási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="779e7-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="779e7-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="779e7-119">-BillingProfileName</span></span>
<span data-ttu-id="779e7-120">Az adott számlázási profil neve.</span><span class="sxs-lookup"><span data-stu-id="779e7-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="779e7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="779e7-121">-Name</span></span>
<span data-ttu-id="779e7-122">A számla adott részének neve.</span><span class="sxs-lookup"><span data-stu-id="779e7-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="779e7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="779e7-123">CommonParameters</span></span>
<span data-ttu-id="779e7-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="779e7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="779e7-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="779e7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="779e7-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="779e7-126">INPUTS</span></span>

### <span data-ttu-id="779e7-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="779e7-127">None</span></span>

## <span data-ttu-id="779e7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="779e7-128">OUTPUTS</span></span>

### <span data-ttu-id="779e7-129">Microsoft. Azure. commands. számlázás. modellek. PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="779e7-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="779e7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="779e7-130">NOTES</span></span>

## <span data-ttu-id="779e7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="779e7-131">RELATED LINKS</span></span>
