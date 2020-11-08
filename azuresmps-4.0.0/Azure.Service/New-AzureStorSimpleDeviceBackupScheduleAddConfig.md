---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015528"
---
# <span data-ttu-id="024bd-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="024bd-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>

## <span data-ttu-id="024bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="024bd-102">SYNOPSIS</span></span>
<span data-ttu-id="024bd-103">Biztonságimásolat-ütemterv konfigurációs objektumának létrehozása</span><span class="sxs-lookup"><span data-stu-id="024bd-103">Creates a backup schedule configuration object.</span></span>

## <span data-ttu-id="024bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="024bd-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="024bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="024bd-105">DESCRIPTION</span></span>
<span data-ttu-id="024bd-106">A **New-AzureStorSimpleDeviceBackupScheduleAddConfig** parancsmag létrehoz egy **BackupScheduleBase** konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="024bd-106">The **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet creates a **BackupScheduleBase** configuration object.</span></span>
<span data-ttu-id="024bd-107">Ezzel a konfigurációs objektummal új biztonsági házirendeket hozhat létre a **New-AzureStorSimpleDeviceBackupPolicy** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="024bd-107">Use this configuration object to create new backup policy by using the **New-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="024bd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="024bd-108">EXAMPLES</span></span>

### <span data-ttu-id="024bd-109">Példa 1: biztonságimásolat-konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="024bd-109">Example 1: Create a backup configuration object</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

<span data-ttu-id="024bd-110">Ez a parancs létrehoz egy biztonsági ütemezési alapobjektumot a felhőalapú pillanatkép biztonsági másolatai számára.</span><span class="sxs-lookup"><span data-stu-id="024bd-110">This command creates a backup schedule base object for cloud snapshot backups.</span></span>
<span data-ttu-id="024bd-111">A biztonsági másolat minden nap megismétlődik, és a biztonsági másolatok a 100 napokra kerülnek.</span><span class="sxs-lookup"><span data-stu-id="024bd-111">The backup occurs every day, and the backups are kept for 100 days.</span></span>
<span data-ttu-id="024bd-112">Ez az ütemezés az alapértelmezett időponttól, azaz az aktuális időponttól engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="024bd-112">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="024bd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="024bd-113">PARAMETERS</span></span>

### <span data-ttu-id="024bd-114">-BackupType</span><span class="sxs-lookup"><span data-stu-id="024bd-114">-BackupType</span></span>
<span data-ttu-id="024bd-115">A biztonságimásolat-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="024bd-115">Specifies the backup type.</span></span>
<span data-ttu-id="024bd-116">Az érvényes értékek a következők: LocalSnapshot és CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="024bd-116">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="024bd-117">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="024bd-117">-Enabled</span></span>
<span data-ttu-id="024bd-118">Azt jelzi, hogy engedélyezi-e a biztonsági ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="024bd-118">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024bd-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="024bd-119">-Profile</span></span>
<span data-ttu-id="024bd-120">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="024bd-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="024bd-121">-Naptárkivételhez RecurrenceType érték</span><span class="sxs-lookup"><span data-stu-id="024bd-121">-RecurrenceType</span></span>
<span data-ttu-id="024bd-122">A biztonságimásolat-ütemterv ismétlődési típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="024bd-122">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="024bd-123">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="024bd-123">Valid values are:</span></span> 

- <span data-ttu-id="024bd-124">Perc</span><span class="sxs-lookup"><span data-stu-id="024bd-124">Minutes</span></span>
- <span data-ttu-id="024bd-125">Óránkénti</span><span class="sxs-lookup"><span data-stu-id="024bd-125">Hourly</span></span>
- <span data-ttu-id="024bd-126">Napi</span><span class="sxs-lookup"><span data-stu-id="024bd-126">Daily</span></span>
- <span data-ttu-id="024bd-127">Heti</span><span class="sxs-lookup"><span data-stu-id="024bd-127">Weekly</span></span>

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

### <span data-ttu-id="024bd-128">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="024bd-128">-RecurrenceValue</span></span>
<span data-ttu-id="024bd-129">Megadja, hogy milyen gyakran készítsen biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="024bd-129">Specifies how often to make a backup.</span></span>
<span data-ttu-id="024bd-130">Ez a paraméter a *naptárkivételhez RecurrenceType érték* paraméter által megadott egységet használja.</span><span class="sxs-lookup"><span data-stu-id="024bd-130">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

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

### <span data-ttu-id="024bd-131">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="024bd-131">-RetentionCount</span></span>
<span data-ttu-id="024bd-132">A biztonsági másolat megtartására szolgáló napok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="024bd-132">Specifies the number of days to keep a backup.</span></span>

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

### <span data-ttu-id="024bd-133">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="024bd-133">-StartFromDateTime</span></span>
<span data-ttu-id="024bd-134">A biztonsági másolatok készítésének kezdési dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="024bd-134">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="024bd-135">Az alapértelmezett érték az aktuális idő.</span><span class="sxs-lookup"><span data-stu-id="024bd-135">The default value is the current time.</span></span>

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

### <span data-ttu-id="024bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024bd-136">CommonParameters</span></span>
<span data-ttu-id="024bd-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="024bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024bd-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="024bd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024bd-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="024bd-139">INPUTS</span></span>

### <span data-ttu-id="024bd-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="024bd-140">None</span></span>

## <span data-ttu-id="024bd-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="024bd-141">OUTPUTS</span></span>

### <span data-ttu-id="024bd-142">BackupScheduleBase</span><span class="sxs-lookup"><span data-stu-id="024bd-142">BackupScheduleBase</span></span>
<span data-ttu-id="024bd-143">Ez a parancsmag egy **BackupScheduleBase** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="024bd-143">This cmdlet returns a **BackupScheduleBase** object.</span></span>
<span data-ttu-id="024bd-144">Új biztonsági házirend létrehozása **BackupScheduleBase** használatával</span><span class="sxs-lookup"><span data-stu-id="024bd-144">Use a **BackupScheduleBase** to construct new backup policy.</span></span>

## <span data-ttu-id="024bd-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="024bd-145">NOTES</span></span>

## <span data-ttu-id="024bd-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="024bd-146">RELATED LINKS</span></span>

[<span data-ttu-id="024bd-147">Új – AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="024bd-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[<span data-ttu-id="024bd-148">Új – AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="024bd-148">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)


