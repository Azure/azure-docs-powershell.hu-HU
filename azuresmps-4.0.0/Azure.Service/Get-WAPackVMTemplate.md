---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017391"
---
# <span data-ttu-id="b1930-101">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="b1930-101">Get-WAPackVMTemplate</span></span>

## <span data-ttu-id="b1930-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1930-102">SYNOPSIS</span></span>
<span data-ttu-id="b1930-103">Virtuális gépi sablonokba kerül.</span><span class="sxs-lookup"><span data-stu-id="b1930-103">Gets virtual machine templates.</span></span>

## <span data-ttu-id="b1930-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1930-104">SYNTAX</span></span>

### <span data-ttu-id="b1930-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1930-105">Empty (Default)</span></span>
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b1930-106">FromId</span><span class="sxs-lookup"><span data-stu-id="b1930-106">FromId</span></span>
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b1930-107">FromName</span><span class="sxs-lookup"><span data-stu-id="b1930-107">FromName</span></span>
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b1930-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1930-108">DESCRIPTION</span></span>
<span data-ttu-id="b1930-109">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="b1930-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="b1930-110">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="b1930-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b1930-111">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b1930-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b1930-112">A **Get-WAPackVMTemplate** parancsmag virtuális Machine-sablonokat kap.</span><span class="sxs-lookup"><span data-stu-id="b1930-112">The **Get-WAPackVMTemplate** cmdlet gets virtual machine templates.</span></span>

## <span data-ttu-id="b1930-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b1930-113">EXAMPLES</span></span>

### <span data-ttu-id="b1930-114">Példa 1: virtuális gép sablonjának beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="b1930-114">Example 1: Get a virtual machine template by using a name</span></span>
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

<span data-ttu-id="b1930-115">Ez a parancs a ContosoTemplate04 nevű virtuálisgép-sablont kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b1930-115">This command gets the virtual machine template named ContosoTemplate04.</span></span>

### <span data-ttu-id="b1930-116">2. példa: virtuális gép sablonjának beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="b1930-116">Example 2: Get a virtual machine template by using an ID</span></span>
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="b1930-117">Ez a parancs a megadott azonosítót tartalmazó virtuális gép sablonját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b1930-117">This command gets the virtual machine template that has the specified ID.</span></span>

### <span data-ttu-id="b1930-118">3. példa: az összes virtuálisgép-sablon beszerzése</span><span class="sxs-lookup"><span data-stu-id="b1930-118">Example 3: Get all virtual machine templates</span></span>
```
PS C:\> Get-WAPackVMTemplate
```

<span data-ttu-id="b1930-119">Ez a parancs a virtuális gép összes sablonját bekapja.</span><span class="sxs-lookup"><span data-stu-id="b1930-119">This command gets all the virtual machine templates.</span></span>

## <span data-ttu-id="b1930-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1930-120">PARAMETERS</span></span>

### <span data-ttu-id="b1930-121">-AZONOSÍTÓ</span><span class="sxs-lookup"><span data-stu-id="b1930-121">-ID</span></span>
<span data-ttu-id="b1930-122">A sablon egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1930-122">Specifies the unique ID of a template.</span></span>

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

### <span data-ttu-id="b1930-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1930-123">-Name</span></span>
<span data-ttu-id="b1930-124">A sablon nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1930-124">Specifies the name of a template.</span></span>

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

### <span data-ttu-id="b1930-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="b1930-125">-Profile</span></span>
<span data-ttu-id="b1930-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b1930-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1930-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b1930-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1930-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1930-128">CommonParameters</span></span>
<span data-ttu-id="b1930-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1930-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1930-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1930-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1930-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1930-131">INPUTS</span></span>

## <span data-ttu-id="b1930-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1930-132">OUTPUTS</span></span>

## <span data-ttu-id="b1930-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1930-133">NOTES</span></span>

## <span data-ttu-id="b1930-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1930-134">RELATED LINKS</span></span>

[<span data-ttu-id="b1930-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="b1930-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


