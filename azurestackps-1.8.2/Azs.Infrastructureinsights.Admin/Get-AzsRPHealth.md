---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 752bd7f183bf5a5bdad7950e6567024cbe5b8dec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017114"
---
# <span data-ttu-id="eaa69-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="eaa69-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="eaa69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eaa69-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa69-103">Az egyes szolgáltatások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="eaa69-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="eaa69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eaa69-104">SYNTAX</span></span>

### <span data-ttu-id="eaa69-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eaa69-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="eaa69-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="eaa69-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="eaa69-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eaa69-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="eaa69-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eaa69-108">DESCRIPTION</span></span>
<span data-ttu-id="eaa69-109">Az egyes szolgáltatások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="eaa69-109">Returns a list of each service's health.</span></span> <span data-ttu-id="eaa69-110">A AlertSummary tulajdonság a figyelmeztetés/hibák számát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="eaa69-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="eaa69-111">Példák</span><span class="sxs-lookup"><span data-stu-id="eaa69-111">EXAMPLES</span></span>

### <span data-ttu-id="eaa69-112">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="eaa69-112">EXAMPLE 1</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="eaa69-113">Az egyes szolgáltatások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="eaa69-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="eaa69-114">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="eaa69-114">EXAMPLE 2</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="eaa69-115">Egy szolgáltatás állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="eaa69-115">Returns a service's health.</span></span>

## <span data-ttu-id="eaa69-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eaa69-116">PARAMETERS</span></span>

### <span data-ttu-id="eaa69-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eaa69-117">-Name</span></span>
<span data-ttu-id="eaa69-118">Szolgáltatás állapota név.</span><span class="sxs-lookup"><span data-stu-id="eaa69-118">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaa69-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="eaa69-119">-Location</span></span>
<span data-ttu-id="eaa69-120">A régió neve</span><span class="sxs-lookup"><span data-stu-id="eaa69-120">Name of the region</span></span>

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

### <span data-ttu-id="eaa69-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaa69-121">-ResourceGroupName</span></span>
<span data-ttu-id="eaa69-122">Az erőforráscsoport neve, nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="eaa69-122">Name of the resource group, optional.</span></span>

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

### <span data-ttu-id="eaa69-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eaa69-123">-ResourceId</span></span>
<span data-ttu-id="eaa69-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="eaa69-124">The resource id.</span></span>

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

### <span data-ttu-id="eaa69-125">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="eaa69-125">-Filter</span></span>
<span data-ttu-id="eaa69-126">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="eaa69-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="eaa69-127">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="eaa69-127">-Skip</span></span>
<span data-ttu-id="eaa69-128">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="eaa69-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="eaa69-129">-Top</span><span class="sxs-lookup"><span data-stu-id="eaa69-129">-Top</span></span>
<span data-ttu-id="eaa69-130">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="eaa69-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="eaa69-131">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="eaa69-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="eaa69-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa69-132">CommonParameters</span></span>
<span data-ttu-id="eaa69-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eaa69-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa69-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa69-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa69-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eaa69-135">INPUTS</span></span>

## <span data-ttu-id="eaa69-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eaa69-136">OUTPUTS</span></span>

### <span data-ttu-id="eaa69-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="eaa69-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="eaa69-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eaa69-138">NOTES</span></span>

## <span data-ttu-id="eaa69-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eaa69-139">RELATED LINKS</span></span>
