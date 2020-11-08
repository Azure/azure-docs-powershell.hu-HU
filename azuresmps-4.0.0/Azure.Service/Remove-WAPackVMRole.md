---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017411"
---
# <span data-ttu-id="cb131-101">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="cb131-101">Remove-WAPackVMRole</span></span>

## <span data-ttu-id="cb131-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb131-102">SYNOPSIS</span></span>
<span data-ttu-id="cb131-103">Eltávolítja a virtuálisgép-szerepkörök objektumait.</span><span class="sxs-lookup"><span data-stu-id="cb131-103">Removes virtual machine role objects.</span></span>

## <span data-ttu-id="cb131-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb131-104">SYNTAX</span></span>

### <span data-ttu-id="cb131-105">FromVMRoleObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb131-105">FromVMRoleObject (Default)</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb131-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="cb131-106">FromCloudService</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb131-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb131-107">DESCRIPTION</span></span>
<span data-ttu-id="cb131-108">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="cb131-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="cb131-109">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="cb131-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cb131-110">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="cb131-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="cb131-111">A **Remove-WAPackVMRole** parancsmag eltávolítja a virtuálisgép-szerepkörök objektumait.</span><span class="sxs-lookup"><span data-stu-id="cb131-111">The **Remove-WAPackVMRole** cmdlet removes virtual machine role objects.</span></span>

## <span data-ttu-id="cb131-112">Példák</span><span class="sxs-lookup"><span data-stu-id="cb131-112">EXAMPLES</span></span>

### <span data-ttu-id="cb131-113">1. példa: a virtuálisgép-szerepkörök eltávolítása (amelyet a WAP-portál használatával hoztak létre)</span><span class="sxs-lookup"><span data-stu-id="cb131-113">Example 1: Remove a virtual machine role (which was created using the WAP portal)</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

<span data-ttu-id="cb131-114">Az első parancs megkapja a ContosoVMRole01 nevű virtuális gép szerepkört a **Get-WAPackVMRole** parancsmaggal, majd az objektumot a $VMRole változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cb131-114">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="cb131-115">A második parancs eltávolítja a $VMRoleban tárolt virtuális gép szerepkört.</span><span class="sxs-lookup"><span data-stu-id="cb131-115">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="cb131-116">A parancs a megerősítést kéri. Feltételezve, hogy ez a virtuális gép szerepkör a WAP-portálon keresztül jött létre, nem kell megadnia a felhőalapú szolgáltatás nevét.</span><span class="sxs-lookup"><span data-stu-id="cb131-116">The command prompts you for confirmation.Assuming this virtual machine role was created using the WAP portal, there's no need to specify the cloud service name.</span></span>

### <span data-ttu-id="cb131-117">2. példa: a felhőalapú szolgáltatás kézi létrehozása után létrehozott virtuális gép szerepkör eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cb131-117">Example 2: Remove a virtual machine role which was created after manually creating a cloud service</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

<span data-ttu-id="cb131-118">Az első parancs a **Get-WAPackVMRole** parancsmaggal az "ContosoVMRole02" nevű virtuális gép szerepkört kapja, majd az objektumot a $VMRole változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cb131-118">The first command gets the virtual machine role named "ContosoVMRole02" by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="cb131-119">A második parancs eltávolítja a $VMRoleban tárolt virtuális gép szerepkört.</span><span class="sxs-lookup"><span data-stu-id="cb131-119">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="cb131-120">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="cb131-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="cb131-121">Feltételezve, hogy ez a virtuális gép szerepkör nem a portál használatával jött létre, a felhasználónak meg kell adnia a felhő szolgáltatás nevét.</span><span class="sxs-lookup"><span data-stu-id="cb131-121">Assuming this virtual machine role was not created using the portal, the user needs to specify the cloud service name.</span></span>
<span data-ttu-id="cb131-122">Ebben az esetben a "ContosoCloudService02" nevet kell elnevezni.</span><span class="sxs-lookup"><span data-stu-id="cb131-122">In this case named "ContosoCloudService02".</span></span>

### <span data-ttu-id="cb131-123">3. példa: virtuális gép szerepkörének eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="cb131-123">Example 3: Remove a virtual machine role without confirmation</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

<span data-ttu-id="cb131-124">Az első parancs a **Get-WAPackVMRole** parancsmaggal kapja meg a ContosoVMRole03 nevű felhőalapú szolgáltatást, majd a $VMRole változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="cb131-124">The first command gets the cloud service named ContosoVMRole03 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="cb131-125">A második parancs eltávolítja a $VMRoleban tárolt virtuális gép szerepkört.</span><span class="sxs-lookup"><span data-stu-id="cb131-125">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="cb131-126">Ez a parancs az *erő* paramétert tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cb131-126">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="cb131-127">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb131-127">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cb131-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb131-128">PARAMETERS</span></span>

### <span data-ttu-id="cb131-129">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="cb131-129">-CloudServiceName</span></span>
<span data-ttu-id="cb131-130">A virtuális gép szerepkör Felhőbeli szolgáltatásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb131-130">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb131-131">-Force</span><span class="sxs-lookup"><span data-stu-id="cb131-131">-Force</span></span>
<span data-ttu-id="cb131-132">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="cb131-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb131-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb131-133">-PassThru</span></span>
<span data-ttu-id="cb131-134">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="cb131-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cb131-135">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="cb131-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb131-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="cb131-136">-Profile</span></span>
<span data-ttu-id="cb131-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cb131-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cb131-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cb131-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cb131-139">-VMRole</span><span class="sxs-lookup"><span data-stu-id="cb131-139">-VMRole</span></span>
<span data-ttu-id="cb131-140">Virtuális gép szerepkört ad meg.</span><span class="sxs-lookup"><span data-stu-id="cb131-140">Specifies a virtual machine role.</span></span>
<span data-ttu-id="cb131-141">Virtuális gép szerepkör beszerzéséhez használja a **Get-WAPackVMRole** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cb131-141">To get a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb131-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb131-142">-Confirm</span></span>
<span data-ttu-id="cb131-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb131-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb131-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb131-144">-WhatIf</span></span>
<span data-ttu-id="cb131-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb131-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb131-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb131-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb131-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb131-147">CommonParameters</span></span>
<span data-ttu-id="cb131-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb131-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb131-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb131-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb131-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb131-150">INPUTS</span></span>

## <span data-ttu-id="cb131-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb131-151">OUTPUTS</span></span>

## <span data-ttu-id="cb131-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb131-152">NOTES</span></span>

## <span data-ttu-id="cb131-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb131-153">RELATED LINKS</span></span>

[<span data-ttu-id="cb131-154">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="cb131-154">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="cb131-155">Új – WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="cb131-155">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="cb131-156">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="cb131-156">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


