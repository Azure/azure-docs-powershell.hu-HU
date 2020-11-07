---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840188"
---
# <span data-ttu-id="705d0-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="705d0-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="705d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="705d0-102">SYNOPSIS</span></span>
<span data-ttu-id="705d0-103">A hely összes tárolási alrendszerének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="705d0-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="705d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="705d0-104">SYNTAX</span></span>

### <span data-ttu-id="705d0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="705d0-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="705d0-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="705d0-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="705d0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="705d0-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="705d0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="705d0-108">DESCRIPTION</span></span>
<span data-ttu-id="705d0-109">A hely összes tárolási alrendszerének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="705d0-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="705d0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="705d0-110">EXAMPLES</span></span>

### <span data-ttu-id="705d0-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="705d0-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="705d0-112">A tárolási alrendszerek beszerzése egy helyről.</span><span class="sxs-lookup"><span data-stu-id="705d0-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="705d0-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="705d0-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="705d0-114">A tárolási alrendszer helyét és nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="705d0-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="705d0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="705d0-115">PARAMETERS</span></span>

### <span data-ttu-id="705d0-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="705d0-116">-Name</span></span>
<span data-ttu-id="705d0-117">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="705d0-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="705d0-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="705d0-118">-Location</span></span>
<span data-ttu-id="705d0-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="705d0-119">Location of the resource.</span></span>

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

### <span data-ttu-id="705d0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="705d0-120">-ResourceGroupName</span></span>
<span data-ttu-id="705d0-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="705d0-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="705d0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="705d0-122">-ResourceId</span></span>
<span data-ttu-id="705d0-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="705d0-123">The resource id.</span></span>

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

### <span data-ttu-id="705d0-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="705d0-124">-Filter</span></span>
<span data-ttu-id="705d0-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="705d0-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="705d0-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="705d0-126">-Skip</span></span>
<span data-ttu-id="705d0-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="705d0-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="705d0-128">-Top</span><span class="sxs-lookup"><span data-stu-id="705d0-128">-Top</span></span>
<span data-ttu-id="705d0-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="705d0-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="705d0-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="705d0-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="705d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705d0-131">CommonParameters</span></span>
<span data-ttu-id="705d0-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="705d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705d0-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="705d0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705d0-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="705d0-134">INPUTS</span></span>

## <span data-ttu-id="705d0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="705d0-135">OUTPUTS</span></span>

### <span data-ttu-id="705d0-136">Microsoft. AzureStack. Management. Fabric. admin. models. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="705d0-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="705d0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="705d0-137">NOTES</span></span>

## <span data-ttu-id="705d0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="705d0-138">RELATED LINKS</span></span>
