---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42181271e9295212f256cfc519e8ecc32eeae048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491760"
---
# <span data-ttu-id="5f91c-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="5f91c-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="5f91c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f91c-102">SYNOPSIS</span></span>
<span data-ttu-id="5f91c-103">Új virtuálisgép-kiterjesztési kép létrehozása</span><span class="sxs-lookup"><span data-stu-id="5f91c-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="5f91c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f91c-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f91c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f91c-105">DESCRIPTION</span></span>
<span data-ttu-id="5f91c-106">A virtuálisgép-bővítmények lemezképének létrehozása</span><span class="sxs-lookup"><span data-stu-id="5f91c-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="5f91c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5f91c-107">EXAMPLES</span></span>

### <span data-ttu-id="5f91c-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f91c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="5f91c-109">Vegyen fel egy új platform képkiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="5f91c-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="5f91c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f91c-110">PARAMETERS</span></span>

### <span data-ttu-id="5f91c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f91c-111">-AsJob</span></span>
<span data-ttu-id="5f91c-112">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="5f91c-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5f91c-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="5f91c-113">-ComputeRole</span></span>
<span data-ttu-id="5f91c-114">A szerepkör, a IaaS vagy a Péter, ez a bővítmény támogatja.</span><span class="sxs-lookup"><span data-stu-id="5f91c-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="5f91c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5f91c-115">-Force</span></span>
<span data-ttu-id="5f91c-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f91c-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5f91c-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="5f91c-117">-IsSystemExtension</span></span>
<span data-ttu-id="5f91c-118">Azt jelzi, hogy a kiterjesztés a rendszerhez van-e kijelölve.</span><span class="sxs-lookup"><span data-stu-id="5f91c-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="5f91c-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="5f91c-119">-Location</span></span>
<span data-ttu-id="5f91c-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="5f91c-120">Location of the resource.</span></span>

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

### <span data-ttu-id="5f91c-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5f91c-121">-Publisher</span></span>
<span data-ttu-id="5f91c-122">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="5f91c-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="5f91c-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="5f91c-123">-SourceBlob</span></span>
<span data-ttu-id="5f91c-124">URI a Virtual Machine Extension csomaghoz.</span><span class="sxs-lookup"><span data-stu-id="5f91c-124">URI to virtual machine extension package.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f91c-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="5f91c-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="5f91c-126">Igaz, ha támogatja a több bővítményt.</span><span class="sxs-lookup"><span data-stu-id="5f91c-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="5f91c-127">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="5f91c-127">-Type</span></span>
<span data-ttu-id="5f91c-128">A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="5f91c-128">Type of extension.</span></span>

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

### <span data-ttu-id="5f91c-129">-Verzió</span><span class="sxs-lookup"><span data-stu-id="5f91c-129">-Version</span></span>
<span data-ttu-id="5f91c-130">A vritual Machine Image Extension verziója.</span><span class="sxs-lookup"><span data-stu-id="5f91c-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="5f91c-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="5f91c-131">-VmOsType</span></span>
<span data-ttu-id="5f91c-132">A kiterjesztés-kezelő központi telepítéséhez szükséges cél a virtuális gép operációs rendszerének típusa.</span><span class="sxs-lookup"><span data-stu-id="5f91c-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="5f91c-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="5f91c-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="5f91c-134">Az az érték, amely azt jelzi, hogy a bővítmény engedélyezve van-e a virtuálisgép-készlet támogatásához.</span><span class="sxs-lookup"><span data-stu-id="5f91c-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="5f91c-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5f91c-135">-Confirm</span></span>
<span data-ttu-id="5f91c-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f91c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f91c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f91c-137">-WhatIf</span></span>
<span data-ttu-id="5f91c-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5f91c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f91c-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f91c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f91c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f91c-140">CommonParameters</span></span>
<span data-ttu-id="5f91c-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f91c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f91c-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f91c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f91c-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f91c-143">INPUTS</span></span>

## <span data-ttu-id="5f91c-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f91c-144">OUTPUTS</span></span>

### <span data-ttu-id="5f91c-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="5f91c-145">VmExtensionObject</span></span>

## <span data-ttu-id="5f91c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f91c-146">NOTES</span></span>

## <span data-ttu-id="5f91c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f91c-147">RELATED LINKS</span></span>

