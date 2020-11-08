---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017406"
---
# <span data-ttu-id="6a226-101">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="6a226-101">Remove-WAPackVNet</span></span>

## <span data-ttu-id="6a226-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a226-102">SYNOPSIS</span></span>
<span data-ttu-id="6a226-103">Eltávolítja a virtuális hálózati objektumokat.</span><span class="sxs-lookup"><span data-stu-id="6a226-103">Removes virtual network objects.</span></span>

## <span data-ttu-id="6a226-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a226-104">SYNTAX</span></span>

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6a226-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a226-105">DESCRIPTION</span></span>
<span data-ttu-id="6a226-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="6a226-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="6a226-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="6a226-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6a226-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6a226-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6a226-109">A **Remove-WAPackVNet** parancsmag eltávolítja a virtuális hálózati objektumokat.</span><span class="sxs-lookup"><span data-stu-id="6a226-109">The **Remove-WAPackVNet** cmdlet removes virtual network objects.</span></span>

## <span data-ttu-id="6a226-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6a226-110">EXAMPLES</span></span>

### <span data-ttu-id="6a226-111">1. példa: virtualizált hálózat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6a226-111">Example 1: Remove a virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

<span data-ttu-id="6a226-112">Az első parancs a **Get-WAPackVNet** parancsmaggal kapja meg a ContosoVNet01 nevű virtuális hálózatot, majd a $VNet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="6a226-112">The first command gets the virtualized network named ContosoVNet01 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="6a226-113">A második parancs eltávolítja a $VNet-ban tárolt virtualizált hálózatot.</span><span class="sxs-lookup"><span data-stu-id="6a226-113">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="6a226-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="6a226-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="6a226-115">2. példa: virtualizált hálózat eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="6a226-115">Example 2: Remove a virtualized network without confirmation</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

<span data-ttu-id="6a226-116">Az első parancs a **Get-WAPackVNet** parancsmaggal kapja meg a ContosoVNet02 nevű felhőalapú szolgáltatást, majd a $VNet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="6a226-116">The first command gets the cloud service named ContosoVNet02 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="6a226-117">A második parancs eltávolítja a $VNet-ban tárolt virtualizált hálózatot.</span><span class="sxs-lookup"><span data-stu-id="6a226-117">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="6a226-118">Ez a parancs az *erő* paramétert tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6a226-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="6a226-119">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a226-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6a226-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a226-120">PARAMETERS</span></span>

### <span data-ttu-id="6a226-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6a226-121">-Force</span></span>
<span data-ttu-id="6a226-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6a226-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a226-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a226-123">-PassThru</span></span>
<span data-ttu-id="6a226-124">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6a226-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6a226-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6a226-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a226-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="6a226-126">-Profile</span></span>
<span data-ttu-id="6a226-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6a226-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6a226-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6a226-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a226-129">-VNet</span><span class="sxs-lookup"><span data-stu-id="6a226-129">-VNet</span></span>
<span data-ttu-id="6a226-130">Virtualizált hálózatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6a226-130">Specifies a virtualized network.</span></span>
<span data-ttu-id="6a226-131">Virtualizált hálózat beszerzéséhez használja a **Get-WAPackVNet** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6a226-131">To obtain a virtualized network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a226-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a226-132">CommonParameters</span></span>
<span data-ttu-id="6a226-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a226-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a226-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a226-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a226-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a226-135">INPUTS</span></span>

## <span data-ttu-id="6a226-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a226-136">OUTPUTS</span></span>

## <span data-ttu-id="6a226-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a226-137">NOTES</span></span>

## <span data-ttu-id="6a226-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a226-138">RELATED LINKS</span></span>

[<span data-ttu-id="6a226-139">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="6a226-139">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="6a226-140">Új – WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="6a226-140">New-WAPackVNet</span></span>](./New-WAPackVNet.md)


