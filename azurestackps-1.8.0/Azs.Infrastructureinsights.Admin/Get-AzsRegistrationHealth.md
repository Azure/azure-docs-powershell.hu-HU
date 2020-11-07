---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840436"
---
# <span data-ttu-id="09636-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="09636-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="09636-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09636-102">SYNOPSIS</span></span>
<span data-ttu-id="09636-103">A szolgáltatás alatti erőforrások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="09636-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="09636-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09636-104">SYNTAX</span></span>

### <span data-ttu-id="09636-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09636-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="09636-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="09636-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="09636-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="09636-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="09636-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="09636-108">DESCRIPTION</span></span>
<span data-ttu-id="09636-109">A szolgáltatás alatti erőforrások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="09636-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="09636-110">Példák</span><span class="sxs-lookup"><span data-stu-id="09636-110">EXAMPLES</span></span>

### <span data-ttu-id="09636-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="09636-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="09636-112">A szolgáltatás alatti erőforrások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="09636-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="09636-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="09636-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="09636-114">Az a for Microsoft. Fabric. admin elemhez tartozó állapotot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="09636-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="09636-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09636-115">PARAMETERS</span></span>

### <span data-ttu-id="09636-116">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="09636-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="09636-117">Szolgáltatás-regisztrációs azonosító</span><span class="sxs-lookup"><span data-stu-id="09636-117">Service registration id.</span></span>

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

### <span data-ttu-id="09636-118">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="09636-118">-ResourceRegistrationId</span></span>


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

### <span data-ttu-id="09636-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="09636-119">-Location</span></span>
<span data-ttu-id="09636-120">A régió neve</span><span class="sxs-lookup"><span data-stu-id="09636-120">Name of the region</span></span>

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

### <span data-ttu-id="09636-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09636-121">-ResourceGroupName</span></span>
<span data-ttu-id="09636-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="09636-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="09636-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09636-123">-ResourceId</span></span>
<span data-ttu-id="09636-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="09636-124">The resource id.</span></span>

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

### <span data-ttu-id="09636-125">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="09636-125">-Filter</span></span>
<span data-ttu-id="09636-126">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="09636-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="09636-127">-Top</span><span class="sxs-lookup"><span data-stu-id="09636-127">-Top</span></span>
<span data-ttu-id="09636-128">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="09636-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="09636-129">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="09636-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="09636-130">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="09636-130">-Skip</span></span>
<span data-ttu-id="09636-131">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="09636-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="09636-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09636-132">CommonParameters</span></span>
<span data-ttu-id="09636-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09636-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09636-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09636-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09636-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09636-135">INPUTS</span></span>

## <span data-ttu-id="09636-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09636-136">OUTPUTS</span></span>

### <span data-ttu-id="09636-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="09636-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="09636-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09636-138">NOTES</span></span>

## <span data-ttu-id="09636-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09636-139">RELATED LINKS</span></span>
