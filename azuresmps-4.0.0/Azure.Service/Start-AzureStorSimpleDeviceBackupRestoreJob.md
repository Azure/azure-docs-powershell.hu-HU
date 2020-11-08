---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015747"
---
# <span data-ttu-id="9fab3-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="9fab3-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>

## <span data-ttu-id="9fab3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fab3-102">SYNOPSIS</span></span>
<span data-ttu-id="9fab3-103">Elindítja azt a feladatot, amely egy StorSimple-eszköz biztonsági másolatát Visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="9fab3-103">Starts a job that restores a backup on a StorSimple device.</span></span>

## <span data-ttu-id="9fab3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fab3-104">SYNTAX</span></span>

### <span data-ttu-id="9fab3-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9fab3-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9fab3-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="9fab3-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9fab3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fab3-107">DESCRIPTION</span></span>
<span data-ttu-id="9fab3-108">A **Start-AzureStorSimpleDeviceBackupRestoreJob** parancsmag olyan feladatot kezd el, amely visszaállítja a StorSimple-eszközök biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="9fab3-108">The **Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet starts a job that restores a backup on a StorSimple device.</span></span>
<span data-ttu-id="9fab3-109">Adja meg a biztonságimásolat-azonosítót és a választható pillanatkép-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="9fab3-109">Specify a backup ID and an optional snapshot ID.</span></span>

## <span data-ttu-id="9fab3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9fab3-110">EXAMPLES</span></span>

### <span data-ttu-id="9fab3-111">1. példa: feladat indítása a biztonsági másolat visszaállításához</span><span class="sxs-lookup"><span data-stu-id="9fab3-111">Example 1: Start a job to restore a backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

<span data-ttu-id="9fab3-112">Ez a parancs elindítja azt a feladatot, amely visszaállítja a megadott azonosítót tartalmazó biztonságimásolat-objektumot és a hozzá tartozó pillanatképeket az Contoso63-AppVm nevű eszközön.</span><span class="sxs-lookup"><span data-stu-id="9fab3-112">This command starts a job that restores the backup object that has the specified ID, and its associated snapshots, on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="9fab3-113">A parancs a *WaitForComplete* paramétert adja meg, így a feladat befejeződött, mielőtt a parancsmag a vezérlőt visszaadja a konzolnak.</span><span class="sxs-lookup"><span data-stu-id="9fab3-113">The command specifies the *WaitForComplete* parameter, so the job finishes before the cmdlet returns control to the console.</span></span>

### <span data-ttu-id="9fab3-114">2. példa: feladat indítása egy adott pillanatkép visszaállításához</span><span class="sxs-lookup"><span data-stu-id="9fab3-114">Example 2: Start a job to restore a specific snapshot</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

<span data-ttu-id="9fab3-115">Ez a parancs elindítja azt a feladatot, amely visszaállítja a megadott azonosítót tartalmazó biztonságimásolat-pillanatfelvételt.</span><span class="sxs-lookup"><span data-stu-id="9fab3-115">This command starts a job that restores the backup snapshot that has the specified ID.</span></span>
<span data-ttu-id="9fab3-116">A parancs azt adja meg, hogy a Contoso63-AppVm nevű eszközben a biztonsági másolat objektum AZONOSÍTÓval rendelkezik-e.</span><span class="sxs-lookup"><span data-stu-id="9fab3-116">The command specifies the backup object by ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="9fab3-117">A parancs az *erő* paramétert adja meg, ezért a feladatot a megerősítést kérő üzenet nélkül indítja el.</span><span class="sxs-lookup"><span data-stu-id="9fab3-117">The command specifies the *Force* parameter, so it starts the job without prompting you to confirm.</span></span>

## <span data-ttu-id="9fab3-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fab3-118">PARAMETERS</span></span>

### <span data-ttu-id="9fab3-119">-BackupId</span><span class="sxs-lookup"><span data-stu-id="9fab3-119">-BackupId</span></span>
<span data-ttu-id="9fab3-120">A visszaállítandó biztonsági másolat példányának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fab3-120">Specifies the instance ID of the backup to restore.</span></span>

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

### <span data-ttu-id="9fab3-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9fab3-121">-DeviceName</span></span>
<span data-ttu-id="9fab3-122">Annak a StorSimple-eszköznek a nevét adja meg, amelyen a biztonsági másolat létezik.</span><span class="sxs-lookup"><span data-stu-id="9fab3-122">Specifies the name of the StorSimple device on which the backup exists.</span></span>

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

### <span data-ttu-id="9fab3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9fab3-123">-Force</span></span>
<span data-ttu-id="9fab3-124">Azt jelzi, hogy ez a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9fab3-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="9fab3-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="9fab3-125">-Profile</span></span>
<span data-ttu-id="9fab3-126">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="9fab3-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9fab3-127">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="9fab3-127">-SnapshotId</span></span>
<span data-ttu-id="9fab3-128">A visszaállítandó pillanatkép példányának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fab3-128">Specifies the instance ID of the snapshot to restore.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fab3-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="9fab3-129">-WaitForComplete</span></span>
<span data-ttu-id="9fab3-130">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="9fab3-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="9fab3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fab3-131">CommonParameters</span></span>
<span data-ttu-id="9fab3-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fab3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fab3-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fab3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fab3-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fab3-134">INPUTS</span></span>

### <span data-ttu-id="9fab3-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="9fab3-135">None</span></span>

## <span data-ttu-id="9fab3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fab3-136">OUTPUTS</span></span>

### <span data-ttu-id="9fab3-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="9fab3-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="9fab3-138">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fab3-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="9fab3-139">Ha nem adja meg ezt a paramétert, az eredmény egy **TaskResponse** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="9fab3-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="9fab3-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fab3-140">NOTES</span></span>

## <span data-ttu-id="9fab3-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fab3-141">RELATED LINKS</span></span>

[<span data-ttu-id="9fab3-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="9fab3-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="9fab3-143">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="9fab3-143">Start-AzureStorSimpleDeviceBackupJob</span></span>](./Start-AzureStorSimpleDeviceBackupJob.md)


