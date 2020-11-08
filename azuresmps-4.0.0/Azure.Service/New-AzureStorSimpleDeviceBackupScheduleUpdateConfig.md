---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015524"
---
# <span data-ttu-id="e283b-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="e283b-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>

## <span data-ttu-id="e283b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e283b-102">SYNOPSIS</span></span>
<span data-ttu-id="e283b-103">Biztonságimásolat-ütemezett frissítési konfigurációs objektum létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e283b-103">Creates a backup schedule update configuration object.</span></span>

## <span data-ttu-id="e283b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e283b-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e283b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e283b-105">DESCRIPTION</span></span>
<span data-ttu-id="e283b-106">A **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** parancsmag létrehoz egy **BackupScheduleUpdateRequest** konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="e283b-106">The **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet creates a **BackupScheduleUpdateRequest** configuration object.</span></span>
<span data-ttu-id="e283b-107">Ezzel a konfigurációs objektummal frissítheti a biztonságimásolat-házirendet a **set-AzureStorSimpleDeviceBackupPolicy** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="e283b-107">Use this configuration object to update a backup policy by using the **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="e283b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e283b-108">EXAMPLES</span></span>

### <span data-ttu-id="e283b-109">Példa 1: ütemterv frissítési kérésének létrehozása</span><span class="sxs-lookup"><span data-stu-id="e283b-109">Example 1: Create a schedule update request</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

<span data-ttu-id="e283b-110">Ez a parancs létrehoz egy biztonságimásolat-ütemterv frissítési kérését a megadott azonosítót tartalmazó ütemtervhez.</span><span class="sxs-lookup"><span data-stu-id="e283b-110">This command creates a backup schedule update request for the schedule that has the specified ID.</span></span>
<span data-ttu-id="e283b-111">A kérés célja, hogy egy olyan felhőalapú pillanatkép-biztonsági másolatot készítsen, amely óránként ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="e283b-111">The request is to make the schedule a cloud snapshot backup that recurs every hour.</span></span>
<span data-ttu-id="e283b-112">A biztonsági másolatok 50 napra megmaradnak.</span><span class="sxs-lookup"><span data-stu-id="e283b-112">The backups are kept for 50 days.</span></span>
<span data-ttu-id="e283b-113">Ez az ütemezés az alapértelmezett időponttól, azaz az aktuális időponttól engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="e283b-113">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="e283b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e283b-114">PARAMETERS</span></span>

### <span data-ttu-id="e283b-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="e283b-115">-BackupType</span></span>
<span data-ttu-id="e283b-116">A biztonságimásolat-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="e283b-116">Specifies the backup type.</span></span>
<span data-ttu-id="e283b-117">Az érvényes értékek a következők: LocalSnapshot és CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="e283b-117">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e283b-118">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="e283b-118">-Enabled</span></span>
<span data-ttu-id="e283b-119">Azt jelzi, hogy engedélyezi-e a biztonsági ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="e283b-119">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e283b-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e283b-120">-Id</span></span>
<span data-ttu-id="e283b-121">A frissítendő biztonsági ütemterv példányának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e283b-121">Specifies the instance ID of the backup schedule to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e283b-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="e283b-122">-Profile</span></span>
<span data-ttu-id="e283b-123">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="e283b-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e283b-124">-Naptárkivételhez RecurrenceType érték</span><span class="sxs-lookup"><span data-stu-id="e283b-124">-RecurrenceType</span></span>
<span data-ttu-id="e283b-125">A biztonságimásolat-ütemterv ismétlődési típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e283b-125">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="e283b-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="e283b-126">Valid values are:</span></span> 

- <span data-ttu-id="e283b-127">Perc</span><span class="sxs-lookup"><span data-stu-id="e283b-127">Minutes</span></span>
- <span data-ttu-id="e283b-128">Óránkénti</span><span class="sxs-lookup"><span data-stu-id="e283b-128">Hourly</span></span>
- <span data-ttu-id="e283b-129">Napi</span><span class="sxs-lookup"><span data-stu-id="e283b-129">Daily</span></span>
- <span data-ttu-id="e283b-130">Heti</span><span class="sxs-lookup"><span data-stu-id="e283b-130">Weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e283b-131">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="e283b-131">-RecurrenceValue</span></span>
<span data-ttu-id="e283b-132">Megadja, hogy milyen gyakran készítsen biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="e283b-132">Specifies how often to make a backup.</span></span>
<span data-ttu-id="e283b-133">Ez a paraméter a *naptárkivételhez RecurrenceType érték* paraméter által megadott egységet használja.</span><span class="sxs-lookup"><span data-stu-id="e283b-133">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e283b-134">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="e283b-134">-RetentionCount</span></span>
<span data-ttu-id="e283b-135">A biztonsági másolat megtartására szolgáló napok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e283b-135">Specifies the number of days to keep a backup.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e283b-136">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="e283b-136">-StartFromDateTime</span></span>
<span data-ttu-id="e283b-137">A biztonsági másolatok készítésének kezdési dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e283b-137">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="e283b-138">Az alapértelmezett érték az aktuális idő.</span><span class="sxs-lookup"><span data-stu-id="e283b-138">The default value is the current time.</span></span>

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

### <span data-ttu-id="e283b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e283b-139">CommonParameters</span></span>
<span data-ttu-id="e283b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e283b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e283b-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e283b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e283b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e283b-142">INPUTS</span></span>

### <span data-ttu-id="e283b-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="e283b-143">None</span></span>

## <span data-ttu-id="e283b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e283b-144">OUTPUTS</span></span>

### <span data-ttu-id="e283b-145">BackupScheduleUpdateRequest</span><span class="sxs-lookup"><span data-stu-id="e283b-145">BackupScheduleUpdateRequest</span></span>
<span data-ttu-id="e283b-146">Ez a parancsmag egy **BackupScheduleUpdateRequest** objektumot ad eredményül, amely a frissített biztonsági ütemtervekre vonatkozó információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e283b-146">This cmdlet returns a **BackupScheduleUpdateRequest** object that contains information about updated backup schedules.</span></span>

## <span data-ttu-id="e283b-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e283b-147">NOTES</span></span>

## <span data-ttu-id="e283b-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e283b-148">RELATED LINKS</span></span>

[<span data-ttu-id="e283b-149">Új – AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="e283b-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[<span data-ttu-id="e283b-150">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e283b-150">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


