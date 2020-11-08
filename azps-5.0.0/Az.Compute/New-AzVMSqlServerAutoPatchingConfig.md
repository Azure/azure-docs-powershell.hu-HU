---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185728"
---
# <span data-ttu-id="a8ec6-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="a8ec6-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="a8ec6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ec6-103">Létrehoz egy konfigurációs objektumot egy virtuális gépen történő automatikus javításhoz.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="a8ec6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8ec6-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="a8ec6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8ec6-105">DESCRIPTION</span></span>
<span data-ttu-id="a8ec6-106">A **New-AzVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot egy virtuális gépen az automatikus javításhoz.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="a8ec6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8ec6-107">EXAMPLES</span></span>

### <span data-ttu-id="a8ec6-108">Példa 1: konfigurációs objektum létrehozása az automatikus javítás konfigurálásához</span><span class="sxs-lookup"><span data-stu-id="a8ec6-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="a8ec6-109">Ez a parancs konfigurációs objektumot hoz létre a javításhoz.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="a8ec6-110">A parancs a hét napját adja meg, és meghatározza a karbantartási ablakot.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="a8ec6-111">Ez a beállítás lehetővé teszi az ezeket az értékeket használó javítások javítását.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="a8ec6-112">A parancs az eredményt a $AutoBackupConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="a8ec6-113">Ezt a konfigurációs elemet más parancsmagok, például az Set-AzVMSqlServerExtension parancsmag esetében is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="a8ec6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8ec6-114">PARAMETERS</span></span>

### <span data-ttu-id="a8ec6-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="a8ec6-115">-DayOfWeek</span></span>
<span data-ttu-id="a8ec6-116">A hét azon napját adja meg, amikor a frissítéseket telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="a8ec6-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a8ec6-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8ec6-118">Vasárnap</span><span class="sxs-lookup"><span data-stu-id="a8ec6-118">Sunday</span></span>
- <span data-ttu-id="a8ec6-119">Hétfő</span><span class="sxs-lookup"><span data-stu-id="a8ec6-119">Monday</span></span>
- <span data-ttu-id="a8ec6-120">Kedd</span><span class="sxs-lookup"><span data-stu-id="a8ec6-120">Tuesday</span></span>
- <span data-ttu-id="a8ec6-121">Szerda</span><span class="sxs-lookup"><span data-stu-id="a8ec6-121">Wednesday</span></span>
- <span data-ttu-id="a8ec6-122">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="a8ec6-122">Thursday</span></span>
- <span data-ttu-id="a8ec6-123">Péntek</span><span class="sxs-lookup"><span data-stu-id="a8ec6-123">Friday</span></span>
- <span data-ttu-id="a8ec6-124">Szombat</span><span class="sxs-lookup"><span data-stu-id="a8ec6-124">Saturday</span></span>
- <span data-ttu-id="a8ec6-125">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="a8ec6-125">Everyday</span></span>

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

### <span data-ttu-id="a8ec6-126">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="a8ec6-126">-Enable</span></span>
<span data-ttu-id="a8ec6-127">Azt jelzi, hogy a virtuális gép automatikus javítás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="a8ec6-128">Ha engedélyezi az automatikus javítást, a parancsmag a Windows Update funkciót interaktív módba teszi.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="a8ec6-129">Ha letiltja az automatikus javítást, a Windows Update beállításai nem változnak.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="a8ec6-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="a8ec6-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="a8ec6-131">A karbantartási ablak időtartamát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="a8ec6-132">Az automatizált javítás elkerüli az ablakon kívüli virtuális gépek elérhetőségét érintő műveletek végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="a8ec6-133">30 perc többszörösét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="a8ec6-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="a8ec6-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="a8ec6-135">A karbantartás ablak indításakor megjelenő nap óráját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="a8ec6-136">Ez az időpont határozza meg, hogy mikor induljon el a frissítések telepítése.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="a8ec6-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="a8ec6-137">-PatchCategory</span></span>
<span data-ttu-id="a8ec6-138">Annak meghatározása, hogy fontos frissítéseket kell-e szerepeltetni.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="a8ec6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ec6-139">CommonParameters</span></span>
<span data-ttu-id="a8ec6-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8ec6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ec6-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a8ec6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ec6-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8ec6-142">INPUTS</span></span>

### <span data-ttu-id="a8ec6-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="a8ec6-143">None</span></span>

## <span data-ttu-id="a8ec6-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8ec6-144">OUTPUTS</span></span>

### <span data-ttu-id="a8ec6-145">Microsoft. Azure. commands. kiszámítás. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="a8ec6-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="a8ec6-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8ec6-146">NOTES</span></span>

## <span data-ttu-id="a8ec6-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8ec6-147">RELATED LINKS</span></span>

[<span data-ttu-id="a8ec6-148">Új – AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="a8ec6-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="a8ec6-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a8ec6-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


