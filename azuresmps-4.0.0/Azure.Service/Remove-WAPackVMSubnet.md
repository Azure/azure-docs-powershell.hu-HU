---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017407"
---
# <span data-ttu-id="9f1fa-101">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="9f1fa-101">Remove-WAPackVMSubnet</span></span>

## <span data-ttu-id="9f1fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f1fa-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1fa-103">Eltávolítja a virtuális gép alhálózati objektumait.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-103">Removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="9f1fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f1fa-104">SYNTAX</span></span>

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f1fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f1fa-105">DESCRIPTION</span></span>
<span data-ttu-id="9f1fa-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9f1fa-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9f1fa-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9f1fa-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9f1fa-109">A **Remove-WAPackVMSubnet** parancsmag eltávolítja a virtuális gép alhálózati objektumait.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-109">The **Remove-WAPackVMSubnet** cmdlet removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="9f1fa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9f1fa-110">EXAMPLES</span></span>

### <span data-ttu-id="9f1fa-111">Példa 1: virtuális gép alhálózatának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9f1fa-111">Example 1: Remove a virtual machine subnet</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

<span data-ttu-id="9f1fa-112">Az első parancs a **Get-WAPackVMSubnet** parancsmag használatával kapja meg a ContosoVMSubnet01 nevű virtuális gép alhálózatát, majd az $VMSubnet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-112">The first command gets the virtual machine subnet named ContosoVMSubnet01 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="9f1fa-113">A második parancs eltávolítja a $VMSubnetban tárolt virtuális gép alhálózatát.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-113">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="9f1fa-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="9f1fa-115">2. példa: a virtuális gép eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="9f1fa-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

<span data-ttu-id="9f1fa-116">Az első parancs a **Get-WAPackVMSubnet** parancsmaggal kapja meg a ContosoVMSubnet02 nevű felhőalapú szolgáltatást, majd a $VMSubnet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-116">The first command gets the cloud service named ContosoVMSubnet02 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="9f1fa-117">A második parancs eltávolítja a $VMSubnetban tárolt virtuális gép alhálózatát.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-117">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="9f1fa-118">Ez a parancs az *erő* paramétert tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="9f1fa-119">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9f1fa-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f1fa-120">PARAMETERS</span></span>

### <span data-ttu-id="9f1fa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9f1fa-121">-Force</span></span>
<span data-ttu-id="9f1fa-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f1fa-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f1fa-123">-PassThru</span></span>
<span data-ttu-id="9f1fa-124">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9f1fa-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9f1fa-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="9f1fa-126">-Profile</span></span>
<span data-ttu-id="9f1fa-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9f1fa-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9f1fa-129">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="9f1fa-129">-VMSubnet</span></span>
<span data-ttu-id="9f1fa-130">Egy virtuális gép alhálózatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-130">Specifies a virtual machine subnet.</span></span>
<span data-ttu-id="9f1fa-131">Virtuális gép alhálózatának beszerzéséhez használja a **Get-WAPackVMSubnet** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-131">To obtain a virtual machine subnet, use the **Get-WAPackVMSubnet** cmdlet.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1fa-132">CommonParameters</span></span>
<span data-ttu-id="9f1fa-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f1fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1fa-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f1fa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1fa-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f1fa-135">INPUTS</span></span>

## <span data-ttu-id="9f1fa-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f1fa-136">OUTPUTS</span></span>

## <span data-ttu-id="9f1fa-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f1fa-137">NOTES</span></span>

## <span data-ttu-id="9f1fa-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f1fa-138">RELATED LINKS</span></span>

[<span data-ttu-id="9f1fa-139">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="9f1fa-139">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="9f1fa-140">Új – WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="9f1fa-140">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)


