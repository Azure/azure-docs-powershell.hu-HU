---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67835cc0ae5191f50aefb79f76148752c68508bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839683"
---
# <span data-ttu-id="2432d-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="2432d-101">Get-AzsVolume</span></span>

## <span data-ttu-id="2432d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2432d-102">SYNOPSIS</span></span>
<span data-ttu-id="2432d-103">A hely összes tárolási kötetének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="2432d-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="2432d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2432d-104">SYNTAX</span></span>

### <span data-ttu-id="2432d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2432d-105">List (Default)</span></span>
```
Get-AzsVolume -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2432d-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="2432d-106">Get</span></span>
```
Get-AzsVolume -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2432d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2432d-107">ResourceId</span></span>
```
Get-AzsVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2432d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2432d-108">DESCRIPTION</span></span>
<span data-ttu-id="2432d-109">A hely összes tárolási kötetének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="2432d-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="2432d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2432d-110">EXAMPLES</span></span>

### <span data-ttu-id="2432d-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2432d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="2432d-112">A tárterület minden tárolási kötetének listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="2432d-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="2432d-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2432d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="2432d-114">A tárterületet a megadott helyen, név szerint érheti el.</span><span class="sxs-lookup"><span data-stu-id="2432d-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="2432d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2432d-115">PARAMETERS</span></span>

### <span data-ttu-id="2432d-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="2432d-116">-Filter</span></span>
<span data-ttu-id="2432d-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="2432d-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="2432d-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="2432d-118">-Location</span></span>
<span data-ttu-id="2432d-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="2432d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="2432d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2432d-120">-Name</span></span>
<span data-ttu-id="2432d-121">A tárterület neve.</span><span class="sxs-lookup"><span data-stu-id="2432d-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="2432d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2432d-122">-ResourceGroupName</span></span>
<span data-ttu-id="2432d-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="2432d-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2432d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2432d-124">-ResourceId</span></span>
<span data-ttu-id="2432d-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2432d-125">The resource id.</span></span>

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

### <span data-ttu-id="2432d-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="2432d-126">-ScaleUnit</span></span>
<span data-ttu-id="2432d-127">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="2432d-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="2432d-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="2432d-128">-StorageSubSystem</span></span>
<span data-ttu-id="2432d-129">Tároló alrendszer, amelyben a kötet található.</span><span class="sxs-lookup"><span data-stu-id="2432d-129">Storage subsystem in which the volume is located.</span></span>

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

### <span data-ttu-id="2432d-130">-Top</span><span class="sxs-lookup"><span data-stu-id="2432d-130">-Top</span></span>
<span data-ttu-id="2432d-131">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="2432d-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2432d-132">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="2432d-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2432d-133">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="2432d-133">-Skip</span></span>
<span data-ttu-id="2432d-134">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="2432d-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2432d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2432d-135">CommonParameters</span></span>
<span data-ttu-id="2432d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2432d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2432d-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2432d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2432d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2432d-138">INPUTS</span></span>

## <span data-ttu-id="2432d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2432d-139">OUTPUTS</span></span>

### <span data-ttu-id="2432d-140">Microsoft. AzureStack. Management. Fabric. admin. models. Volume</span><span class="sxs-lookup"><span data-stu-id="2432d-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>
## <span data-ttu-id="2432d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2432d-141">NOTES</span></span>

## <span data-ttu-id="2432d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2432d-142">RELATED LINKS</span></span>
