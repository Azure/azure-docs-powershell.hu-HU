---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 5dab5eaca48152dc573caf75f5d80737802bfcdf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399821"
---
# <span data-ttu-id="28f8c-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="28f8c-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="28f8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="28f8c-103">Biztonsági mentési feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="28f8c-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="28f8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="28f8c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28f8c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="28f8c-105">DESCRIPTION</span></span>
<span data-ttu-id="28f8c-106">A **Get-AzRecoveryServicesBackupServicesBackupService** parancsmag azure biztonsági mentési feladatokat kap egy adott tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="28f8c-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="28f8c-107">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="28f8c-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="28f8c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="28f8c-108">EXAMPLES</span></span>

### <span data-ttu-id="28f8c-109">1. példa: Az összes folyamatban lévő feladat lekérte</span><span class="sxs-lookup"><span data-stu-id="28f8c-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="28f8c-110">Az első parancs egy folyamatban lévő feladat állapotát tömbként kapja meg, majd a folyamatban lévő $Joblist tárolja.</span><span class="sxs-lookup"><span data-stu-id="28f8c-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="28f8c-111">A második parancs a tömb első elemét $Joblist jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="28f8c-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="28f8c-112">2. példa: Az összes sikertelen feladat be szerezze az elmúlt 7 napban</span><span class="sxs-lookup"><span data-stu-id="28f8c-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="28f8c-113">Ez a parancs sikertelen feladatokat kap a tároló utolsó hetében.</span><span class="sxs-lookup"><span data-stu-id="28f8c-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="28f8c-114">A *From* paraméter az UTC-ben megadott múltbeli hét napot ad meg.</span><span class="sxs-lookup"><span data-stu-id="28f8c-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="28f8c-115">A parancs nem ad meg értéket a *To paraméternek.*</span><span class="sxs-lookup"><span data-stu-id="28f8c-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="28f8c-116">Ezért az aktuális idő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="28f8c-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="28f8c-117">3. példa: Folyamatban lévő feladat elvégzése és várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="28f8c-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="28f8c-118">Ez a parancsprogram lekérdezi az első folyamatban lévő feladatot, amíg a feladat be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="28f8c-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="28f8c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28f8c-119">PARAMETERS</span></span>

### <span data-ttu-id="28f8c-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="28f8c-120">-BackupManagementType</span></span>
<span data-ttu-id="28f8c-121">A biztonsági mentés kezelési típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28f8c-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="28f8c-122">Jelenleg csak az AzureVM, az AzureStorage támogatott.</span><span class="sxs-lookup"><span data-stu-id="28f8c-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="28f8c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f8c-123">-DefaultProfile</span></span>
<span data-ttu-id="28f8c-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28f8c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28f8c-125">-From</span><span class="sxs-lookup"><span data-stu-id="28f8c-125">-From</span></span>
<span data-ttu-id="28f8c-126">A parancsmag által begyakorolt feladatok időtartományának **kezdését adja** meg DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="28f8c-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="28f8c-127">**DateTime-objektum** beszerzéséhez használja a Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="28f8c-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="28f8c-128">A DateTime-objektumokról a **következőt** írja be: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="28f8c-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="28f8c-129">Dátumokhoz használja az UTC formátumot.</span><span class="sxs-lookup"><span data-stu-id="28f8c-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="28f8c-130">-Job</span><span class="sxs-lookup"><span data-stu-id="28f8c-130">-Job</span></span>
<span data-ttu-id="28f8c-131">A lekért biztonsági másolati feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28f8c-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="28f8c-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="28f8c-132">-JobId</span></span>
<span data-ttu-id="28f8c-133">A parancsmag által lekért feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="28f8c-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="28f8c-134">Az azonosító egy **AzureRmRecoveryServicesBackupServicesBackupService objektum InstanceId tulajdonsága.**</span><span class="sxs-lookup"><span data-stu-id="28f8c-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="28f8c-135">**AzureRmRecoveryServicesBackupServices Object** beszerzéséhez használja a Get-AzRecoveryServicesBackupService-t.</span><span class="sxs-lookup"><span data-stu-id="28f8c-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="28f8c-136">-Operation</span><span class="sxs-lookup"><span data-stu-id="28f8c-136">-Operation</span></span>
<span data-ttu-id="28f8c-137">A parancsmag által lekért feladatok műveletét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28f8c-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="28f8c-138">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="28f8c-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28f8c-139">Biztonsági másolat</span><span class="sxs-lookup"><span data-stu-id="28f8c-139">Backup</span></span>
- <span data-ttu-id="28f8c-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="28f8c-140">ConfigureBackup</span></span>
- <span data-ttu-id="28f8c-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="28f8c-141">DeleteBackupData</span></span>
- <span data-ttu-id="28f8c-142">Regisztráció</span><span class="sxs-lookup"><span data-stu-id="28f8c-142">Register</span></span>
- <span data-ttu-id="28f8c-143">Visszaállítás</span><span class="sxs-lookup"><span data-stu-id="28f8c-143">Restore</span></span>
- <span data-ttu-id="28f8c-144">Védelem feloldása</span><span class="sxs-lookup"><span data-stu-id="28f8c-144">UnProtect</span></span>
- <span data-ttu-id="28f8c-145">Regisztrációt nem lehet</span><span class="sxs-lookup"><span data-stu-id="28f8c-145">Unregister</span></span>

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

### <span data-ttu-id="28f8c-146">-Állapot</span><span class="sxs-lookup"><span data-stu-id="28f8c-146">-Status</span></span>
<span data-ttu-id="28f8c-147">Megadja a parancsmag által begyabatolt feladatok állapotát.</span><span class="sxs-lookup"><span data-stu-id="28f8c-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="28f8c-148">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="28f8c-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28f8c-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="28f8c-149">InProgress</span></span>
- <span data-ttu-id="28f8c-150">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="28f8c-150">Failed</span></span>
- <span data-ttu-id="28f8c-151">Megszakítva</span><span class="sxs-lookup"><span data-stu-id="28f8c-151">Cancelled</span></span>
- <span data-ttu-id="28f8c-152">Lemondás</span><span class="sxs-lookup"><span data-stu-id="28f8c-152">Cancelling</span></span>
- <span data-ttu-id="28f8c-153">Befejezve</span><span class="sxs-lookup"><span data-stu-id="28f8c-153">Completed</span></span>
- <span data-ttu-id="28f8c-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="28f8c-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="28f8c-155">-To</span><span class="sxs-lookup"><span data-stu-id="28f8c-155">-To</span></span>
<span data-ttu-id="28f8c-156">A parancsmag által lekért feladatok időtartományának **DateTime-objektumként** való végét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28f8c-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="28f8c-157">Az alapértelmezett érték a rendszer aktuális ideje.</span><span class="sxs-lookup"><span data-stu-id="28f8c-157">The default value is the current system time.</span></span>
<span data-ttu-id="28f8c-158">Ha ezt a paramétert adja meg, a From paramétert *is meg kell adnia.*</span><span class="sxs-lookup"><span data-stu-id="28f8c-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="28f8c-159">Dátumokhoz használja az UTC formátumot.</span><span class="sxs-lookup"><span data-stu-id="28f8c-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="28f8c-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="28f8c-160">-VaultId</span></span>
<span data-ttu-id="28f8c-161">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="28f8c-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="28f8c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f8c-162">CommonParameters</span></span>
<span data-ttu-id="28f8c-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f8c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f8c-164">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28f8c-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f8c-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28f8c-165">INPUTS</span></span>

### <span data-ttu-id="28f8c-166">System.String</span><span class="sxs-lookup"><span data-stu-id="28f8c-166">System.String</span></span>

## <span data-ttu-id="28f8c-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28f8c-167">OUTPUTS</span></span>

### <span data-ttu-id="28f8c-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="28f8c-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="28f8c-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="28f8c-169">NOTES</span></span>

## <span data-ttu-id="28f8c-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28f8c-170">RELATED LINKS</span></span>


[<span data-ttu-id="28f8c-171">Stop-AzRecoveryServicesBackupService</span><span class="sxs-lookup"><span data-stu-id="28f8c-171">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="28f8c-172">Wait-AzRecoveryServicesBackupService</span><span class="sxs-lookup"><span data-stu-id="28f8c-172">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


