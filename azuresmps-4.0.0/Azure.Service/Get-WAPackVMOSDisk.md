---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017352"
---
# <span data-ttu-id="87275-101">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="87275-101">Get-WAPackVMOSDisk</span></span>

## <span data-ttu-id="87275-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87275-102">SYNOPSIS</span></span>
<span data-ttu-id="87275-103">A virtuális gépekhez az operációs rendszer Disk objektumait kapja.</span><span class="sxs-lookup"><span data-stu-id="87275-103">Gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="87275-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87275-104">SYNTAX</span></span>

### <span data-ttu-id="87275-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87275-105">Empty (Default)</span></span>
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="87275-106">FromId</span><span class="sxs-lookup"><span data-stu-id="87275-106">FromId</span></span>
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="87275-107">FromName</span><span class="sxs-lookup"><span data-stu-id="87275-107">FromName</span></span>
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="87275-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="87275-108">DESCRIPTION</span></span>
<span data-ttu-id="87275-109">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="87275-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="87275-110">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="87275-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="87275-111">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="87275-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="87275-112">A **Get-WAPackVMOSDisk** parancsmag a virtuális gépek operációs rendszerbeli merevlemez-objektumait kapja.</span><span class="sxs-lookup"><span data-stu-id="87275-112">The **Get-WAPackVMOSDisk** cmdlet gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="87275-113">Példák</span><span class="sxs-lookup"><span data-stu-id="87275-113">EXAMPLES</span></span>

### <span data-ttu-id="87275-114">1. példa: operációs rendszer lemezének beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="87275-114">Example 1: Get an operating system disk by using a name</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

<span data-ttu-id="87275-115">Ez a parancs a ContosoOSDisk nevű operációs rendszer lemezét kapja.</span><span class="sxs-lookup"><span data-stu-id="87275-115">This command gets an operating system disk named ContosoOSDisk.</span></span>

### <span data-ttu-id="87275-116">2. példa: operációs rendszer lemezének beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="87275-116">Example 2: Get an operating system disk by using an ID</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="87275-117">Ez a parancs a megadott azonosítót tartalmazó operációs rendszer lemezét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="87275-117">This command gets the operating system disk that has the specified ID.</span></span>

### <span data-ttu-id="87275-118">3. példa: az összes operációs rendszer lemezének beszerzése</span><span class="sxs-lookup"><span data-stu-id="87275-118">Example 3: Get all operating system disks</span></span>
```
PS C:\> Get-WAPackVMOSDisk
```

<span data-ttu-id="87275-119">Ez a parancs az operációs rendszer összes lemezét bekapja.</span><span class="sxs-lookup"><span data-stu-id="87275-119">This command gets all operating system disks.</span></span>

## <span data-ttu-id="87275-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87275-120">PARAMETERS</span></span>

### <span data-ttu-id="87275-121">-AZONOSÍTÓ</span><span class="sxs-lookup"><span data-stu-id="87275-121">-ID</span></span>
<span data-ttu-id="87275-122">Az operációs rendszer lemezének egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="87275-122">Specifies the unique ID of an operating system disk.</span></span>

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

### <span data-ttu-id="87275-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87275-123">-Name</span></span>
<span data-ttu-id="87275-124">Egy operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87275-124">Specifies the name of an operating system disk.</span></span>

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

### <span data-ttu-id="87275-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="87275-125">-Profile</span></span>
<span data-ttu-id="87275-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="87275-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87275-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="87275-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87275-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87275-128">CommonParameters</span></span>
<span data-ttu-id="87275-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87275-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87275-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87275-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87275-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87275-131">INPUTS</span></span>

## <span data-ttu-id="87275-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87275-132">OUTPUTS</span></span>

## <span data-ttu-id="87275-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87275-133">NOTES</span></span>

## <span data-ttu-id="87275-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87275-134">RELATED LINKS</span></span>

[<span data-ttu-id="87275-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="87275-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


