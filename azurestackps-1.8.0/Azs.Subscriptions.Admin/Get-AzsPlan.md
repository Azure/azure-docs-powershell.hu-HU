---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02baf67cc13269d9d53c0adb40337adbd9929641
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840173"
---
# <span data-ttu-id="7d523-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="7d523-101">Get-AzsPlan</span></span>

## <span data-ttu-id="7d523-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d523-102">SYNOPSIS</span></span>
<span data-ttu-id="7d523-103">Az összes előfizetéshez tartozó összes terv listázása.</span><span class="sxs-lookup"><span data-stu-id="7d523-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="7d523-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d523-104">SYNTAX</span></span>

### <span data-ttu-id="7d523-105">ListAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d523-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7d523-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="7d523-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="7d523-107">Lista</span><span class="sxs-lookup"><span data-stu-id="7d523-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7d523-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d523-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7d523-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d523-109">DESCRIPTION</span></span>
<span data-ttu-id="7d523-110">Az összes előfizetéshez tartozó összes terv listázása.</span><span class="sxs-lookup"><span data-stu-id="7d523-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="7d523-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7d523-111">EXAMPLES</span></span>

### <span data-ttu-id="7d523-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d523-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="7d523-113">Konkrét-terv beszerzése az előfizetések csoportban</span><span class="sxs-lookup"><span data-stu-id="7d523-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="7d523-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d523-114">PARAMETERS</span></span>

### <span data-ttu-id="7d523-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d523-115">-Name</span></span>
<span data-ttu-id="7d523-116">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="7d523-116">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d523-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d523-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d523-118">Annak az erőforráscsoportnek a neve, amelyben az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="7d523-118">The name of the resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d523-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d523-119">-ResourceId</span></span>
<span data-ttu-id="7d523-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7d523-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d523-121">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="7d523-121">-Skip</span></span>
<span data-ttu-id="7d523-122">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="7d523-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d523-123">-Top</span><span class="sxs-lookup"><span data-stu-id="7d523-123">-Top</span></span>
<span data-ttu-id="7d523-124">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="7d523-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7d523-125">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="7d523-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d523-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d523-126">CommonParameters</span></span>
<span data-ttu-id="7d523-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d523-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d523-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d523-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d523-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d523-129">INPUTS</span></span>

## <span data-ttu-id="7d523-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d523-130">OUTPUTS</span></span>

### <span data-ttu-id="7d523-131">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. terv</span><span class="sxs-lookup"><span data-stu-id="7d523-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="7d523-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d523-132">NOTES</span></span>

## <span data-ttu-id="7d523-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d523-133">RELATED LINKS</span></span>

