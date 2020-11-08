---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4FB7096E-DDA1-474C-BF0C-D910681BE58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4ef4660761ab29e738050c0445534602accda6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017396"
---
# <span data-ttu-id="86498-101">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="86498-101">Stop-WAPackVM</span></span>

## <span data-ttu-id="86498-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86498-102">SYNOPSIS</span></span>
<span data-ttu-id="86498-103">Virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="86498-103">Stops a virtual machine.</span></span>

## <span data-ttu-id="86498-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86498-104">SYNTAX</span></span>

```
Stop-WAPackVM [-Shutdown] -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86498-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86498-105">DESCRIPTION</span></span>
<span data-ttu-id="86498-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="86498-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="86498-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="86498-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="86498-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="86498-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="86498-109">A **stop-WAPackVM** parancsmag leállítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="86498-109">The **Stop-WAPackVM** cmdlet stops a virtual machine.</span></span>

## <span data-ttu-id="86498-110">Példák</span><span class="sxs-lookup"><span data-stu-id="86498-110">EXAMPLES</span></span>

### <span data-ttu-id="86498-111">Példa 1: virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="86498-111">Example 1: Stop a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Stop-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="86498-112">Az első parancs a **Get-WAPackVM** parancsmag használatával kapja meg a ContosoV126 nevű virtuális gépet, majd a $VirtualMachine változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="86498-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="86498-113">A második parancs leállítja a $VirtualMachineban tárolt virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="86498-113">The second command stops the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="86498-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86498-114">PARAMETERS</span></span>

### <span data-ttu-id="86498-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86498-115">-PassThru</span></span>
<span data-ttu-id="86498-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="86498-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="86498-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="86498-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="86498-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="86498-118">-Profile</span></span>
<span data-ttu-id="86498-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="86498-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86498-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="86498-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86498-121">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="86498-121">-Shutdown</span></span>
<span data-ttu-id="86498-122">Azt jelzi, hogy a parancsmag leállítja a virtuális gép operációs rendszerét.</span><span class="sxs-lookup"><span data-stu-id="86498-122">Indicates that the cmdlet shuts down the operating system of the virtual machine.</span></span>

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

### <span data-ttu-id="86498-123">-VM</span><span class="sxs-lookup"><span data-stu-id="86498-123">-VM</span></span>
<span data-ttu-id="86498-124">Virtuális gépet ad meg.</span><span class="sxs-lookup"><span data-stu-id="86498-124">Specifies a virtual machine.</span></span>
<span data-ttu-id="86498-125">Virtuális gép beszerzéséhez használja a **Get-WAPackVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="86498-125">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="86498-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86498-126">CommonParameters</span></span>
<span data-ttu-id="86498-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86498-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86498-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86498-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86498-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86498-129">INPUTS</span></span>

## <span data-ttu-id="86498-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86498-130">OUTPUTS</span></span>

## <span data-ttu-id="86498-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86498-131">NOTES</span></span>

## <span data-ttu-id="86498-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86498-132">RELATED LINKS</span></span>

[<span data-ttu-id="86498-133">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="86498-133">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="86498-134">Új – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="86498-134">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="86498-135">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="86498-135">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="86498-136">Újraindítás – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="86498-136">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="86498-137">Önéletrajz – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="86498-137">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="86498-138">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="86498-138">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="86498-139">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="86498-139">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="86498-140">Felfüggesztés – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="86498-140">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


