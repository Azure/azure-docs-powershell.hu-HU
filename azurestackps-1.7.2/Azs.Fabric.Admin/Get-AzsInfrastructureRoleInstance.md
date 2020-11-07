---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39955a2b99ffd7e3c604b4fc288f117face8205f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840056"
---
# <span data-ttu-id="6cd4f-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="6cd4f-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="6cd4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cd4f-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd4f-103">A helyhez tartozó összes infrastruktúra-szerepkör-példány listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="6cd4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cd4f-104">SYNTAX</span></span>

### <span data-ttu-id="6cd4f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cd4f-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6cd4f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="6cd4f-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cd4f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cd4f-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6cd4f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cd4f-108">DESCRIPTION</span></span>
<span data-ttu-id="6cd4f-109">A helyhez tartozó összes infrastruktúra-szerepkör-példány listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="6cd4f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6cd4f-110">EXAMPLES</span></span>

### <span data-ttu-id="6cd4f-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6cd4f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="6cd4f-112">Visszaadja az összes infrastruktúra-szerepkör-példány listáját.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="6cd4f-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6cd4f-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="6cd4f-114">A név alapján egyetlen infrastrukturális szerepkört ad vissza.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="6cd4f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cd4f-115">PARAMETERS</span></span>

### <span data-ttu-id="6cd4f-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="6cd4f-116">-Filter</span></span>
<span data-ttu-id="6cd4f-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="6cd4f-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="6cd4f-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="6cd4f-118">-Location</span></span>
<span data-ttu-id="6cd4f-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-119">Location of the resource.</span></span>

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

### <span data-ttu-id="6cd4f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6cd4f-120">-Name</span></span>
<span data-ttu-id="6cd4f-121">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="6cd4f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd4f-122">-ResourceGroupName</span></span>
<span data-ttu-id="6cd4f-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6cd4f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cd4f-124">-ResourceId</span></span>
<span data-ttu-id="6cd4f-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-125">The resource id.</span></span>

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

### <span data-ttu-id="6cd4f-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="6cd4f-126">-Skip</span></span>
<span data-ttu-id="6cd4f-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6cd4f-128">-Top</span><span class="sxs-lookup"><span data-stu-id="6cd4f-128">-Top</span></span>
<span data-ttu-id="6cd4f-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6cd4f-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="6cd4f-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6cd4f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd4f-131">CommonParameters</span></span>
<span data-ttu-id="6cd4f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cd4f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd4f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd4f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd4f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cd4f-134">INPUTS</span></span>

## <span data-ttu-id="6cd4f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cd4f-135">OUTPUTS</span></span>

### <span data-ttu-id="6cd4f-136">Microsoft. AzureStack. Management. Fabric. admin. models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="6cd4f-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="6cd4f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cd4f-137">NOTES</span></span>

## <span data-ttu-id="6cd4f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cd4f-138">RELATED LINKS</span></span>

