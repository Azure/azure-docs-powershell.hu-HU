---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02baf67cc13269d9d53c0adb40337adbd9929641
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016748"
---
# <span data-ttu-id="b5af5-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="b5af5-101">Get-AzsPlan</span></span>

## <span data-ttu-id="b5af5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5af5-102">SYNOPSIS</span></span>
<span data-ttu-id="b5af5-103">Az összes előfizetéshez tartozó összes terv listázása.</span><span class="sxs-lookup"><span data-stu-id="b5af5-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="b5af5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5af5-104">SYNTAX</span></span>

### <span data-ttu-id="b5af5-105">ListAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5af5-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b5af5-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b5af5-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="b5af5-107">Lista</span><span class="sxs-lookup"><span data-stu-id="b5af5-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b5af5-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5af5-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b5af5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5af5-109">DESCRIPTION</span></span>
<span data-ttu-id="b5af5-110">Az összes előfizetéshez tartozó összes terv listázása.</span><span class="sxs-lookup"><span data-stu-id="b5af5-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="b5af5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b5af5-111">EXAMPLES</span></span>

### <span data-ttu-id="b5af5-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b5af5-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="b5af5-113">Konkrét-terv beszerzése az előfizetések csoportban</span><span class="sxs-lookup"><span data-stu-id="b5af5-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="b5af5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5af5-114">PARAMETERS</span></span>

### <span data-ttu-id="b5af5-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5af5-115">-Name</span></span>
<span data-ttu-id="b5af5-116">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="b5af5-116">Name of the plan.</span></span>

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

### <span data-ttu-id="b5af5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5af5-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5af5-118">Annak az erőforráscsoportnek a neve, amelyben az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="b5af5-118">The name of the resource group the resource is located under.</span></span>

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

### <span data-ttu-id="b5af5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5af5-119">-ResourceId</span></span>
<span data-ttu-id="b5af5-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b5af5-120">The resource id.</span></span>

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

### <span data-ttu-id="b5af5-121">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="b5af5-121">-Skip</span></span>
<span data-ttu-id="b5af5-122">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="b5af5-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b5af5-123">-Top</span><span class="sxs-lookup"><span data-stu-id="b5af5-123">-Top</span></span>
<span data-ttu-id="b5af5-124">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="b5af5-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b5af5-125">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="b5af5-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b5af5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5af5-126">CommonParameters</span></span>
<span data-ttu-id="b5af5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5af5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5af5-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5af5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5af5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5af5-129">INPUTS</span></span>

## <span data-ttu-id="b5af5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5af5-130">OUTPUTS</span></span>

### <span data-ttu-id="b5af5-131">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. terv</span><span class="sxs-lookup"><span data-stu-id="b5af5-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="b5af5-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5af5-132">NOTES</span></span>

## <span data-ttu-id="b5af5-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5af5-133">RELATED LINKS</span></span>

