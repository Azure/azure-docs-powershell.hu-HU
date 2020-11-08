---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 08A7556E-C07F-4B3B-B9D6-B241C72860FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b01ac318982b62499164cd54c9d9a51356ad9830
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017385"
---
# <span data-ttu-id="9b28c-101">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9b28c-101">Set-WAPackVM</span></span>

## <span data-ttu-id="9b28c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b28c-102">SYNOPSIS</span></span>
<span data-ttu-id="9b28c-103">Megváltoztatja a virtuális gép méretének tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="9b28c-103">Changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="9b28c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b28c-104">SYNTAX</span></span>

```
Set-WAPackVM -VM <VirtualMachine> -VMSizeProfile <HardwareProfile> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b28c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b28c-105">DESCRIPTION</span></span>
<span data-ttu-id="9b28c-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="9b28c-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9b28c-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="9b28c-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9b28c-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9b28c-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9b28c-109">A **set-WAPackVM** parancsmag egy virtuális gép méret tulajdonságát módosítja.</span><span class="sxs-lookup"><span data-stu-id="9b28c-109">The **Set-WAPackVM** cmdlet changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="9b28c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9b28c-110">EXAMPLES</span></span>

### <span data-ttu-id="9b28c-111">Példa 1: virtuális gép méretének megadása</span><span class="sxs-lookup"><span data-stu-id="9b28c-111">Example 1: Specify the size for a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> Set-WAPackVM -VM $VirtualMachine -VMSizeProfile $SizeProfile
```

<span data-ttu-id="9b28c-112">Az első parancs a **Get-WAPackVM** parancsmag használatával kapja meg a ContosoV126 nevű virtuális gépet, majd a $VirtualMachine változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="9b28c-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="9b28c-113">A második parancs a **Get-WAPackVMSizeProfile** parancsmaggal kapja meg a MediumSizeVM nevű méret profilt, majd az objektumot a $SizeProfile változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9b28c-113">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores that object in the $SizeProfile variable.</span></span>

<span data-ttu-id="9b28c-114">A végleges parancs a $VirtualMachine-ban tárolt virtuális gépnek a $SizeProfileban tárolt méret profilt rendeli hozzá.</span><span class="sxs-lookup"><span data-stu-id="9b28c-114">The final command assigns the size profile stored in $SizeProfile to the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="9b28c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b28c-115">PARAMETERS</span></span>

### <span data-ttu-id="9b28c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b28c-116">-PassThru</span></span>
<span data-ttu-id="9b28c-117">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9b28c-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9b28c-118">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9b28c-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9b28c-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="9b28c-119">-Profile</span></span>
<span data-ttu-id="9b28c-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9b28c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b28c-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9b28c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9b28c-122">-VM</span><span class="sxs-lookup"><span data-stu-id="9b28c-122">-VM</span></span>
<span data-ttu-id="9b28c-123">Virtuális gépet ad meg.</span><span class="sxs-lookup"><span data-stu-id="9b28c-123">Specifies a virtual machine.</span></span>
<span data-ttu-id="9b28c-124">Virtuális gép beszerzéséhez használja a **Get-WAPackVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9b28c-124">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="9b28c-125">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="9b28c-125">-VMSizeProfile</span></span>
<span data-ttu-id="9b28c-126">A virtuális gép **HardwareProfile** -objektumként használt méret profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b28c-126">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="9b28c-127">Ha szeretné beolvasni a méretet, használja a **Get-WAPackVMSizeProfile** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9b28c-127">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b28c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b28c-128">CommonParameters</span></span>
<span data-ttu-id="9b28c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b28c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b28c-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b28c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b28c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b28c-131">INPUTS</span></span>

## <span data-ttu-id="9b28c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b28c-132">OUTPUTS</span></span>

## <span data-ttu-id="9b28c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b28c-133">NOTES</span></span>

## <span data-ttu-id="9b28c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b28c-134">RELATED LINKS</span></span>

[<span data-ttu-id="9b28c-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9b28c-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="9b28c-136">Új – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9b28c-136">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="9b28c-137">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9b28c-137">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="9b28c-138">Újraindítás – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9b28c-138">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="9b28c-139">Önéletrajz – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9b28c-139">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="9b28c-140">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9b28c-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="9b28c-141">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9b28c-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="9b28c-142">Felfüggesztés – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9b28c-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="9b28c-143">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="9b28c-143">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)


