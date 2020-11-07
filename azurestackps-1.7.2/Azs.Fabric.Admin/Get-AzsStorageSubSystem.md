---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2abc9073b9e7bcbcd4644150ada4c19cd351f660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839684"
---
# <span data-ttu-id="de4ac-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="de4ac-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="de4ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de4ac-102">SYNOPSIS</span></span>
<span data-ttu-id="de4ac-103">A méretarány minden tárolási alrendszerének listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="de4ac-103">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="de4ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de4ac-104">SYNTAX</span></span>

### <span data-ttu-id="de4ac-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de4ac-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="de4ac-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="de4ac-106">Get</span></span>
```
Get-AzsStorageSubSystem [-Name] <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="de4ac-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="de4ac-107">ResourceId</span></span>
```
Get-AzsStorageSubSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="de4ac-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="de4ac-108">DESCRIPTION</span></span>
<span data-ttu-id="de4ac-109">A méretarány minden tárolási alrendszerének listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="de4ac-109">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="de4ac-110">Példák</span><span class="sxs-lookup"><span data-stu-id="de4ac-110">EXAMPLES</span></span>

### <span data-ttu-id="de4ac-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="de4ac-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster
```

<span data-ttu-id="de4ac-112">Az összes tárterület-alrendszert letölthet egy méretarányból.</span><span class="sxs-lookup"><span data-stu-id="de4ac-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="de4ac-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="de4ac-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster -Name S-Cluster.azurestack.local
```

<span data-ttu-id="de4ac-114">Adja meg a tárterület-alrendszer méretarányát és nevét.</span><span class="sxs-lookup"><span data-stu-id="de4ac-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="de4ac-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de4ac-115">PARAMETERS</span></span>

### <span data-ttu-id="de4ac-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="de4ac-116">-Filter</span></span>
<span data-ttu-id="de4ac-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="de4ac-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="de4ac-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="de4ac-118">-Location</span></span>
<span data-ttu-id="de4ac-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="de4ac-119">Location of the resource.</span></span>

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

### <span data-ttu-id="de4ac-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de4ac-120">-Name</span></span>
<span data-ttu-id="de4ac-121">A tárolási alrendszer neve.</span><span class="sxs-lookup"><span data-stu-id="de4ac-121">Name of the storage subsystem.</span></span>

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

### <span data-ttu-id="de4ac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de4ac-122">-ResourceGroupName</span></span>
<span data-ttu-id="de4ac-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="de4ac-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="de4ac-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de4ac-124">-ResourceId</span></span>
<span data-ttu-id="de4ac-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="de4ac-125">The resource id.</span></span>

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

### <span data-ttu-id="de4ac-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="de4ac-126">-ScaleUnit</span></span>
<span data-ttu-id="de4ac-127">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="de4ac-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="de4ac-128">-Top</span><span class="sxs-lookup"><span data-stu-id="de4ac-128">-Top</span></span>
<span data-ttu-id="de4ac-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="de4ac-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="de4ac-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="de4ac-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="de4ac-131">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="de4ac-131">-Skip</span></span>
<span data-ttu-id="de4ac-132">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="de4ac-132">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="de4ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4ac-133">CommonParameters</span></span>
<span data-ttu-id="de4ac-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de4ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4ac-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de4ac-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4ac-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de4ac-136">INPUTS</span></span>

## <span data-ttu-id="de4ac-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de4ac-137">OUTPUTS</span></span>

### <span data-ttu-id="de4ac-138">Microsoft. AzureStack. Management. Fabric. admin. models. StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="de4ac-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSubSystem</span></span>
## <span data-ttu-id="de4ac-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de4ac-139">NOTES</span></span>

## <span data-ttu-id="de4ac-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de4ac-140">RELATED LINKS</span></span>
