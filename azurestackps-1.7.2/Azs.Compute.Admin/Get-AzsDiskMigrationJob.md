---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839500"
---
# <span data-ttu-id="8da57-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="8da57-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="8da57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8da57-102">SYNOPSIS</span></span>
<span data-ttu-id="8da57-103">A felügyelt áttelepítési feladatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8da57-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="8da57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8da57-104">SYNTAX</span></span>

### <span data-ttu-id="8da57-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8da57-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="8da57-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8da57-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="8da57-107">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="8da57-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="8da57-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8da57-108">DESCRIPTION</span></span>
<span data-ttu-id="8da57-109">A lemezvezérlő-áttelepítési feladatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8da57-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="8da57-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8da57-110">EXAMPLES</span></span>

### <span data-ttu-id="8da57-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8da57-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="8da57-112">Adott távtárolású áttelepítési feladat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="8da57-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="8da57-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8da57-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="8da57-114">A távtárolású áttelepítési feladatok listáját jeleníti meg a helyi helyen.</span><span class="sxs-lookup"><span data-stu-id="8da57-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="8da57-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8da57-115">PARAMETERS</span></span>

### <span data-ttu-id="8da57-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="8da57-116">-Location</span></span>
<span data-ttu-id="8da57-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="8da57-117">Location of the resource.</span></span>

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

### <span data-ttu-id="8da57-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8da57-118">-Name</span></span>
<span data-ttu-id="8da57-119">Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="8da57-119">The migration job guid name.</span></span>

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

### <span data-ttu-id="8da57-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8da57-120">-ResourceId</span></span>
<span data-ttu-id="8da57-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="8da57-121">The resource id.</span></span>

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

### <span data-ttu-id="8da57-122">-Állapot</span><span class="sxs-lookup"><span data-stu-id="8da57-122">-Status</span></span>
<span data-ttu-id="8da57-123">A lemezvezérlő-áttelepítési feladat állapotának paraméterei.</span><span class="sxs-lookup"><span data-stu-id="8da57-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="8da57-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da57-124">CommonParameters</span></span>
<span data-ttu-id="8da57-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8da57-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da57-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da57-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da57-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8da57-127">INPUTS</span></span>

## <span data-ttu-id="8da57-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8da57-128">OUTPUTS</span></span>

### <span data-ttu-id="8da57-129">Microsoft. AzureStack. Management. kiszámítás. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="8da57-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="8da57-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8da57-130">NOTES</span></span>

## <span data-ttu-id="8da57-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8da57-131">RELATED LINKS</span></span>

