---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75fef110a1266ca34bef645f39a879dda4aeeda4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491523"
---
# <span data-ttu-id="813fe-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="813fe-101">Get-AzsPlan</span></span>

## <span data-ttu-id="813fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="813fe-102">SYNOPSIS</span></span>
<span data-ttu-id="813fe-103">Az összes előfizetéshez tartozó összes terv listázása.</span><span class="sxs-lookup"><span data-stu-id="813fe-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="813fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="813fe-104">SYNTAX</span></span>

### <span data-ttu-id="813fe-105">ListAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="813fe-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="813fe-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="813fe-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="813fe-107">Lista</span><span class="sxs-lookup"><span data-stu-id="813fe-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="813fe-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="813fe-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="813fe-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="813fe-109">DESCRIPTION</span></span>
<span data-ttu-id="813fe-110">Az összes előfizetéshez tartozó összes terv listázása.</span><span class="sxs-lookup"><span data-stu-id="813fe-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="813fe-111">Példák</span><span class="sxs-lookup"><span data-stu-id="813fe-111">EXAMPLES</span></span>

### <span data-ttu-id="813fe-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="813fe-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="813fe-113">Konkrét-terv beszerzése az előfizetések csoportban</span><span class="sxs-lookup"><span data-stu-id="813fe-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="813fe-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="813fe-114">PARAMETERS</span></span>

### <span data-ttu-id="813fe-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="813fe-115">-Name</span></span>
<span data-ttu-id="813fe-116">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="813fe-116">Name of the plan.</span></span>

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

### <span data-ttu-id="813fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="813fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="813fe-118">Annak az erőforráscsoportnek a neve, amelyben az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="813fe-118">The name of the resource group the resource is located under.</span></span>

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

### <span data-ttu-id="813fe-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="813fe-119">-ResourceId</span></span>
<span data-ttu-id="813fe-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="813fe-120">The resource id.</span></span>

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

### <span data-ttu-id="813fe-121">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="813fe-121">-Skip</span></span>
<span data-ttu-id="813fe-122">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="813fe-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="813fe-123">-Top</span><span class="sxs-lookup"><span data-stu-id="813fe-123">-Top</span></span>
<span data-ttu-id="813fe-124">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="813fe-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="813fe-125">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="813fe-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="813fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813fe-126">CommonParameters</span></span>
<span data-ttu-id="813fe-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="813fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813fe-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="813fe-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813fe-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="813fe-129">INPUTS</span></span>

## <span data-ttu-id="813fe-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="813fe-130">OUTPUTS</span></span>

### <span data-ttu-id="813fe-131">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. terv</span><span class="sxs-lookup"><span data-stu-id="813fe-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="813fe-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="813fe-132">NOTES</span></span>

## <span data-ttu-id="813fe-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="813fe-133">RELATED LINKS</span></span>

