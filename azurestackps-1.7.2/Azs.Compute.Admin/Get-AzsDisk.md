---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4c464d2d0e822b745acc2a7c6daecf329449105
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839501"
---
# <span data-ttu-id="04ed4-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="04ed4-101">Get-AzsDisk</span></span>

## <span data-ttu-id="04ed4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="04ed4-103">Azoknak a felügyelt lemezeknek a listáját adja eredményül, amelyek áttelepíthetők a megadott megosztásban.</span><span class="sxs-lookup"><span data-stu-id="04ed4-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="04ed4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04ed4-104">SYNTAX</span></span>

### <span data-ttu-id="04ed4-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04ed4-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="04ed4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="04ed4-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="04ed4-107">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="04ed4-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="04ed4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="04ed4-108">DESCRIPTION</span></span>
<span data-ttu-id="04ed4-109">A lemezek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="04ed4-109">Returns a list of disks.</span></span>

## <span data-ttu-id="04ed4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="04ed4-110">EXAMPLES</span></span>

### <span data-ttu-id="04ed4-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="04ed4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="04ed4-112">A felügyelt lemezek listáját a helyi helyen jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="04ed4-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="04ed4-113">Alapértelmezés szerint az első 100-lemezek lesznek</span><span class="sxs-lookup"><span data-stu-id="04ed4-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="04ed4-114">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="04ed4-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="04ed4-115">Adott távtárolású lemez beszerzése.</span><span class="sxs-lookup"><span data-stu-id="04ed4-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="04ed4-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04ed4-116">PARAMETERS</span></span>

### <span data-ttu-id="04ed4-117">-Count</span><span class="sxs-lookup"><span data-stu-id="04ed4-117">-Count</span></span>
<span data-ttu-id="04ed4-118">A visszaadni kívánt lemezek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="04ed4-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ed4-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="04ed4-119">-Location</span></span>
<span data-ttu-id="04ed4-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="04ed4-120">Location of the resource.</span></span>

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

### <span data-ttu-id="04ed4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04ed4-121">-Name</span></span>
<span data-ttu-id="04ed4-122">A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="04ed4-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ed4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04ed4-123">-ResourceId</span></span>
<span data-ttu-id="04ed4-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="04ed4-124">The resource id.</span></span>

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

### <span data-ttu-id="04ed4-125">-MegosztásElérésiÚtja</span><span class="sxs-lookup"><span data-stu-id="04ed4-125">-SharePath</span></span>
<span data-ttu-id="04ed4-126">Annak a forrásnak a megosztása, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="04ed4-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="04ed4-127">– Első lépések</span><span class="sxs-lookup"><span data-stu-id="04ed4-127">-Start</span></span>
<span data-ttu-id="04ed4-128">A lekérdezett lemezek kezdési indexe.</span><span class="sxs-lookup"><span data-stu-id="04ed4-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ed4-129">-Állapot</span><span class="sxs-lookup"><span data-stu-id="04ed4-129">-Status</span></span>
<span data-ttu-id="04ed4-130">A Disk State paraméterei.</span><span class="sxs-lookup"><span data-stu-id="04ed4-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="04ed4-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04ed4-131">-UserSubscriptionId</span></span>
<span data-ttu-id="04ed4-132">Bérlői előfizetés azonosítója, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="04ed4-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="04ed4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ed4-133">CommonParameters</span></span>
<span data-ttu-id="04ed4-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04ed4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ed4-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ed4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ed4-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04ed4-136">INPUTS</span></span>

## <span data-ttu-id="04ed4-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04ed4-137">OUTPUTS</span></span>

### <span data-ttu-id="04ed4-138">Microsoft. AzureStack. Management. számítás. admin. models. Disk</span><span class="sxs-lookup"><span data-stu-id="04ed4-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="04ed4-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04ed4-139">NOTES</span></span>

## <span data-ttu-id="04ed4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04ed4-140">RELATED LINKS</span></span>

