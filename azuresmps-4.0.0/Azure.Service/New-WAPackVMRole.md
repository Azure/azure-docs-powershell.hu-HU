---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017390"
---
# <span data-ttu-id="80a66-101">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="80a66-101">New-WAPackVMRole</span></span>

## <span data-ttu-id="80a66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80a66-102">SYNOPSIS</span></span>
<span data-ttu-id="80a66-103">Virtuális gép szerepkört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="80a66-103">Creates a virtual machine role.</span></span>

## <span data-ttu-id="80a66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80a66-104">SYNTAX</span></span>

### <span data-ttu-id="80a66-105">QuickCreate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80a66-105">QuickCreate (Default)</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="80a66-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="80a66-106">FromCloudService</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="80a66-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="80a66-107">DESCRIPTION</span></span>
<span data-ttu-id="80a66-108">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="80a66-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="80a66-109">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="80a66-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="80a66-110">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="80a66-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="80a66-111">A **New-WAPackVMRole** parancsmag virtuális gép szerepkört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="80a66-111">The **New-WAPackVMRole** cmdlet creates a virtual machine role.</span></span>

## <span data-ttu-id="80a66-112">Példák</span><span class="sxs-lookup"><span data-stu-id="80a66-112">EXAMPLES</span></span>

### <span data-ttu-id="80a66-113">Példa 1: virtuális gép szerepkör létrehozása (a WAP viselkedésének emulálása)</span><span class="sxs-lookup"><span data-stu-id="80a66-113">Example 1: Create a virtual machine role (emulating WAP behavior)</span></span>
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

<span data-ttu-id="80a66-114">Mivel nem adunk meg semmilyen felhőalapú szolgáltatást (emulálni a WAP működését), a parancs létrehoz egy felhőalapú szolgáltatást, amely a virtuális gép szerepkör nevével megegyező nevet ad.</span><span class="sxs-lookup"><span data-stu-id="80a66-114">Since we do not specify any cloud service (emulating WAP behavior), the command will create a cloud service for us which will have the same name as the virtual machine role.</span></span>
<span data-ttu-id="80a66-115">Ebben az esetben az alábbi parancs egy virtuális gép szerepkört hoz létre a ContosoVMRole01 név, címke ContosoVMRoleLabel01.</span><span class="sxs-lookup"><span data-stu-id="80a66-115">In this case, the following command will create a virtual machine role with the name ContosoVMRole01, label ContosoVMRoleLabel01.</span></span>
<span data-ttu-id="80a66-116">Figyelje meg, hogy az itt használt erőforrás-definíciót manuálisan kell létrehozni, bár PowerShell.</span><span class="sxs-lookup"><span data-stu-id="80a66-116">Note that the resource definition being used here has to be manually created though PowerShell.</span></span>

## <span data-ttu-id="80a66-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80a66-117">PARAMETERS</span></span>

### <span data-ttu-id="80a66-118">-CloudService</span><span class="sxs-lookup"><span data-stu-id="80a66-118">-CloudService</span></span>
<span data-ttu-id="80a66-119">A virtuális gép szerepkör felhőalapú szolgáltatását adja meg.</span><span class="sxs-lookup"><span data-stu-id="80a66-119">Specifies a cloud service for the virtual machine role.</span></span>

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a66-120">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="80a66-120">-Label</span></span>
<span data-ttu-id="80a66-121">A virtuális gép szerepkör címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80a66-121">Specifies a label for the virtual machine role.</span></span>

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

### <span data-ttu-id="80a66-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="80a66-122">-Name</span></span>
<span data-ttu-id="80a66-123">A virtuális gép szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80a66-123">Specifies a name for the virtual machine role.</span></span>

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

### <span data-ttu-id="80a66-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="80a66-124">-Profile</span></span>
<span data-ttu-id="80a66-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="80a66-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80a66-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="80a66-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80a66-127">-ResourceDefinition</span><span class="sxs-lookup"><span data-stu-id="80a66-127">-ResourceDefinition</span></span>
<span data-ttu-id="80a66-128">A virtuális gép szerepkör erőforrás-definícióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="80a66-128">Specifies a resource definition for the virtual machine role.</span></span>

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a66-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a66-129">CommonParameters</span></span>
<span data-ttu-id="80a66-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80a66-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a66-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a66-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a66-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80a66-132">INPUTS</span></span>

## <span data-ttu-id="80a66-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80a66-133">OUTPUTS</span></span>

## <span data-ttu-id="80a66-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80a66-134">NOTES</span></span>

## <span data-ttu-id="80a66-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80a66-135">RELATED LINKS</span></span>

[<span data-ttu-id="80a66-136">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="80a66-136">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="80a66-137">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="80a66-137">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="80a66-138">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="80a66-138">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


