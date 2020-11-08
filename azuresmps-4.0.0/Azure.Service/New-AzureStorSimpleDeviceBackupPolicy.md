---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016208"
---
# <span data-ttu-id="9add0-101">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9add0-101">New-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="9add0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9add0-102">SYNOPSIS</span></span>
<span data-ttu-id="9add0-103">Biztonsági házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9add0-103">Creates a backup policy.</span></span>

## <span data-ttu-id="9add0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9add0-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9add0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9add0-105">DESCRIPTION</span></span>
<span data-ttu-id="9add0-106">A **New-AzureStorSimpleDeviceBackupPolicy** parancsmag biztonsági mentési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9add0-106">The **New-AzureStorSimpleDeviceBackupPolicy** cmdlet creates a backup policy.</span></span>
<span data-ttu-id="9add0-107">A biztonsági házirend egy vagy több köteten futtatható biztonsági ütemtervet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9add0-107">A backup policy contains one or more backup schedules that can run on one or more volumes.</span></span>
<span data-ttu-id="9add0-108">Ha biztonsági ütemtervet szeretne létrehozni, használja a **New-AzureStorSimpleDeviceBackupScheduleAddConfig** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9add0-108">To create a backup schedule, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

## <span data-ttu-id="9add0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9add0-109">EXAMPLES</span></span>

### <span data-ttu-id="9add0-110">1. példa: biztonsági házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="9add0-110">Example 1: Create a backup policy</span></span>
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="9add0-111">Az első parancs a **New-AzureStorSimpleDeviceBackupScheduleAddConfig** parancsmaggal hozza létre a biztonsági ütemterv konfigurációs objektumát, majd az $Schedule 01 változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="9add0-111">The first command creates a backup schedule configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet, and then stores that object in the $Schedule01 variable.</span></span>

<span data-ttu-id="9add0-112">A második parancs új biztonsági konfigurációs objektumot hoz létre a **New-AzureStorSimpleDeviceBackupScheduleAddConfig** használatával, majd az objektumot a $Schedule 02 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9add0-112">The second command creates another backup configuration object by using **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , and then stores that object in the $Schedule02 variable.</span></span>

<span data-ttu-id="9add0-113">A harmadik parancs létrehozza a $ScheduleArray nevű üres tömbös változót.</span><span class="sxs-lookup"><span data-stu-id="9add0-113">The third command creates an empty array variable, named $ScheduleArray.</span></span>
<span data-ttu-id="9add0-114">A következő két parancs hozzáadja az első két parancsban létrehozott objektumokat a $ScheduleArrayhoz.</span><span class="sxs-lookup"><span data-stu-id="9add0-114">The next two commands add the objects created in the first two commands to $ScheduleArray.</span></span>

<span data-ttu-id="9add0-115">A hatodik parancs a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmag használatával kapja meg a Contoso63-AppVm nevű eszköz mennyiségi tárolóját, majd a tároló objektumot a $DeviceContainer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9add0-115">The sixth command gets a volume container for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet, and then stores that container object in the $DeviceContainer variable.</span></span>

<span data-ttu-id="9add0-116">A hetedik parancs a **Get-AzureStorSimpleDeviceVolume** parancsmaggal az $DeviceContainer első tagjában tárolt mennyiségi tároló kötetét kapja, majd a $Volume változóban tárolja a kötetet.</span><span class="sxs-lookup"><span data-stu-id="9add0-116">The seventh command gets a volume for the volume container stored in the first member of $DeviceContainer by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then stores that volume in the $Volume variable.</span></span>

<span data-ttu-id="9add0-117">A nyolcadik parancs létrehozza az $VolumeArray nevű üres tömbös változót.</span><span class="sxs-lookup"><span data-stu-id="9add0-117">The eighth command creates an empty array variable, named $VolumeArray.</span></span>
<span data-ttu-id="9add0-118">A következő parancs mennyiségi azonosítót ad a $VolumeArrayhoz.</span><span class="sxs-lookup"><span data-stu-id="9add0-118">The next command adds a volume ID to $VolumeArray.</span></span>
<span data-ttu-id="9add0-119">Ez az érték azonosítja azt a kötetet, amelyet a biztonsági házirend futásakor $Volume tárolnak.</span><span class="sxs-lookup"><span data-stu-id="9add0-119">This value identifies the volume, stored in $Volume, on which the backup policy runs.</span></span>
<span data-ttu-id="9add0-120">További mennyiségi azonosítókat is hozzáadhat a $VolumeArrayhoz.</span><span class="sxs-lookup"><span data-stu-id="9add0-120">You can add additional volume IDs to $VolumeArray.</span></span>

<span data-ttu-id="9add0-121">A végleges parancs létrehozza a GeneralPolicy07 nevű biztonsági mentési házirendet a Contoso63-AppVm nevű eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="9add0-121">The final command creates the backup policy named GeneralPolicy07 for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="9add0-122">A parancs a $ScheduleArrayban tárolt konfiguráció-objektumok ütemezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="9add0-122">The command specifies the schedule configuration objects stored in $ScheduleArray.</span></span>
<span data-ttu-id="9add0-123">A parancs azt a kötetet vagy köteteket adja meg, amelyekre a házirendet alkalmazni szeretné $VolumeArrayben.</span><span class="sxs-lookup"><span data-stu-id="9add0-123">The command specifies the volume or volumes to which to apply the policy in $VolumeArray.</span></span>
<span data-ttu-id="9add0-124">Ellenőrizheti a biztonságimásolat-házirendet a **Get-AzureStorSimpleDeviceBackupPolicy** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="9add0-124">You can verify the backup policy by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="9add0-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9add0-125">PARAMETERS</span></span>

### <span data-ttu-id="9add0-126">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="9add0-126">-BackupPolicyName</span></span>
<span data-ttu-id="9add0-127">A biztonságimásolat-házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9add0-127">Specifies the name of the backup policy.</span></span>

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

### <span data-ttu-id="9add0-128">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="9add0-128">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="9add0-129">A házirendhez hozzáadni kívánt **BackupScheduleBase** -objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9add0-129">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="9add0-130">Minden objektum ütemtervet képvisel.</span><span class="sxs-lookup"><span data-stu-id="9add0-130">Each object represents a schedule.</span></span>
<span data-ttu-id="9add0-131">A biztonságimásolat-házirend egy vagy több ütemtervet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9add0-131">A backup policy contains one or more schedules.</span></span>
<span data-ttu-id="9add0-132">**BackupScheduleBase** -objektum beolvasásához használja a **New-AzureStorSimpleDeviceBackupScheduleAddConfig** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9add0-132">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9add0-133">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9add0-133">-DeviceName</span></span>
<span data-ttu-id="9add0-134">Annak a StorSimple-eszköznek a nevét adja meg, amelyen létre szeretné hozni a biztonsági házirendet.</span><span class="sxs-lookup"><span data-stu-id="9add0-134">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="9add0-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="9add0-135">-Profile</span></span>
<span data-ttu-id="9add0-136">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="9add0-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9add0-137">-VolumeIdsToAdd</span><span class="sxs-lookup"><span data-stu-id="9add0-137">-VolumeIdsToAdd</span></span>
<span data-ttu-id="9add0-138">A biztonságimásolat-házirendhez hozzáadni kívánt kötetek azonosítóinak tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9add0-138">Specifies an array of the IDs of volumes to add to the backup policy.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9add0-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="9add0-139">-WaitForComplete</span></span>
<span data-ttu-id="9add0-140">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="9add0-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="9add0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9add0-141">CommonParameters</span></span>
<span data-ttu-id="9add0-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9add0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9add0-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9add0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9add0-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9add0-144">INPUTS</span></span>

### <span data-ttu-id="9add0-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="9add0-145">None</span></span>

## <span data-ttu-id="9add0-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9add0-146">OUTPUTS</span></span>

### <span data-ttu-id="9add0-147">BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9add0-147">BackupPolicy</span></span>
<span data-ttu-id="9add0-148">Ez a parancsmag egy **BackupPolicy** objektumot ad eredményül, amely az új ütemterveket és köteteket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9add0-148">This cmdlet returns a **BackupPolicy** object that contains the new schedules and volumes.</span></span>

## <span data-ttu-id="9add0-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9add0-149">NOTES</span></span>

## <span data-ttu-id="9add0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9add0-150">RELATED LINKS</span></span>

[<span data-ttu-id="9add0-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9add0-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="9add0-152">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9add0-152">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="9add0-153">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9add0-153">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="9add0-154">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9add0-154">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="9add0-155">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9add0-155">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="9add0-156">Új – AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="9add0-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


