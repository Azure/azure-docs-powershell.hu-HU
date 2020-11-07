---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840584"
---
# <span data-ttu-id="4bd2b-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4bd2b-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="4bd2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd2b-103">A felügyelt áttelepítési feladatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="4bd2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bd2b-104">SYNTAX</span></span>

### <span data-ttu-id="4bd2b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4bd2b-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="4bd2b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd2b-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="4bd2b-107">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="4bd2b-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="4bd2b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bd2b-108">DESCRIPTION</span></span>
<span data-ttu-id="4bd2b-109">A lemezvezérlő-áttelepítési feladatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="4bd2b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4bd2b-110">EXAMPLES</span></span>

### <span data-ttu-id="4bd2b-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4bd2b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="4bd2b-112">Adott távtárolású áttelepítési feladat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="4bd2b-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4bd2b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="4bd2b-114">A távtárolású áttelepítési feladatok listáját jeleníti meg a helyi helyen.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="4bd2b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bd2b-115">PARAMETERS</span></span>

### <span data-ttu-id="4bd2b-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="4bd2b-116">-Location</span></span>
<span data-ttu-id="4bd2b-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-117">Location of the resource.</span></span>

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

### <span data-ttu-id="4bd2b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4bd2b-118">-Name</span></span>
<span data-ttu-id="4bd2b-119">Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-119">The migration job guid name.</span></span>

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

### <span data-ttu-id="4bd2b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd2b-120">-ResourceId</span></span>
<span data-ttu-id="4bd2b-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-121">The resource id.</span></span>

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

### <span data-ttu-id="4bd2b-122">-Állapot</span><span class="sxs-lookup"><span data-stu-id="4bd2b-122">-Status</span></span>
<span data-ttu-id="4bd2b-123">A lemezvezérlő-áttelepítési feladat állapotának paraméterei.</span><span class="sxs-lookup"><span data-stu-id="4bd2b-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="4bd2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd2b-124">CommonParameters</span></span>
<span data-ttu-id="4bd2b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4bd2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd2b-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd2b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd2b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bd2b-127">INPUTS</span></span>

## <span data-ttu-id="4bd2b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bd2b-128">OUTPUTS</span></span>

### <span data-ttu-id="4bd2b-129">Microsoft. AzureStack. Management. kiszámítás. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4bd2b-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="4bd2b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bd2b-130">NOTES</span></span>

## <span data-ttu-id="4bd2b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bd2b-131">RELATED LINKS</span></span>

