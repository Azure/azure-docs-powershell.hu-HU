---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840209"
---
# <span data-ttu-id="033c9-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="033c9-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="033c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="033c9-102">SYNOPSIS</span></span>
<span data-ttu-id="033c9-103">A hely összes tárolási kötetének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="033c9-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="033c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="033c9-104">SYNTAX</span></span>

### <span data-ttu-id="033c9-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="033c9-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="033c9-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="033c9-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="033c9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="033c9-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="033c9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="033c9-108">DESCRIPTION</span></span>
<span data-ttu-id="033c9-109">A hely összes tárolási kötetének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="033c9-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="033c9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="033c9-110">EXAMPLES</span></span>

### <span data-ttu-id="033c9-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="033c9-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="033c9-112">A tárterület minden tárolási kötetének listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="033c9-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="033c9-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="033c9-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="033c9-114">A tárterületet a megadott helyen, név szerint érheti el.</span><span class="sxs-lookup"><span data-stu-id="033c9-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="033c9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="033c9-115">PARAMETERS</span></span>

### <span data-ttu-id="033c9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="033c9-116">-Name</span></span>
<span data-ttu-id="033c9-117">A tárterület neve.</span><span class="sxs-lookup"><span data-stu-id="033c9-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="033c9-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="033c9-118">-StoragePool</span></span>
<span data-ttu-id="033c9-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="033c9-119">Storage pool name.</span></span>

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

### <span data-ttu-id="033c9-120">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="033c9-120">-StorageSystem</span></span>
<span data-ttu-id="033c9-121">A tárolási rendszer erőforrásának megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="033c9-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="033c9-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="033c9-122">-Location</span></span>
<span data-ttu-id="033c9-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="033c9-123">Location of the resource.</span></span>

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

### <span data-ttu-id="033c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="033c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="033c9-125">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="033c9-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="033c9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="033c9-126">-ResourceId</span></span>
<span data-ttu-id="033c9-127">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="033c9-127">The resource id.</span></span>

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

### <span data-ttu-id="033c9-128">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="033c9-128">-Filter</span></span>
<span data-ttu-id="033c9-129">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="033c9-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="033c9-130">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="033c9-130">-Skip</span></span>
<span data-ttu-id="033c9-131">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="033c9-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="033c9-132">-Top</span><span class="sxs-lookup"><span data-stu-id="033c9-132">-Top</span></span>
<span data-ttu-id="033c9-133">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="033c9-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="033c9-134">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="033c9-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="033c9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033c9-135">CommonParameters</span></span>
<span data-ttu-id="033c9-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="033c9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033c9-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="033c9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033c9-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="033c9-138">INPUTS</span></span>

## <span data-ttu-id="033c9-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="033c9-139">OUTPUTS</span></span>

### <span data-ttu-id="033c9-140">Microsoft. AzureStack. Management. Fabric. admin. models. Volume</span><span class="sxs-lookup"><span data-stu-id="033c9-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="033c9-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="033c9-141">NOTES</span></span>

## <span data-ttu-id="033c9-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="033c9-142">RELATED LINKS</span></span>
