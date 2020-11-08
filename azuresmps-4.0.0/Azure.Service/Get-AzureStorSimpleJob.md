---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015558"
---
# <span data-ttu-id="33f6c-101">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="33f6c-101">Get-AzureStorSimpleJob</span></span>

## <span data-ttu-id="33f6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="33f6c-103">Megkapja a StorSimple munkákat.</span><span class="sxs-lookup"><span data-stu-id="33f6c-103">Gets StorSimple jobs.</span></span>

## <span data-ttu-id="33f6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33f6c-104">SYNTAX</span></span>

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="33f6c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="33f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="33f6c-106">A **Get-AzureStorSimpleJob** parancsmag Azure StorSimple-feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="33f6c-106">The **Get-AzureStorSimpleJob** cmdlet gets Azure StorSimple jobs.</span></span>
<span data-ttu-id="33f6c-107">Adjon meg egy példány-azonosítót egy adott feladat beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="33f6c-107">Specify an instance ID to get a specific job.</span></span>
<span data-ttu-id="33f6c-108">Adjon meg további paramétereket a parancsmag által kapott feladatok korlátozásához.</span><span class="sxs-lookup"><span data-stu-id="33f6c-108">Specify other parameters to limit the jobs that this cmdlet gets.</span></span>

<span data-ttu-id="33f6c-109">Ez a parancsmag legfeljebb 200 feladatot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="33f6c-109">This cmdlet returns a maximum of 200 jobs.</span></span>
<span data-ttu-id="33f6c-110">Ha több mint 200-feladatot tartalmaz, a hátralévő feladatokat az *első* és a *kihagyás* paraméter segítségével érheti el.</span><span class="sxs-lookup"><span data-stu-id="33f6c-110">If more than 200 jobs exist, get the remaining jobs by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="33f6c-111">Ha az 100 értékét adja meg *először* a *kihagyás* és az 50 beállításhoz, ez a parancsmag nem az első 100-találatokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="33f6c-111">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="33f6c-112">A 50 a 100 után a következő eredményt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="33f6c-112">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="33f6c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="33f6c-113">EXAMPLES</span></span>

### <span data-ttu-id="33f6c-114">Példa 1: feladat beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="33f6c-114">Example 1: Get a job by using an ID</span></span>
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

<span data-ttu-id="33f6c-115">Ez a parancs a megadott azonosítót tartalmazó feladatra vonatkozó információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="33f6c-115">This command gets information for the job that has the specified ID.</span></span>

### <span data-ttu-id="33f6c-116">2. példa: a feladatok eszköz nevének beszerzése</span><span class="sxs-lookup"><span data-stu-id="33f6c-116">Example 2: Get jobs by using a device name</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

<span data-ttu-id="33f6c-117">Ez a parancs a 8600-Bravo 001 nevű eszközhöz tartozó feladatok adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="33f6c-117">This command gets information for the jobs for the device named 8600-Bravo 001.</span></span>
<span data-ttu-id="33f6c-118">A parancs az első két feladatot kapja az eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="33f6c-118">The command gets the first two jobs for the device.</span></span>

### <span data-ttu-id="33f6c-119">3. példa: Befejezett feladatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="33f6c-119">Example 3: Get completed jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

<span data-ttu-id="33f6c-120">Ez a parancs befejezte a feladatok elvégzését.</span><span class="sxs-lookup"><span data-stu-id="33f6c-120">This command gets completed jobs.</span></span>
<span data-ttu-id="33f6c-121">A parancs csak az első két feladatot kapja, miután az első tíz feladatot kihagyja.</span><span class="sxs-lookup"><span data-stu-id="33f6c-121">The command gets only the first two jobs after it skips the first ten jobs.</span></span>

### <span data-ttu-id="33f6c-122">Példa 4: kézi mentési feladatok kérése</span><span class="sxs-lookup"><span data-stu-id="33f6c-122">Example 4: Get manual backup jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

<span data-ttu-id="33f6c-123">Ez a parancs a kézi biztonsági másolat típusának megfelelő feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="33f6c-123">This command gets jobs of the manual backup type.</span></span>

### <span data-ttu-id="33f6c-124">Példa 5: a feladatok beszerzése a megadott időpontok között</span><span class="sxs-lookup"><span data-stu-id="33f6c-124">Example 5: Get jobs between specified times</span></span>
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

<span data-ttu-id="33f6c-125">Az első két parancs a **datetime** -objektumokat hozza létre a Get-Date parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="33f6c-125">The first two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="33f6c-126">A parancsok az új időpontokat tárolják a $StartTime és $EndTime változókban.</span><span class="sxs-lookup"><span data-stu-id="33f6c-126">The commands store the new times in the $StartTime and $EndTime variables.</span></span>
<span data-ttu-id="33f6c-127">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="33f6c-127">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="33f6c-128">A végleges parancs a Device07 nevű eszköznek a $StartTime-ban és a $EndTime-ban tárolt idő között kap munkahelyeket.</span><span class="sxs-lookup"><span data-stu-id="33f6c-128">The final command gets jobs for the device named Device07 between the times stored in $StartTime and $EndTime.</span></span>

## <span data-ttu-id="33f6c-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33f6c-129">PARAMETERS</span></span>

### <span data-ttu-id="33f6c-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="33f6c-130">-DeviceName</span></span>
<span data-ttu-id="33f6c-131">Egy StorSimple-eszköz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33f6c-131">Specifies the name of a StorSimple device.</span></span>

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

### <span data-ttu-id="33f6c-132">– Első</span><span class="sxs-lookup"><span data-stu-id="33f6c-132">-First</span></span>
<span data-ttu-id="33f6c-133">Csak a megadott számú objektumot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="33f6c-133">Gets only the specified number of objects.</span></span>
<span data-ttu-id="33f6c-134">Adja meg a bejutni kívánt objektumok számát.</span><span class="sxs-lookup"><span data-stu-id="33f6c-134">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="33f6c-135">-From</span><span class="sxs-lookup"><span data-stu-id="33f6c-135">-From</span></span>
<span data-ttu-id="33f6c-136">A parancsmag által kapott feladatok kezdési dátumát és idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33f6c-136">Specifies the start date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f6c-137">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="33f6c-137">-InstanceId</span></span>
<span data-ttu-id="33f6c-138">A beolvasott feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="33f6c-138">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="33f6c-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="33f6c-139">-Profile</span></span>
<span data-ttu-id="33f6c-140">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="33f6c-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="33f6c-141">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="33f6c-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33f6c-142">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="33f6c-142">-Skip</span></span>
<span data-ttu-id="33f6c-143">Figyelmen kívül hagyja a megadott számú objektumot, majd Kinyeri a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="33f6c-143">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="33f6c-144">Adja meg, hogy hány objektum legyen kihagyva.</span><span class="sxs-lookup"><span data-stu-id="33f6c-144">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="33f6c-145">-Állapot</span><span class="sxs-lookup"><span data-stu-id="33f6c-145">-Status</span></span>
<span data-ttu-id="33f6c-146">Az állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="33f6c-146">Specifies the status.</span></span>
<span data-ttu-id="33f6c-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="33f6c-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33f6c-148">Fut</span><span class="sxs-lookup"><span data-stu-id="33f6c-148">Running</span></span>
- <span data-ttu-id="33f6c-149">Kész</span><span class="sxs-lookup"><span data-stu-id="33f6c-149">Completed</span></span>
- <span data-ttu-id="33f6c-150">Lemondott</span><span class="sxs-lookup"><span data-stu-id="33f6c-150">Cancelled</span></span>
- <span data-ttu-id="33f6c-151">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="33f6c-151">Failed</span></span>
- <span data-ttu-id="33f6c-152">Megszüntetésével lehet megszüntetni</span><span class="sxs-lookup"><span data-stu-id="33f6c-152">Canceling</span></span>
- <span data-ttu-id="33f6c-153">CompletedWithErrors</span><span class="sxs-lookup"><span data-stu-id="33f6c-153">CompletedWithErrors</span></span>

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

### <span data-ttu-id="33f6c-154">-To</span><span class="sxs-lookup"><span data-stu-id="33f6c-154">-To</span></span>
<span data-ttu-id="33f6c-155">A parancsmag által kapott feladatok befejezési dátumát és idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33f6c-155">Specifies the end date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f6c-156">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="33f6c-156">-Type</span></span>
<span data-ttu-id="33f6c-157">A feladattípust adja meg.</span><span class="sxs-lookup"><span data-stu-id="33f6c-157">Specifies the job type.</span></span>
<span data-ttu-id="33f6c-158">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="33f6c-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33f6c-159">Hát</span><span class="sxs-lookup"><span data-stu-id="33f6c-159">Backup</span></span>
- <span data-ttu-id="33f6c-160">ManualBackup</span><span class="sxs-lookup"><span data-stu-id="33f6c-160">ManualBackup</span></span>
- <span data-ttu-id="33f6c-161">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="33f6c-161">Restore</span></span>
- <span data-ttu-id="33f6c-162">CloneWorkflow</span><span class="sxs-lookup"><span data-stu-id="33f6c-162">CloneWorkflow</span></span>
- <span data-ttu-id="33f6c-163">DeviceRestore</span><span class="sxs-lookup"><span data-stu-id="33f6c-163">DeviceRestore</span></span>
- <span data-ttu-id="33f6c-164">Frissítés</span><span class="sxs-lookup"><span data-stu-id="33f6c-164">Update</span></span>
- <span data-ttu-id="33f6c-165">SupportPackage</span><span class="sxs-lookup"><span data-stu-id="33f6c-165">SupportPackage</span></span>
- <span data-ttu-id="33f6c-166">VirtualApplianceProvisioning</span><span class="sxs-lookup"><span data-stu-id="33f6c-166">VirtualApplianceProvisioning</span></span>

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

### <span data-ttu-id="33f6c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f6c-167">CommonParameters</span></span>
<span data-ttu-id="33f6c-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33f6c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f6c-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33f6c-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f6c-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33f6c-170">INPUTS</span></span>

### <span data-ttu-id="33f6c-171">Nincs</span><span class="sxs-lookup"><span data-stu-id="33f6c-171">None</span></span>
<span data-ttu-id="33f6c-172">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="33f6c-172">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="33f6c-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33f6c-173">OUTPUTS</span></span>

### <span data-ttu-id="33f6c-174">IList \<DeviceJobDetails\> , DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="33f6c-174">IList\<DeviceJobDetails\>, DeviceJobDetails</span></span>
<span data-ttu-id="33f6c-175">Ez a parancsmag a projektfeladat-adatobjektumok listáját adja eredményül, vagy ha a *InstanceId* paramétert adja meg, akkor az egyetlen feladat részlet objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="33f6c-175">This cmdlet returns a list of job details objects, or, if you specify the *InstanceID* parameter, it returns a single job detail object.</span></span>

## <span data-ttu-id="33f6c-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33f6c-176">NOTES</span></span>

## <span data-ttu-id="33f6c-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33f6c-177">RELATED LINKS</span></span>

[<span data-ttu-id="33f6c-178">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="33f6c-178">Stop-AzureStorSimpleJob</span></span>](./Stop-AzureStorSimpleJob.md)


