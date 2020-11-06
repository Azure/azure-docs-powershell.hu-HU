---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 516192dab6d075979a2d78cea72afaedb7a18231
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495448"
---
# <span data-ttu-id="c272b-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="c272b-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="c272b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c272b-102">SYNOPSIS</span></span>
<span data-ttu-id="c272b-103">Létrehoz egy konfigurációs objektumot egy virtuális gépen történő automatikus javításhoz.</span><span class="sxs-lookup"><span data-stu-id="c272b-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c272b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c272b-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="c272b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c272b-105">DESCRIPTION</span></span>
<span data-ttu-id="c272b-106">A **New-AzureVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot egy virtuális gépen az automatikus javításhoz.</span><span class="sxs-lookup"><span data-stu-id="c272b-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="c272b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c272b-107">EXAMPLES</span></span>

### <span data-ttu-id="c272b-108">Példa 1: konfigurációs objektum létrehozása az automatikus javítás konfigurálásához</span><span class="sxs-lookup"><span data-stu-id="c272b-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="c272b-109">Ez a parancs konfigurációs objektumot hoz létre a javításhoz.</span><span class="sxs-lookup"><span data-stu-id="c272b-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="c272b-110">A parancs a hét napját adja meg, és meghatározza a karbantartási ablakot.</span><span class="sxs-lookup"><span data-stu-id="c272b-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="c272b-111">Ez a beállítás lehetővé teszi az ezeket az értékeket használó javítások javítását.</span><span class="sxs-lookup"><span data-stu-id="c272b-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="c272b-112">A parancs az eredményt a $AutoBackupConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c272b-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="c272b-113">Ezt a konfigurációs elemet más parancsmagok, például az Set-AzureRmVMSqlServerExtension parancsmag esetében is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="c272b-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="c272b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c272b-114">PARAMETERS</span></span>

### <span data-ttu-id="c272b-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="c272b-115">-DayOfWeek</span></span>
<span data-ttu-id="c272b-116">A hét azon napját adja meg, amikor a frissítéseket telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="c272b-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="c272b-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c272b-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c272b-118">Vasárnap</span><span class="sxs-lookup"><span data-stu-id="c272b-118">Sunday</span></span>
- <span data-ttu-id="c272b-119">Hétfő</span><span class="sxs-lookup"><span data-stu-id="c272b-119">Monday</span></span>
- <span data-ttu-id="c272b-120">Kedd</span><span class="sxs-lookup"><span data-stu-id="c272b-120">Tuesday</span></span>
- <span data-ttu-id="c272b-121">Szerda</span><span class="sxs-lookup"><span data-stu-id="c272b-121">Wednesday</span></span>
- <span data-ttu-id="c272b-122">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="c272b-122">Thursday</span></span>
- <span data-ttu-id="c272b-123">Péntek</span><span class="sxs-lookup"><span data-stu-id="c272b-123">Friday</span></span>
- <span data-ttu-id="c272b-124">Szombat</span><span class="sxs-lookup"><span data-stu-id="c272b-124">Saturday</span></span>
- <span data-ttu-id="c272b-125">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="c272b-125">Everyday</span></span>

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

### <span data-ttu-id="c272b-126">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="c272b-126">-Enable</span></span>
<span data-ttu-id="c272b-127">Azt jelzi, hogy a virtuális gép automatikus javítás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="c272b-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="c272b-128">Ha engedélyezi az automatikus javítást, a parancsmag a Windows Update funkciót interaktív módba teszi.</span><span class="sxs-lookup"><span data-stu-id="c272b-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="c272b-129">Ha letiltja az automatikus javítást, a Windows Update beállításai nem változnak.</span><span class="sxs-lookup"><span data-stu-id="c272b-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="c272b-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="c272b-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="c272b-131">A karbantartási ablak időtartamát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="c272b-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="c272b-132">Az automatizált javítás elkerüli az ablakon kívüli virtuális gépek elérhetőségét érintő műveletek végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="c272b-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="c272b-133">30 perc többszörösét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c272b-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="c272b-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="c272b-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="c272b-135">A karbantartás ablak indításakor megjelenő nap óráját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c272b-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="c272b-136">Ez az időpont határozza meg, hogy mikor induljon el a frissítések telepítése.</span><span class="sxs-lookup"><span data-stu-id="c272b-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="c272b-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="c272b-137">-PatchCategory</span></span>
<span data-ttu-id="c272b-138">Annak meghatározása, hogy fontos frissítéseket kell-e szerepeltetni.</span><span class="sxs-lookup"><span data-stu-id="c272b-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="c272b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c272b-139">CommonParameters</span></span>
<span data-ttu-id="c272b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c272b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c272b-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c272b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c272b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c272b-142">INPUTS</span></span>

### <span data-ttu-id="c272b-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="c272b-143">None</span></span>
<span data-ttu-id="c272b-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c272b-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c272b-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c272b-145">OUTPUTS</span></span>

### <span data-ttu-id="c272b-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="c272b-146">AutoPatchingSettings</span></span>
<span data-ttu-id="c272b-147">Ez a parancsmag visszaadja az objektumot az automatizált javítások beállításai között.</span><span class="sxs-lookup"><span data-stu-id="c272b-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="c272b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c272b-148">NOTES</span></span>

## <span data-ttu-id="c272b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c272b-149">RELATED LINKS</span></span>

[<span data-ttu-id="c272b-150">Új – AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="c272b-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="c272b-151">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c272b-151">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


