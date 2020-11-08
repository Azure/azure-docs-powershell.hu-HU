---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015748"
---
# <span data-ttu-id="2ab26-101">Start-AzureStorSimpleBackupCloneJob</span><span class="sxs-lookup"><span data-stu-id="2ab26-101">Start-AzureStorSimpleBackupCloneJob</span></span>

## <span data-ttu-id="2ab26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ab26-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab26-103">Elindítja azt a feladatot, amely egy eszköz biztonsági másolatát klónja.</span><span class="sxs-lookup"><span data-stu-id="2ab26-103">Starts a job that clones a backup on a device.</span></span>

## <span data-ttu-id="2ab26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ab26-104">SYNTAX</span></span>

### <span data-ttu-id="2ab26-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ab26-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2ab26-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="2ab26-106">IdentifyByName</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2ab26-107">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="2ab26-107">IdentifyById</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2ab26-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ab26-108">DESCRIPTION</span></span>
<span data-ttu-id="2ab26-109">A **Start-AzureStorSimpleBackupCloneJob** parancsmag olyan feladatot kezd el, amely egy StorSimple-eszköz meglévő biztonsági másolatát klónja.</span><span class="sxs-lookup"><span data-stu-id="2ab26-109">The **Start-AzureStorSimpleBackupCloneJob** cmdlet starts a job that clones an existing backup on a StorSimple device.</span></span>

## <span data-ttu-id="2ab26-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2ab26-110">EXAMPLES</span></span>

### <span data-ttu-id="2ab26-111">Példa 1: biztonsági másolat másolása másik kötetre az eszközök neveivel</span><span class="sxs-lookup"><span data-stu-id="2ab26-111">Example 1: Clone a backup to a different volume by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="2ab26-112">Az első parancs a **Get-AzureStorSimpleDeviceBackup** parancsmag használatával kapja meg a ContosoDev07 nevű eszköz első biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="2ab26-112">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="2ab26-113">A parancs a $Backup változóban tárolja a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="2ab26-113">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="2ab26-114">A második parancs a **Get-AzureStorSimpleAccessControlRecord** parancsmag használatával érheti el a rekordok vezérlését.</span><span class="sxs-lookup"><span data-stu-id="2ab26-114">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="2ab26-115">A parancs az eredményt a $Acrs változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2ab26-115">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="2ab26-116">A végleges parancs egy olyan munkafolyamatot kezd el, amely egy eszköz adott kötetének meghatározott biztonsági másolatát ugyanazon eszközön lévő másik kötetre másolta.</span><span class="sxs-lookup"><span data-stu-id="2ab26-116">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="2ab26-117">Ez a példa megadja az eszközt név szerint.</span><span class="sxs-lookup"><span data-stu-id="2ab26-117">This example specifies the device by name.</span></span>
<span data-ttu-id="2ab26-118">A parancs a $Backup és a $Acrsban tárolt értékeket használja.</span><span class="sxs-lookup"><span data-stu-id="2ab26-118">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="2ab26-119">A parancs a feladat AZONOSÍTÓját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2ab26-119">The command returns the ID of the job.</span></span>

### <span data-ttu-id="2ab26-120">2. példa: biztonsági másolat másolása másik kötethez az eszközök azonosítói segítségével</span><span class="sxs-lookup"><span data-stu-id="2ab26-120">Example 2: Clone a backup to a different volume by using device IDs</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="2ab26-121">Az első parancs a **Get-AzureStorSimpleDeviceBackup** parancsmag használatával kapja meg a ContosoDev07 nevű eszköz első biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="2ab26-121">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="2ab26-122">A parancs a $Backup változóban tárolja a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="2ab26-122">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="2ab26-123">A második parancs a **Get-AzureStorSimpleAccessControlRecord** parancsmag használatával érheti el a rekordok vezérlését.</span><span class="sxs-lookup"><span data-stu-id="2ab26-123">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="2ab26-124">A parancs az eredményt a $Acrs változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2ab26-124">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="2ab26-125">A végleges parancs egy olyan munkafolyamatot kezd el, amely egy eszköz adott kötetének meghatározott biztonsági másolatát ugyanazon eszközön lévő másik kötetre másolta.</span><span class="sxs-lookup"><span data-stu-id="2ab26-125">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="2ab26-126">Ez a példa az eszköz azonosító szerinti azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ab26-126">This example specifies the device by device ID.</span></span>
<span data-ttu-id="2ab26-127">A parancs a $Backup és a $Acrsban tárolt értékeket használja.</span><span class="sxs-lookup"><span data-stu-id="2ab26-127">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="2ab26-128">A parancs a feladat AZONOSÍTÓját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2ab26-128">The command returns the ID of the job.</span></span>

### <span data-ttu-id="2ab26-129">3. példa: biztonsági másolatok másolása egy másik eszközön lévő kötetre az eszközök neveivel</span><span class="sxs-lookup"><span data-stu-id="2ab26-129">Example 3: Clone a backup to a volume on a different device by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="2ab26-130">Az első parancs a **Get-AzureStorSimpleDeviceBackup** parancsmag használatával kapja meg a ContosoDev07 nevű eszköz első biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="2ab26-130">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="2ab26-131">A parancs a $Backup változóban tárolja a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="2ab26-131">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="2ab26-132">A második parancs a **Get-AzureStorSimpleAccessControlRecord** parancsmag használatával érheti el a rekordok vezérlését.</span><span class="sxs-lookup"><span data-stu-id="2ab26-132">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="2ab26-133">A parancs az eredményt a $Acrs változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2ab26-133">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="2ab26-134">A végleges parancs egy olyan munkafolyamatot kezd el, amely a kötet egy másik eszközön lévő kötetének meghatározott biztonsági másolatát az eszközön lévő kötetre másolta.</span><span class="sxs-lookup"><span data-stu-id="2ab26-134">The final command begins a job that clones a specified backup of a volume on a device to a volume on a different device.</span></span>
<span data-ttu-id="2ab26-135">Ez a példa megadja az eszközöket név szerint.</span><span class="sxs-lookup"><span data-stu-id="2ab26-135">This example specifies the devices by name.</span></span>
<span data-ttu-id="2ab26-136">A parancs a $Backup és a $Acrsban tárolt értékeket használja.</span><span class="sxs-lookup"><span data-stu-id="2ab26-136">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="2ab26-137">A parancs a feladat AZONOSÍTÓját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2ab26-137">The command returns the ID of the job.</span></span>

### <span data-ttu-id="2ab26-138">Példa 4: biztonsági másolat másolása másik kötetre az eszközök neveivel és a csővezeték-kezelővel</span><span class="sxs-lookup"><span data-stu-id="2ab26-138">Example 4: Clone a backup to a different volume by using device names and the pipeline operator</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

<span data-ttu-id="2ab26-139">Az első parancs a **Get-AzureStorSimpleDeviceBackup** parancsmag használatával kapja meg a ContosoDev07 nevű eszköz első biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="2ab26-139">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="2ab26-140">A parancs a $Backup változóban tárolja a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="2ab26-140">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="2ab26-141">A második parancs a **Get-AzureStorSimpleAccessControlRecord** parancsmag használatával érheti el a rekordok vezérlését.</span><span class="sxs-lookup"><span data-stu-id="2ab26-141">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="2ab26-142">A parancs a csővezeték-kezelő segítségével átadja az eredményét az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="2ab26-142">The command passes its results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2ab26-143">Az aktuális parancsmag egy olyan feladatot kezd el, amely egy eszközön lévő kötet meghatározott biztonsági másolatát egy másik kötetre másolta ugyanazon az eszközön.</span><span class="sxs-lookup"><span data-stu-id="2ab26-143">The current cmdlet begins a job that clones a specified backup of a volume on a device, to a different volume on the same device.</span></span>
<span data-ttu-id="2ab26-144">Ez a példa megadja az eszközt név szerint.</span><span class="sxs-lookup"><span data-stu-id="2ab26-144">This example specifies the device by name.</span></span>
<span data-ttu-id="2ab26-145">A parancs a $Backupban tárolt értéket használja.</span><span class="sxs-lookup"><span data-stu-id="2ab26-145">The command uses the value stored in $Backup.</span></span>
<span data-ttu-id="2ab26-146">A parancs a *TargetAccessControlRecords* paraméter értékét a csővezetékről veszi át.</span><span class="sxs-lookup"><span data-stu-id="2ab26-146">The command takes the value of the *TargetAccessControlRecords* parameter from the pipeline.</span></span>
<span data-ttu-id="2ab26-147">A parancs a feladat AZONOSÍTÓját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2ab26-147">The command returns the ID of the job.</span></span>

## <span data-ttu-id="2ab26-148">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ab26-148">PARAMETERS</span></span>

### <span data-ttu-id="2ab26-149">-BackupId</span><span class="sxs-lookup"><span data-stu-id="2ab26-149">-BackupId</span></span>
<span data-ttu-id="2ab26-150">A klónozás biztonsági másolatának példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ab26-150">Specifies the instance ID of the backup to clone.</span></span>

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

### <span data-ttu-id="2ab26-151">-CloneVolumeName</span><span class="sxs-lookup"><span data-stu-id="2ab26-151">-CloneVolumeName</span></span>
<span data-ttu-id="2ab26-152">A céleszköz új klónozott kötetének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ab26-152">Specifies the name for the new cloned volume on the target device.</span></span>

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

### <span data-ttu-id="2ab26-153">-Force</span><span class="sxs-lookup"><span data-stu-id="2ab26-153">-Force</span></span>
<span data-ttu-id="2ab26-154">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2ab26-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2ab26-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="2ab26-155">-Profile</span></span>
<span data-ttu-id="2ab26-156">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="2ab26-156">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="2ab26-157">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="2ab26-157">-Snapshot</span></span>
<span data-ttu-id="2ab26-158">Annak a pillanatkép-objektumnak a meghatározása, amelyet a parancsmag klónja tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2ab26-158">Specifies the snapshot object that this cmdlet clones.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab26-159">-SourceDeviceId</span><span class="sxs-lookup"><span data-stu-id="2ab26-159">-SourceDeviceId</span></span>
<span data-ttu-id="2ab26-160">A forrás eszköz példány-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ab26-160">Specifies the instance ID of the source device.</span></span>
<span data-ttu-id="2ab26-161">Ezzel a parancsmaggal a program visszamásolja a forrást az eszközről.</span><span class="sxs-lookup"><span data-stu-id="2ab26-161">This cmdlet clones the back from the source device.</span></span>

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

### <span data-ttu-id="2ab26-162">-SourceDeviceName</span><span class="sxs-lookup"><span data-stu-id="2ab26-162">-SourceDeviceName</span></span>
<span data-ttu-id="2ab26-163">A forrás eszköz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ab26-163">Specifies the name of the source device.</span></span>
<span data-ttu-id="2ab26-164">Ezzel a parancsmaggal a program visszamásolja a forrást az eszközről.</span><span class="sxs-lookup"><span data-stu-id="2ab26-164">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab26-165">-TargetAccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="2ab26-165">-TargetAccessControlRecords</span></span>
<span data-ttu-id="2ab26-166">A hozzáférés-vezérlési rekordokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ab26-166">Specifies the access control records.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab26-167">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="2ab26-167">-TargetDeviceId</span></span>
<span data-ttu-id="2ab26-168">A céleszköz példányának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ab26-168">Specifies the instance ID of the target device.</span></span>

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

### <span data-ttu-id="2ab26-169">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="2ab26-169">-TargetDeviceName</span></span>
<span data-ttu-id="2ab26-170">Annak az eszköznek a nevét adja meg, amelyre a parancsmag klónja a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="2ab26-170">Specifies the name of the device to which this cmdlet clones the backup.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab26-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab26-171">CommonParameters</span></span>
<span data-ttu-id="2ab26-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ab26-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab26-173">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab26-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab26-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ab26-174">INPUTS</span></span>

### <span data-ttu-id="2ab26-175">Pillanatkép a AccessControlRecord listájáról</span><span class="sxs-lookup"><span data-stu-id="2ab26-175">Snapshot, List of AccessControlRecord</span></span>
<span data-ttu-id="2ab26-176">Ezt a parancsmagot kikapcsolhatja a **AccessControlRecord** **-objektumok vagy** a hozzájuk tartozó objektumok listájával.</span><span class="sxs-lookup"><span data-stu-id="2ab26-176">You can pipe **Snapshot** objects or a list of **AccessControlRecord** objects to this cmdlet.</span></span>

## <span data-ttu-id="2ab26-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ab26-177">OUTPUTS</span></span>

## <span data-ttu-id="2ab26-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ab26-178">NOTES</span></span>

## <span data-ttu-id="2ab26-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ab26-179">RELATED LINKS</span></span>

[<span data-ttu-id="2ab26-180">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="2ab26-180">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="2ab26-181">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="2ab26-181">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


