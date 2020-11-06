---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2528d9b4f9443d8857006b6fc1e94100b0b477ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490911"
---
# <span data-ttu-id="24a55-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="24a55-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="24a55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24a55-102">SYNOPSIS</span></span>
<span data-ttu-id="24a55-103">Egy adott helyen található összes IP-készlet listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="24a55-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="24a55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24a55-104">SYNTAX</span></span>

### <span data-ttu-id="24a55-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24a55-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="24a55-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="24a55-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="24a55-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="24a55-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="24a55-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="24a55-108">DESCRIPTION</span></span>
<span data-ttu-id="24a55-109">Egy adott helyen található összes IP-készlet listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="24a55-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="24a55-110">Példák</span><span class="sxs-lookup"><span data-stu-id="24a55-110">EXAMPLES</span></span>

### <span data-ttu-id="24a55-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="24a55-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="24a55-112">Az összes infrastruktúra IP-készletének beszerzése.</span><span class="sxs-lookup"><span data-stu-id="24a55-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="24a55-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="24a55-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="24a55-114">Infrastruktúra IP-készletének beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="24a55-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="24a55-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24a55-115">PARAMETERS</span></span>

### <span data-ttu-id="24a55-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="24a55-116">-Filter</span></span>
<span data-ttu-id="24a55-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="24a55-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="24a55-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="24a55-118">-Location</span></span>
<span data-ttu-id="24a55-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="24a55-119">Location of the resource.</span></span>

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

### <span data-ttu-id="24a55-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24a55-120">-Name</span></span>
<span data-ttu-id="24a55-121">Az IP-készlet neve</span><span class="sxs-lookup"><span data-stu-id="24a55-121">IP pool name.</span></span>

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

### <span data-ttu-id="24a55-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a55-122">-ResourceGroupName</span></span>
<span data-ttu-id="24a55-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="24a55-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="24a55-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24a55-124">-ResourceId</span></span>
<span data-ttu-id="24a55-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="24a55-125">The resource id.</span></span>

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

### <span data-ttu-id="24a55-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="24a55-126">-Skip</span></span>
<span data-ttu-id="24a55-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="24a55-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="24a55-128">-Top</span><span class="sxs-lookup"><span data-stu-id="24a55-128">-Top</span></span>
<span data-ttu-id="24a55-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="24a55-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="24a55-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="24a55-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="24a55-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a55-131">CommonParameters</span></span>
<span data-ttu-id="24a55-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24a55-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a55-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a55-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a55-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a55-134">INPUTS</span></span>

## <span data-ttu-id="24a55-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a55-135">OUTPUTS</span></span>

### <span data-ttu-id="24a55-136">Microsoft. AzureStack. Management. Fabric. admin. models. IpPool</span><span class="sxs-lookup"><span data-stu-id="24a55-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="24a55-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24a55-137">NOTES</span></span>

## <span data-ttu-id="24a55-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24a55-138">RELATED LINKS</span></span>

