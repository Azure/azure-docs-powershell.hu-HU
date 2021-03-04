---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: d2a859740d2e5627eca3ca0748aab8e72c1ee9af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938274"
---
# <span data-ttu-id="c4ec0-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="c4ec0-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="c4ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ec0-103">Lekérte az előfizetés számlázási időszakát.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="c4ec0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4ec0-104">SYNTAX</span></span>

### <span data-ttu-id="c4ec0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4ec0-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4ec0-106">Single</span><span class="sxs-lookup"><span data-stu-id="c4ec0-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4ec0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4ec0-107">DESCRIPTION</span></span>
<span data-ttu-id="c4ec0-108">A **Get-AzBillingPeriod** parancsmag az előfizetés számlázási időszakát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="c4ec0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4ec0-109">EXAMPLES</span></span>

### <span data-ttu-id="c4ec0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c4ec0-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="c4ec0-111">Szerezze be az előfizetés összes rendelkezésre álló számlázási időszakát.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="c4ec0-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c4ec0-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="c4ec0-113">Szerezze be az előfizetés számlázási időszakát a megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="c4ec0-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c4ec0-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="c4ec0-115">Az előfizetés legalább 2 számlázási időszakát le kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="c4ec0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4ec0-116">PARAMETERS</span></span>

### <span data-ttu-id="c4ec0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ec0-117">-DefaultProfile</span></span>
<span data-ttu-id="c4ec0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c4ec0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4ec0-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c4ec0-119">-MaxCount</span></span>
<span data-ttu-id="c4ec0-120">Határozza meg, hogy legfeljebb hány rekordot kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="c4ec0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c4ec0-121">-Name</span></span>
<span data-ttu-id="c4ec0-122">A lekért számlázási időszak neve.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="c4ec0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ec0-123">CommonParameters</span></span>
<span data-ttu-id="c4ec0-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ec0-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ec0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ec0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4ec0-126">INPUTS</span></span>

### <span data-ttu-id="c4ec0-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="c4ec0-127">None</span></span>

## <span data-ttu-id="c4ec0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4ec0-128">OUTPUTS</span></span>

### <span data-ttu-id="c4ec0-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="c4ec0-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="c4ec0-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4ec0-130">NOTES</span></span>

## <span data-ttu-id="c4ec0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4ec0-131">RELATED LINKS</span></span>
