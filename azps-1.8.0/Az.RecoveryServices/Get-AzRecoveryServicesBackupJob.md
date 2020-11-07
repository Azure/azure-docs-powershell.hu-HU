---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 21498e13490b22b58621e2100dcc885442db7607
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669706"
---
# <span data-ttu-id="0401a-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0401a-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="0401a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0401a-102">SYNOPSIS</span></span>
<span data-ttu-id="0401a-103">Biztonsági mentési feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="0401a-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="0401a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0401a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0401a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0401a-105">DESCRIPTION</span></span>
<span data-ttu-id="0401a-106">A **Get-AzRecoveryServicesBackupJob** parancsmag Azure biztonságimásolat-készítési feladatokat kap egy adott boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="0401a-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="0401a-107">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="0401a-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0401a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0401a-108">EXAMPLES</span></span>

### <span data-ttu-id="0401a-109">Példa 1: minden folyamatban lévő feladat beolvasása</span><span class="sxs-lookup"><span data-stu-id="0401a-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="0401a-110">Az első parancs a folyamatban lévő munka állapotát tömbként kapja, majd a $Joblist változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0401a-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="0401a-111">A második parancs a $Joblist tömb első elemét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0401a-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="0401a-112">2. példa: az összes sikertelen feladat beolvasása az elmúlt 7 napban</span><span class="sxs-lookup"><span data-stu-id="0401a-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="0401a-113">Ez a parancs a boltozat utolsó hetében sikertelen feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="0401a-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="0401a-114">A *from* paraméter egy, az UTC által megadott időpontban hét napot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0401a-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="0401a-115">A parancs nem adja meg *a paraméter értékét* .</span><span class="sxs-lookup"><span data-stu-id="0401a-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="0401a-116">Ennek megfelelően az aktuális idő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="0401a-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="0401a-117">3. példa: folyamatban lévő munka beszerzése és várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="0401a-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="0401a-118">Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="0401a-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="0401a-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0401a-119">PARAMETERS</span></span>

### <span data-ttu-id="0401a-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0401a-120">-BackupManagementType</span></span>
<span data-ttu-id="0401a-121">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0401a-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="0401a-122">Jelenleg csak a AzureVM és a AzureStorage támogatott.</span><span class="sxs-lookup"><span data-stu-id="0401a-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0401a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0401a-123">-DefaultProfile</span></span>
<span data-ttu-id="0401a-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0401a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0401a-125">-From</span><span class="sxs-lookup"><span data-stu-id="0401a-125">-From</span></span>
<span data-ttu-id="0401a-126">A parancsmag által beolvasott feladatok időtartományának kezdetét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="0401a-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0401a-127">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0401a-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="0401a-128">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0401a-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="0401a-129">A dátumok esetében az UTC formátumot használhatja.</span><span class="sxs-lookup"><span data-stu-id="0401a-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="0401a-130">-Job</span><span class="sxs-lookup"><span data-stu-id="0401a-130">-Job</span></span>
<span data-ttu-id="0401a-131">A beolvasott biztonságimásolat-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0401a-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="0401a-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="0401a-132">-JobId</span></span>
<span data-ttu-id="0401a-133">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="0401a-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="0401a-134">Az azonosító egy **AzureRmRecoveryServicesBackupJob** objektum InstanceId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="0401a-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="0401a-135">**AzureRmRecoveryServicesBackupJob** -objektum beszerzéséhez használja a Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="0401a-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="0401a-136">-Művelet</span><span class="sxs-lookup"><span data-stu-id="0401a-136">-Operation</span></span>
<span data-ttu-id="0401a-137">A parancsmag által kapott feladatok működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="0401a-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0401a-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0401a-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0401a-139">Hát</span><span class="sxs-lookup"><span data-stu-id="0401a-139">Backup</span></span>
- <span data-ttu-id="0401a-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="0401a-140">ConfigureBackup</span></span>
- <span data-ttu-id="0401a-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="0401a-141">DeleteBackupData</span></span>
- <span data-ttu-id="0401a-142">Regisztráció</span><span class="sxs-lookup"><span data-stu-id="0401a-142">Register</span></span>
- <span data-ttu-id="0401a-143">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="0401a-143">Restore</span></span>
- <span data-ttu-id="0401a-144">Védtelen</span><span class="sxs-lookup"><span data-stu-id="0401a-144">UnProtect</span></span>
- <span data-ttu-id="0401a-145">Regisztrációját</span><span class="sxs-lookup"><span data-stu-id="0401a-145">Unregister</span></span>

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

### <span data-ttu-id="0401a-146">-Állapot</span><span class="sxs-lookup"><span data-stu-id="0401a-146">-Status</span></span>
<span data-ttu-id="0401a-147">A parancsmag által kapott feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0401a-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0401a-148">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0401a-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0401a-149">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="0401a-149">InProgress</span></span>
- <span data-ttu-id="0401a-150">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="0401a-150">Failed</span></span>
- <span data-ttu-id="0401a-151">Lemondott</span><span class="sxs-lookup"><span data-stu-id="0401a-151">Cancelled</span></span>
- <span data-ttu-id="0401a-152">Értekezletének lemondása</span><span class="sxs-lookup"><span data-stu-id="0401a-152">Cancelling</span></span>
- <span data-ttu-id="0401a-153">Kész</span><span class="sxs-lookup"><span data-stu-id="0401a-153">Completed</span></span>
- <span data-ttu-id="0401a-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="0401a-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="0401a-155">-To</span><span class="sxs-lookup"><span data-stu-id="0401a-155">-To</span></span>
<span data-ttu-id="0401a-156">Annak a projektnek az időtartományának a végét adja meg **datetime** -objektumként, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="0401a-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0401a-157">Az alapértelmezett érték az aktuális rendszer idő.</span><span class="sxs-lookup"><span data-stu-id="0401a-157">The default value is the current system time.</span></span>
<span data-ttu-id="0401a-158">Ha ezt a paramétert adja meg, a *from* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="0401a-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="0401a-159">A dátumok esetében az UTC formátumot használhatja.</span><span class="sxs-lookup"><span data-stu-id="0401a-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="0401a-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0401a-160">-VaultId</span></span>
<span data-ttu-id="0401a-161">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="0401a-161">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0401a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0401a-162">CommonParameters</span></span>
<span data-ttu-id="0401a-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0401a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0401a-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0401a-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0401a-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0401a-165">INPUTS</span></span>

### <span data-ttu-id="0401a-166">System. String</span><span class="sxs-lookup"><span data-stu-id="0401a-166">System.String</span></span>

## <span data-ttu-id="0401a-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0401a-167">OUTPUTS</span></span>

### <span data-ttu-id="0401a-168">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="0401a-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0401a-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0401a-169">NOTES</span></span>

## <span data-ttu-id="0401a-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0401a-170">RELATED LINKS</span></span>

[<span data-ttu-id="0401a-171">Get-AzRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="0401a-171">Get-AzRecoveryServicesBackupJobDetails</span></span>](./Get-AzRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="0401a-172">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0401a-172">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="0401a-173">Várjon-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0401a-173">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


