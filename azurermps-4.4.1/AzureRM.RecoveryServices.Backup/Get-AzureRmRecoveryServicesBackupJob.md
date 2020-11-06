---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 3fb6b89f5708c951731c45e0d32e0f7a379cf754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504799"
---
# <span data-ttu-id="535dd-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="535dd-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="535dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="535dd-102">SYNOPSIS</span></span>
<span data-ttu-id="535dd-103">Biztonsági mentési feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="535dd-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="535dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="535dd-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="535dd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="535dd-105">DESCRIPTION</span></span>
<span data-ttu-id="535dd-106">A **Get-AzureRmRecoveryServicesBackupJob** parancsmag Azure biztonságimásolat-készítési feladatokat kap egy adott boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="535dd-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

<span data-ttu-id="535dd-107">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="535dd-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="535dd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="535dd-108">EXAMPLES</span></span>

### <span data-ttu-id="535dd-109">Példa 1: minden folyamatban lévő feladat beolvasása</span><span class="sxs-lookup"><span data-stu-id="535dd-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="535dd-110">Az első parancs a folyamatban lévő munka állapotát tömbként kapja, majd a $Joblist változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="535dd-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>

<span data-ttu-id="535dd-111">A második parancs a $Joblist tömb első elemét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="535dd-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="535dd-112">2. példa: az összes sikertelen feladat beolvasása az elmúlt 7 napban</span><span class="sxs-lookup"><span data-stu-id="535dd-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="535dd-113">Ez a parancs a boltozat utolsó hetében sikertelen feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="535dd-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="535dd-114">A *from* paraméter egy, az UTC által megadott időpontban hét napot ad meg.</span><span class="sxs-lookup"><span data-stu-id="535dd-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="535dd-115">A parancs nem adja meg *a paraméter értékét* .</span><span class="sxs-lookup"><span data-stu-id="535dd-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="535dd-116">Ennek megfelelően az aktuális idő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="535dd-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="535dd-117">3. példa: folyamatban lévő munka beszerzése és várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="535dd-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="535dd-118">Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="535dd-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="535dd-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="535dd-119">PARAMETERS</span></span>

### <span data-ttu-id="535dd-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="535dd-120">-BackupManagementType</span></span>
<span data-ttu-id="535dd-121">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="535dd-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="535dd-122">Jelenleg csak a AzureVM támogatott.</span><span class="sxs-lookup"><span data-stu-id="535dd-122">Currently, only AzureVM is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535dd-123">-From</span><span class="sxs-lookup"><span data-stu-id="535dd-123">-From</span></span>
<span data-ttu-id="535dd-124">A parancsmag által beolvasott feladatok időtartományának kezdetét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="535dd-124">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="535dd-125">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="535dd-125">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="535dd-126">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="535dd-126">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="535dd-127">A dátumok esetében az UTC formátumot használhatja.</span><span class="sxs-lookup"><span data-stu-id="535dd-127">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535dd-128">-Job</span><span class="sxs-lookup"><span data-stu-id="535dd-128">-Job</span></span>
<span data-ttu-id="535dd-129">A beolvasott biztonságimásolat-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="535dd-129">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535dd-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="535dd-130">-JobId</span></span>
<span data-ttu-id="535dd-131">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="535dd-131">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="535dd-132">Az azonosító egy **AzureRmRecoveryServicesBackupJob** objektum InstanceId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="535dd-132">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="535dd-133">**AzureRmRecoveryServicesBackupJob** -objektum beszerzéséhez használja a Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="535dd-133">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535dd-134">-Művelet</span><span class="sxs-lookup"><span data-stu-id="535dd-134">-Operation</span></span>
<span data-ttu-id="535dd-135">A parancsmag által kapott feladatok működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="535dd-135">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="535dd-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="535dd-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="535dd-137">Hát</span><span class="sxs-lookup"><span data-stu-id="535dd-137">Backup</span></span>
- <span data-ttu-id="535dd-138">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="535dd-138">ConfigureBackup</span></span>
- <span data-ttu-id="535dd-139">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="535dd-139">DeleteBackupData</span></span>
- <span data-ttu-id="535dd-140">Regisztráció</span><span class="sxs-lookup"><span data-stu-id="535dd-140">Register</span></span>
- <span data-ttu-id="535dd-141">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="535dd-141">Restore</span></span>
- <span data-ttu-id="535dd-142">Védtelen</span><span class="sxs-lookup"><span data-stu-id="535dd-142">UnProtect</span></span>
- <span data-ttu-id="535dd-143">Regisztrációját</span><span class="sxs-lookup"><span data-stu-id="535dd-143">Unregister</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535dd-144">-Állapot</span><span class="sxs-lookup"><span data-stu-id="535dd-144">-Status</span></span>
<span data-ttu-id="535dd-145">A parancsmag által kapott feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="535dd-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="535dd-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="535dd-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="535dd-147">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="535dd-147">InProgress</span></span>
- <span data-ttu-id="535dd-148">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="535dd-148">Failed</span></span>
- <span data-ttu-id="535dd-149">Lemondott</span><span class="sxs-lookup"><span data-stu-id="535dd-149">Cancelled</span></span>
- <span data-ttu-id="535dd-150">Értekezletének lemondása</span><span class="sxs-lookup"><span data-stu-id="535dd-150">Cancelling</span></span>
- <span data-ttu-id="535dd-151">Kész</span><span class="sxs-lookup"><span data-stu-id="535dd-151">Completed</span></span>
- <span data-ttu-id="535dd-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="535dd-152">CompletedWithWarnings</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535dd-153">-To</span><span class="sxs-lookup"><span data-stu-id="535dd-153">-To</span></span>
<span data-ttu-id="535dd-154">Annak a projektnek az időtartományának a végét adja meg **datetime** -objektumként, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="535dd-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="535dd-155">Az alapértelmezett érték az aktuális rendszer idő.</span><span class="sxs-lookup"><span data-stu-id="535dd-155">The default value is the current system time.</span></span>
<span data-ttu-id="535dd-156">Ha ezt a paramétert adja meg, a *from* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="535dd-156">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="535dd-157">A dátumok esetében az UTC formátumot használhatja.</span><span class="sxs-lookup"><span data-stu-id="535dd-157">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535dd-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535dd-158">-DefaultProfile</span></span>
<span data-ttu-id="535dd-159">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="535dd-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535dd-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535dd-160">CommonParameters</span></span>
<span data-ttu-id="535dd-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="535dd-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535dd-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="535dd-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535dd-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="535dd-163">INPUTS</span></span>

## <span data-ttu-id="535dd-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="535dd-164">OUTPUTS</span></span>

### <span data-ttu-id="535dd-165">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="535dd-165">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="535dd-166">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="535dd-166">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="535dd-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="535dd-167">NOTES</span></span>

## <span data-ttu-id="535dd-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="535dd-168">RELATED LINKS</span></span>

[<span data-ttu-id="535dd-169">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="535dd-169">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="535dd-170">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="535dd-170">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="535dd-171">Várjon-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="535dd-171">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


