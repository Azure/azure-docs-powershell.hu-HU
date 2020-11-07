---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d39721f1a9ed243242bd08053f9a22f0ed53df30
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840809"
---
# <span data-ttu-id="7aa51-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="7aa51-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="7aa51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7aa51-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa51-103">Virtuális gép platformjának képe egy adott képkonfigurációból.</span><span class="sxs-lookup"><span data-stu-id="7aa51-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="7aa51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7aa51-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aa51-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7aa51-105">DESCRIPTION</span></span>
<span data-ttu-id="7aa51-106">Platform-kép hozzáadása</span><span class="sxs-lookup"><span data-stu-id="7aa51-106">Add a platform image.</span></span>

## <span data-ttu-id="7aa51-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7aa51-107">EXAMPLES</span></span>

### <span data-ttu-id="7aa51-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7aa51-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="7aa51-109">Új platformot tartalmazó kép hozzáadása</span><span class="sxs-lookup"><span data-stu-id="7aa51-109">Add a new platform image.</span></span>

## <span data-ttu-id="7aa51-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7aa51-110">PARAMETERS</span></span>

### <span data-ttu-id="7aa51-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7aa51-111">-AsJob</span></span>
<span data-ttu-id="7aa51-112">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="7aa51-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="7aa51-113">-BillingPartNumber</span></span>
<span data-ttu-id="7aa51-114">A szoftver költségeinek kiszámlázására használt cikkszám.</span><span class="sxs-lookup"><span data-stu-id="7aa51-114">The part number is used to bill for software costs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-115">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="7aa51-115">-DataDisks</span></span>
<span data-ttu-id="7aa51-116">A platform képe által használt adatlemezek.</span><span class="sxs-lookup"><span data-stu-id="7aa51-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7aa51-117">-Force</span></span>
<span data-ttu-id="7aa51-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7aa51-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="7aa51-119">-Location</span></span>
<span data-ttu-id="7aa51-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="7aa51-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-121">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="7aa51-121">-Offer</span></span>
<span data-ttu-id="7aa51-122">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="7aa51-122">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="7aa51-123">-OsType</span></span>
<span data-ttu-id="7aa51-124">Operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="7aa51-124">Operating system type.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="7aa51-125">-OsUri</span></span>
<span data-ttu-id="7aa51-126">A lemez helye.</span><span class="sxs-lookup"><span data-stu-id="7aa51-126">Location of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7aa51-127">-Publisher</span></span>
<span data-ttu-id="7aa51-128">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="7aa51-128">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="7aa51-129">-Sku</span></span>
<span data-ttu-id="7aa51-130">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="7aa51-130">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-131">-Verzió</span><span class="sxs-lookup"><span data-stu-id="7aa51-131">-Version</span></span>
<span data-ttu-id="7aa51-132">A virtuális gép platformjának a verziója.</span><span class="sxs-lookup"><span data-stu-id="7aa51-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7aa51-133">-Confirm</span></span>
<span data-ttu-id="7aa51-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7aa51-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aa51-135">-WhatIf</span></span>
<span data-ttu-id="7aa51-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7aa51-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aa51-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7aa51-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa51-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa51-138">CommonParameters</span></span>
<span data-ttu-id="7aa51-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7aa51-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa51-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aa51-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa51-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aa51-141">INPUTS</span></span>

## <span data-ttu-id="7aa51-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aa51-142">OUTPUTS</span></span>

### <span data-ttu-id="7aa51-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="7aa51-143">PlatformImageObject</span></span>

## <span data-ttu-id="7aa51-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7aa51-144">NOTES</span></span>

## <span data-ttu-id="7aa51-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7aa51-145">RELATED LINKS</span></span>

