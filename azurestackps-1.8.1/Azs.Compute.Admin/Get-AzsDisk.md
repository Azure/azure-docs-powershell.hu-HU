---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840587"
---
# <span data-ttu-id="588bb-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="588bb-101">Get-AzsDisk</span></span>

## <span data-ttu-id="588bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="588bb-102">SYNOPSIS</span></span>
<span data-ttu-id="588bb-103">Azoknak a felügyelt lemezeknek a listáját adja eredményül, amelyek áttelepíthetők a megadott megosztásban.</span><span class="sxs-lookup"><span data-stu-id="588bb-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="588bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="588bb-104">SYNTAX</span></span>

### <span data-ttu-id="588bb-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="588bb-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="588bb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="588bb-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="588bb-107">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="588bb-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="588bb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="588bb-108">DESCRIPTION</span></span>
<span data-ttu-id="588bb-109">A lemezek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="588bb-109">Returns a list of disks.</span></span>

## <span data-ttu-id="588bb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="588bb-110">EXAMPLES</span></span>

### <span data-ttu-id="588bb-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="588bb-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="588bb-112">A felügyelt lemezek listáját a helyi helyen jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="588bb-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="588bb-113">Alapértelmezés szerint az első 100-lemezek lesznek</span><span class="sxs-lookup"><span data-stu-id="588bb-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="588bb-114">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="588bb-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="588bb-115">Adott távtárolású lemez beszerzése.</span><span class="sxs-lookup"><span data-stu-id="588bb-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="588bb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="588bb-116">PARAMETERS</span></span>

### <span data-ttu-id="588bb-117">-Count</span><span class="sxs-lookup"><span data-stu-id="588bb-117">-Count</span></span>
<span data-ttu-id="588bb-118">A visszaadni kívánt lemezek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="588bb-118">The maximum number of disks to return.</span></span>

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

### <span data-ttu-id="588bb-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="588bb-119">-Location</span></span>
<span data-ttu-id="588bb-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="588bb-120">Location of the resource.</span></span>

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

### <span data-ttu-id="588bb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="588bb-121">-Name</span></span>
<span data-ttu-id="588bb-122">A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="588bb-122">The disk guid as identity.</span></span>

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

### <span data-ttu-id="588bb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="588bb-123">-ResourceId</span></span>
<span data-ttu-id="588bb-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="588bb-124">The resource id.</span></span>

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

### <span data-ttu-id="588bb-125">-MegosztásElérésiÚtja</span><span class="sxs-lookup"><span data-stu-id="588bb-125">-SharePath</span></span>
<span data-ttu-id="588bb-126">Annak a forrásnak a megosztása, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="588bb-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="588bb-127">– Első lépések</span><span class="sxs-lookup"><span data-stu-id="588bb-127">-Start</span></span>
<span data-ttu-id="588bb-128">A lekérdezett lemezek kezdési indexe.</span><span class="sxs-lookup"><span data-stu-id="588bb-128">The start index of disks in query.</span></span>

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

### <span data-ttu-id="588bb-129">-Állapot</span><span class="sxs-lookup"><span data-stu-id="588bb-129">-Status</span></span>
<span data-ttu-id="588bb-130">A Disk State paraméterei.</span><span class="sxs-lookup"><span data-stu-id="588bb-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="588bb-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="588bb-131">-UserSubscriptionId</span></span>
<span data-ttu-id="588bb-132">Bérlői előfizetés azonosítója, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="588bb-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="588bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588bb-133">CommonParameters</span></span>
<span data-ttu-id="588bb-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="588bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588bb-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="588bb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588bb-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="588bb-136">INPUTS</span></span>

## <span data-ttu-id="588bb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="588bb-137">OUTPUTS</span></span>

### <span data-ttu-id="588bb-138">Microsoft. AzureStack. Management. számítás. admin. models. Disk</span><span class="sxs-lookup"><span data-stu-id="588bb-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="588bb-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="588bb-139">NOTES</span></span>

## <span data-ttu-id="588bb-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="588bb-140">RELATED LINKS</span></span>

