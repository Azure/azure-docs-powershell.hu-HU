---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017400"
---
# <span data-ttu-id="1f510-101">New-WAPackQuickVM</span><span class="sxs-lookup"><span data-stu-id="1f510-101">New-WAPackQuickVM</span></span>

## <span data-ttu-id="1f510-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f510-102">SYNOPSIS</span></span>
<span data-ttu-id="1f510-103">Virtuális gépet hoz létre sablon alapján.</span><span class="sxs-lookup"><span data-stu-id="1f510-103">Creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="1f510-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f510-104">SYNTAX</span></span>

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1f510-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f510-105">DESCRIPTION</span></span>
<span data-ttu-id="1f510-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="1f510-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="1f510-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="1f510-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1f510-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1f510-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1f510-109">A **New-WAPackQuickVM** parancsmag a virtuális gépet sablon alapján hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1f510-109">The **New-WAPackQuickVM** cmdlet creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="1f510-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1f510-110">EXAMPLES</span></span>

### <span data-ttu-id="1f510-111">Példa 1: virtuális gép létrehozása sablon alapján</span><span class="sxs-lookup"><span data-stu-id="1f510-111">Example 1: Create a virtual machine based on a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

<span data-ttu-id="1f510-112">Az első parancs létrehozza a **PSCredential** objektumot, majd a $credentials változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1f510-112">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="1f510-113">A parancsmag a fiók és a jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="1f510-113">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="1f510-114">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1f510-114">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="1f510-115">A második parancs a **Get-WAPackVMTemplate** parancsmag segítségével kap sablont.</span><span class="sxs-lookup"><span data-stu-id="1f510-115">The second command gets a template by using the **Get-WAPackVMTemplate** cmdlet.</span></span>
<span data-ttu-id="1f510-116">A parancs a sablon AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f510-116">The command specifies the ID of a template.</span></span>
<span data-ttu-id="1f510-117">A parancs a Template objektumot a $TemplateID változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1f510-117">The command stores the template object in the $TemplateID variable.</span></span>

<span data-ttu-id="1f510-118">A végleges parancs egy VirtualMachine023 nevű virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1f510-118">The final command creates a virtual machine named VirtualMachine023.</span></span>
<span data-ttu-id="1f510-119">A parancs a virtuális gépet az $TemplateId tárolt sablonon alapozza meg.</span><span class="sxs-lookup"><span data-stu-id="1f510-119">The command bases the virtual machine on the template stored in $TemplateId.</span></span>

## <span data-ttu-id="1f510-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f510-120">PARAMETERS</span></span>

### <span data-ttu-id="1f510-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f510-121">-Name</span></span>
<span data-ttu-id="1f510-122">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f510-122">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f510-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="1f510-123">-Profile</span></span>
<span data-ttu-id="1f510-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1f510-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1f510-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1f510-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1f510-126">-Sablon</span><span class="sxs-lookup"><span data-stu-id="1f510-126">-Template</span></span>
<span data-ttu-id="1f510-127">Egy sablont ad meg.</span><span class="sxs-lookup"><span data-stu-id="1f510-127">Specifies a template.</span></span>
<span data-ttu-id="1f510-128">A parancsmag a megadott sablonon alapuló virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1f510-128">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="1f510-129">Sablon objektum beszerzéséhez használja a **Get-WAPackVMTemplate** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1f510-129">To obtain a template object, use the **Get-WAPackVMTemplate** cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f510-130">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="1f510-130">-VMCredential</span></span>
<span data-ttu-id="1f510-131">A helyi rendszergazdai fiók hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f510-131">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="1f510-132">Ha **PSCredential** objektumot szeretne beolvasni, használja a **Get-hitelesítőadat** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1f510-132">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="1f510-133">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1f510-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f510-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f510-134">CommonParameters</span></span>
<span data-ttu-id="1f510-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f510-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f510-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f510-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f510-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f510-137">INPUTS</span></span>

## <span data-ttu-id="1f510-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f510-138">OUTPUTS</span></span>

## <span data-ttu-id="1f510-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f510-139">NOTES</span></span>

## <span data-ttu-id="1f510-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f510-140">RELATED LINKS</span></span>

[<span data-ttu-id="1f510-141">Új – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1f510-141">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="1f510-142">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="1f510-142">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)


