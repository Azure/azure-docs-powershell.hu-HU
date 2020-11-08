---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016191"
---
# <span data-ttu-id="8244c-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="8244c-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="8244c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8244c-102">SYNOPSIS</span></span>
<span data-ttu-id="8244c-103">Létrehoz egy konfigurációs objektumot a virtuális gép automatikus javításához.</span><span class="sxs-lookup"><span data-stu-id="8244c-103">Creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="8244c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8244c-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8244c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8244c-105">DESCRIPTION</span></span>
<span data-ttu-id="8244c-106">A **New-AzureVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot a virtuális gép automatikus javításához.</span><span class="sxs-lookup"><span data-stu-id="8244c-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="8244c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8244c-107">EXAMPLES</span></span>

### <span data-ttu-id="8244c-108">Példa 1: konfigurációs objektum létrehozása az automatikus javítás konfigurálásához</span><span class="sxs-lookup"><span data-stu-id="8244c-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

<span data-ttu-id="8244c-109">Ez a parancs konfigurációs objektumot hoz létre, amellyel beállítható az automatikus javítás a set-AzureVMSqlServerExtension használatával.</span><span class="sxs-lookup"><span data-stu-id="8244c-109">This command creates configuration object that can be used to configure automatic patching using Set-AzureVMSqlServerExtension.</span></span>

## <span data-ttu-id="8244c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8244c-110">PARAMETERS</span></span>

### <span data-ttu-id="8244c-111">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="8244c-111">-DayOfWeek</span></span>
<span data-ttu-id="8244c-112">A hét azon napját adja meg, amikor a frissítéseket telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="8244c-112">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="8244c-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8244c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8244c-114">Vasárnap</span><span class="sxs-lookup"><span data-stu-id="8244c-114">Sunday</span></span>
- <span data-ttu-id="8244c-115">Hétfő</span><span class="sxs-lookup"><span data-stu-id="8244c-115">Monday</span></span>
- <span data-ttu-id="8244c-116">Kedd</span><span class="sxs-lookup"><span data-stu-id="8244c-116">Tuesday</span></span>
- <span data-ttu-id="8244c-117">Szerda</span><span class="sxs-lookup"><span data-stu-id="8244c-117">Wednesday</span></span>
- <span data-ttu-id="8244c-118">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="8244c-118">Thursday</span></span>
- <span data-ttu-id="8244c-119">Péntek</span><span class="sxs-lookup"><span data-stu-id="8244c-119">Friday</span></span>
- <span data-ttu-id="8244c-120">Szombat</span><span class="sxs-lookup"><span data-stu-id="8244c-120">Saturday</span></span>
- <span data-ttu-id="8244c-121">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="8244c-121">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8244c-122">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="8244c-122">-Enable</span></span>
<span data-ttu-id="8244c-123">Azt jelzi, hogy a virtuális gép automatikus javítás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="8244c-123">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="8244c-124">Ha engedélyezi az automatikus javítást, a parancsmag interaktív módba fogja helyezni a Windows Update szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="8244c-124">If you enable automated patching the cmdlet will put Windows Update into interactive mode.</span></span>
<span data-ttu-id="8244c-125">Ha letiltja az automatikus javítást, a Windows Update beállításai nem változnak.</span><span class="sxs-lookup"><span data-stu-id="8244c-125">If you disable automated patching, Windows Update settings will not change.</span></span>

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

### <span data-ttu-id="8244c-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8244c-126">-InformationAction</span></span>
<span data-ttu-id="8244c-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="8244c-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8244c-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8244c-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8244c-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="8244c-129">Continue</span></span>
- <span data-ttu-id="8244c-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="8244c-130">Ignore</span></span>
- <span data-ttu-id="8244c-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="8244c-131">Inquire</span></span>
- <span data-ttu-id="8244c-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8244c-132">SilentlyContinue</span></span>
- <span data-ttu-id="8244c-133">állj</span><span class="sxs-lookup"><span data-stu-id="8244c-133">Stop</span></span>
- <span data-ttu-id="8244c-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="8244c-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8244c-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8244c-135">-InformationVariable</span></span>
<span data-ttu-id="8244c-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="8244c-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8244c-137">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="8244c-137">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="8244c-138">A karbantartás ablak időtartamát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8244c-138">Specifies the duration of the maintenance window.</span></span>
<span data-ttu-id="8244c-139">Az automatizált javítással elkerülhetők az adott ablakon kívüli virtuális gépek elérhetőségét befolyásoló műveletek.</span><span class="sxs-lookup"><span data-stu-id="8244c-139">Automated patching will avoid performing an action that can impact a virtual machine availability outside of that window.</span></span>
<span data-ttu-id="8244c-140">Csak 30 perc lépés megengedett.</span><span class="sxs-lookup"><span data-stu-id="8244c-140">Only 30 minutes increments are allowed.</span></span>

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

### <span data-ttu-id="8244c-141">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="8244c-141">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="8244c-142">A karbantartás ablak indításakor megjelenő nap óráját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8244c-142">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="8244c-143">Ez az időpont határozza meg, hogy mikor induljon el a frissítések telepítése, és az órára van kerekítve.</span><span class="sxs-lookup"><span data-stu-id="8244c-143">This time defines when updates start installing and is rounded to the hour.</span></span>

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

### <span data-ttu-id="8244c-144">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="8244c-144">-PatchCategory</span></span>
<span data-ttu-id="8244c-145">Annak meghatározása, hogy fontos frissítéseket kell-e szerepeltetni.</span><span class="sxs-lookup"><span data-stu-id="8244c-145">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8244c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8244c-146">CommonParameters</span></span>
<span data-ttu-id="8244c-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8244c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8244c-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8244c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8244c-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8244c-149">INPUTS</span></span>

## <span data-ttu-id="8244c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8244c-150">OUTPUTS</span></span>

### <span data-ttu-id="8244c-151">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="8244c-151">AutoPatchingSettings</span></span>
<span data-ttu-id="8244c-152">Ez a parancsmag visszaadja az objektumot az automatizált javítások beállításai között.</span><span class="sxs-lookup"><span data-stu-id="8244c-152">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="8244c-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8244c-153">NOTES</span></span>

## <span data-ttu-id="8244c-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8244c-154">RELATED LINKS</span></span>

[<span data-ttu-id="8244c-155">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8244c-155">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)

[<span data-ttu-id="8244c-156">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8244c-156">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="8244c-157">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8244c-157">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


