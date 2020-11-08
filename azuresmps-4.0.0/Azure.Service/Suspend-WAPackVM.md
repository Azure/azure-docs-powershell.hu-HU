---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: ABF5B4EB-0908-4103-B0BF-69A68A21D69C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 296a37d00c97bc3af849886593e09a1a0a9ff863
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017367"
---
# <span data-ttu-id="284b4-101">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="284b4-101">Suspend-WAPackVM</span></span>

## <span data-ttu-id="284b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="284b4-102">SYNOPSIS</span></span>
<span data-ttu-id="284b4-103">Virtuális gép felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="284b4-103">Suspends a virtual machine.</span></span>

## <span data-ttu-id="284b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="284b4-104">SYNTAX</span></span>

```
Suspend-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="284b4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="284b4-105">DESCRIPTION</span></span>
<span data-ttu-id="284b4-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="284b4-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="284b4-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="284b4-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="284b4-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="284b4-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="284b4-109">A **felfüggesztés – WAPackVM** parancsmag felfüggeszti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="284b4-109">The **Suspend-WAPackVM** cmdlet suspends a virtual machine.</span></span>

## <span data-ttu-id="284b4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="284b4-110">EXAMPLES</span></span>

### <span data-ttu-id="284b4-111">1. példa: virtuális gép felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="284b4-111">Example 1: Suspend a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Suspend-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="284b4-112">Az első parancs a **Get-WAPackVM** parancsmag használatával kapja meg a ContosoV126 nevű virtuális gépet, majd a $VirtualMachine változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="284b4-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="284b4-113">A második parancs felfüggeszti a $VirtualMachine-ban tárolt virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="284b4-113">The second command suspends the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="284b4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="284b4-114">PARAMETERS</span></span>

### <span data-ttu-id="284b4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="284b4-115">-PassThru</span></span>
<span data-ttu-id="284b4-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="284b4-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="284b4-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="284b4-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="284b4-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="284b4-118">-Profile</span></span>
<span data-ttu-id="284b4-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="284b4-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="284b4-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="284b4-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="284b4-121">-VM</span><span class="sxs-lookup"><span data-stu-id="284b4-121">-VM</span></span>
<span data-ttu-id="284b4-122">Virtuális gépet ad meg.</span><span class="sxs-lookup"><span data-stu-id="284b4-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="284b4-123">Virtuális gép beszerzéséhez használja a **Get-WAPackVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="284b4-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="284b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="284b4-124">CommonParameters</span></span>
<span data-ttu-id="284b4-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="284b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="284b4-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="284b4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="284b4-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="284b4-127">INPUTS</span></span>

## <span data-ttu-id="284b4-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="284b4-128">OUTPUTS</span></span>

## <span data-ttu-id="284b4-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="284b4-129">NOTES</span></span>

## <span data-ttu-id="284b4-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="284b4-130">RELATED LINKS</span></span>

[<span data-ttu-id="284b4-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="284b4-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="284b4-132">Új – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="284b4-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="284b4-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="284b4-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="284b4-134">Újraindítás – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="284b4-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="284b4-135">Önéletrajz – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="284b4-135">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="284b4-136">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="284b4-136">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="284b4-137">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="284b4-137">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="284b4-138">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="284b4-138">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)


