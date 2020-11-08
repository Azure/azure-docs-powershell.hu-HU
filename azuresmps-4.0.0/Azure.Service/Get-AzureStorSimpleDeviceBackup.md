---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016290"
---
# <span data-ttu-id="7cdca-101">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="7cdca-101">Get-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="7cdca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cdca-102">SYNOPSIS</span></span>
<span data-ttu-id="7cdca-103">Biztonsági másolatot kap egy eszközről.</span><span class="sxs-lookup"><span data-stu-id="7cdca-103">Gets backups from a device.</span></span>

## <span data-ttu-id="7cdca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cdca-104">SYNTAX</span></span>

### <span data-ttu-id="7cdca-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7cdca-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7cdca-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="7cdca-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7cdca-107">IdentifyById2</span><span class="sxs-lookup"><span data-stu-id="7cdca-107">IdentifyById2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7cdca-108">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="7cdca-108">IdentifyByObject</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7cdca-109">IdentifyByObject2</span><span class="sxs-lookup"><span data-stu-id="7cdca-109">IdentifyByObject2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7cdca-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cdca-110">DESCRIPTION</span></span>
<span data-ttu-id="7cdca-111">A **Get-AzureStorSimpleDeviceBackup** parancsmag egy eszközről kap biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="7cdca-111">The **Get-AzureStorSimpleDeviceBackup** cmdlet gets backups from a device.</span></span>
<span data-ttu-id="7cdca-112">Megadhatja a biztonsági mentési házirendet, a kötetet és a létrehozási időpontot a biztonsági mentéshez.</span><span class="sxs-lookup"><span data-stu-id="7cdca-112">You can specify the backup policy, volume, and creation time for backups.</span></span>

<span data-ttu-id="7cdca-113">Ez a parancsmag legfeljebb 100 biztonsági másolatot adhat vissza az első oldalon.</span><span class="sxs-lookup"><span data-stu-id="7cdca-113">This cmdlet can return a maximum of 100 backups in the first page.</span></span>
<span data-ttu-id="7cdca-114">Ha több mint 100 biztonsági másolat létezik, az *első* és a *kihagyás* paraméter segítségével beolvashatja a további lapokat.</span><span class="sxs-lookup"><span data-stu-id="7cdca-114">If more than 100 backups exist, retrieve subsequent pages by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="7cdca-115">Ha az 100 értékét adja meg *először* a *kihagyás* és az 50 beállításhoz, ez a parancsmag nem az első 100-találatokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="7cdca-115">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="7cdca-116">A 50 a 100 után a következő eredményt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="7cdca-116">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="7cdca-117">Példák</span><span class="sxs-lookup"><span data-stu-id="7cdca-117">EXAMPLES</span></span>

### <span data-ttu-id="7cdca-118">Példa 1: minden biztonsági másolat beszerzése egy eszközön</span><span class="sxs-lookup"><span data-stu-id="7cdca-118">Example 1: Get all backups on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

<span data-ttu-id="7cdca-119">Ez a parancs minden olyan biztonsági másolatot kap, amely a Contoso63-AppVm nevű eszközön található.</span><span class="sxs-lookup"><span data-stu-id="7cdca-119">This command gets all backups that exist on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="7cdca-120">Ha az első oldalnál több 100-biztonsági másolat is engedélyezve van, az *első* és a *kihagyás* paraméterrel további eredményeket jeleníthet meg.</span><span class="sxs-lookup"><span data-stu-id="7cdca-120">If there are more than the maximum of 100 backups allowed for the first page, use the *First* and *Skip* parameters to view additional results.</span></span>

### <span data-ttu-id="7cdca-121">2. példa: két dátum között létrehozott biztonsági másolatok beolvasása</span><span class="sxs-lookup"><span data-stu-id="7cdca-121">Example 2: Get backups created between two dates</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

<span data-ttu-id="7cdca-122">Ez a parancs biztonsági másolatot kap az 10/7/2014 Contoso63-AppVm nevű eszközről, amely a-on vagy a-on vagy a 10/8/2014 előtt lett létrehozva.</span><span class="sxs-lookup"><span data-stu-id="7cdca-122">This command gets backups on the device named Contoso63-AppVm that were created on or after 10/7/2014 and on or before 10/8/2014.</span></span>
<span data-ttu-id="7cdca-123">Ez a parancsmag kihagyja az első eredményt, és az első eredmény után az első két találatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7cdca-123">This cmdlet skips the first result and returns the first two results after that first result.</span></span>
<span data-ttu-id="7cdca-124">Módosítsa az értékeket az *első* és a *kihagyás* gombra az egyéb találatok megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="7cdca-124">Modify values for *First* and *Skip* to view other results.</span></span>

### <span data-ttu-id="7cdca-125">3. példa: biztonsági másolatok készítése biztonsági házirend-AZONOSÍTÓról</span><span class="sxs-lookup"><span data-stu-id="7cdca-125">Example 3: Get backups for a backup policy ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="7cdca-126">Ez a parancs biztonsági másolatot kap a megadott napon vagy azt megelőzően létrehozott Contoso63-AppVm nevű eszközről.</span><span class="sxs-lookup"><span data-stu-id="7cdca-126">This command gets backups on the device named Contoso63-AppVm created on or before the specified date.</span></span>
<span data-ttu-id="7cdca-127">A parancs a megadott azonosítót tartalmazó biztonsági házirend használatával létrehozott biztonsági másolatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="7cdca-127">The command gets backups that were created by using the backup policy that has the specified ID.</span></span>
<span data-ttu-id="7cdca-128">Ez a parancs az *első* paramétert adja meg, ezért csak az első 10 találatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7cdca-128">This command specifies the *First* parameter, so it returns only the first 10 results.</span></span>

### <span data-ttu-id="7cdca-129">4. példa: biztonsági másolatok készítése biztonsági házirend-objektumról</span><span class="sxs-lookup"><span data-stu-id="7cdca-129">Example 4: Get backups for a backup policy object</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="7cdca-130">Ez a parancs a **Get-AzureStorSimpleDeviceBackupPolicy** parancsmaggal kapja meg a **BackupPolicyDetails** objektumot, majd a pipeline operátor segítségével átadja az adott objektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="7cdca-130">This command gets a **BackupPolicyDetails** object by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7cdca-131">Ez a parancsmag a parancs első részéből a biztonsági házirend segítségével készít biztonsági másolatokat a Contoso63-AppVm nevű eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="7cdca-131">That cmdlet gets backups for the device named Contoso63-AppVm created by using the backup policy from the first part of the command.</span></span>
<span data-ttu-id="7cdca-132">A parancs a megadott napon vagy azt megelőzően létrehozott biztonsági másolatokat kapja, ugyanúgy, mint az előző példában.</span><span class="sxs-lookup"><span data-stu-id="7cdca-132">The command gets backups created on or before the specified date, just as in the previous example.</span></span>
<span data-ttu-id="7cdca-133">Ez a parancs csak az első 10 találatot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="7cdca-133">This command returns only the first 10 results.</span></span>

### <span data-ttu-id="7cdca-134">Példa 5: biztonsági másolat kérése mennyiségi AZONOSÍTÓhoz</span><span class="sxs-lookup"><span data-stu-id="7cdca-134">Example 5: Get a backup for a volume ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="7cdca-135">Ez a parancs biztonsági másolatot kap a megadott példány-azonosítót tartalmazó köteten létrehozott eszközről.</span><span class="sxs-lookup"><span data-stu-id="7cdca-135">This command gets a backup on the device that is created on the volume that has the specified instance ID.</span></span>
<span data-ttu-id="7cdca-136">Ez a parancs az *első* paramétert adja meg, ezért csak az első eredményt adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7cdca-136">This command specifies the *First* parameter, so it returns only the first one result.</span></span>

### <span data-ttu-id="7cdca-137">6. példa: biztonsági másolat készítése a kötet nevéről</span><span class="sxs-lookup"><span data-stu-id="7cdca-137">Example 6: Get a backup for a volume name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="7cdca-138">Ez a parancs a **Get-AzureStorSimpleDeviceVolume** parancsmaggal kapja meg a **VirtualDisk** objektumot, majd a pipeline operátor segítségével átadja az adott objektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="7cdca-138">This command gets a **VirtualDisk** object by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7cdca-139">Ez a parancsmag biztonsági másolatot kap a parancs első részéből a köteten létrehozott Contoso63-AppVm nevű eszközről.</span><span class="sxs-lookup"><span data-stu-id="7cdca-139">That cmdlet gets backups for the device named Contoso63-AppVm created on the volume from the first part of the command.</span></span>
<span data-ttu-id="7cdca-140">Ez a parancs csak az első eredményt adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7cdca-140">This command returns only the first result.</span></span>

## <span data-ttu-id="7cdca-141">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cdca-141">PARAMETERS</span></span>

### <span data-ttu-id="7cdca-142">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7cdca-142">-BackupPolicy</span></span>
<span data-ttu-id="7cdca-143">Egy **BackupPolicyDetails** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7cdca-143">Specifies a **BackupPolicyDetails** object.</span></span>
<span data-ttu-id="7cdca-144">Ez a parancsmag az objektum **InstanceId** határozza meg, hogy mely biztonsági másolatok legyenek elérhetők.</span><span class="sxs-lookup"><span data-stu-id="7cdca-144">This cmdlet uses the **InstanceId** of this object to determine which backups to get.</span></span>
<span data-ttu-id="7cdca-145">Ha **BackupPolicyDetails** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleDeviceBackupPolicy** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7cdca-145">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cdca-146">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="7cdca-146">-BackupPolicyId</span></span>
<span data-ttu-id="7cdca-147">A biztonságimásolat-házirendek példányának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cdca-147">Specifies an instance ID of a backup policy.</span></span>
<span data-ttu-id="7cdca-148">Ez a parancsmag a paraméter által megadott házirendek biztonsági másolatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7cdca-148">This cmdlet gets device backups for policy that this parameter specifies.</span></span>

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

### <span data-ttu-id="7cdca-149">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7cdca-149">-DeviceName</span></span>
<span data-ttu-id="7cdca-150">Annak a StorSimple-eszköznek a nevét adja meg, amelyhez biztonsági másolatot szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="7cdca-150">Specifies the name of the StorSimple device for which to get backups.</span></span>

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

### <span data-ttu-id="7cdca-151">– Első</span><span class="sxs-lookup"><span data-stu-id="7cdca-151">-First</span></span>
<span data-ttu-id="7cdca-152">Csak a megadott számú objektumot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7cdca-152">Gets only the specified number of objects.</span></span>
<span data-ttu-id="7cdca-153">Adja meg a bejutni kívánt objektumok számát.</span><span class="sxs-lookup"><span data-stu-id="7cdca-153">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cdca-154">-From</span><span class="sxs-lookup"><span data-stu-id="7cdca-154">-From</span></span>
<span data-ttu-id="7cdca-155">Annak a biztonsági másolatnak a kezdési dátumát és időpontját adja meg, amelyre a parancsmag eljut.</span><span class="sxs-lookup"><span data-stu-id="7cdca-155">Specifies the start date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7cdca-156">-Profil</span><span class="sxs-lookup"><span data-stu-id="7cdca-156">-Profile</span></span>
<span data-ttu-id="7cdca-157">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="7cdca-157">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7cdca-158">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="7cdca-158">-Skip</span></span>
<span data-ttu-id="7cdca-159">Figyelmen kívül hagyja a megadott számú objektumot, majd Kinyeri a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="7cdca-159">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="7cdca-160">Adja meg, hogy hány objektum legyen kihagyva.</span><span class="sxs-lookup"><span data-stu-id="7cdca-160">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cdca-161">-To</span><span class="sxs-lookup"><span data-stu-id="7cdca-161">-To</span></span>
<span data-ttu-id="7cdca-162">A parancsmag által beolvasott biztonsági másolatok befejezési dátumát és idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cdca-162">Specifies the end date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7cdca-163">-Volume</span><span class="sxs-lookup"><span data-stu-id="7cdca-163">-Volume</span></span>
<span data-ttu-id="7cdca-164">Egy **VirtualDisk** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7cdca-164">Specifies a **VirtualDisk** object.</span></span>
<span data-ttu-id="7cdca-165">Ez a parancsmag az objektum **InstanceId** határozza meg, hogy melyik köteten találhatók a biztonsági másolatok.</span><span class="sxs-lookup"><span data-stu-id="7cdca-165">This cmdlet uses the **InstanceId** of this object to determine the volume in which backups exist.</span></span>
<span data-ttu-id="7cdca-166">Ha **VirtualDisk** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleDeviceVolume** paramétert.</span><span class="sxs-lookup"><span data-stu-id="7cdca-166">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** parameter.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cdca-167">-VolumeId</span><span class="sxs-lookup"><span data-stu-id="7cdca-167">-VolumeId</span></span>
<span data-ttu-id="7cdca-168">Annak a kötetnek a példány-AZONOSÍTÓját adja meg, amelyben a biztonsági másolatok találhatók.</span><span class="sxs-lookup"><span data-stu-id="7cdca-168">Specifies the instance ID of the volume in which backups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cdca-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cdca-169">CommonParameters</span></span>
<span data-ttu-id="7cdca-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cdca-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cdca-171">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cdca-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cdca-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cdca-172">INPUTS</span></span>

### <span data-ttu-id="7cdca-173">BackupPolicyDetails, VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="7cdca-173">BackupPolicyDetails, VirtualDisk</span></span>
<span data-ttu-id="7cdca-174">Ez a parancsmag elfogadja a **BackupPolicyDetails** és a **VirtualDisk** objektumokat.</span><span class="sxs-lookup"><span data-stu-id="7cdca-174">This cmdlet accepts **BackupPolicyDetails** and **VirtualDisk** objects.</span></span>

## <span data-ttu-id="7cdca-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cdca-175">OUTPUTS</span></span>

### <span data-ttu-id="7cdca-176">IList\<Backup\></span><span class="sxs-lookup"><span data-stu-id="7cdca-176">IList\<Backup\></span></span>
<span data-ttu-id="7cdca-177">Ez a parancsmag a **biztonságimásolat** -objektumok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="7cdca-177">This cmdlet returns a list of **Backup** objects.</span></span>

## <span data-ttu-id="7cdca-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cdca-178">NOTES</span></span>

## <span data-ttu-id="7cdca-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cdca-179">RELATED LINKS</span></span>

[<span data-ttu-id="7cdca-180">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="7cdca-180">Remove-AzureStorSimpleDeviceBackup</span></span>](./Remove-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="7cdca-181">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7cdca-181">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="7cdca-182">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7cdca-182">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)


