---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc8b9017180c431caabc31970877d9fe0e4c346a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151154"
---
# <span data-ttu-id="7155f-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7155f-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="7155f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7155f-102">SYNOPSIS</span></span>

<span data-ttu-id="7155f-103">Biztonsági mentési feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="7155f-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="7155f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7155f-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7155f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7155f-105">DESCRIPTION</span></span>

<span data-ttu-id="7155f-106">A **Get-AzRecoveryServicesBackupServicesBackupService** parancsmag azure biztonsági mentési feladatokat kap egy adott tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="7155f-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="7155f-107">Állítsa be a tároló környezetét a -VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="7155f-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="7155f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7155f-108">EXAMPLES</span></span>

### <span data-ttu-id="7155f-109">1. példa: Az összes folyamatban lévő feladat lekérte</span><span class="sxs-lookup"><span data-stu-id="7155f-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="7155f-110">Az első parancs tömbként kapja meg a folyamatban lévő feladatok állapotát, majd azt a $Joblist tárolja.</span><span class="sxs-lookup"><span data-stu-id="7155f-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="7155f-111">A második parancs a tömb első elemét $Joblist jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7155f-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="7155f-112">2. példa: Az összes sikertelen feladat be szerezze az elmúlt 7 napban</span><span class="sxs-lookup"><span data-stu-id="7155f-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="7155f-113">Ez a parancs sikertelen feladatokat kap a tároló utolsó hetében.</span><span class="sxs-lookup"><span data-stu-id="7155f-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="7155f-114">A *From* paraméter az UTC-ben megadott múltbeli hét napot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7155f-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="7155f-115">A parancs nem ad meg értéket a *To paraméternek.*</span><span class="sxs-lookup"><span data-stu-id="7155f-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="7155f-116">Ezért az aktuális idő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="7155f-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="7155f-117">3. példa: Folyamatban lévő feladat elvégzése és várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="7155f-117">Example 3: Get an in-progress job and wait for completion</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="7155f-118">Ez a parancsprogram lekérdezi az első folyamatban lévő feladatot, amíg a feladat be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="7155f-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="7155f-119">Megjegyzés: A **Wait-AzRecoveryServicesBackup Job** parancsmagot használva megvárhatja, amíg az Azure biztonságimásolat-feladat befejeződik a While ismétlés helyett.</span><span class="sxs-lookup"><span data-stu-id="7155f-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="7155f-120">4. példa: Az összes AzureVM-feladat lekérte az elmúlt 2 napban, amely sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="7155f-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="7155f-121">Az első parancsmag lekéri a tárolóobjektumot.</span><span class="sxs-lookup"><span data-stu-id="7155f-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="7155f-122">A második parancsmag az adott tárolóban tárolja az összes AzureVM-$jobs.</span><span class="sxs-lookup"><span data-stu-id="7155f-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="7155f-123">Módosítsa a BackupManagementType paraméter értékét MAB értékre a MAB-ügynök feladatok lehívása érdekében.</span><span class="sxs-lookup"><span data-stu-id="7155f-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="7155f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7155f-124">PARAMETERS</span></span>

### <span data-ttu-id="7155f-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7155f-125">-BackupManagementType</span></span>

<span data-ttu-id="7155f-126">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="7155f-126">The class of resources being protected.</span></span> <span data-ttu-id="7155f-127">Jelenleg a parancsmag által támogatott értékek: AzureVM, AzureStorage, AzureWorkload, MAB.</span><span class="sxs-lookup"><span data-stu-id="7155f-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7155f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7155f-128">-DefaultProfile</span></span>

<span data-ttu-id="7155f-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7155f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7155f-130">-From</span><span class="sxs-lookup"><span data-stu-id="7155f-130">-From</span></span>

<span data-ttu-id="7155f-131">A parancsmag által begyakorolt feladatok időtartományának **kezdését adja** meg DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="7155f-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7155f-132">**DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7155f-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="7155f-133">A **DateTime-objektumokról** a . `Get-Help Get-Date`</span><span class="sxs-lookup"><span data-stu-id="7155f-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="7155f-134">Dátumokhoz használja az UTC formátumot.</span><span class="sxs-lookup"><span data-stu-id="7155f-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="7155f-135">-Job</span><span class="sxs-lookup"><span data-stu-id="7155f-135">-Job</span></span>

<span data-ttu-id="7155f-136">A lekért feladat megadása.</span><span class="sxs-lookup"><span data-stu-id="7155f-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="7155f-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="7155f-137">-JobId</span></span>

<span data-ttu-id="7155f-138">A parancsmag által lekért feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7155f-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="7155f-139">Az azonosító a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase objektum JobId tulajdonsága.**</span><span class="sxs-lookup"><span data-stu-id="7155f-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="7155f-140">-Operation</span><span class="sxs-lookup"><span data-stu-id="7155f-140">-Operation</span></span>

<span data-ttu-id="7155f-141">A parancsmag által lekért feladatok műveletét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7155f-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7155f-142">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="7155f-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7155f-143">Biztonsági másolat</span><span class="sxs-lookup"><span data-stu-id="7155f-143">Backup</span></span>
- <span data-ttu-id="7155f-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="7155f-144">ConfigureBackup</span></span>
- <span data-ttu-id="7155f-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="7155f-145">DeleteBackupData</span></span>
- <span data-ttu-id="7155f-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="7155f-146">DisableBackup</span></span>
- <span data-ttu-id="7155f-147">Visszaállítás</span><span class="sxs-lookup"><span data-stu-id="7155f-147">Restore</span></span>
- <span data-ttu-id="7155f-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="7155f-148">BackupDataMove</span></span>

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

### <span data-ttu-id="7155f-149">-Állapot</span><span class="sxs-lookup"><span data-stu-id="7155f-149">-Status</span></span>

<span data-ttu-id="7155f-150">A parancsmag által lekért feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7155f-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7155f-151">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="7155f-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7155f-152">InProgress</span><span class="sxs-lookup"><span data-stu-id="7155f-152">InProgress</span></span>
- <span data-ttu-id="7155f-153">Nem sikerült</span><span class="sxs-lookup"><span data-stu-id="7155f-153">Failed</span></span>
- <span data-ttu-id="7155f-154">Megszakítva</span><span class="sxs-lookup"><span data-stu-id="7155f-154">Cancelled</span></span>
- <span data-ttu-id="7155f-155">Lemondás</span><span class="sxs-lookup"><span data-stu-id="7155f-155">Cancelling</span></span>
- <span data-ttu-id="7155f-156">Befejezve</span><span class="sxs-lookup"><span data-stu-id="7155f-156">Completed</span></span>
- <span data-ttu-id="7155f-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="7155f-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="7155f-158">-To</span><span class="sxs-lookup"><span data-stu-id="7155f-158">-To</span></span>

<span data-ttu-id="7155f-159">A parancsmag által lekért feladatok időtartományának **DateTime-objektumként** való végét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7155f-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7155f-160">Az alapértelmezett érték a rendszer aktuális ideje.</span><span class="sxs-lookup"><span data-stu-id="7155f-160">The default value is the current system time.</span></span>
<span data-ttu-id="7155f-161">Ha ezt a paramétert adja meg, a **-From** paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="7155f-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="7155f-162">Dátumokhoz használja az UTC formátumot.</span><span class="sxs-lookup"><span data-stu-id="7155f-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="7155f-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7155f-163">-VaultId</span></span>

<span data-ttu-id="7155f-164">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7155f-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7155f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7155f-165">CommonParameters</span></span>
<span data-ttu-id="7155f-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7155f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7155f-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7155f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7155f-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7155f-168">INPUTS</span></span>

### <span data-ttu-id="7155f-169">System.String</span><span class="sxs-lookup"><span data-stu-id="7155f-169">System.String</span></span>

## <span data-ttu-id="7155f-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7155f-170">OUTPUTS</span></span>

### <span data-ttu-id="7155f-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="7155f-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="7155f-172">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7155f-172">NOTES</span></span>

## <span data-ttu-id="7155f-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7155f-173">RELATED LINKS</span></span>

[<span data-ttu-id="7155f-174">Get-AzRecoveryServicesBackupServiceDetail</span><span class="sxs-lookup"><span data-stu-id="7155f-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="7155f-175">Stop-AzRecoveryServicesBackupService</span><span class="sxs-lookup"><span data-stu-id="7155f-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="7155f-176">Wait-AzRecoveryServicesBackupService</span><span class="sxs-lookup"><span data-stu-id="7155f-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
