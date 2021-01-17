---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335741"
---
# <span data-ttu-id="30cf6-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="30cf6-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="30cf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="30cf6-103">Számlaszakaszok megtekintése</span><span class="sxs-lookup"><span data-stu-id="30cf6-103">Get invoice sections.</span></span>

## <span data-ttu-id="30cf6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30cf6-104">SYNTAX</span></span>

### <span data-ttu-id="30cf6-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30cf6-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30cf6-106">Single</span><span class="sxs-lookup"><span data-stu-id="30cf6-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30cf6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30cf6-107">DESCRIPTION</span></span>
<span data-ttu-id="30cf6-108">A **Get-AzInvoiceSection** parancsmag a megadott számlázási profilon belül kap számlaszakaszokat.</span><span class="sxs-lookup"><span data-stu-id="30cf6-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="30cf6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30cf6-109">EXAMPLES</span></span>

### <span data-ttu-id="30cf6-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="30cf6-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="30cf6-111">A megadott számlázási profilon belül az összes számlaszakasz lekérte.</span><span class="sxs-lookup"><span data-stu-id="30cf6-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="30cf6-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="30cf6-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="30cf6-113">Szerezze be a megadott nevű számlaszakaszt.</span><span class="sxs-lookup"><span data-stu-id="30cf6-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="30cf6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30cf6-114">PARAMETERS</span></span>

### <span data-ttu-id="30cf6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30cf6-115">-DefaultProfile</span></span>
<span data-ttu-id="30cf6-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="30cf6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30cf6-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="30cf6-117">-BillingAccountName</span></span>
<span data-ttu-id="30cf6-118">Az adott számlázási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="30cf6-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="30cf6-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="30cf6-119">-BillingProfileName</span></span>
<span data-ttu-id="30cf6-120">Az adott számlázási profil neve.</span><span class="sxs-lookup"><span data-stu-id="30cf6-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="30cf6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="30cf6-121">-Name</span></span>
<span data-ttu-id="30cf6-122">Egy adott számlaszakasz neve.</span><span class="sxs-lookup"><span data-stu-id="30cf6-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="30cf6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30cf6-123">CommonParameters</span></span>
<span data-ttu-id="30cf6-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30cf6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30cf6-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30cf6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30cf6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30cf6-126">INPUTS</span></span>

### <span data-ttu-id="30cf6-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="30cf6-127">None</span></span>

## <span data-ttu-id="30cf6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30cf6-128">OUTPUTS</span></span>

### <span data-ttu-id="30cf6-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="30cf6-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="30cf6-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30cf6-130">NOTES</span></span>

## <span data-ttu-id="30cf6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30cf6-131">RELATED LINKS</span></span>
