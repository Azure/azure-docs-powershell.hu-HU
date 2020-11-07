---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 0ce851373ac31aaef4c5664db7085f345e9b947d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844454"
---
# <span data-ttu-id="61a65-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="61a65-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="61a65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61a65-102">SYNOPSIS</span></span>
<span data-ttu-id="61a65-103">Létrehoz egy konfigurációs objektumot egy virtuális gépen történő automatikus javításhoz.</span><span class="sxs-lookup"><span data-stu-id="61a65-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="61a65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61a65-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="61a65-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61a65-105">DESCRIPTION</span></span>
<span data-ttu-id="61a65-106">A **New-AzVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot egy virtuális gépen az automatikus javításhoz.</span><span class="sxs-lookup"><span data-stu-id="61a65-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="61a65-107">Példák</span><span class="sxs-lookup"><span data-stu-id="61a65-107">EXAMPLES</span></span>

### <span data-ttu-id="61a65-108">Példa 1: konfigurációs objektum létrehozása az automatikus javítás konfigurálásához</span><span class="sxs-lookup"><span data-stu-id="61a65-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="61a65-109">Ez a parancs konfigurációs objektumot hoz létre a javításhoz.</span><span class="sxs-lookup"><span data-stu-id="61a65-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="61a65-110">A parancs a hét napját adja meg, és meghatározza a karbantartási ablakot.</span><span class="sxs-lookup"><span data-stu-id="61a65-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="61a65-111">Ez a beállítás lehetővé teszi az ezeket az értékeket használó javítások javítását.</span><span class="sxs-lookup"><span data-stu-id="61a65-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="61a65-112">A parancs az eredményt a $AutoBackupConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="61a65-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="61a65-113">Ezt a konfigurációs elemet más parancsmagok, például az Set-AzVMSqlServerExtension parancsmag esetében is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="61a65-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="61a65-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61a65-114">PARAMETERS</span></span>

### <span data-ttu-id="61a65-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="61a65-115">-DayOfWeek</span></span>
<span data-ttu-id="61a65-116">A hét azon napját adja meg, amikor a frissítéseket telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="61a65-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="61a65-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="61a65-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61a65-118">Vasárnap</span><span class="sxs-lookup"><span data-stu-id="61a65-118">Sunday</span></span>
- <span data-ttu-id="61a65-119">Hétfő</span><span class="sxs-lookup"><span data-stu-id="61a65-119">Monday</span></span>
- <span data-ttu-id="61a65-120">Kedd</span><span class="sxs-lookup"><span data-stu-id="61a65-120">Tuesday</span></span>
- <span data-ttu-id="61a65-121">Szerda</span><span class="sxs-lookup"><span data-stu-id="61a65-121">Wednesday</span></span>
- <span data-ttu-id="61a65-122">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="61a65-122">Thursday</span></span>
- <span data-ttu-id="61a65-123">Péntek</span><span class="sxs-lookup"><span data-stu-id="61a65-123">Friday</span></span>
- <span data-ttu-id="61a65-124">Szombat</span><span class="sxs-lookup"><span data-stu-id="61a65-124">Saturday</span></span>
- <span data-ttu-id="61a65-125">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="61a65-125">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a65-126">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="61a65-126">-Enable</span></span>
<span data-ttu-id="61a65-127">Azt jelzi, hogy a virtuális gép automatikus javítás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="61a65-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="61a65-128">Ha engedélyezi az automatikus javítást, a parancsmag a Windows Update funkciót interaktív módba teszi.</span><span class="sxs-lookup"><span data-stu-id="61a65-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="61a65-129">Ha letiltja az automatikus javítást, a Windows Update beállításai nem változnak.</span><span class="sxs-lookup"><span data-stu-id="61a65-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="61a65-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="61a65-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="61a65-131">A karbantartási ablak időtartamát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="61a65-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="61a65-132">Az automatizált javítás elkerüli az ablakon kívüli virtuális gépek elérhetőségét érintő műveletek végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="61a65-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="61a65-133">30 perc többszörösét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61a65-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a65-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="61a65-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="61a65-135">A karbantartás ablak indításakor megjelenő nap óráját adja meg.</span><span class="sxs-lookup"><span data-stu-id="61a65-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="61a65-136">Ez az időpont határozza meg, hogy mikor induljon el a frissítések telepítése.</span><span class="sxs-lookup"><span data-stu-id="61a65-136">This time defines when updates start to install.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a65-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="61a65-137">-PatchCategory</span></span>
<span data-ttu-id="61a65-138">Annak meghatározása, hogy fontos frissítéseket kell-e szerepeltetni.</span><span class="sxs-lookup"><span data-stu-id="61a65-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a65-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a65-139">CommonParameters</span></span>
<span data-ttu-id="61a65-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61a65-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a65-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a65-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a65-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61a65-142">INPUTS</span></span>

### <span data-ttu-id="61a65-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="61a65-143">None</span></span>
<span data-ttu-id="61a65-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="61a65-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61a65-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61a65-145">OUTPUTS</span></span>

### <span data-ttu-id="61a65-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="61a65-146">AutoPatchingSettings</span></span>
<span data-ttu-id="61a65-147">Ez a parancsmag visszaadja az objektumot az automatizált javítások beállításai között.</span><span class="sxs-lookup"><span data-stu-id="61a65-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="61a65-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61a65-148">NOTES</span></span>

## <span data-ttu-id="61a65-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61a65-149">RELATED LINKS</span></span>

[<span data-ttu-id="61a65-150">Új – AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="61a65-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="61a65-151">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="61a65-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


