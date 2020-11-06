---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dac95eced72f70d3471019136d302fcdfe95f86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490884"
---
# <span data-ttu-id="a5afd-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="a5afd-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="a5afd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5afd-102">SYNOPSIS</span></span>
<span data-ttu-id="a5afd-103">Az infrastruktúra-szerepkörök listáját számítja ki egy helyen.</span><span class="sxs-lookup"><span data-stu-id="a5afd-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="a5afd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5afd-104">SYNTAX</span></span>

### <span data-ttu-id="a5afd-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5afd-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a5afd-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a5afd-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5afd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5afd-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a5afd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5afd-108">DESCRIPTION</span></span>
<span data-ttu-id="a5afd-109">Az infrastruktúra-szerepkörök listáját számítja ki egy helyen.</span><span class="sxs-lookup"><span data-stu-id="a5afd-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="a5afd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a5afd-110">EXAMPLES</span></span>

### <span data-ttu-id="a5afd-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a5afd-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="a5afd-112">A teljes infrastruktúra-szerepkörök listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a5afd-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="a5afd-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a5afd-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="a5afd-114">A név alapján Ismerje meg az infrastruktúra szerepkört.</span><span class="sxs-lookup"><span data-stu-id="a5afd-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="a5afd-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5afd-115">PARAMETERS</span></span>

### <span data-ttu-id="a5afd-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="a5afd-116">-Filter</span></span>
<span data-ttu-id="a5afd-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="a5afd-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a5afd-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="a5afd-118">-Location</span></span>
<span data-ttu-id="a5afd-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a5afd-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a5afd-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5afd-120">-Name</span></span>
<span data-ttu-id="a5afd-121">Infrastruktúra-szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="a5afd-121">Infrastructure role name.</span></span>

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

### <span data-ttu-id="a5afd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5afd-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5afd-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="a5afd-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a5afd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5afd-124">-ResourceId</span></span>
<span data-ttu-id="a5afd-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a5afd-125">The resource id.</span></span>

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

### <span data-ttu-id="a5afd-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="a5afd-126">-Skip</span></span>
<span data-ttu-id="a5afd-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="a5afd-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a5afd-128">-Top</span><span class="sxs-lookup"><span data-stu-id="a5afd-128">-Top</span></span>
<span data-ttu-id="a5afd-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="a5afd-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a5afd-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="a5afd-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a5afd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5afd-131">CommonParameters</span></span>
<span data-ttu-id="a5afd-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5afd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5afd-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5afd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5afd-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5afd-134">INPUTS</span></span>

## <span data-ttu-id="a5afd-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5afd-135">OUTPUTS</span></span>

### <span data-ttu-id="a5afd-136">Microsoft. AzureStack. Management. Fabric. admin. models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="a5afd-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="a5afd-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5afd-137">NOTES</span></span>

## <span data-ttu-id="a5afd-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5afd-138">RELATED LINKS</span></span>

