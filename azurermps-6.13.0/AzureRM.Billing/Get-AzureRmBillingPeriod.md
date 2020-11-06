---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 66c9a0bb9ba4aa2f17c48ffb737f1c8d72034f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501196"
---
# <span data-ttu-id="13b8e-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="13b8e-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="13b8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="13b8e-103">Az előfizetés számlázási időszakának beszerzése</span><span class="sxs-lookup"><span data-stu-id="13b8e-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13b8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13b8e-104">SYNTAX</span></span>

### <span data-ttu-id="13b8e-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13b8e-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13b8e-106">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="13b8e-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13b8e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="13b8e-107">DESCRIPTION</span></span>
<span data-ttu-id="13b8e-108">A **Get-AzureRmBillingPeriod** parancsmag az előfizetés számlázási időszakait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13b8e-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="13b8e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="13b8e-109">EXAMPLES</span></span>

### <span data-ttu-id="13b8e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13b8e-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="13b8e-111">Az előfizetés összes rendelkezésre álló számlázási időszakának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="13b8e-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="13b8e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="13b8e-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="13b8e-113">A megadott nevű előfizetés számlázási időszakának beszerzése</span><span class="sxs-lookup"><span data-stu-id="13b8e-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="13b8e-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="13b8e-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="13b8e-115">Az előfizetés legfeljebb 2 számlázási időszakának beszerzése</span><span class="sxs-lookup"><span data-stu-id="13b8e-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="13b8e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13b8e-116">PARAMETERS</span></span>

### <span data-ttu-id="13b8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b8e-117">-DefaultProfile</span></span>
<span data-ttu-id="13b8e-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="13b8e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13b8e-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="13b8e-119">-MaxCount</span></span>
<span data-ttu-id="13b8e-120">Adja meg, hogy legfeljebb hány rekordot szeretne megadni.</span><span class="sxs-lookup"><span data-stu-id="13b8e-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="13b8e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13b8e-121">-Name</span></span>
<span data-ttu-id="13b8e-122">A beszerzéshez megadott számlázási időszak neve.</span><span class="sxs-lookup"><span data-stu-id="13b8e-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="13b8e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b8e-123">CommonParameters</span></span>
<span data-ttu-id="13b8e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13b8e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b8e-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13b8e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b8e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13b8e-126">INPUTS</span></span>

### <span data-ttu-id="13b8e-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="13b8e-127">None</span></span>

## <span data-ttu-id="13b8e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13b8e-128">OUTPUTS</span></span>

### <span data-ttu-id="13b8e-129">Microsoft. Azure. commands. számlázás. modellek. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="13b8e-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="13b8e-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13b8e-130">NOTES</span></span>

## <span data-ttu-id="13b8e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13b8e-131">RELATED LINKS</span></span>
