---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1ECF6BB5-3751-4DA0-AC6C-A64F15F46D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552c2511a806abb4329860e7c15d8a68b5e03f79
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017413"
---
# <span data-ttu-id="139b5-101">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="139b5-101">Remove-WAPackCloudService</span></span>

## <span data-ttu-id="139b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="139b5-102">SYNOPSIS</span></span>
<span data-ttu-id="139b5-103">Eltávolítja a Felhőbeli szolgáltatások objektumait.</span><span class="sxs-lookup"><span data-stu-id="139b5-103">Removes cloud service objects.</span></span>

## <span data-ttu-id="139b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="139b5-104">SYNTAX</span></span>

```
Remove-WAPackCloudService -CloudService <CloudService> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="139b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="139b5-105">DESCRIPTION</span></span>
<span data-ttu-id="139b5-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="139b5-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="139b5-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="139b5-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="139b5-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="139b5-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="139b5-109">A **Remove-WAPackCloudService** parancsmag eltávolítja a felhőalapú szolgáltatás objektumait.</span><span class="sxs-lookup"><span data-stu-id="139b5-109">The **Remove-WAPackCloudService** cmdlet removes cloud service objects.</span></span>

## <span data-ttu-id="139b5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="139b5-110">EXAMPLES</span></span>

### <span data-ttu-id="139b5-111">1. példa: Felhőbeli szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="139b5-111">Example 1: Remove a cloud service</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService01"
PS C:\> Remove-WAPackVM -VM $CloudService
```

<span data-ttu-id="139b5-112">Az első parancs a **Get-WAPackCloudService** parancsmaggal kapja meg a ContosoCloudService01 nevű felhőalapú szolgáltatást, majd a $CloudService változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="139b5-112">The first command gets the cloud service named ContosoCloudService01 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="139b5-113">A második parancs eltávolítja a $CloudService-ban tárolt cloudservice.</span><span class="sxs-lookup"><span data-stu-id="139b5-113">The second command removes the cloudservice stored in $CloudService.</span></span>
<span data-ttu-id="139b5-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="139b5-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="139b5-115">2. példa: felhőalapú szolgáltatás eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="139b5-115">Example 2: Remove a cloud service without confirmation</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService02"
PS C:\> Remove-WAPackCloudService -VM $CloudService -Force
```

<span data-ttu-id="139b5-116">Az első parancs a **Get-WAPackCloudService** parancsmaggal kapja meg a ContosoCloudService02 nevű felhőalapú szolgáltatást, majd a $CloudService változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="139b5-116">The first command gets the cloud service named ContosoCloudService02 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="139b5-117">A második parancs eltávolítja a $CloudServiceban tárolt felhőalapú szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="139b5-117">The second command removes the cloud service stored in $CloudService.</span></span>
<span data-ttu-id="139b5-118">Ez a parancs az *erő* paramétert tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="139b5-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="139b5-119">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="139b5-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="139b5-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="139b5-120">PARAMETERS</span></span>

### <span data-ttu-id="139b5-121">-CloudService</span><span class="sxs-lookup"><span data-stu-id="139b5-121">-CloudService</span></span>
<span data-ttu-id="139b5-122">Egy felhőalapú szolgáltatás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="139b5-122">Specifies a cloud service object.</span></span>
<span data-ttu-id="139b5-123">Felhőalapú szolgáltatás beszerzéséhez használja a **Get-WAPackCloudService** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="139b5-123">To obtain a cloud service, use the **Get-WAPackCloudService** cmdlet.</span></span>

```yaml
Type: CloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="139b5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="139b5-124">-Force</span></span>
<span data-ttu-id="139b5-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="139b5-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="139b5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="139b5-126">-PassThru</span></span>
<span data-ttu-id="139b5-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="139b5-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="139b5-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="139b5-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="139b5-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="139b5-129">-Profile</span></span>
<span data-ttu-id="139b5-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="139b5-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="139b5-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="139b5-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="139b5-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="139b5-132">-Confirm</span></span>
<span data-ttu-id="139b5-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="139b5-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139b5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="139b5-134">-WhatIf</span></span>
<span data-ttu-id="139b5-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="139b5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="139b5-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="139b5-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139b5-137">CommonParameters</span></span>
<span data-ttu-id="139b5-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="139b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139b5-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="139b5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139b5-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="139b5-140">INPUTS</span></span>

## <span data-ttu-id="139b5-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="139b5-141">OUTPUTS</span></span>

## <span data-ttu-id="139b5-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="139b5-142">NOTES</span></span>

## <span data-ttu-id="139b5-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="139b5-143">RELATED LINKS</span></span>

[<span data-ttu-id="139b5-144">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="139b5-144">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="139b5-145">Új – WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="139b5-145">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)


