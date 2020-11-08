---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017408"
---
# <span data-ttu-id="4036a-101">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4036a-101">Remove-WAPackVM</span></span>

## <span data-ttu-id="4036a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4036a-102">SYNOPSIS</span></span>
<span data-ttu-id="4036a-103">Eltávolítja a virtuálisgép-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="4036a-103">Removes virtual machine objects.</span></span>

## <span data-ttu-id="4036a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4036a-104">SYNTAX</span></span>

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4036a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4036a-105">DESCRIPTION</span></span>
<span data-ttu-id="4036a-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="4036a-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="4036a-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="4036a-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4036a-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4036a-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4036a-109">A **Remove-WAPackVM** parancsmag eltávolítja a virtuálisgép-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="4036a-109">The **Remove-WAPackVM** cmdlet removes virtual machine objects.</span></span>

## <span data-ttu-id="4036a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4036a-110">EXAMPLES</span></span>

### <span data-ttu-id="4036a-111">Példa 1: virtuális gép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4036a-111">Example 1: Remove a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="4036a-112">Az első parancs a **Get-WAPackVM** parancsmag használatával kapja meg a ContosoV126 nevű virtuális gépet, majd a $VirtualMachine változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="4036a-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="4036a-113">A második parancs eltávolítja a $VirtualMachineban tárolt virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="4036a-113">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4036a-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="4036a-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="4036a-115">2. példa: a virtuális gép eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="4036a-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

<span data-ttu-id="4036a-116">Az első parancs a **Get-WAPackVM** parancsmag használatával kapja meg a ContosoV126 nevű virtuális gépet, majd a $VirtualMachine változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="4036a-116">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="4036a-117">A második parancs eltávolítja a $VirtualMachineban tárolt virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="4036a-117">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4036a-118">Ez a parancs az *erő* paramétert tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4036a-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="4036a-119">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4036a-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4036a-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4036a-120">PARAMETERS</span></span>

### <span data-ttu-id="4036a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4036a-121">-Force</span></span>
<span data-ttu-id="4036a-122">Azt jelzi, hogy a parancsmag eltávolítja a virtuális gépet a megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4036a-122">Indicates that the cmdlet removes a virtual machine without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4036a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4036a-123">-PassThru</span></span>
<span data-ttu-id="4036a-124">Azt jelzi, hogy a parancsmag logikai értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="4036a-124">Indicates that the cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="4036a-125">Ha a művelet sikeres, a parancsmag az $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4036a-125">If the operation succeeds, the cmdlet returns a value of $True.</span></span>
<span data-ttu-id="4036a-126">Ellenkező esetben az $False értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4036a-126">Otherwise, it returns a value of $False.</span></span>
<span data-ttu-id="4036a-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4036a-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4036a-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="4036a-128">-Profile</span></span>
<span data-ttu-id="4036a-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4036a-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4036a-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4036a-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4036a-131">-VM</span><span class="sxs-lookup"><span data-stu-id="4036a-131">-VM</span></span>
<span data-ttu-id="4036a-132">Virtuális gépet ad meg.</span><span class="sxs-lookup"><span data-stu-id="4036a-132">Specifies a virtual machine.</span></span>
<span data-ttu-id="4036a-133">Virtuális gép beszerzéséhez használja a **Get-WAPackVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4036a-133">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4036a-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4036a-134">-Confirm</span></span>
<span data-ttu-id="4036a-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4036a-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4036a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4036a-136">-WhatIf</span></span>
<span data-ttu-id="4036a-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4036a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4036a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4036a-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4036a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4036a-139">CommonParameters</span></span>
<span data-ttu-id="4036a-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4036a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4036a-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4036a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4036a-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4036a-142">INPUTS</span></span>

## <span data-ttu-id="4036a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4036a-143">OUTPUTS</span></span>

## <span data-ttu-id="4036a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4036a-144">NOTES</span></span>

## <span data-ttu-id="4036a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4036a-145">RELATED LINKS</span></span>

[<span data-ttu-id="4036a-146">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4036a-146">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="4036a-147">Új – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4036a-147">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="4036a-148">Újraindítás – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4036a-148">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="4036a-149">Önéletrajz – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4036a-149">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="4036a-150">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4036a-150">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="4036a-151">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4036a-151">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="4036a-152">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4036a-152">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="4036a-153">Felfüggesztés – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4036a-153">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


