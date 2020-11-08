---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016467"
---
# <span data-ttu-id="c3cff-101">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="c3cff-101">Remove-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="c3cff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3cff-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cff-103">Törli a biztonsági másolatot tartalmazó objektumot.</span><span class="sxs-lookup"><span data-stu-id="c3cff-103">Deletes a backup object.</span></span>

## <span data-ttu-id="c3cff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3cff-104">SYNTAX</span></span>

### <span data-ttu-id="c3cff-105">IdentifyById (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3cff-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3cff-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="c3cff-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c3cff-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3cff-107">DESCRIPTION</span></span>
<span data-ttu-id="c3cff-108">A **Remove-AzureStorSimpleDeviceBackup** parancsmag egyetlen biztonságimásolat-objektumot töröl.</span><span class="sxs-lookup"><span data-stu-id="c3cff-108">The **Remove-AzureStorSimpleDeviceBackup** cmdlet deletes a single backup object.</span></span>
<span data-ttu-id="c3cff-109">Ha már törölt biztonsági másolatot próbál törölni, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="c3cff-109">If you attempt to delete a backup that has already been deleted, this cmdlet returns an error.</span></span>

## <span data-ttu-id="c3cff-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c3cff-110">EXAMPLES</span></span>

### <span data-ttu-id="c3cff-111">1. példa: biztonsági másolat eltávolítása az eszközről</span><span class="sxs-lookup"><span data-stu-id="c3cff-111">Example 1: Remove a backup for a device</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

<span data-ttu-id="c3cff-112">Ez a parancs eltávolítja a Contoso63-AppVm nevű eszközhöz megadott azonosítót tartalmazó biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="c3cff-112">This command removes the backup that has the specified ID for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="c3cff-113">A parancs elindítja azt a műveletet, amely eltávolítja a **biztonságimásolat** -objektumot, majd egy **TaskResponse** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c3cff-113">The command starts the operation that removes the **Backup** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="c3cff-114">A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c3cff-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="c3cff-115">2. példa: az eszköz első biztonsági másolatának eltávolítása az azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="c3cff-115">Example 2: Remove the first backup for a device by using its ID</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

<span data-ttu-id="c3cff-116">Az első parancs a Contoso63-AppVm nevű eszköz biztonsági másolatait kapja, majd a $Backup változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="c3cff-116">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="c3cff-117">A második parancs törli az Contoso63-AppVm nevű eszköz biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="c3cff-117">The second command deletes a backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="c3cff-118">A parancs normál képpont jelöléssel hivatkozik a $Backup tömb első eleme **InstanceId** tulajdonságára.</span><span class="sxs-lookup"><span data-stu-id="c3cff-118">The command uses standard dot notation to refer to the **InstanceId** property of the first element of the $Backup array.</span></span>
<span data-ttu-id="c3cff-119">Ez a parancs a *WaitForComplete* paramétert adja meg, ezért a parancs mindaddig megvárja, amíg a művelet be nem fejeződik, majd egy **TaskStatusInfo** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c3cff-119">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="c3cff-120">3. példa: az eszköz első biztonsági másolatának eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="c3cff-120">Example 3: Remove the first backup for a device by using the pipeline</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

<span data-ttu-id="c3cff-121">Az első parancs a Contoso63-AppVm nevű eszköz biztonsági másolatait kapja, majd a $Backup változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="c3cff-121">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="c3cff-122">A második parancs átadja az első objektumot a $Backup tömbben az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="c3cff-122">The second command passes the first object stored in the $Backup array to the current cmdlet.</span></span>
<span data-ttu-id="c3cff-123">Ez a parancsmag törli azt a biztonsági másolatot a Contoso63-AppVm nevű eszközről.</span><span class="sxs-lookup"><span data-stu-id="c3cff-123">That cmdlet deletes that backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="c3cff-124">Ez a parancs a *WaitForComplete* paramétert adja meg, ezért a parancs mindaddig megvárja, amíg a művelet be nem fejeződik, majd egy **TaskStatusInfo** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c3cff-124">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="c3cff-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3cff-125">PARAMETERS</span></span>

### <span data-ttu-id="c3cff-126">-Backup</span><span class="sxs-lookup"><span data-stu-id="c3cff-126">-Backup</span></span>
<span data-ttu-id="c3cff-127">A törlendő **biztonságimásolat** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3cff-127">Specifies the **Backup** object to delete.</span></span>
<span data-ttu-id="c3cff-128">**Biztonsági másolat készítéséhez** használja a **Get-AzureStorSimpleDeviceBackup** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c3cff-128">To obtain a **Backup** object, use the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3cff-129">-BackupId</span><span class="sxs-lookup"><span data-stu-id="c3cff-129">-BackupId</span></span>
<span data-ttu-id="c3cff-130">A törlendő biztonsági másolat példányának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3cff-130">Specifies the instance ID of a backup to delete.</span></span>

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

### <span data-ttu-id="c3cff-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c3cff-131">-DeviceName</span></span>
<span data-ttu-id="c3cff-132">Annak a StorSimple-eszköznek a nevét adja meg, amelyen törölni szeretne egy biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="c3cff-132">Specifies the name of the StorSimple device on which to delete a backup.</span></span>

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

### <span data-ttu-id="c3cff-133">-Force</span><span class="sxs-lookup"><span data-stu-id="c3cff-133">-Force</span></span>
<span data-ttu-id="c3cff-134">Azt jelzi, hogy ez a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3cff-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="c3cff-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="c3cff-135">-Profile</span></span>
<span data-ttu-id="c3cff-136">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="c3cff-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="c3cff-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="c3cff-137">-WaitForComplete</span></span>
<span data-ttu-id="c3cff-138">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="c3cff-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="c3cff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cff-139">CommonParameters</span></span>
<span data-ttu-id="c3cff-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3cff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cff-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3cff-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cff-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3cff-142">INPUTS</span></span>

### <span data-ttu-id="c3cff-143">Hát</span><span class="sxs-lookup"><span data-stu-id="c3cff-143">Backup</span></span>

## <span data-ttu-id="c3cff-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3cff-144">OUTPUTS</span></span>

### <span data-ttu-id="c3cff-145">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="c3cff-145">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="c3cff-146">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg, ha nem adja meg ezt a paramétert, hanem egy **TaskResponse** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c3cff-146">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="c3cff-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3cff-147">NOTES</span></span>

## <span data-ttu-id="c3cff-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3cff-148">RELATED LINKS</span></span>

[<span data-ttu-id="c3cff-149">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="c3cff-149">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)


