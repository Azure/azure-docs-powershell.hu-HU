---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840546"
---
# <span data-ttu-id="6ca04-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="6ca04-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="6ca04-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ca04-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca04-103">Egy adott helyen található összes IP-készlet listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6ca04-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="6ca04-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ca04-104">SYNTAX</span></span>

### <span data-ttu-id="6ca04-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ca04-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6ca04-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="6ca04-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="6ca04-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca04-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6ca04-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ca04-108">DESCRIPTION</span></span>
<span data-ttu-id="6ca04-109">Egy adott helyen található összes IP-készlet listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6ca04-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="6ca04-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6ca04-110">EXAMPLES</span></span>

### <span data-ttu-id="6ca04-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="6ca04-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="6ca04-112">Az összes infrastruktúra IP-készletének beszerzése.</span><span class="sxs-lookup"><span data-stu-id="6ca04-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="6ca04-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="6ca04-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="6ca04-114">Infrastruktúra IP-készletének beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="6ca04-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="6ca04-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ca04-115">PARAMETERS</span></span>

### <span data-ttu-id="6ca04-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ca04-116">-Name</span></span>
<span data-ttu-id="6ca04-117">Az IP-készlet neve</span><span class="sxs-lookup"><span data-stu-id="6ca04-117">IP pool name.</span></span>

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

### <span data-ttu-id="6ca04-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="6ca04-118">-Location</span></span>
<span data-ttu-id="6ca04-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="6ca04-119">Location of the resource.</span></span>

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

### <span data-ttu-id="6ca04-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca04-120">-ResourceGroupName</span></span>
<span data-ttu-id="6ca04-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="6ca04-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6ca04-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca04-122">-ResourceId</span></span>
<span data-ttu-id="6ca04-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6ca04-123">The resource id.</span></span>

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

### <span data-ttu-id="6ca04-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="6ca04-124">-Filter</span></span>
<span data-ttu-id="6ca04-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="6ca04-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="6ca04-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="6ca04-126">-Skip</span></span>
<span data-ttu-id="6ca04-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="6ca04-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6ca04-128">-Top</span><span class="sxs-lookup"><span data-stu-id="6ca04-128">-Top</span></span>
<span data-ttu-id="6ca04-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="6ca04-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6ca04-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="6ca04-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6ca04-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca04-131">CommonParameters</span></span>
<span data-ttu-id="6ca04-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ca04-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca04-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca04-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca04-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ca04-134">INPUTS</span></span>

## <span data-ttu-id="6ca04-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ca04-135">OUTPUTS</span></span>

### <span data-ttu-id="6ca04-136">Microsoft. AzureStack. Management. Fabric. admin. models. IpPool</span><span class="sxs-lookup"><span data-stu-id="6ca04-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="6ca04-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ca04-137">NOTES</span></span>

## <span data-ttu-id="6ca04-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ca04-138">RELATED LINKS</span></span>
