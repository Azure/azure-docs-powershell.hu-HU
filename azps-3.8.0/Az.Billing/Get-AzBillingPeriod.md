---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012419"
---
# <span data-ttu-id="0d3bb-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="0d3bb-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="0d3bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d3bb-102">SYNOPSIS</span></span>
<span data-ttu-id="0d3bb-103">Az előfizetés számlázási időszakának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0d3bb-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="0d3bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d3bb-104">SYNTAX</span></span>

### <span data-ttu-id="0d3bb-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d3bb-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d3bb-106">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="0d3bb-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d3bb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d3bb-107">DESCRIPTION</span></span>
<span data-ttu-id="0d3bb-108">A **Get-AzBillingPeriod** parancsmag az előfizetés számlázási időszakait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0d3bb-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="0d3bb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0d3bb-109">EXAMPLES</span></span>

### <span data-ttu-id="0d3bb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0d3bb-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="0d3bb-111">Az előfizetés összes rendelkezésre álló számlázási időszakának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="0d3bb-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="0d3bb-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0d3bb-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="0d3bb-113">A megadott nevű előfizetés számlázási időszakának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0d3bb-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="0d3bb-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="0d3bb-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="0d3bb-115">Az előfizetés legfeljebb 2 számlázási időszakának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0d3bb-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="0d3bb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d3bb-116">PARAMETERS</span></span>

### <span data-ttu-id="0d3bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d3bb-117">-DefaultProfile</span></span>
<span data-ttu-id="0d3bb-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0d3bb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d3bb-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0d3bb-119">-MaxCount</span></span>
<span data-ttu-id="0d3bb-120">Adja meg, hogy legfeljebb hány rekordot szeretne megadni.</span><span class="sxs-lookup"><span data-stu-id="0d3bb-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="0d3bb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0d3bb-121">-Name</span></span>
<span data-ttu-id="0d3bb-122">A beszerzéshez megadott számlázási időszak neve.</span><span class="sxs-lookup"><span data-stu-id="0d3bb-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="0d3bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d3bb-123">CommonParameters</span></span>
<span data-ttu-id="0d3bb-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d3bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d3bb-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d3bb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d3bb-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d3bb-126">INPUTS</span></span>

### <span data-ttu-id="0d3bb-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="0d3bb-127">None</span></span>

## <span data-ttu-id="0d3bb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d3bb-128">OUTPUTS</span></span>

### <span data-ttu-id="0d3bb-129">Microsoft. Azure. commands. számlázás. modellek. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="0d3bb-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="0d3bb-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d3bb-130">NOTES</span></span>

## <span data-ttu-id="0d3bb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d3bb-131">RELATED LINKS</span></span>
