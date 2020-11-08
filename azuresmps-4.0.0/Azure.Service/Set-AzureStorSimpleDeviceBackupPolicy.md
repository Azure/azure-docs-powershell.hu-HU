---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015852"
---
# <span data-ttu-id="da623-101">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="da623-101">Set-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="da623-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da623-102">SYNOPSIS</span></span>
<span data-ttu-id="da623-103">Frissít egy meglévő biztonsági házirendet.</span><span class="sxs-lookup"><span data-stu-id="da623-103">Updates an existing backup policy.</span></span>

## <span data-ttu-id="da623-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da623-104">SYNTAX</span></span>

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="da623-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da623-105">DESCRIPTION</span></span>
<span data-ttu-id="da623-106">A **set-AzureStorSimpleDeviceBackupPolicy** parancsmag egy meglévő biztonsági házirendet frissít.</span><span class="sxs-lookup"><span data-stu-id="da623-106">The **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet updates an existing backup policy.</span></span>
<span data-ttu-id="da623-107">Átnevezheti a házirendet, megadhatja, frissítheti vagy törölheti az ütemezéseket, illetve frissítheti a házirendhez társított köteteket.</span><span class="sxs-lookup"><span data-stu-id="da623-107">You can rename the policy, add, update or delete schedules, and update the volumes associated with the policy.</span></span>

## <span data-ttu-id="da623-108">Példák</span><span class="sxs-lookup"><span data-stu-id="da623-108">EXAMPLES</span></span>

### <span data-ttu-id="da623-109">1. példa: biztonsági házirend nevének módosítása</span><span class="sxs-lookup"><span data-stu-id="da623-109">Example 1: Change the name of a backup policy</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="da623-110">Ez a parancs megváltoztatja annak a biztonságimásolat-házirendnek a nevét, amely a UpdatedGeneralPolicy07 megadott azonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="da623-110">This command changes the name of the backup policy that has the specified ID to UpdatedGeneralPolicy07.</span></span>
<span data-ttu-id="da623-111">Ez a parancs a *WaitForComplete* paramétert adja meg, így a parancs végrehajtja a feladatot, majd egy **TaskStatusInfo** objektumot ad a tevékenységhez.</span><span class="sxs-lookup"><span data-stu-id="da623-111">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="da623-112">2. példa: biztonsági mentési házirend ütemezésének frissítése</span><span class="sxs-lookup"><span data-stu-id="da623-112">Example 2: Update the schedule for a backup policy</span></span>
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

<span data-ttu-id="da623-113">Az első parancs létrehoz egy Update Configuration objectt a **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** parancsmag használatával, majd a $UpdateConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="da623-113">The first command creates an update configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet, and then stores it in the $UpdateConfig variable.</span></span>

<span data-ttu-id="da623-114">A második parancs létrehoz egy új tömbös változót, az $UpdateArray nevűt.</span><span class="sxs-lookup"><span data-stu-id="da623-114">The second command creates a new array variable, named $UpdateArray.</span></span>
<span data-ttu-id="da623-115">A következő parancs hozzáadja a $UpdateConfigban tárolt frissítést a tömbhöz.</span><span class="sxs-lookup"><span data-stu-id="da623-115">The next command adds the update stored in $UpdateConfig to that array.</span></span>
<span data-ttu-id="da623-116">A tömbhöz több frissítést is hozzáadhat.</span><span class="sxs-lookup"><span data-stu-id="da623-116">You can add more than one update to the array.</span></span>

<span data-ttu-id="da623-117">A végleges parancs frissíti a Contoso63-AppVm nevű eszközön megadott azonosítót tartalmazó biztonsági házirendet.</span><span class="sxs-lookup"><span data-stu-id="da623-117">The final command updates the backup policy that has the specified ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="da623-118">A házirend most már a $UpdateArray tárolt frissített ütemtervet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="da623-118">The policy now has the updated schedule stored in $UpdateArray.</span></span>

## <span data-ttu-id="da623-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da623-119">PARAMETERS</span></span>

### <span data-ttu-id="da623-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="da623-120">-BackupPolicyId</span></span>
<span data-ttu-id="da623-121">A frissítendő **BackupPolicy** objektum PÉLDÁNYának azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="da623-121">Specifies the instance ID of the **BackupPolicy** object to update.</span></span>

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

### <span data-ttu-id="da623-122">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="da623-122">-BackupPolicyName</span></span>
<span data-ttu-id="da623-123">A biztonságimásolat-házirend új nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da623-123">Specifies a new name for the backup policy.</span></span>

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

### <span data-ttu-id="da623-124">-BackupScheduleIdsToDelete</span><span class="sxs-lookup"><span data-stu-id="da623-124">-BackupScheduleIdsToDelete</span></span>
<span data-ttu-id="da623-125">A törölni kívánt **BackupSchedule** -objektumok példány-azonosítóinak tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da623-125">Specifies an array of instance IDs of **BackupSchedule** objects to delete.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-126">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="da623-126">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="da623-127">A házirendhez hozzáadni kívánt **BackupScheduleBase** -objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da623-127">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="da623-128">**BackupScheduleBase** -objektum beolvasásához használja a **New-AzureStorSimpleDeviceBackupScheduleAddConfig** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="da623-128">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-129">-BackupSchedulesToUpdate</span><span class="sxs-lookup"><span data-stu-id="da623-129">-BackupSchedulesToUpdate</span></span>
<span data-ttu-id="da623-130">A frissítendő **BackupScheduleUpdateRequest** -objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da623-130">Specifies an array of **BackupScheduleUpdateRequest** objects to update.</span></span>
<span data-ttu-id="da623-131">**BackupScheduleUpdateRequest** -objektum beolvasásához használja a **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="da623-131">To obtain a **BackupScheduleUpdateRequest** object, use the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="da623-132">-DeviceName</span></span>
<span data-ttu-id="da623-133">Annak a StorSimple-eszköznek a nevét adja meg, amelyre frissíteni szeretné a biztonsági házirendet.</span><span class="sxs-lookup"><span data-stu-id="da623-133">Specifies the name of the StorSimple device for which to update the backup policy.</span></span>

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

### <span data-ttu-id="da623-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="da623-134">-NewName</span></span>
<span data-ttu-id="da623-135">Az eszköz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da623-135">Specifies a name for the device.</span></span>

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

### <span data-ttu-id="da623-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="da623-136">-Profile</span></span>
<span data-ttu-id="da623-137">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="da623-137">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="da623-138">-VolumeIdsToUpdate</span><span class="sxs-lookup"><span data-stu-id="da623-138">-VolumeIdsToUpdate</span></span>
<span data-ttu-id="da623-139">A kötetek azonosítóit adja meg, amelyekre a biztonsági házirendek frissíthetők.</span><span class="sxs-lookup"><span data-stu-id="da623-139">Specifies an array of IDs of volumes for which to update backup policies.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da623-140">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="da623-140">-WaitForComplete</span></span>
<span data-ttu-id="da623-141">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="da623-141">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="da623-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da623-142">CommonParameters</span></span>
<span data-ttu-id="da623-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da623-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da623-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da623-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da623-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da623-145">INPUTS</span></span>

### <span data-ttu-id="da623-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="da623-146">None</span></span>

## <span data-ttu-id="da623-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da623-147">OUTPUTS</span></span>

### <span data-ttu-id="da623-148">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="da623-148">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="da623-149">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="da623-149">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="da623-150">Ha nem adja meg ezt a paramétert, az eredmény egy **TaskResponse** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="da623-150">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="da623-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da623-151">NOTES</span></span>

## <span data-ttu-id="da623-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da623-152">RELATED LINKS</span></span>

[<span data-ttu-id="da623-153">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="da623-153">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="da623-154">Új – AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="da623-154">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="da623-155">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="da623-155">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="da623-156">Új – AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="da623-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)


