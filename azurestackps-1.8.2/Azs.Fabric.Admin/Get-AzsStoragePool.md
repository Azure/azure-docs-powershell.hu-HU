---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017015"
---
# <span data-ttu-id="6ffdd-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="6ffdd-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="6ffdd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ffdd-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffdd-103">A hely összes tárolási készletének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="6ffdd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ffdd-104">SYNTAX</span></span>

### <span data-ttu-id="6ffdd-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ffdd-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6ffdd-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="6ffdd-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ffdd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ffdd-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6ffdd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ffdd-108">DESCRIPTION</span></span>
<span data-ttu-id="6ffdd-109">A hely összes tárolási készletének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="6ffdd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6ffdd-110">EXAMPLES</span></span>

### <span data-ttu-id="6ffdd-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="6ffdd-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="6ffdd-112">Az összes tárterület beszerzése adott helyen.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="6ffdd-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="6ffdd-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="6ffdd-114">Tároljon egy tárolót, amely a tároló nevét adja meg az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="6ffdd-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ffdd-115">PARAMETERS</span></span>

### <span data-ttu-id="6ffdd-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ffdd-116">-Name</span></span>
<span data-ttu-id="6ffdd-117">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-117">Storage pool name.</span></span>

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

### <span data-ttu-id="6ffdd-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="6ffdd-118">-StorageSystem</span></span>
<span data-ttu-id="6ffdd-119">A tárolási alrendszer neve</span><span class="sxs-lookup"><span data-stu-id="6ffdd-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="6ffdd-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="6ffdd-120">-Location</span></span>
<span data-ttu-id="6ffdd-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-121">Location of the resource.</span></span>

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

### <span data-ttu-id="6ffdd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffdd-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ffdd-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6ffdd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ffdd-124">-ResourceId</span></span>
<span data-ttu-id="6ffdd-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-125">The resource id.</span></span>

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

### <span data-ttu-id="6ffdd-126">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="6ffdd-126">-Filter</span></span>
<span data-ttu-id="6ffdd-127">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="6ffdd-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="6ffdd-128">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="6ffdd-128">-Skip</span></span>
<span data-ttu-id="6ffdd-129">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6ffdd-130">-Top</span><span class="sxs-lookup"><span data-stu-id="6ffdd-130">-Top</span></span>
<span data-ttu-id="6ffdd-131">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6ffdd-132">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6ffdd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffdd-133">CommonParameters</span></span>
<span data-ttu-id="6ffdd-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ffdd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffdd-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ffdd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffdd-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ffdd-136">INPUTS</span></span>

## <span data-ttu-id="6ffdd-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ffdd-137">OUTPUTS</span></span>

### <span data-ttu-id="6ffdd-138">Microsoft. AzureStack. Management. Fabric. admin. models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="6ffdd-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="6ffdd-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ffdd-139">NOTES</span></span>

## <span data-ttu-id="6ffdd-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ffdd-140">RELATED LINKS</span></span>
