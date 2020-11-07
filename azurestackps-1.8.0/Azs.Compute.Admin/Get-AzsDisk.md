---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840253"
---
# <span data-ttu-id="176b1-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="176b1-101">Get-AzsDisk</span></span>

## <span data-ttu-id="176b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="176b1-102">SYNOPSIS</span></span>
<span data-ttu-id="176b1-103">Azoknak a felügyelt lemezeknek a listáját adja eredményül, amelyek áttelepíthetők a megadott megosztásban.</span><span class="sxs-lookup"><span data-stu-id="176b1-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="176b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="176b1-104">SYNTAX</span></span>

### <span data-ttu-id="176b1-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="176b1-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="176b1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="176b1-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="176b1-107">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="176b1-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="176b1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="176b1-108">DESCRIPTION</span></span>
<span data-ttu-id="176b1-109">A lemezek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="176b1-109">Returns a list of disks.</span></span>

## <span data-ttu-id="176b1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="176b1-110">EXAMPLES</span></span>

### <span data-ttu-id="176b1-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="176b1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="176b1-112">A felügyelt lemezek listáját a helyi helyen jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="176b1-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="176b1-113">Alapértelmezés szerint az első 100-lemezek lesznek</span><span class="sxs-lookup"><span data-stu-id="176b1-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="176b1-114">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="176b1-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="176b1-115">Adott távtárolású lemez beszerzése.</span><span class="sxs-lookup"><span data-stu-id="176b1-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="176b1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="176b1-116">PARAMETERS</span></span>

### <span data-ttu-id="176b1-117">-Count</span><span class="sxs-lookup"><span data-stu-id="176b1-117">-Count</span></span>
<span data-ttu-id="176b1-118">A visszaadni kívánt lemezek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="176b1-118">The maximum number of disks to return.</span></span>

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

### <span data-ttu-id="176b1-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="176b1-119">-Location</span></span>
<span data-ttu-id="176b1-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="176b1-120">Location of the resource.</span></span>

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

### <span data-ttu-id="176b1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="176b1-121">-Name</span></span>
<span data-ttu-id="176b1-122">A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="176b1-122">The disk guid as identity.</span></span>

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

### <span data-ttu-id="176b1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="176b1-123">-ResourceId</span></span>
<span data-ttu-id="176b1-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="176b1-124">The resource id.</span></span>

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

### <span data-ttu-id="176b1-125">-MegosztásElérésiÚtja</span><span class="sxs-lookup"><span data-stu-id="176b1-125">-SharePath</span></span>
<span data-ttu-id="176b1-126">Annak a forrásnak a megosztása, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="176b1-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="176b1-127">– Első lépések</span><span class="sxs-lookup"><span data-stu-id="176b1-127">-Start</span></span>
<span data-ttu-id="176b1-128">A lekérdezett lemezek kezdési indexe.</span><span class="sxs-lookup"><span data-stu-id="176b1-128">The start index of disks in query.</span></span>

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

### <span data-ttu-id="176b1-129">-Állapot</span><span class="sxs-lookup"><span data-stu-id="176b1-129">-Status</span></span>
<span data-ttu-id="176b1-130">A Disk State paraméterei.</span><span class="sxs-lookup"><span data-stu-id="176b1-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="176b1-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="176b1-131">-UserSubscriptionId</span></span>
<span data-ttu-id="176b1-132">Bérlői előfizetés azonosítója, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="176b1-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="176b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176b1-133">CommonParameters</span></span>
<span data-ttu-id="176b1-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="176b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176b1-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="176b1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176b1-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="176b1-136">INPUTS</span></span>

## <span data-ttu-id="176b1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="176b1-137">OUTPUTS</span></span>

### <span data-ttu-id="176b1-138">Microsoft. AzureStack. Management. számítás. admin. models. Disk</span><span class="sxs-lookup"><span data-stu-id="176b1-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="176b1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="176b1-139">NOTES</span></span>

## <span data-ttu-id="176b1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="176b1-140">RELATED LINKS</span></span>

