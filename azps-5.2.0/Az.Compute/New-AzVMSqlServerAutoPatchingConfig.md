---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331890"
---
# <span data-ttu-id="90a69-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="90a69-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="90a69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90a69-102">SYNOPSIS</span></span>
<span data-ttu-id="90a69-103">Konfigurációs objektumot hoz létre automatikus javításhoz egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="90a69-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="90a69-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90a69-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="90a69-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90a69-105">DESCRIPTION</span></span>
<span data-ttu-id="90a69-106">A **New-AzVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot az automatikus javításhoz egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="90a69-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="90a69-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90a69-107">EXAMPLES</span></span>

### <span data-ttu-id="90a69-108">1. példa: Az automatikus javítás konfigurálása konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="90a69-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="90a69-109">Ez a parancs konfigurációs objektumot hoz létre javításra.</span><span class="sxs-lookup"><span data-stu-id="90a69-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="90a69-110">A parancs megadja a hét napját és a karbantartási ablakot.</span><span class="sxs-lookup"><span data-stu-id="90a69-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="90a69-111">Ez a konfiguráció lehetővé teszi az ezeket az értékeket használó javításokat.</span><span class="sxs-lookup"><span data-stu-id="90a69-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="90a69-112">A parancs az eredményt a $AutoBackupConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="90a69-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="90a69-113">Ezt a konfigurációs elemet más parancsmagok, például a Set-AzVMSqlServerExtension is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="90a69-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="90a69-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90a69-114">PARAMETERS</span></span>

### <span data-ttu-id="90a69-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="90a69-115">-DayOfWeek</span></span>
<span data-ttu-id="90a69-116">A hétnek azt a napját adja meg, amikor frissítéseket kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="90a69-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="90a69-117">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="90a69-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90a69-118">vasárnap</span><span class="sxs-lookup"><span data-stu-id="90a69-118">Sunday</span></span>
- <span data-ttu-id="90a69-119">Hétfő</span><span class="sxs-lookup"><span data-stu-id="90a69-119">Monday</span></span>
- <span data-ttu-id="90a69-120">Kedd</span><span class="sxs-lookup"><span data-stu-id="90a69-120">Tuesday</span></span>
- <span data-ttu-id="90a69-121">Szerda</span><span class="sxs-lookup"><span data-stu-id="90a69-121">Wednesday</span></span>
- <span data-ttu-id="90a69-122">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="90a69-122">Thursday</span></span>
- <span data-ttu-id="90a69-123">Péntek</span><span class="sxs-lookup"><span data-stu-id="90a69-123">Friday</span></span>
- <span data-ttu-id="90a69-124">Szombat</span><span class="sxs-lookup"><span data-stu-id="90a69-124">Saturday</span></span>
- <span data-ttu-id="90a69-125">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="90a69-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a69-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="90a69-126">-Enable</span></span>
<span data-ttu-id="90a69-127">Azt jelzi, hogy a virtuális géphez engedélyezve van az automatikus javítás.</span><span class="sxs-lookup"><span data-stu-id="90a69-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="90a69-128">Ha engedélyezi a parancsmag automatikus javítását, a Windows Update interaktív üzemmódba vált.</span><span class="sxs-lookup"><span data-stu-id="90a69-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="90a69-129">Ha letiltja az automatikus javításokat, a Windows Update beállításai nem változnak.</span><span class="sxs-lookup"><span data-stu-id="90a69-129">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a69-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="90a69-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="90a69-131">A karbantartási ablak időtartamát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="90a69-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="90a69-132">Az automatikus javításokkal elkerülheti az olyan műveletek elvégzését, amelyek hatással lehetnek a virtuális gépek ezen az ablakon kívüli elérhetőségére.</span><span class="sxs-lookup"><span data-stu-id="90a69-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="90a69-133">Adja meg a 30 perc többszörösét.</span><span class="sxs-lookup"><span data-stu-id="90a69-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a69-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="90a69-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="90a69-135">A karbantartási ablak indításakor a nap óráját adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a69-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="90a69-136">Ez az idő azt határozza meg, hogy mikor indulnak el a frissítések.</span><span class="sxs-lookup"><span data-stu-id="90a69-136">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a69-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="90a69-137">-PatchCategory</span></span>
<span data-ttu-id="90a69-138">Megadja, hogy a fontos frissítéseket is meg kell-e kapni.</span><span class="sxs-lookup"><span data-stu-id="90a69-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a69-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a69-139">CommonParameters</span></span>
<span data-ttu-id="90a69-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90a69-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a69-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90a69-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a69-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90a69-142">INPUTS</span></span>

### <span data-ttu-id="90a69-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="90a69-143">None</span></span>

## <span data-ttu-id="90a69-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a69-144">OUTPUTS</span></span>

### <span data-ttu-id="90a69-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="90a69-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="90a69-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90a69-146">NOTES</span></span>

## <span data-ttu-id="90a69-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90a69-147">RELATED LINKS</span></span>

[<span data-ttu-id="90a69-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="90a69-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="90a69-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="90a69-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


