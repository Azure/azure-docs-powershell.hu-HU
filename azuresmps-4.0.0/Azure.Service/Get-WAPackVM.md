---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017356"
---
# <span data-ttu-id="bd8b6-101">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bd8b6-101">Get-WAPackVM</span></span>

## <span data-ttu-id="bd8b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd8b6-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8b6-103">Virtuális gép objektumait kapja.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-103">Gets virtual machine objects.</span></span>

## <span data-ttu-id="bd8b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd8b6-104">SYNTAX</span></span>

### <span data-ttu-id="bd8b6-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd8b6-105">Empty (Default)</span></span>
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bd8b6-106">FromName</span><span class="sxs-lookup"><span data-stu-id="bd8b6-106">FromName</span></span>
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bd8b6-107">FromId</span><span class="sxs-lookup"><span data-stu-id="bd8b6-107">FromId</span></span>
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bd8b6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd8b6-108">DESCRIPTION</span></span>
<span data-ttu-id="bd8b6-109">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="bd8b6-110">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bd8b6-111">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bd8b6-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bd8b6-112">A **Get-WAPackVM** parancsmag virtuális gép objektumait kapja.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-112">The **Get-WAPackVM** cmdlet gets virtual machine objects.</span></span>

## <span data-ttu-id="bd8b6-113">Példák</span><span class="sxs-lookup"><span data-stu-id="bd8b6-113">EXAMPLES</span></span>

### <span data-ttu-id="bd8b6-114">Példa 1: virtuális gép beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="bd8b6-114">Example 1: Get a virtual machine by using a name</span></span>
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

<span data-ttu-id="bd8b6-115">Ez a parancs a ContosoV126 nevű virtuális gépet kapja.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-115">This command gets the virtual machine named ContosoV126.</span></span>

### <span data-ttu-id="bd8b6-116">2. példa: virtuális gép beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="bd8b6-116">Example 2: Get a virtual machine by using an ID</span></span>
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="bd8b6-117">Ez a parancs a megadott azonosítót tartalmazó virtuális gépet kapja.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-117">This command gets the virtual machine that has the specified ID.</span></span>

### <span data-ttu-id="bd8b6-118">3. példa: az összes virtuális gép beszerzése</span><span class="sxs-lookup"><span data-stu-id="bd8b6-118">Example 3: Get all virtual machines</span></span>
```
PS C:\> Get-WAPackVM
```

<span data-ttu-id="bd8b6-119">Ez a parancs a virtuális gépeket kapja.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-119">This command gets all virtual machines.</span></span>

## <span data-ttu-id="bd8b6-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd8b6-120">PARAMETERS</span></span>

### <span data-ttu-id="bd8b6-121">-AZONOSÍTÓ</span><span class="sxs-lookup"><span data-stu-id="bd8b6-121">-ID</span></span>
<span data-ttu-id="bd8b6-122">A virtuális gép egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-122">Specifies the unique ID of a virtual machine.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8b6-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd8b6-123">-Name</span></span>
<span data-ttu-id="bd8b6-124">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-124">Specifies the name of a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8b6-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="bd8b6-125">-Profile</span></span>
<span data-ttu-id="bd8b6-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bd8b6-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="bd8b6-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bd8b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8b6-128">CommonParameters</span></span>
<span data-ttu-id="bd8b6-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd8b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8b6-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd8b6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8b6-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd8b6-131">INPUTS</span></span>

## <span data-ttu-id="bd8b6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd8b6-132">OUTPUTS</span></span>

## <span data-ttu-id="bd8b6-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd8b6-133">NOTES</span></span>

## <span data-ttu-id="bd8b6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd8b6-134">RELATED LINKS</span></span>

[<span data-ttu-id="bd8b6-135">Új – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bd8b6-135">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="bd8b6-136">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bd8b6-136">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="bd8b6-137">Újraindítás – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bd8b6-137">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="bd8b6-138">Önéletrajz – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bd8b6-138">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="bd8b6-139">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bd8b6-139">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="bd8b6-140">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bd8b6-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="bd8b6-141">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bd8b6-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="bd8b6-142">Felfüggesztés – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bd8b6-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="bd8b6-143">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="bd8b6-143">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


