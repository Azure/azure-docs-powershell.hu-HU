---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 0ed0ed82c1f2c030ab10fc6a96d1582fdb34b7d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501984"
---
# <span data-ttu-id="6b8ca-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b8ca-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="6b8ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b8ca-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8ca-103">Biztonsági mentési feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b8ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b8ca-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b8ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b8ca-105">DESCRIPTION</span></span>
<span data-ttu-id="6b8ca-106">A **Get-AzureRmRecoveryServicesBackupJob** parancsmag Azure biztonságimásolat-készítési feladatokat kap egy adott boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="6b8ca-107">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6b8ca-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6b8ca-108">EXAMPLES</span></span>

### <span data-ttu-id="6b8ca-109">Példa 1: minden folyamatban lévő feladat beolvasása</span><span class="sxs-lookup"><span data-stu-id="6b8ca-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="6b8ca-110">Az első parancs a folyamatban lévő munka állapotát tömbként kapja, majd a $Joblist változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="6b8ca-111">A második parancs a $Joblist tömb első elemét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="6b8ca-112">2. példa: az összes sikertelen feladat beolvasása az elmúlt 7 napban</span><span class="sxs-lookup"><span data-stu-id="6b8ca-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="6b8ca-113">Ez a parancs a boltozat utolsó hetében sikertelen feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="6b8ca-114">A *from* paraméter egy, az UTC által megadott időpontban hét napot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="6b8ca-115">A parancs nem adja meg *a paraméter értékét* .</span><span class="sxs-lookup"><span data-stu-id="6b8ca-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="6b8ca-116">Ennek megfelelően az aktuális idő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="6b8ca-117">3. példa: folyamatban lévő munka beszerzése és várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="6b8ca-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="6b8ca-118">Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="6b8ca-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b8ca-119">PARAMETERS</span></span>

### <span data-ttu-id="6b8ca-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="6b8ca-120">-BackupManagementType</span></span>
<span data-ttu-id="6b8ca-121">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="6b8ca-122">Jelenleg csak a AzureVM és a AzureStorage támogatott.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8ca-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8ca-123">-DefaultProfile</span></span>
<span data-ttu-id="6b8ca-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b8ca-125">-From</span><span class="sxs-lookup"><span data-stu-id="6b8ca-125">-From</span></span>
<span data-ttu-id="6b8ca-126">A parancsmag által beolvasott feladatok időtartományának kezdetét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6b8ca-127">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="6b8ca-128">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6b8ca-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="6b8ca-129">A dátumok esetében az UTC formátumot használhatja.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="6b8ca-130">-Job</span><span class="sxs-lookup"><span data-stu-id="6b8ca-130">-Job</span></span>
<span data-ttu-id="6b8ca-131">A beolvasott biztonságimásolat-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="6b8ca-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="6b8ca-132">-JobId</span></span>
<span data-ttu-id="6b8ca-133">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="6b8ca-134">Az azonosító egy **AzureRmRecoveryServicesBackupJob** objektum InstanceId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="6b8ca-135">**AzureRmRecoveryServicesBackupJob** -objektum beszerzéséhez használja a Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="6b8ca-136">-Művelet</span><span class="sxs-lookup"><span data-stu-id="6b8ca-136">-Operation</span></span>
<span data-ttu-id="6b8ca-137">A parancsmag által kapott feladatok működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6b8ca-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6b8ca-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b8ca-139">Hát</span><span class="sxs-lookup"><span data-stu-id="6b8ca-139">Backup</span></span>
- <span data-ttu-id="6b8ca-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="6b8ca-140">ConfigureBackup</span></span>
- <span data-ttu-id="6b8ca-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="6b8ca-141">DeleteBackupData</span></span>
- <span data-ttu-id="6b8ca-142">Regisztráció</span><span class="sxs-lookup"><span data-stu-id="6b8ca-142">Register</span></span>
- <span data-ttu-id="6b8ca-143">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="6b8ca-143">Restore</span></span>
- <span data-ttu-id="6b8ca-144">Védtelen</span><span class="sxs-lookup"><span data-stu-id="6b8ca-144">UnProtect</span></span>
- <span data-ttu-id="6b8ca-145">Regisztrációját</span><span class="sxs-lookup"><span data-stu-id="6b8ca-145">Unregister</span></span>

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

### <span data-ttu-id="6b8ca-146">-Állapot</span><span class="sxs-lookup"><span data-stu-id="6b8ca-146">-Status</span></span>
<span data-ttu-id="6b8ca-147">A parancsmag által kapott feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6b8ca-148">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6b8ca-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b8ca-149">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="6b8ca-149">InProgress</span></span>
- <span data-ttu-id="6b8ca-150">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="6b8ca-150">Failed</span></span>
- <span data-ttu-id="6b8ca-151">Lemondott</span><span class="sxs-lookup"><span data-stu-id="6b8ca-151">Cancelled</span></span>
- <span data-ttu-id="6b8ca-152">Értekezletének lemondása</span><span class="sxs-lookup"><span data-stu-id="6b8ca-152">Cancelling</span></span>
- <span data-ttu-id="6b8ca-153">Kész</span><span class="sxs-lookup"><span data-stu-id="6b8ca-153">Completed</span></span>
- <span data-ttu-id="6b8ca-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="6b8ca-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="6b8ca-155">-To</span><span class="sxs-lookup"><span data-stu-id="6b8ca-155">-To</span></span>
<span data-ttu-id="6b8ca-156">Annak a projektnek az időtartományának a végét adja meg **datetime** -objektumként, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6b8ca-157">Az alapértelmezett érték az aktuális rendszer idő.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-157">The default value is the current system time.</span></span>
<span data-ttu-id="6b8ca-158">Ha ezt a paramétert adja meg, a *from* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="6b8ca-159">A dátumok esetében az UTC formátumot használhatja.</span><span class="sxs-lookup"><span data-stu-id="6b8ca-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="6b8ca-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6b8ca-160">-VaultId</span></span>
<span data-ttu-id="6b8ca-161">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="6b8ca-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6b8ca-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8ca-162">CommonParameters</span></span>
<span data-ttu-id="6b8ca-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b8ca-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8ca-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b8ca-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8ca-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b8ca-165">INPUTS</span></span>

### <span data-ttu-id="6b8ca-166">System. String</span><span class="sxs-lookup"><span data-stu-id="6b8ca-166">System.String</span></span>
<span data-ttu-id="6b8ca-167">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b8ca-167">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="6b8ca-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b8ca-168">OUTPUTS</span></span>

### <span data-ttu-id="6b8ca-169">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="6b8ca-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6b8ca-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b8ca-170">NOTES</span></span>

## <span data-ttu-id="6b8ca-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b8ca-171">RELATED LINKS</span></span>

[<span data-ttu-id="6b8ca-172">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="6b8ca-172">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="6b8ca-173">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b8ca-173">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="6b8ca-174">Várjon-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b8ca-174">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


