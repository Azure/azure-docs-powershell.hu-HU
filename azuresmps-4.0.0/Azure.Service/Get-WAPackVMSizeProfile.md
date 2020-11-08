---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017430"
---
# <span data-ttu-id="ec945-101">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="ec945-101">Get-WAPackVMSizeProfile</span></span>

## <span data-ttu-id="ec945-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec945-102">SYNOPSIS</span></span>
<span data-ttu-id="ec945-103">A profilba beilleszthető objektumok mérete.</span><span class="sxs-lookup"><span data-stu-id="ec945-103">Gets size profile objects.</span></span>

## <span data-ttu-id="ec945-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec945-104">SYNTAX</span></span>

### <span data-ttu-id="ec945-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec945-105">Empty (Default)</span></span>
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec945-106">FromId</span><span class="sxs-lookup"><span data-stu-id="ec945-106">FromId</span></span>
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec945-107">FromName</span><span class="sxs-lookup"><span data-stu-id="ec945-107">FromName</span></span>
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec945-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec945-108">DESCRIPTION</span></span>
<span data-ttu-id="ec945-109">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="ec945-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ec945-110">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="ec945-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ec945-111">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ec945-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ec945-112">A **Get-WAPackVMSizeProfile** parancsmag a virtuális gépek méretének profil objektumait kapja.</span><span class="sxs-lookup"><span data-stu-id="ec945-112">The **Get-WAPackVMSizeProfile** cmdlet gets size profile objects for virtual machines.</span></span>

## <span data-ttu-id="ec945-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ec945-113">EXAMPLES</span></span>

### <span data-ttu-id="ec945-114">Példa 1: méret-profil beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="ec945-114">Example 1: Get a size profile by using a name</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

<span data-ttu-id="ec945-115">Ez a parancs a ContosoSizeProfile07 nevű méret profilt kapja.</span><span class="sxs-lookup"><span data-stu-id="ec945-115">This command gets the size profile named ContosoSizeProfile07.</span></span>

### <span data-ttu-id="ec945-116">2. példa: adatméreti profil beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="ec945-116">Example 2: Get a size profile by using an ID</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="ec945-117">Ez a parancs a megadott azonosítót tartalmazó méretű profilt kapja.</span><span class="sxs-lookup"><span data-stu-id="ec945-117">This command gets the size profile that has the specified ID.</span></span>

### <span data-ttu-id="ec945-118">3. példa: az összes méret-profil beolvasása</span><span class="sxs-lookup"><span data-stu-id="ec945-118">Example 3: Get all size profiles</span></span>
```
PS C:\> Get-WAPackVMSizeProfile
```

<span data-ttu-id="ec945-119">Ez a parancs a teljes méretű profilokat kapja.</span><span class="sxs-lookup"><span data-stu-id="ec945-119">This command gets all the size profiles.</span></span>

## <span data-ttu-id="ec945-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec945-120">PARAMETERS</span></span>

### <span data-ttu-id="ec945-121">-AZONOSÍTÓ</span><span class="sxs-lookup"><span data-stu-id="ec945-121">-ID</span></span>
<span data-ttu-id="ec945-122">A méret profil egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec945-122">Specifies the unique ID of a size profile.</span></span>

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

### <span data-ttu-id="ec945-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec945-123">-Name</span></span>
<span data-ttu-id="ec945-124">A méret profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec945-124">Specifies the name of a size profile.</span></span>

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

### <span data-ttu-id="ec945-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="ec945-125">-Profile</span></span>
<span data-ttu-id="ec945-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ec945-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec945-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ec945-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec945-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec945-128">CommonParameters</span></span>
<span data-ttu-id="ec945-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec945-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec945-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec945-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec945-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec945-131">INPUTS</span></span>

## <span data-ttu-id="ec945-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec945-132">OUTPUTS</span></span>

## <span data-ttu-id="ec945-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec945-133">NOTES</span></span>

## <span data-ttu-id="ec945-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec945-134">RELATED LINKS</span></span>

[<span data-ttu-id="ec945-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ec945-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


