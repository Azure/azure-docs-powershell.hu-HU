---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fbec7ec2f8bcfc0d7595658f84866cf449d3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840023"
---
# <span data-ttu-id="7d62e-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="7d62e-101">Get-AzsAlert</span></span>

## <span data-ttu-id="7d62e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d62e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d62e-103">Egy adott helyen található összes értesítés listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7d62e-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="7d62e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d62e-104">SYNTAX</span></span>

### <span data-ttu-id="7d62e-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d62e-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7d62e-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="7d62e-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="7d62e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d62e-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7d62e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d62e-108">DESCRIPTION</span></span>
<span data-ttu-id="7d62e-109">Egy adott helyen található összes értesítés listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7d62e-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="7d62e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7d62e-110">EXAMPLES</span></span>

### <span data-ttu-id="7d62e-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d62e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="7d62e-112">Értesítés kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="7d62e-112">Get an alert by Name.</span></span>

### <span data-ttu-id="7d62e-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d62e-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="7d62e-114">Az összes aktív riasztás beolvasása és a hiba és a cím megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="7d62e-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="7d62e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d62e-115">PARAMETERS</span></span>

### <span data-ttu-id="7d62e-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="7d62e-116">-Filter</span></span>
<span data-ttu-id="7d62e-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="7d62e-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="7d62e-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="7d62e-118">-Location</span></span>
<span data-ttu-id="7d62e-119">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="7d62e-119">Name of the location.</span></span>

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

### <span data-ttu-id="7d62e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d62e-120">-Name</span></span>
<span data-ttu-id="7d62e-121">Az értesítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7d62e-121">The alert identifier.</span></span>

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

### <span data-ttu-id="7d62e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d62e-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d62e-123">Erőforráscsoport neve, amely az erőforrás lakik.</span><span class="sxs-lookup"><span data-stu-id="7d62e-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="7d62e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d62e-124">-ResourceId</span></span>
<span data-ttu-id="7d62e-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7d62e-125">The resource id.</span></span>

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

### <span data-ttu-id="7d62e-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="7d62e-126">-Skip</span></span>
<span data-ttu-id="7d62e-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="7d62e-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7d62e-128">-Top</span><span class="sxs-lookup"><span data-stu-id="7d62e-128">-Top</span></span>
<span data-ttu-id="7d62e-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="7d62e-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7d62e-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="7d62e-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7d62e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d62e-131">CommonParameters</span></span>
<span data-ttu-id="7d62e-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d62e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d62e-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d62e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d62e-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d62e-134">INPUTS</span></span>

## <span data-ttu-id="7d62e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d62e-135">OUTPUTS</span></span>

### <span data-ttu-id="7d62e-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. riasztás</span><span class="sxs-lookup"><span data-stu-id="7d62e-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="7d62e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d62e-137">NOTES</span></span>

## <span data-ttu-id="7d62e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d62e-138">RELATED LINKS</span></span>

