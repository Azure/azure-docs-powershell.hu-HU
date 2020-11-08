---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5AB916CB-A141-4662-8220-6C1FBB58FC69
online version: ''
schema: 2.0.0
ms.openlocfilehash: aab5e0f3ef432333eeb4aff68673c0d5c2219521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016464"
---
# <span data-ttu-id="47d1f-101">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="47d1f-101">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="47d1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="47d1f-103">Eltávolít egy meglévő biztonsági házirendet.</span><span class="sxs-lookup"><span data-stu-id="47d1f-103">Removes an existing backup policy.</span></span>

## <span data-ttu-id="47d1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47d1f-104">SYNTAX</span></span>

### <span data-ttu-id="47d1f-105">IdentifyById (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47d1f-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="47d1f-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="47d1f-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="47d1f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="47d1f-107">DESCRIPTION</span></span>
<span data-ttu-id="47d1f-108">A **Remove-AzureStorSimpleDeviceBackupPolicy** parancsmag eltávolítja a meglévő **BackupPolicy** -objektumokat.</span><span class="sxs-lookup"><span data-stu-id="47d1f-108">The **Remove-AzureStorSimpleDeviceBackupPolicy** cmdlet removes an existing **BackupPolicy** object.</span></span>
<span data-ttu-id="47d1f-109">Miután eltávolította a biztonsági házirendet, az adott házirend alapján további biztonsági másolatokat nem kell mentenie.</span><span class="sxs-lookup"><span data-stu-id="47d1f-109">After you remove a backup policy, no further backups take place based on that policy.</span></span>
<span data-ttu-id="47d1f-110">Ez a parancsmag a törölt házirendhez társított összes ütemtervet is törli.</span><span class="sxs-lookup"><span data-stu-id="47d1f-110">This cmdlet also deletes all schedules associated with the deleted policy.</span></span>

## <span data-ttu-id="47d1f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="47d1f-111">EXAMPLES</span></span>

### <span data-ttu-id="47d1f-112">1. példa: biztonsági házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="47d1f-112">Example 1: Remove a backup policy</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "03710b4c-82c1-40ca-be5c-40289dc49642" -Force
VERBOSE: ClientRequestId: b3e4d485-eae4-4cf4-a43b-815f3abcd2dd_PS
VERBOSE: ClientRequestId: a260ee98-46aa-49e0-91ac-31d4155f4cae_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: 92a9c264-90df-4345-a495-92767dd266f2_PS
695be190-ac81-4cf2-b1c5-03ef6b08d005
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
695be190-ac81-4cf2-b1c5-03ef6b08d005 for tracking the task's status
```

<span data-ttu-id="47d1f-113">Ez a parancs eltávolítja azt a **BackupPolicy** , amely a példány-azonosítóval rendelkezik, így a rendszer nem készít további biztonsági másolatokat a 03710b4c-82c1-40Ca-be5c-40289dc49642.</span><span class="sxs-lookup"><span data-stu-id="47d1f-113">This command removes the **BackupPolicy** that has the instance ID 03710b4c-82c1-40ca-be5c-40289dc49642, so that no more backups are made based on this policy.</span></span>
<span data-ttu-id="47d1f-114">A parancs törli az ehhez a házirendhez társított összes ütemtervet is.</span><span class="sxs-lookup"><span data-stu-id="47d1f-114">The command also deletes all schedules associated with this policy.</span></span>
<span data-ttu-id="47d1f-115">A parancs elindítja azt a műveletet, amely eltávolítja a **BackupPolicy** objektumot, majd egy **TaskResponse** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="47d1f-115">The command starts the operation that removes the **BackupPolicy** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="47d1f-116">A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="47d1f-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="47d1f-117">2. példa: az eszközre vonatkozó biztonságimásolat-házirendek első részének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="47d1f-117">Example 2: Remove the first of the backup policies for a device</span></span>
```
PS C:\>$Policies = Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId $Policies[0].InstanceId -Force -WaitForComplete
VERBOSE: ClientRequestId: db3b49fa-cffa-446d-ba52-daa6802e00f7_PS
VERBOSE: ClientRequestId: 70e2b56f-c2df-40d0-a1e5-d7a4d7e25962_PS
VERBOSE: About to run a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: f8eb3d4d-2c57-4fc9-9f40-79d0f2ea1b6a_PS


JobId        : 820a246e-54b6-41a9-bdd5-15d5daea9b0a
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your remove operation has completed successfully.
```

<span data-ttu-id="47d1f-118">Az első parancs a Contoso63-AppVm nevű eszköz biztonságimásolat-házirendjeit kapja, majd a $Policies változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="47d1f-118">The first command gets the backup policies for the device named Contoso63-AppVm, and then stores them in the $Policies variable.</span></span>

<span data-ttu-id="47d1f-119">A második parancs eltávolítja az első biztonsági házirendet a Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="47d1f-119">The second command removes the first backup policy from Contoso63-AppVm.</span></span>
<span data-ttu-id="47d1f-120">A parancs a standard dot szintaxist használja a $Policies első elemének **InstanceId** tulajdonságának meghatározására.</span><span class="sxs-lookup"><span data-stu-id="47d1f-120">The command uses standard dot syntax to identify the **InstanceId** property of the first item in $Policies.</span></span>
<span data-ttu-id="47d1f-121">Ez a parancs a *WaitForComplete* paramétert adja meg, így a parancs végrehajtja a feladatot, majd egy **TaskStatusInfo** objektumot ad a tevékenységhez.</span><span class="sxs-lookup"><span data-stu-id="47d1f-121">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="47d1f-122">3. példa: biztonsági házirend eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="47d1f-122">Example 3: Remove a backup policy by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQAVolume01_Default" | Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -Force -WaitForComplete
VERBOSE: ClientRequestId: 60080fb1-2f88-4c17-bfd7-21aa73440a9c_PS
VERBOSE: ClientRequestId: 04c91121-50d7-4796-9af6-fc6a7d6b6a0e_PS
VERBOSE: ClientRequestId: 47ceb37c-672f-42e8-bd19-1190925c46cd_PS
VERBOSE: ClientRequestId: cbc39757-f2cc-4cc5-93ea-4ec0fbfb0ca8_PS
VERBOSE: ClientRequestId: 3614d47a-51fc-4500-a5f1-5401301ca4e3_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: dbd7166e-1888-4b11-9af9-8d49712a8c8b_PS
702ad240-5730-4015-b051-56055bd2c2d3
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
702ad240-5730-4015-b051-56055bd2c2d3 for tracking the task's status
VERBOSE: BackupPolicy with id bfe0bf8a-2d09-4690-93da-38a4f24e9f4f found!
```

<span data-ttu-id="47d1f-123">Ez a parancs beolvassa a **BackupPolicyDetails** objektumot a **Get-AzureStorSimpleDeviceBackupPolicy** függvénnyel, majd a pipeline operátor segítségével átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="47d1f-123">This command gets a **BackupPolicyDetails** object by using **Get-AzureStorSimpleDeviceBackupPolicy** , and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="47d1f-124">Az aktuális parancsmag eltávolítja a TSQAVolume01_Default nevű biztonsági házirendet.</span><span class="sxs-lookup"><span data-stu-id="47d1f-124">The current cmdlet removes the backup policy named TSQAVolume01_Default.</span></span>

## <span data-ttu-id="47d1f-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47d1f-125">PARAMETERS</span></span>

### <span data-ttu-id="47d1f-126">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="47d1f-126">-BackupPolicy</span></span>
<span data-ttu-id="47d1f-127">A törlendő **BackupPolicyDetails** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d1f-127">Specifies the **BackupPolicyDetails** object to delete.</span></span>
<span data-ttu-id="47d1f-128">Ha **BackupPolicyDetails** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleDeviceBackupPolicy** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="47d1f-128">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47d1f-129">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="47d1f-129">-BackupPolicyId</span></span>
<span data-ttu-id="47d1f-130">A törlendő **BackupPolicy** objektum PÉLDÁNYának azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d1f-130">Specifies the instance ID of the **BackupPolicy** object to delete.</span></span>

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

### <span data-ttu-id="47d1f-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="47d1f-131">-DeviceName</span></span>
<span data-ttu-id="47d1f-132">Annak a StorSimple-eszköznek a nevét adja meg, amelyen törölni szeretné a biztonsági házirendet.</span><span class="sxs-lookup"><span data-stu-id="47d1f-132">Specifies the name of the StorSimple device on which to delete the backup policy.</span></span>

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

### <span data-ttu-id="47d1f-133">-Force</span><span class="sxs-lookup"><span data-stu-id="47d1f-133">-Force</span></span>
<span data-ttu-id="47d1f-134">Azt jelzi, hogy ez a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47d1f-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="47d1f-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="47d1f-135">-Profile</span></span>
<span data-ttu-id="47d1f-136">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="47d1f-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="47d1f-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="47d1f-137">-WaitForComplete</span></span>
<span data-ttu-id="47d1f-138">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="47d1f-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="47d1f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d1f-139">CommonParameters</span></span>
<span data-ttu-id="47d1f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47d1f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d1f-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47d1f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d1f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47d1f-142">INPUTS</span></span>

### <span data-ttu-id="47d1f-143">BackupPolicyDetails</span><span class="sxs-lookup"><span data-stu-id="47d1f-143">BackupPolicyDetails</span></span>
<span data-ttu-id="47d1f-144">Ez a parancsmag a törölni kívánt **BackupPolicyDetails** objektumot fogadja.</span><span class="sxs-lookup"><span data-stu-id="47d1f-144">This cmdlet accepts a **BackupPolicyDetails** object to delete.</span></span>

## <span data-ttu-id="47d1f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47d1f-145">OUTPUTS</span></span>

### <span data-ttu-id="47d1f-146">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="47d1f-146">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="47d1f-147">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d1f-147">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="47d1f-148">Ha nem adja meg ezt a paramétert, az eredmény egy **TaskResponse** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="47d1f-148">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="47d1f-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47d1f-149">NOTES</span></span>

## <span data-ttu-id="47d1f-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47d1f-150">RELATED LINKS</span></span>

[<span data-ttu-id="47d1f-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="47d1f-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="47d1f-152">Új – AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="47d1f-152">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="47d1f-153">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="47d1f-153">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="47d1f-154">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="47d1f-154">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


