---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8A6B4C8C-B990-443B-9157-B5C35824269A
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2d87c92f18c3aeb25aad210922dea0c93287fa6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017424"
---
# <span data-ttu-id="ae683-101">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ae683-101">Start-WAPackVM</span></span>

## <span data-ttu-id="ae683-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae683-102">SYNOPSIS</span></span>
<span data-ttu-id="ae683-103">Elindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="ae683-103">Starts a virtual machine.</span></span>

## <span data-ttu-id="ae683-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae683-104">SYNTAX</span></span>

```
Start-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae683-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae683-105">DESCRIPTION</span></span>
<span data-ttu-id="ae683-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="ae683-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ae683-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="ae683-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ae683-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ae683-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ae683-109">A **Start-WAPackVM** parancsmag egy virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="ae683-109">The **Start-WAPackVM** cmdlet starts a virtual machine.</span></span>

## <span data-ttu-id="ae683-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ae683-110">EXAMPLES</span></span>

### <span data-ttu-id="ae683-111">Példa 1: virtuális gép indítása</span><span class="sxs-lookup"><span data-stu-id="ae683-111">Example 1: Start a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Start-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="ae683-112">Az első parancs a **Get-WAPackVM** parancsmag használatával kapja meg a ContosoV126 nevű virtuális gépet, majd a $VirtualMachine változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="ae683-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="ae683-113">A második parancs elindítja a $VirtualMachineban tárolt virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="ae683-113">The second command starts the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="ae683-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae683-114">PARAMETERS</span></span>

### <span data-ttu-id="ae683-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae683-115">-PassThru</span></span>
<span data-ttu-id="ae683-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ae683-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ae683-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ae683-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae683-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="ae683-118">-Profile</span></span>
<span data-ttu-id="ae683-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ae683-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae683-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ae683-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae683-121">-VM</span><span class="sxs-lookup"><span data-stu-id="ae683-121">-VM</span></span>
<span data-ttu-id="ae683-122">Virtuális gépet ad meg.</span><span class="sxs-lookup"><span data-stu-id="ae683-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="ae683-123">Virtuális gép beszerzéséhez használja a **Get-WAPackVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ae683-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="ae683-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae683-124">CommonParameters</span></span>
<span data-ttu-id="ae683-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae683-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae683-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae683-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae683-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae683-127">INPUTS</span></span>

## <span data-ttu-id="ae683-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae683-128">OUTPUTS</span></span>

## <span data-ttu-id="ae683-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae683-129">NOTES</span></span>

## <span data-ttu-id="ae683-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae683-130">RELATED LINKS</span></span>

[<span data-ttu-id="ae683-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ae683-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="ae683-132">Új – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ae683-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="ae683-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ae683-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="ae683-134">Újraindítás – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ae683-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="ae683-135">Önéletrajz – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ae683-135">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="ae683-136">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ae683-136">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="ae683-137">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ae683-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="ae683-138">Felfüggesztés – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ae683-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


