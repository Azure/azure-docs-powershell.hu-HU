---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: f6b75a1c161515ee45571ba3db6d2f84b95af967
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493852"
---
# <span data-ttu-id="0e00b-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="0e00b-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="0e00b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e00b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e00b-103">Az előfizetés számlázási időszakának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0e00b-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e00b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e00b-104">SYNTAX</span></span>

### <span data-ttu-id="0e00b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e00b-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e00b-106">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="0e00b-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e00b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e00b-107">DESCRIPTION</span></span>
<span data-ttu-id="0e00b-108">A **Get-AzureRmBillingPeriod** parancsmag az előfizetés számlázási időszakait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0e00b-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="0e00b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0e00b-109">EXAMPLES</span></span>

### <span data-ttu-id="0e00b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0e00b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="0e00b-111">Az előfizetés összes rendelkezésre álló számlázási időszakának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="0e00b-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="0e00b-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0e00b-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="0e00b-113">A megadott nevű előfizetés számlázási időszakának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0e00b-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="0e00b-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="0e00b-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="0e00b-115">Az előfizetés legfeljebb 2 számlázási időszakának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0e00b-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="0e00b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e00b-116">PARAMETERS</span></span>

### <span data-ttu-id="0e00b-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0e00b-117">-MaxCount</span></span>
<span data-ttu-id="0e00b-118">Adja meg, hogy legfeljebb hány rekordot szeretne megadni.</span><span class="sxs-lookup"><span data-stu-id="0e00b-118">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="0e00b-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0e00b-119">-Name</span></span>
<span data-ttu-id="0e00b-120">A beszerzéshez megadott számlázási időszak neve.</span><span class="sxs-lookup"><span data-stu-id="0e00b-120">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="0e00b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e00b-121">-DefaultProfile</span></span>
<span data-ttu-id="0e00b-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e00b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e00b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e00b-123">CommonParameters</span></span>
<span data-ttu-id="0e00b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e00b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e00b-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e00b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e00b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e00b-126">INPUTS</span></span>

### <span data-ttu-id="0e00b-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="0e00b-127">None</span></span>

## <span data-ttu-id="0e00b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e00b-128">OUTPUTS</span></span>

### <span data-ttu-id="0e00b-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. számlázás. models. PSBillingPeriod, Microsoft. Azure. commands. számlázás, verzió = 0.12.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0e00b-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod, Microsoft.Azure.Commands.Billing, Version=0.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0e00b-130">Microsoft. Azure. commands. számlázás. modellek. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="0e00b-130">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="0e00b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e00b-131">NOTES</span></span>

## <span data-ttu-id="0e00b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e00b-132">RELATED LINKS</span></span>

