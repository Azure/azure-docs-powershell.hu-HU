---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3a64a045d988d59c2b1aefa650aa695ba09486f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016916"
---
# <span data-ttu-id="b405a-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="b405a-101">Get-AzsAlert</span></span>

## <span data-ttu-id="b405a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b405a-102">SYNOPSIS</span></span>
<span data-ttu-id="b405a-103">Egy adott helyen található összes értesítés listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b405a-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="b405a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b405a-104">SYNTAX</span></span>

### <span data-ttu-id="b405a-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b405a-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b405a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b405a-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b405a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b405a-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b405a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b405a-108">DESCRIPTION</span></span>
<span data-ttu-id="b405a-109">Egy adott helyen található összes értesítés listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b405a-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="b405a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b405a-110">EXAMPLES</span></span>

### <span data-ttu-id="b405a-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="b405a-111">EXAMPLE 1</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="b405a-112">Értesítés kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="b405a-112">Get an alert by Name.</span></span>

### <span data-ttu-id="b405a-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b405a-113">EXAMPLE 2</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="b405a-114">Az összes aktív riasztás beolvasása és a hiba és a cím megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="b405a-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="b405a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b405a-115">PARAMETERS</span></span>

### <span data-ttu-id="b405a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b405a-116">-Name</span></span>
<span data-ttu-id="b405a-117">Az értesítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b405a-117">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b405a-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="b405a-118">-Location</span></span>
<span data-ttu-id="b405a-119">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="b405a-119">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b405a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b405a-120">-ResourceGroupName</span></span>
<span data-ttu-id="b405a-121">A riasztás erőforrás-csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="b405a-121">Resource group name of the alert.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b405a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b405a-122">-ResourceId</span></span>
<span data-ttu-id="b405a-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b405a-123">The resource id.</span></span>

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

### <span data-ttu-id="b405a-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b405a-124">-Filter</span></span>
<span data-ttu-id="b405a-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="b405a-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b405a-126">-Top</span><span class="sxs-lookup"><span data-stu-id="b405a-126">-Top</span></span>
<span data-ttu-id="b405a-127">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="b405a-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b405a-128">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="b405a-128">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b405a-129">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="b405a-129">-Skip</span></span>
<span data-ttu-id="b405a-130">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="b405a-130">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b405a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b405a-131">CommonParameters</span></span>
<span data-ttu-id="b405a-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b405a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b405a-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b405a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b405a-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b405a-134">INPUTS</span></span>

## <span data-ttu-id="b405a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b405a-135">OUTPUTS</span></span>

### <span data-ttu-id="b405a-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. riasztás</span><span class="sxs-lookup"><span data-stu-id="b405a-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="b405a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b405a-137">NOTES</span></span>

## <span data-ttu-id="b405a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b405a-138">RELATED LINKS</span></span>
