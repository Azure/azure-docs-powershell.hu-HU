---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015523"
---
# <span data-ttu-id="dada8-101">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="dada8-101">New-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="dada8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dada8-102">SYNOPSIS</span></span>
<span data-ttu-id="dada8-103">Kötetet hoz létre a megadott mennyiségi tárolóban.</span><span class="sxs-lookup"><span data-stu-id="dada8-103">Creates a volume in a specified volume container.</span></span>

## <span data-ttu-id="dada8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dada8-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dada8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dada8-105">DESCRIPTION</span></span>
<span data-ttu-id="dada8-106">A **New-AzureStorSimpleDeviceVolume** parancsmag egy kötetet hoz létre egy megadott mennyiségi tárolóban.</span><span class="sxs-lookup"><span data-stu-id="dada8-106">The **New-AzureStorSimpleDeviceVolume** cmdlet creates a volume in a specified volume container.</span></span>
<span data-ttu-id="dada8-107">Ez a parancsmag minden kötethez társít egy vagy több hozzáférés-vezérlési rekordot.</span><span class="sxs-lookup"><span data-stu-id="dada8-107">This cmdlet associates each volume with one or more access control records.</span></span>
<span data-ttu-id="dada8-108">Ha **AccessControlRecord** -objektumokat szeretne beolvasni, használja a **Get-AzureStorSimpleAccessControlRecord** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dada8-108">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="dada8-109">Adjon meg egy nevet, méretet és AppType a kötethez.</span><span class="sxs-lookup"><span data-stu-id="dada8-109">Specify a name, size, and AppType for the volume.</span></span>
<span data-ttu-id="dada8-110">Azt is megadhatja, hogy az online kötetet szeretné-e létrehozni, legyen szó akár az alapértelmezett biztonsági mentés engedélyezéséről, akár a figyelés engedélyezéséről.</span><span class="sxs-lookup"><span data-stu-id="dada8-110">Also, specify whether to create the volume online, whether to enable default backup, and whether to enable monitoring.</span></span>

## <span data-ttu-id="dada8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="dada8-111">EXAMPLES</span></span>

### <span data-ttu-id="dada8-112">Példa 1: kötet létrehozása</span><span class="sxs-lookup"><span data-stu-id="dada8-112">Example 1: Create a volume</span></span>
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

<span data-ttu-id="dada8-113">Az első parancs a **Get-AzureStorSimpleAccessControlRecord** parancsmaggal kapja meg a hozzáférés-vezérlési rekordokat az StorSimple-kezelő szolgáltatás beállításai között, majd a $AcrList változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="dada8-113">The first command gets the access control records in the StorSimple Manager service configuration by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet, and then stores them in the $AcrList variable.</span></span>

<span data-ttu-id="dada8-114">A második parancs a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmaggal kapja meg a VolumeContainer07 nevű kötet tárolóját a Contoso63-AppVm nevű eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="dada8-114">The second command gets the volume container named VolumeContainer07 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="dada8-115">A parancs átadja az adott tárolót az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="dada8-115">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dada8-116">Ezzel a parancsmaggal létrehozhatja a hangerőt.</span><span class="sxs-lookup"><span data-stu-id="dada8-116">This cmdlet creates the volume.</span></span>
<span data-ttu-id="dada8-117">A parancs a $AcrListban tárolt kötet, méret és hozzáférés-vezérlési rekordok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dada8-117">The command specifies the name for the volume, the size, and the access control records stored in $AcrList.</span></span>
<span data-ttu-id="dada8-118">Ez a parancs elindítja a feladatot, majd egy **TaskResponse** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="dada8-118">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="dada8-119">A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dada8-119">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="dada8-120">2. példa: kötet létrehozása Access-Controlaccess vezérlő recordsaccess-vezérlő nélkül</span><span class="sxs-lookup"><span data-stu-id="dada8-120">Example 2: Create a volume without Access Controlaccess control recordsaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

<span data-ttu-id="dada8-121">Ez a parancs a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmaggal kapja meg a VolumeContainer01 nevű kötet tárolóját a Contoso63-AppVm nevű eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="dada8-121">This command gets the volume container named VolumeContainer01 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="dada8-122">A parancs átadja az adott tárolót az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="dada8-122">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dada8-123">Ezzel a parancsmaggal létrehozhatja a hangerőt.</span><span class="sxs-lookup"><span data-stu-id="dada8-123">This cmdlet creates the volume.</span></span>
<span data-ttu-id="dada8-124">A parancs a kötet nevét, a méretet és a hozzáférés-vezérlési rekordok üres értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dada8-124">The command specifies the name for the volume, the size, and an empty value for access control records.</span></span>
<span data-ttu-id="dada8-125">Ez a parancs a *WaitForComplete* paramétert adja meg, így a kötet létrehozása után egy **TaskStatusInfo** ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="dada8-125">This command specifies the *WaitForComplete* parameter, so it returns a **TaskStatusInfo** after it creates the volume.</span></span>

<span data-ttu-id="dada8-126">Mivel a parancs nem tud hozzáférés-vezérlési rekordokat megadni, ez a kötet nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="dada8-126">Because the command specifies no access control records, this volume cannot be accessed.</span></span>
<span data-ttu-id="dada8-127">A **set-AzureStorSimpleDeviceVolume** parancsmaggal később is hozzáadhat hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="dada8-127">You can add access, later, by using **Set-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

## <span data-ttu-id="dada8-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dada8-128">PARAMETERS</span></span>

### <span data-ttu-id="dada8-129">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="dada8-129">-AccessControlRecords</span></span>
<span data-ttu-id="dada8-130">A kötethez társítani kívánt hozzáférés-vezérlési rekordok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dada8-130">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dada8-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dada8-131">-DeviceName</span></span>
<span data-ttu-id="dada8-132">Annak a StorSimple-eszköznek a nevét adja meg, amelybe a kötetet létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="dada8-132">Specifies the name of the StorSimple device on which to create the volume.</span></span>

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

### <span data-ttu-id="dada8-133">-EnableDefaultBackup</span><span class="sxs-lookup"><span data-stu-id="dada8-133">-EnableDefaultBackup</span></span>
<span data-ttu-id="dada8-134">Megadja, hogy engedélyezve van-e az alapértelmezett biztonsági másolat a köteten.</span><span class="sxs-lookup"><span data-stu-id="dada8-134">Specifies whether to enable default backup for the volume.</span></span>

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

### <span data-ttu-id="dada8-135">-EnableMonitoring</span><span class="sxs-lookup"><span data-stu-id="dada8-135">-EnableMonitoring</span></span>
<span data-ttu-id="dada8-136">Itt adhatja meg, hogy engedélyezi-e a kötet figyelését.</span><span class="sxs-lookup"><span data-stu-id="dada8-136">Specifies whether to enable monitoring for the volume.</span></span>

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

### <span data-ttu-id="dada8-137">-Online</span><span class="sxs-lookup"><span data-stu-id="dada8-137">-Online</span></span>
<span data-ttu-id="dada8-138">Itt adhatja meg, hogy az online kötetet szeretné-e létrehozni.</span><span class="sxs-lookup"><span data-stu-id="dada8-138">Specifies whether to create the volume online.</span></span>

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

### <span data-ttu-id="dada8-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="dada8-139">-Profile</span></span>
<span data-ttu-id="dada8-140">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="dada8-140">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="dada8-141">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="dada8-141">-VolumeAppType</span></span>
<span data-ttu-id="dada8-142">Itt adhatja meg, hogy elsődleges vagy archív kötetet szeretne-e létrehozni.</span><span class="sxs-lookup"><span data-stu-id="dada8-142">Specifies whether to create a primary or archive volume.</span></span>
<span data-ttu-id="dada8-143">Az érvényes értékek a következők: PrimaryVolume és ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="dada8-143">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dada8-144">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="dada8-144">-VolumeContainer</span></span>
<span data-ttu-id="dada8-145">A tárolót **DataContainer** objektumként adja meg, amelybe a kötetet hozza létre.</span><span class="sxs-lookup"><span data-stu-id="dada8-145">Specifies the container, as a **DataContainer** object, in which to create the volume.</span></span>
<span data-ttu-id="dada8-146">Ha **VirtualDisk** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dada8-146">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dada8-147">-Kötetnév</span><span class="sxs-lookup"><span data-stu-id="dada8-147">-VolumeName</span></span>
<span data-ttu-id="dada8-148">Az új kötet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dada8-148">Specifies a name for the new volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dada8-149">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="dada8-149">-VolumeSizeInBytes</span></span>
<span data-ttu-id="dada8-150">A kötet méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="dada8-150">Specifies the volume size in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dada8-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="dada8-151">-WaitForComplete</span></span>
<span data-ttu-id="dada8-152">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="dada8-152">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="dada8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dada8-153">CommonParameters</span></span>
<span data-ttu-id="dada8-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dada8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dada8-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dada8-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dada8-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dada8-156">INPUTS</span></span>

### <span data-ttu-id="dada8-157">DataContainer, lista\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="dada8-157">DataContainer, List\<AccessControlRecord\></span></span>
<span data-ttu-id="dada8-158">Ez a parancsmag elfogadja a **DataContainer** objektumot és az új kötet **AccessControlRecord** objektumait.</span><span class="sxs-lookup"><span data-stu-id="dada8-158">This cmdlet accepts a **DataContainer** object and a list of **AccessControlRecord** objects for the new volume.</span></span>

## <span data-ttu-id="dada8-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dada8-159">OUTPUTS</span></span>

### <span data-ttu-id="dada8-160">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="dada8-160">TaskStatusInfo</span></span>
<span data-ttu-id="dada8-161">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="dada8-161">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="dada8-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dada8-162">NOTES</span></span>

## <span data-ttu-id="dada8-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dada8-163">RELATED LINKS</span></span>

[<span data-ttu-id="dada8-164">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="dada8-164">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="dada8-165">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="dada8-165">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="dada8-166">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="dada8-166">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="dada8-167">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="dada8-167">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="dada8-168">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="dada8-168">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="dada8-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="dada8-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


