---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016905"
---
# <span data-ttu-id="d3114-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="d3114-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="d3114-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3114-102">SYNOPSIS</span></span>
<span data-ttu-id="d3114-103">A felügyelt áttelepítési feladatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d3114-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="d3114-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3114-104">SYNTAX</span></span>

### <span data-ttu-id="d3114-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3114-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="d3114-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3114-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="d3114-107">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="d3114-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="d3114-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3114-108">DESCRIPTION</span></span>
<span data-ttu-id="d3114-109">A lemezvezérlő-áttelepítési feladatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d3114-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="d3114-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d3114-110">EXAMPLES</span></span>

### <span data-ttu-id="d3114-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d3114-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="d3114-112">Adott távtárolású áttelepítési feladat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d3114-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="d3114-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d3114-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="d3114-114">A távtárolású áttelepítési feladatok listáját jeleníti meg a helyi helyen.</span><span class="sxs-lookup"><span data-stu-id="d3114-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="d3114-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3114-115">PARAMETERS</span></span>

### <span data-ttu-id="d3114-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="d3114-116">-Location</span></span>
<span data-ttu-id="d3114-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d3114-117">Location of the resource.</span></span>

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

### <span data-ttu-id="d3114-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3114-118">-Name</span></span>
<span data-ttu-id="d3114-119">Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="d3114-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3114-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3114-120">-ResourceId</span></span>
<span data-ttu-id="d3114-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d3114-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3114-122">-Állapot</span><span class="sxs-lookup"><span data-stu-id="d3114-122">-Status</span></span>
<span data-ttu-id="d3114-123">A lemezvezérlő-áttelepítési feladat állapotának paraméterei.</span><span class="sxs-lookup"><span data-stu-id="d3114-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="d3114-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3114-124">CommonParameters</span></span>
<span data-ttu-id="d3114-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3114-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3114-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3114-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3114-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3114-127">INPUTS</span></span>

## <span data-ttu-id="d3114-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3114-128">OUTPUTS</span></span>

### <span data-ttu-id="d3114-129">Microsoft. AzureStack. Management. kiszámítás. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="d3114-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="d3114-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3114-130">NOTES</span></span>

## <span data-ttu-id="d3114-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3114-131">RELATED LINKS</span></span>

