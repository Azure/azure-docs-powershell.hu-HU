---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840547"
---
# <span data-ttu-id="af4bf-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="af4bf-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="af4bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="af4bf-103">A hely összes tárolási kötetének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="af4bf-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="af4bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af4bf-104">SYNTAX</span></span>

### <span data-ttu-id="af4bf-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af4bf-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="af4bf-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="af4bf-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="af4bf-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="af4bf-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="af4bf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="af4bf-108">DESCRIPTION</span></span>
<span data-ttu-id="af4bf-109">A hely összes tárolási kötetének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="af4bf-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="af4bf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="af4bf-110">EXAMPLES</span></span>

### <span data-ttu-id="af4bf-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="af4bf-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="af4bf-112">A tárterület minden tárolási kötetének listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="af4bf-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="af4bf-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="af4bf-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="af4bf-114">A tárterületet a megadott helyen, név szerint érheti el.</span><span class="sxs-lookup"><span data-stu-id="af4bf-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="af4bf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af4bf-115">PARAMETERS</span></span>

### <span data-ttu-id="af4bf-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af4bf-116">-Name</span></span>
<span data-ttu-id="af4bf-117">A tárterület neve.</span><span class="sxs-lookup"><span data-stu-id="af4bf-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="af4bf-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="af4bf-118">-StoragePool</span></span>
<span data-ttu-id="af4bf-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="af4bf-119">Storage pool name.</span></span>

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

### <span data-ttu-id="af4bf-120">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="af4bf-120">-StorageSystem</span></span>
<span data-ttu-id="af4bf-121">A tárolási rendszer erőforrásának megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="af4bf-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="af4bf-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="af4bf-122">-Location</span></span>
<span data-ttu-id="af4bf-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="af4bf-123">Location of the resource.</span></span>

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

### <span data-ttu-id="af4bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="af4bf-125">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="af4bf-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="af4bf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af4bf-126">-ResourceId</span></span>
<span data-ttu-id="af4bf-127">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="af4bf-127">The resource id.</span></span>

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

### <span data-ttu-id="af4bf-128">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="af4bf-128">-Filter</span></span>
<span data-ttu-id="af4bf-129">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="af4bf-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="af4bf-130">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="af4bf-130">-Skip</span></span>
<span data-ttu-id="af4bf-131">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="af4bf-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="af4bf-132">-Top</span><span class="sxs-lookup"><span data-stu-id="af4bf-132">-Top</span></span>
<span data-ttu-id="af4bf-133">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="af4bf-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="af4bf-134">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="af4bf-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="af4bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4bf-135">CommonParameters</span></span>
<span data-ttu-id="af4bf-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af4bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4bf-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af4bf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4bf-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af4bf-138">INPUTS</span></span>

## <span data-ttu-id="af4bf-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af4bf-139">OUTPUTS</span></span>

### <span data-ttu-id="af4bf-140">Microsoft. AzureStack. Management. Fabric. admin. models. Volume</span><span class="sxs-lookup"><span data-stu-id="af4bf-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="af4bf-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af4bf-141">NOTES</span></span>

## <span data-ttu-id="af4bf-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af4bf-142">RELATED LINKS</span></span>
