---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016027"
---
# <span data-ttu-id="3f6c3-101">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="3f6c3-101">Start-AzureStorSimpleDeviceBackupJob</span></span>

## <span data-ttu-id="3f6c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6c3-103">Új munkát indít, amely biztonsági másolatot készít egy meglévő biztonsági házirendről.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-103">Starts a new job that creates a backup from an existing backup policy.</span></span>

## <span data-ttu-id="3f6c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f6c3-104">SYNTAX</span></span>

### <span data-ttu-id="3f6c3-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f6c3-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3f6c3-106">BackupTypeGiven</span><span class="sxs-lookup"><span data-stu-id="3f6c3-106">BackupTypeGiven</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f6c3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f6c3-107">DESCRIPTION</span></span>
<span data-ttu-id="3f6c3-108">A **Start-AzureStorSimpleDeviceBackupJob** parancsmag olyan új feladatot kezd el, amely biztonsági másolatot készít egy meglévő biztonsági házirendről egy StorSimple-eszközön.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-108">The **Start-AzureStorSimpleDeviceBackupJob** cmdlet starts a new job that creates a backup from an existing backup policy on a StorSimple device.</span></span>
<span data-ttu-id="3f6c3-109">Ez a parancsmag alapértelmezés szerint egy helyi pillanatkép biztonsági másolatát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-109">By default, this cmdlet creates a local snapshot backup.</span></span>
<span data-ttu-id="3f6c3-110">Ha Felhőbeli biztonsági másolatot szeretne készíteni, adja meg a CloudSnapshot értékét a *BackupType* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-110">To create a cloud backup, specify a value of CloudSnapshot for the *BackupType* parameter.</span></span>

## <span data-ttu-id="3f6c3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3f6c3-111">EXAMPLES</span></span>

### <span data-ttu-id="3f6c3-112">Példa 1: helyi pillanatkép biztonsági másolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="3f6c3-112">Example 1: Create a local snapshot backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

<span data-ttu-id="3f6c3-113">Ez a parancs létrehoz egy helyi pillanatkép-biztonsági másolatot a megadott házirend-AZONOSÍTÓhoz.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-113">This command creates a local snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="3f6c3-114">Ez a parancs elindítja a feladatot, majd egy **TaskResponse** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="3f6c3-115">A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="3f6c3-116">2. példa: felhőalapú pillanatkép biztonsági mentése és várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="3f6c3-116">Example 2: Create a cloud snapshot backup and wait to finish</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

<span data-ttu-id="3f6c3-117">Ezzel a paranccsal létrehoz egy felhőalapú pillanatkép biztonsági másolatát a megadott házirend-AZONOSÍTÓhoz.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-117">This command creates a cloud snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="3f6c3-118">Ez a parancs a *WaitForComplete* paramétert adja meg, így a parancs végrehajtja a feladatot, majd a feladat **TaskStatusInfo** objektumát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-118">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the job.</span></span>

## <span data-ttu-id="3f6c3-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f6c3-119">PARAMETERS</span></span>

### <span data-ttu-id="3f6c3-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="3f6c3-120">-BackupPolicyId</span></span>
<span data-ttu-id="3f6c3-121">A biztonsági másolat létrehozásához használandó biztonsági házirend AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-121">Specifies the ID of the backup policy to use to create the backup.</span></span>

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

### <span data-ttu-id="3f6c3-122">-BackupType</span><span class="sxs-lookup"><span data-stu-id="3f6c3-122">-BackupType</span></span>
<span data-ttu-id="3f6c3-123">A biztonságimásolat-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-123">Specifies the backup type.</span></span>
<span data-ttu-id="3f6c3-124">Az érvényes értékek a következők: LocalSnapshot és CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-124">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6c3-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3f6c3-125">-DeviceName</span></span>
<span data-ttu-id="3f6c3-126">Annak a StorSimple-eszköznek a nevét adja meg, amelyen a biztonsági mentési feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-126">Specifies the name of the StorSimple device on which to start the backup job.</span></span>

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

### <span data-ttu-id="3f6c3-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f6c3-127">-Profile</span></span>
<span data-ttu-id="3f6c3-128">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-128">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3f6c3-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="3f6c3-129">-WaitForComplete</span></span>
<span data-ttu-id="3f6c3-130">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="3f6c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6c3-131">CommonParameters</span></span>
<span data-ttu-id="3f6c3-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f6c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6c3-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f6c3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6c3-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f6c3-134">INPUTS</span></span>

### <span data-ttu-id="3f6c3-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="3f6c3-135">None</span></span>

## <span data-ttu-id="3f6c3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f6c3-136">OUTPUTS</span></span>

### <span data-ttu-id="3f6c3-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="3f6c3-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="3f6c3-138">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="3f6c3-139">Ha nem adja meg ezt a paramétert, az eredmény egy **TaskResponse** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3f6c3-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="3f6c3-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f6c3-140">NOTES</span></span>

## <span data-ttu-id="3f6c3-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f6c3-141">RELATED LINKS</span></span>

[<span data-ttu-id="3f6c3-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="3f6c3-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="3f6c3-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="3f6c3-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


