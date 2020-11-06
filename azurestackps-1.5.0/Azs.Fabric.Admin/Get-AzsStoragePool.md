---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25243539ef01a7476b6b0befb2d5cb29595001ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491195"
---
# <span data-ttu-id="310c1-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="310c1-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="310c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="310c1-102">SYNOPSIS</span></span>
<span data-ttu-id="310c1-103">A hely összes tárolási készletének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="310c1-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="310c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="310c1-104">SYNTAX</span></span>

### <span data-ttu-id="310c1-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="310c1-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="310c1-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="310c1-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="310c1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="310c1-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="310c1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="310c1-108">DESCRIPTION</span></span>
<span data-ttu-id="310c1-109">A hely összes tárolási készletének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="310c1-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="310c1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="310c1-110">EXAMPLES</span></span>

### <span data-ttu-id="310c1-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="310c1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="310c1-112">Az összes tárterület beszerzése adott helyen.</span><span class="sxs-lookup"><span data-stu-id="310c1-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="310c1-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="310c1-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="310c1-114">Tároljon egy tárolót, amely a tároló nevét adja meg az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="310c1-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="310c1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="310c1-115">PARAMETERS</span></span>

### <span data-ttu-id="310c1-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="310c1-116">-Filter</span></span>
<span data-ttu-id="310c1-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="310c1-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="310c1-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="310c1-118">-Location</span></span>
<span data-ttu-id="310c1-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="310c1-119">Location of the resource.</span></span>

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

### <span data-ttu-id="310c1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="310c1-120">-Name</span></span>
<span data-ttu-id="310c1-121">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="310c1-121">Storage pool name.</span></span>

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

### <span data-ttu-id="310c1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310c1-122">-ResourceGroupName</span></span>
<span data-ttu-id="310c1-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="310c1-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="310c1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="310c1-124">-ResourceId</span></span>
<span data-ttu-id="310c1-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="310c1-125">The resource id.</span></span>

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

### <span data-ttu-id="310c1-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="310c1-126">-Skip</span></span>
<span data-ttu-id="310c1-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="310c1-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="310c1-128">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="310c1-128">-StorageSystem</span></span>
<span data-ttu-id="310c1-129">Az a tárolási rendszer, amelyben a tároló található.</span><span class="sxs-lookup"><span data-stu-id="310c1-129">Storage system in which the storage pool is located.</span></span>

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

### <span data-ttu-id="310c1-130">-Top</span><span class="sxs-lookup"><span data-stu-id="310c1-130">-Top</span></span>
<span data-ttu-id="310c1-131">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="310c1-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="310c1-132">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="310c1-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="310c1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310c1-133">CommonParameters</span></span>
<span data-ttu-id="310c1-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="310c1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310c1-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="310c1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310c1-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="310c1-136">INPUTS</span></span>

## <span data-ttu-id="310c1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="310c1-137">OUTPUTS</span></span>

### <span data-ttu-id="310c1-138">Microsoft. AzureStack. Management. Fabric. admin. models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="310c1-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="310c1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="310c1-139">NOTES</span></span>

## <span data-ttu-id="310c1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="310c1-140">RELATED LINKS</span></span>

