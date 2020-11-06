---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f81cf1ed28b822a0686d1db71541585023f1e57b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491156"
---
# <span data-ttu-id="ccc6b-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="ccc6b-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="ccc6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccc6b-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc6b-103">A virtuális gép képkiterjesztéseit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ccc6b-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="ccc6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccc6b-104">SYNTAX</span></span>

### <span data-ttu-id="ccc6b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ccc6b-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="ccc6b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="ccc6b-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccc6b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccc6b-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ccc6b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccc6b-108">DESCRIPTION</span></span>
<span data-ttu-id="ccc6b-109">A virtuális gép képkiterjesztését számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ccc6b-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="ccc6b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ccc6b-110">EXAMPLES</span></span>

### <span data-ttu-id="ccc6b-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ccc6b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="ccc6b-112">Az összes VM-bővítmény beszerzése egy helyen.</span><span class="sxs-lookup"><span data-stu-id="ccc6b-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="ccc6b-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ccc6b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="ccc6b-114">Konkrét VM-bővítmény beszerzése.</span><span class="sxs-lookup"><span data-stu-id="ccc6b-114">Get specific VM extension.</span></span>

## <span data-ttu-id="ccc6b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccc6b-115">PARAMETERS</span></span>

### <span data-ttu-id="ccc6b-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="ccc6b-116">-Location</span></span>
<span data-ttu-id="ccc6b-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="ccc6b-117">Location of the resource.</span></span>

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

### <span data-ttu-id="ccc6b-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ccc6b-118">-Publisher</span></span>
<span data-ttu-id="ccc6b-119">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="ccc6b-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="ccc6b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccc6b-120">-ResourceId</span></span>
<span data-ttu-id="ccc6b-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ccc6b-121">The resource id.</span></span>

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

### <span data-ttu-id="ccc6b-122">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="ccc6b-122">-Type</span></span>
<span data-ttu-id="ccc6b-123">A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="ccc6b-123">Type of extension.</span></span>

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

### <span data-ttu-id="ccc6b-124">-Verzió</span><span class="sxs-lookup"><span data-stu-id="ccc6b-124">-Version</span></span>
<span data-ttu-id="ccc6b-125">A virtuális gép képkiterjesztésének verziója.</span><span class="sxs-lookup"><span data-stu-id="ccc6b-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="ccc6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc6b-126">CommonParameters</span></span>
<span data-ttu-id="ccc6b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccc6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc6b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccc6b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc6b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccc6b-129">INPUTS</span></span>

## <span data-ttu-id="ccc6b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccc6b-130">OUTPUTS</span></span>

### <span data-ttu-id="ccc6b-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="ccc6b-131">VmExtensionObject</span></span>

## <span data-ttu-id="ccc6b-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccc6b-132">NOTES</span></span>

## <span data-ttu-id="ccc6b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccc6b-133">RELATED LINKS</span></span>

