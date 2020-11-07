---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: d6814131ec4748f95f572762938d3c8bd5135c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672998"
---
# <span data-ttu-id="33807-101">New-AzureRmVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="33807-101">New-AzureRmVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="33807-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33807-102">SYNOPSIS</span></span>
<span data-ttu-id="33807-103">Létrehoz egy konfigurációs objektumot egy virtuális gépen történő automatikus javításhoz.</span><span class="sxs-lookup"><span data-stu-id="33807-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33807-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33807-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="33807-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="33807-105">DESCRIPTION</span></span>
<span data-ttu-id="33807-106">A **New-AzureRmVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot egy virtuális gépen az automatikus javításhoz.</span><span class="sxs-lookup"><span data-stu-id="33807-106">The **New-AzureRmVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="33807-107">Példák</span><span class="sxs-lookup"><span data-stu-id="33807-107">EXAMPLES</span></span>

### <span data-ttu-id="33807-108">Példa 1: konfigurációs objektum létrehozása az automatikus javítás konfigurálásához</span><span class="sxs-lookup"><span data-stu-id="33807-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureRmVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="33807-109">Ez a parancs konfigurációs objektumot hoz létre a javításhoz.</span><span class="sxs-lookup"><span data-stu-id="33807-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="33807-110">A parancs a hét napját adja meg, és meghatározza a karbantartási ablakot.</span><span class="sxs-lookup"><span data-stu-id="33807-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="33807-111">Ez a beállítás lehetővé teszi az ezeket az értékeket használó javítások javítását.</span><span class="sxs-lookup"><span data-stu-id="33807-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="33807-112">A parancs az eredményt a $AutoBackupConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="33807-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="33807-113">Ezt a konfigurációs elemet más parancsmagok, például az Set-AzureRmVMSqlServerExtension parancsmag esetében is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="33807-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="33807-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33807-114">PARAMETERS</span></span>

### <span data-ttu-id="33807-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="33807-115">-DayOfWeek</span></span>
<span data-ttu-id="33807-116">A hét azon napját adja meg, amikor a frissítéseket telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="33807-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="33807-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="33807-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="33807-118">Vasárnap</span><span class="sxs-lookup"><span data-stu-id="33807-118">Sunday</span></span>
- <span data-ttu-id="33807-119">Hétfő</span><span class="sxs-lookup"><span data-stu-id="33807-119">Monday</span></span>
- <span data-ttu-id="33807-120">Kedd</span><span class="sxs-lookup"><span data-stu-id="33807-120">Tuesday</span></span>
- <span data-ttu-id="33807-121">Szerda</span><span class="sxs-lookup"><span data-stu-id="33807-121">Wednesday</span></span>
- <span data-ttu-id="33807-122">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="33807-122">Thursday</span></span>
- <span data-ttu-id="33807-123">Péntek</span><span class="sxs-lookup"><span data-stu-id="33807-123">Friday</span></span>
- <span data-ttu-id="33807-124">Szombat</span><span class="sxs-lookup"><span data-stu-id="33807-124">Saturday</span></span>
- <span data-ttu-id="33807-125">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="33807-125">Everyday</span></span>

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

### <span data-ttu-id="33807-126">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="33807-126">-Enable</span></span>
<span data-ttu-id="33807-127">Azt jelzi, hogy a virtuális gép automatikus javítás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="33807-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="33807-128">Ha engedélyezi az automatikus javítást, a parancsmag a Windows Update funkciót interaktív módba teszi.</span><span class="sxs-lookup"><span data-stu-id="33807-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="33807-129">Ha letiltja az automatikus javítást, a Windows Update beállításai nem változnak.</span><span class="sxs-lookup"><span data-stu-id="33807-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="33807-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="33807-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="33807-131">A karbantartási ablak időtartamát adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="33807-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="33807-132">Az automatizált javítás elkerüli az ablakon kívüli virtuális gépek elérhetőségét érintő műveletek végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="33807-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="33807-133">30 perc többszörösét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33807-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="33807-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="33807-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="33807-135">A karbantartás ablak indításakor megjelenő nap óráját adja meg.</span><span class="sxs-lookup"><span data-stu-id="33807-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="33807-136">Ez az időpont határozza meg, hogy mikor induljon el a frissítések telepítése.</span><span class="sxs-lookup"><span data-stu-id="33807-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="33807-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="33807-137">-PatchCategory</span></span>
<span data-ttu-id="33807-138">Annak meghatározása, hogy fontos frissítéseket kell-e szerepeltetni.</span><span class="sxs-lookup"><span data-stu-id="33807-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="33807-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33807-139">CommonParameters</span></span>
<span data-ttu-id="33807-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33807-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33807-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33807-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33807-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33807-142">INPUTS</span></span>

### <span data-ttu-id="33807-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="33807-143">None</span></span>

## <span data-ttu-id="33807-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33807-144">OUTPUTS</span></span>

### <span data-ttu-id="33807-145">Microsoft. Azure. commands. kiszámítás. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="33807-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="33807-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33807-146">NOTES</span></span>

## <span data-ttu-id="33807-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33807-147">RELATED LINKS</span></span>

[<span data-ttu-id="33807-148">Új – AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="33807-148">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="33807-149">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="33807-149">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


