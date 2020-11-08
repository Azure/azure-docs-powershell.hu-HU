---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017109"
---
# <span data-ttu-id="a0c29-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="a0c29-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="a0c29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0c29-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c29-103">A szolgáltatás alatti erőforrások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a0c29-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="a0c29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0c29-104">SYNTAX</span></span>

### <span data-ttu-id="a0c29-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0c29-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a0c29-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0c29-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="a0c29-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0c29-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="a0c29-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0c29-108">DESCRIPTION</span></span>
<span data-ttu-id="a0c29-109">A szolgáltatás alatti erőforrások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a0c29-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="a0c29-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a0c29-110">EXAMPLES</span></span>

### <span data-ttu-id="a0c29-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="a0c29-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="a0c29-112">A szolgáltatás alatti erőforrások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a0c29-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="a0c29-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="a0c29-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="a0c29-114">Az a for Microsoft. Fabric. admin elemhez tartozó állapotot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a0c29-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="a0c29-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0c29-115">PARAMETERS</span></span>

### <span data-ttu-id="a0c29-116">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="a0c29-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="a0c29-117">Szolgáltatás-regisztrációs azonosító</span><span class="sxs-lookup"><span data-stu-id="a0c29-117">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c29-118">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="a0c29-118">-ResourceRegistrationId</span></span>


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

### <span data-ttu-id="a0c29-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="a0c29-119">-Location</span></span>
<span data-ttu-id="a0c29-120">A régió neve</span><span class="sxs-lookup"><span data-stu-id="a0c29-120">Name of the region</span></span>

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

### <span data-ttu-id="a0c29-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0c29-121">-ResourceGroupName</span></span>
<span data-ttu-id="a0c29-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a0c29-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="a0c29-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0c29-123">-ResourceId</span></span>
<span data-ttu-id="a0c29-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a0c29-124">The resource id.</span></span>

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

### <span data-ttu-id="a0c29-125">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="a0c29-125">-Filter</span></span>
<span data-ttu-id="a0c29-126">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="a0c29-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="a0c29-127">-Top</span><span class="sxs-lookup"><span data-stu-id="a0c29-127">-Top</span></span>
<span data-ttu-id="a0c29-128">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="a0c29-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a0c29-129">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="a0c29-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a0c29-130">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="a0c29-130">-Skip</span></span>
<span data-ttu-id="a0c29-131">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="a0c29-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a0c29-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c29-132">CommonParameters</span></span>
<span data-ttu-id="a0c29-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0c29-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c29-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0c29-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c29-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0c29-135">INPUTS</span></span>

## <span data-ttu-id="a0c29-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0c29-136">OUTPUTS</span></span>

### <span data-ttu-id="a0c29-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="a0c29-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="a0c29-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0c29-138">NOTES</span></span>

## <span data-ttu-id="a0c29-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0c29-139">RELATED LINKS</span></span>
