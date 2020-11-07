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
ms.locfileid: "93839504"
---
# <span data-ttu-id="aa106-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="aa106-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="aa106-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa106-102">SYNOPSIS</span></span>
<span data-ttu-id="aa106-103">Új virtuálisgép-kiterjesztési kép létrehozása</span><span class="sxs-lookup"><span data-stu-id="aa106-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="aa106-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa106-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa106-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa106-105">DESCRIPTION</span></span>
<span data-ttu-id="aa106-106">A virtuálisgép-bővítmények lemezképének létrehozása</span><span class="sxs-lookup"><span data-stu-id="aa106-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="aa106-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa106-107">EXAMPLES</span></span>

### <span data-ttu-id="aa106-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa106-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="aa106-109">Vegyen fel egy új platform képkiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="aa106-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="aa106-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa106-110">PARAMETERS</span></span>

### <span data-ttu-id="aa106-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa106-111">-AsJob</span></span>
<span data-ttu-id="aa106-112">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="aa106-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="aa106-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="aa106-113">-ComputeRole</span></span>
<span data-ttu-id="aa106-114">A szerepkör, a IaaS vagy a Péter, ez a bővítmény támogatja.</span><span class="sxs-lookup"><span data-stu-id="aa106-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="aa106-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aa106-115">-Force</span></span>
<span data-ttu-id="aa106-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa106-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="aa106-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="aa106-117">-IsSystemExtension</span></span>
<span data-ttu-id="aa106-118">Azt jelzi, hogy a kiterjesztés a rendszerhez van-e kijelölve.</span><span class="sxs-lookup"><span data-stu-id="aa106-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="aa106-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="aa106-119">-Location</span></span>
<span data-ttu-id="aa106-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="aa106-120">Location of the resource.</span></span>

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

### <span data-ttu-id="aa106-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="aa106-121">-Publisher</span></span>
<span data-ttu-id="aa106-122">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="aa106-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="aa106-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="aa106-123">-SourceBlob</span></span>
<span data-ttu-id="aa106-124">URI a Virtual Machine Extension csomaghoz.</span><span class="sxs-lookup"><span data-stu-id="aa106-124">URI to virtual machine extension package.</span></span>

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

### <span data-ttu-id="aa106-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="aa106-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="aa106-126">Igaz, ha támogatja a több bővítményt.</span><span class="sxs-lookup"><span data-stu-id="aa106-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="aa106-127">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="aa106-127">-Type</span></span>
<span data-ttu-id="aa106-128">A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="aa106-128">Type of extension.</span></span>

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

### <span data-ttu-id="aa106-129">-Verzió</span><span class="sxs-lookup"><span data-stu-id="aa106-129">-Version</span></span>
<span data-ttu-id="aa106-130">A vritual Machine Image Extension verziója.</span><span class="sxs-lookup"><span data-stu-id="aa106-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="aa106-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="aa106-131">-VmOsType</span></span>
<span data-ttu-id="aa106-132">A kiterjesztés-kezelő központi telepítéséhez szükséges cél a virtuális gép operációs rendszerének típusa.</span><span class="sxs-lookup"><span data-stu-id="aa106-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="aa106-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="aa106-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="aa106-134">Az az érték, amely azt jelzi, hogy a bővítmény engedélyezve van-e a virtuálisgép-készlet támogatásához.</span><span class="sxs-lookup"><span data-stu-id="aa106-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="aa106-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa106-135">-Confirm</span></span>
<span data-ttu-id="aa106-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa106-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa106-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa106-137">-WhatIf</span></span>
<span data-ttu-id="aa106-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa106-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa106-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa106-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa106-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa106-140">CommonParameters</span></span>
<span data-ttu-id="aa106-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa106-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa106-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa106-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa106-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa106-143">INPUTS</span></span>

## <span data-ttu-id="aa106-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa106-144">OUTPUTS</span></span>

### <span data-ttu-id="aa106-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="aa106-145">VmExtensionObject</span></span>

## <span data-ttu-id="aa106-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa106-146">NOTES</span></span>

## <span data-ttu-id="aa106-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa106-147">RELATED LINKS</span></span>

