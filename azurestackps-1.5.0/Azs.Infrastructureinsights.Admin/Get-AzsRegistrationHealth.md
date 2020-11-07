---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d73e2db2f09ba504e9c6adbf15a0bbc2629452ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671725"
---
# <span data-ttu-id="3de9b-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="3de9b-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="3de9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3de9b-102">SYNOPSIS</span></span>
<span data-ttu-id="3de9b-103">A szolgáltatás alatti erőforrások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3de9b-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="3de9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3de9b-104">SYNTAX</span></span>

### <span data-ttu-id="3de9b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3de9b-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3de9b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="3de9b-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="3de9b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3de9b-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="3de9b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3de9b-108">DESCRIPTION</span></span>
<span data-ttu-id="3de9b-109">A szolgáltatás alatti erőforrások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3de9b-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="3de9b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3de9b-110">EXAMPLES</span></span>

### <span data-ttu-id="3de9b-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3de9b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="3de9b-112">A szolgáltatás alatti erőforrások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3de9b-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="3de9b-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3de9b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="3de9b-114">Az a for Microsoft. Fabric. admin elemhez tartozó állapotot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3de9b-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="3de9b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3de9b-115">PARAMETERS</span></span>

### <span data-ttu-id="3de9b-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="3de9b-116">-Filter</span></span>
<span data-ttu-id="3de9b-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="3de9b-117">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de9b-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="3de9b-118">-Location</span></span>
<span data-ttu-id="3de9b-119">A régió neve</span><span class="sxs-lookup"><span data-stu-id="3de9b-119">Name of the region</span></span>

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

### <span data-ttu-id="3de9b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3de9b-120">-Name</span></span>
<span data-ttu-id="3de9b-121">Annak az erőforrásnak a neve, amely az erőforrás-nyilvántartási azonosítónak felel meg.</span><span class="sxs-lookup"><span data-stu-id="3de9b-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de9b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de9b-122">-ResourceGroupName</span></span>
<span data-ttu-id="3de9b-123">Erőforráscsoport neve, amely az erőforrás lakik.</span><span class="sxs-lookup"><span data-stu-id="3de9b-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="3de9b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3de9b-124">-ResourceId</span></span>
<span data-ttu-id="3de9b-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3de9b-125">The resource id.</span></span>

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

### <span data-ttu-id="3de9b-126">-ServiceRegistrationName</span><span class="sxs-lookup"><span data-stu-id="3de9b-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="3de9b-127">Szolgáltatás-regisztrációs azonosító</span><span class="sxs-lookup"><span data-stu-id="3de9b-127">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ServiceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de9b-128">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="3de9b-128">-Skip</span></span>
<span data-ttu-id="3de9b-129">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="3de9b-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3de9b-130">-Top</span><span class="sxs-lookup"><span data-stu-id="3de9b-130">-Top</span></span>
<span data-ttu-id="3de9b-131">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="3de9b-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3de9b-132">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="3de9b-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3de9b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de9b-133">CommonParameters</span></span>
<span data-ttu-id="3de9b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3de9b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de9b-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de9b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de9b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3de9b-136">INPUTS</span></span>

## <span data-ttu-id="3de9b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3de9b-137">OUTPUTS</span></span>

### <span data-ttu-id="3de9b-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="3de9b-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="3de9b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3de9b-139">NOTES</span></span>

## <span data-ttu-id="3de9b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3de9b-140">RELATED LINKS</span></span>

