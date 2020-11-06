---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdb6542f9e7bfd594130374d5d72fed8b26596e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491471"
---
# <span data-ttu-id="abf6f-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="abf6f-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="abf6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abf6f-102">SYNOPSIS</span></span>
<span data-ttu-id="abf6f-103">A hely összes tárolási kötetének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="abf6f-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="abf6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abf6f-104">SYNTAX</span></span>

### <span data-ttu-id="abf6f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abf6f-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="abf6f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="abf6f-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="abf6f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="abf6f-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="abf6f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="abf6f-108">DESCRIPTION</span></span>
<span data-ttu-id="abf6f-109">A hely összes tárolási kötetének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="abf6f-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="abf6f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="abf6f-110">EXAMPLES</span></span>

### <span data-ttu-id="abf6f-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="abf6f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="abf6f-112">A tárterület minden tárolási kötetének listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="abf6f-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="abf6f-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="abf6f-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="abf6f-114">A tárterületet a megadott helyen, név szerint érheti el.</span><span class="sxs-lookup"><span data-stu-id="abf6f-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="abf6f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abf6f-115">PARAMETERS</span></span>

### <span data-ttu-id="abf6f-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="abf6f-116">-Filter</span></span>
<span data-ttu-id="abf6f-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="abf6f-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="abf6f-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="abf6f-118">-Location</span></span>
<span data-ttu-id="abf6f-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="abf6f-119">Location of the resource.</span></span>

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

### <span data-ttu-id="abf6f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abf6f-120">-Name</span></span>
<span data-ttu-id="abf6f-121">A tárterület neve.</span><span class="sxs-lookup"><span data-stu-id="abf6f-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="abf6f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf6f-122">-ResourceGroupName</span></span>
<span data-ttu-id="abf6f-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="abf6f-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="abf6f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abf6f-124">-ResourceId</span></span>
<span data-ttu-id="abf6f-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="abf6f-125">The resource id.</span></span>

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

### <span data-ttu-id="abf6f-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="abf6f-126">-Skip</span></span>
<span data-ttu-id="abf6f-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="abf6f-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="abf6f-128">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="abf6f-128">-StoragePool</span></span>
<span data-ttu-id="abf6f-129">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="abf6f-129">Storage pool name.</span></span>

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

### <span data-ttu-id="abf6f-130">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="abf6f-130">-StorageSystem</span></span>
<span data-ttu-id="abf6f-131">Az a tárolási rendszer, amelyben az infrastruktúra-kötet található.</span><span class="sxs-lookup"><span data-stu-id="abf6f-131">Storage system in which the infrastructure volume is located.</span></span>

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

### <span data-ttu-id="abf6f-132">-Top</span><span class="sxs-lookup"><span data-stu-id="abf6f-132">-Top</span></span>
<span data-ttu-id="abf6f-133">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="abf6f-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="abf6f-134">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="abf6f-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="abf6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf6f-135">CommonParameters</span></span>
<span data-ttu-id="abf6f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abf6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf6f-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf6f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf6f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abf6f-138">INPUTS</span></span>

## <span data-ttu-id="abf6f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abf6f-139">OUTPUTS</span></span>

### <span data-ttu-id="abf6f-140">Microsoft. AzureStack. Management. Fabric. admin. models. Volume</span><span class="sxs-lookup"><span data-stu-id="abf6f-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="abf6f-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abf6f-141">NOTES</span></span>

## <span data-ttu-id="abf6f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abf6f-142">RELATED LINKS</span></span>

