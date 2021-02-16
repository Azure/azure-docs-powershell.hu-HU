---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3ba7ab00076a3a0634a0d4394270fe4a83ec8ede
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398257"
---
# <span data-ttu-id="a561a-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="a561a-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="a561a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a561a-102">SYNOPSIS</span></span>
<span data-ttu-id="a561a-103">Konfigurációs objektumot hoz létre automatikus javításhoz egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="a561a-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="a561a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a561a-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a561a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a561a-105">DESCRIPTION</span></span>
<span data-ttu-id="a561a-106">A **New-AzVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot az automatikus javításhoz egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="a561a-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="a561a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a561a-107">EXAMPLES</span></span>

### <span data-ttu-id="a561a-108">1. példa: Az automatikus javítás konfigurálása konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a561a-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="a561a-109">Ez a parancs konfigurációs objektumot hoz létre javításra.</span><span class="sxs-lookup"><span data-stu-id="a561a-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="a561a-110">A parancs megadja a hét napját és a karbantartási ablakot.</span><span class="sxs-lookup"><span data-stu-id="a561a-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="a561a-111">Ez a konfiguráció lehetővé teszi az ezeket az értékeket használó javításokat.</span><span class="sxs-lookup"><span data-stu-id="a561a-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="a561a-112">A parancs az eredményt a $AutoBackupConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="a561a-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="a561a-113">Ezt a konfigurációs elemet más parancsmagok, például a Set-AzVMSqlServerExtension is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="a561a-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="a561a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a561a-114">PARAMETERS</span></span>

### <span data-ttu-id="a561a-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="a561a-115">-DayOfWeek</span></span>
<span data-ttu-id="a561a-116">A hétnek azt a napját adja meg, amikor frissítéseket kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="a561a-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="a561a-117">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="a561a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a561a-118">vasárnap</span><span class="sxs-lookup"><span data-stu-id="a561a-118">Sunday</span></span>
- <span data-ttu-id="a561a-119">Hétfő</span><span class="sxs-lookup"><span data-stu-id="a561a-119">Monday</span></span>
- <span data-ttu-id="a561a-120">Kedd</span><span class="sxs-lookup"><span data-stu-id="a561a-120">Tuesday</span></span>
- <span data-ttu-id="a561a-121">Szerda</span><span class="sxs-lookup"><span data-stu-id="a561a-121">Wednesday</span></span>
- <span data-ttu-id="a561a-122">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="a561a-122">Thursday</span></span>
- <span data-ttu-id="a561a-123">Péntek</span><span class="sxs-lookup"><span data-stu-id="a561a-123">Friday</span></span>
- <span data-ttu-id="a561a-124">Szombat</span><span class="sxs-lookup"><span data-stu-id="a561a-124">Saturday</span></span>
- <span data-ttu-id="a561a-125">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="a561a-125">Everyday</span></span>

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

### <span data-ttu-id="a561a-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="a561a-126">-Enable</span></span>
<span data-ttu-id="a561a-127">Azt jelzi, hogy a virtuális géphez engedélyezve van az automatikus javítás.</span><span class="sxs-lookup"><span data-stu-id="a561a-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="a561a-128">Ha engedélyezi a parancsmag automatikus javítását, a Windows Update interaktív üzemmódba vált.</span><span class="sxs-lookup"><span data-stu-id="a561a-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="a561a-129">Ha letiltja az automatikus javításokat, a Windows Update beállításai nem változnak.</span><span class="sxs-lookup"><span data-stu-id="a561a-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="a561a-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="a561a-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="a561a-131">A karbantartási ablak időtartamát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="a561a-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="a561a-132">Az automatikus javításokkal elkerülhetők olyan műveletek, amelyek hatással lehetnek a virtuális gépek ezen az ablakon kívüli elérhetőségére.</span><span class="sxs-lookup"><span data-stu-id="a561a-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="a561a-133">Adja meg a 30 perc többszörösét.</span><span class="sxs-lookup"><span data-stu-id="a561a-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="a561a-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="a561a-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="a561a-135">A karbantartási ablak indításakor a nap óráját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a561a-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="a561a-136">Ez az idő azt határozza meg, hogy mikor indulnak el a frissítések.</span><span class="sxs-lookup"><span data-stu-id="a561a-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="a561a-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="a561a-137">-PatchCategory</span></span>
<span data-ttu-id="a561a-138">Megadja, hogy a fontos frissítéseket is meg kell-e kapni.</span><span class="sxs-lookup"><span data-stu-id="a561a-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="a561a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a561a-139">CommonParameters</span></span>
<span data-ttu-id="a561a-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a561a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a561a-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a561a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a561a-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a561a-142">INPUTS</span></span>

### <span data-ttu-id="a561a-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="a561a-143">None</span></span>
<span data-ttu-id="a561a-144">Ez a parancsmag semmilyen bemenetet nem fogad el.</span><span class="sxs-lookup"><span data-stu-id="a561a-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a561a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a561a-145">OUTPUTS</span></span>

### <span data-ttu-id="a561a-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="a561a-146">AutoPatchingSettings</span></span>
<span data-ttu-id="a561a-147">Ez a parancsmag az automatikus javítás beállításait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a561a-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="a561a-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a561a-148">NOTES</span></span>

## <span data-ttu-id="a561a-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a561a-149">RELATED LINKS</span></span>

[<span data-ttu-id="a561a-150">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="a561a-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="a561a-151">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a561a-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


