---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 752bd7f183bf5a5bdad7950e6567024cbe5b8dec
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840761"
---
# <span data-ttu-id="4f89c-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="4f89c-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="4f89c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f89c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f89c-103">Az egyes szolgáltatások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4f89c-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="4f89c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f89c-104">SYNTAX</span></span>

### <span data-ttu-id="4f89c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f89c-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4f89c-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="4f89c-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="4f89c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f89c-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4f89c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f89c-108">DESCRIPTION</span></span>
<span data-ttu-id="4f89c-109">Az egyes szolgáltatások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4f89c-109">Returns a list of each service's health.</span></span> <span data-ttu-id="4f89c-110">A AlertSummary tulajdonság a figyelmeztetés/hibák számát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4f89c-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="4f89c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4f89c-111">EXAMPLES</span></span>

### <span data-ttu-id="4f89c-112">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="4f89c-112">EXAMPLE 1</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="4f89c-113">Az egyes szolgáltatások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4f89c-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="4f89c-114">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="4f89c-114">EXAMPLE 2</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="4f89c-115">Egy szolgáltatás állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4f89c-115">Returns a service's health.</span></span>

## <span data-ttu-id="4f89c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f89c-116">PARAMETERS</span></span>

### <span data-ttu-id="4f89c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4f89c-117">-Name</span></span>
<span data-ttu-id="4f89c-118">Szolgáltatás állapota név.</span><span class="sxs-lookup"><span data-stu-id="4f89c-118">Service Health name.</span></span>

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

### <span data-ttu-id="4f89c-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="4f89c-119">-Location</span></span>
<span data-ttu-id="4f89c-120">A régió neve</span><span class="sxs-lookup"><span data-stu-id="4f89c-120">Name of the region</span></span>

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

### <span data-ttu-id="4f89c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f89c-121">-ResourceGroupName</span></span>
<span data-ttu-id="4f89c-122">Az erőforráscsoport neve, nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4f89c-122">Name of the resource group, optional.</span></span>

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

### <span data-ttu-id="4f89c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f89c-123">-ResourceId</span></span>
<span data-ttu-id="4f89c-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4f89c-124">The resource id.</span></span>

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

### <span data-ttu-id="4f89c-125">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="4f89c-125">-Filter</span></span>
<span data-ttu-id="4f89c-126">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="4f89c-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="4f89c-127">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="4f89c-127">-Skip</span></span>
<span data-ttu-id="4f89c-128">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="4f89c-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4f89c-129">-Top</span><span class="sxs-lookup"><span data-stu-id="4f89c-129">-Top</span></span>
<span data-ttu-id="4f89c-130">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="4f89c-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4f89c-131">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="4f89c-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4f89c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f89c-132">CommonParameters</span></span>
<span data-ttu-id="4f89c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f89c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f89c-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f89c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f89c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f89c-135">INPUTS</span></span>

## <span data-ttu-id="4f89c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f89c-136">OUTPUTS</span></span>

### <span data-ttu-id="4f89c-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="4f89c-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="4f89c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f89c-138">NOTES</span></span>

## <span data-ttu-id="4f89c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f89c-139">RELATED LINKS</span></span>
