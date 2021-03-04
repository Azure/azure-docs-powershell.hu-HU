---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 011b27cfff166173d485636a1e8890d917484651
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934737"
---
# <span data-ttu-id="61153-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="61153-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="61153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61153-102">SYNOPSIS</span></span>

<span data-ttu-id="61153-103">Biztonsági mentési feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="61153-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="61153-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="61153-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61153-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="61153-105">DESCRIPTION</span></span>

<span data-ttu-id="61153-106">A **Get-AzRecoveryServicesBackupServicesBackupService** parancsmag azure biztonsági mentési feladatokat kap egy adott tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="61153-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="61153-107">Állítsa be a tároló környezetét a -VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="61153-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="61153-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="61153-108">EXAMPLES</span></span>

### <span data-ttu-id="61153-109">1. példa: Az összes folyamatban lévő feladat lekérte</span><span class="sxs-lookup"><span data-stu-id="61153-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="61153-110">Az első parancs tömbként kapja meg a folyamatban lévő feladatok állapotát, majd azt a $Joblist változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="61153-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="61153-111">A második parancs a tömb első elemét $Joblist jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="61153-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="61153-112">2. példa: Az összes sikertelen feladat be szerezze az elmúlt 7 napban</span><span class="sxs-lookup"><span data-stu-id="61153-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="61153-113">Ez a parancs sikertelen feladatokat kap a tároló utolsó hetében.</span><span class="sxs-lookup"><span data-stu-id="61153-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="61153-114">A *From* paraméter az UTC-ben megadott múltbeli hét napot ad meg.</span><span class="sxs-lookup"><span data-stu-id="61153-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="61153-115">A parancs nem ad meg értéket a *To paraméternek.*</span><span class="sxs-lookup"><span data-stu-id="61153-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="61153-116">Ezért az aktuális idő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="61153-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="61153-117">3. példa: Folyamatban lévő feladat elvégzése és várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="61153-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="61153-118">Ez a parancsprogram lekérdezi az első folyamatban lévő feladatot, amíg a feladat be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="61153-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="61153-119">Megjegyzés: A **Wait-AzRecoveryServicesBackup Job** parancsmagot használva megvárhatja, amíg az Azure biztonságimásolat-feladat befejeződik a While ismétlés helyett.</span><span class="sxs-lookup"><span data-stu-id="61153-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="61153-120">4. példa: Az összes AzureVM-feladat lekérte az elmúlt 2 napban, amely sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="61153-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="61153-121">Az első parancsmag lekéri a tárolóobjektumot.</span><span class="sxs-lookup"><span data-stu-id="61153-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="61153-122">A második parancsmag az adott tárolóban tárolja az összes AzureVM-$jobs.</span><span class="sxs-lookup"><span data-stu-id="61153-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="61153-123">Módosítsa a BackupManagementType paraméter értékét MAB értékre a MAB-ügynök feladatok lehívása érdekében.</span><span class="sxs-lookup"><span data-stu-id="61153-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="61153-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61153-124">PARAMETERS</span></span>

### <span data-ttu-id="61153-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="61153-125">-BackupManagementType</span></span>

<span data-ttu-id="61153-126">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="61153-126">The class of resources being protected.</span></span> <span data-ttu-id="61153-127">Jelenleg a parancsmag által támogatott értékek: AzureVM, AzureStorage, AzureWorkload, MAB.</span><span class="sxs-lookup"><span data-stu-id="61153-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

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

### <span data-ttu-id="61153-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61153-128">-DefaultProfile</span></span>

<span data-ttu-id="61153-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61153-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61153-130">-From</span><span class="sxs-lookup"><span data-stu-id="61153-130">-From</span></span>

<span data-ttu-id="61153-131">A parancsmag által begyakorolt feladatok időtartományának **kezdését adja** meg DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="61153-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="61153-132">**DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="61153-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="61153-133">A **DateTime-objektumokról** további információt ad `Get-Help Get-Date` meg.</span><span class="sxs-lookup"><span data-stu-id="61153-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="61153-134">Dátumokhoz használja az UTC formátumot.</span><span class="sxs-lookup"><span data-stu-id="61153-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="61153-135">-Job</span><span class="sxs-lookup"><span data-stu-id="61153-135">-Job</span></span>

<span data-ttu-id="61153-136">A lekért feladat megadása.</span><span class="sxs-lookup"><span data-stu-id="61153-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="61153-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="61153-137">-JobId</span></span>

<span data-ttu-id="61153-138">A parancsmag által lekért feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="61153-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="61153-139">Az azonosító a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase objektum JobId tulajdonsága.**</span><span class="sxs-lookup"><span data-stu-id="61153-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="61153-140">-Művelet</span><span class="sxs-lookup"><span data-stu-id="61153-140">-Operation</span></span>

<span data-ttu-id="61153-141">A parancsmag által lekért feladatok műveletét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61153-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="61153-142">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="61153-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61153-143">Biztonsági másolat</span><span class="sxs-lookup"><span data-stu-id="61153-143">Backup</span></span>
- <span data-ttu-id="61153-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="61153-144">ConfigureBackup</span></span>
- <span data-ttu-id="61153-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="61153-145">DeleteBackupData</span></span>
- <span data-ttu-id="61153-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="61153-146">DisableBackup</span></span>
- <span data-ttu-id="61153-147">Visszaállítás</span><span class="sxs-lookup"><span data-stu-id="61153-147">Restore</span></span>
- <span data-ttu-id="61153-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="61153-148">BackupDataMove</span></span>

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

### <span data-ttu-id="61153-149">-Állapot</span><span class="sxs-lookup"><span data-stu-id="61153-149">-Status</span></span>

<span data-ttu-id="61153-150">A parancsmag által lekért feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="61153-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="61153-151">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="61153-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61153-152">InProgress</span><span class="sxs-lookup"><span data-stu-id="61153-152">InProgress</span></span>
- <span data-ttu-id="61153-153">Nem sikerült</span><span class="sxs-lookup"><span data-stu-id="61153-153">Failed</span></span>
- <span data-ttu-id="61153-154">Megszakítva</span><span class="sxs-lookup"><span data-stu-id="61153-154">Cancelled</span></span>
- <span data-ttu-id="61153-155">Lemondás</span><span class="sxs-lookup"><span data-stu-id="61153-155">Cancelling</span></span>
- <span data-ttu-id="61153-156">Befejezve</span><span class="sxs-lookup"><span data-stu-id="61153-156">Completed</span></span>
- <span data-ttu-id="61153-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="61153-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="61153-158">-To</span><span class="sxs-lookup"><span data-stu-id="61153-158">-To</span></span>

<span data-ttu-id="61153-159">A parancsmag által lekért feladatok időtartományának **DateTime-objektumként** való végét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61153-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="61153-160">Az alapértelmezett érték a rendszer aktuális ideje.</span><span class="sxs-lookup"><span data-stu-id="61153-160">The default value is the current system time.</span></span>
<span data-ttu-id="61153-161">Ha ezt a paramétert adja meg, a **-From** paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="61153-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="61153-162">Dátumokhoz használja az UTC formátumot.</span><span class="sxs-lookup"><span data-stu-id="61153-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="61153-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="61153-163">-VaultId</span></span>

<span data-ttu-id="61153-164">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="61153-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="61153-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61153-165">CommonParameters</span></span>
<span data-ttu-id="61153-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61153-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61153-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61153-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61153-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61153-168">INPUTS</span></span>

### <span data-ttu-id="61153-169">System.String</span><span class="sxs-lookup"><span data-stu-id="61153-169">System.String</span></span>

## <span data-ttu-id="61153-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61153-170">OUTPUTS</span></span>

### <span data-ttu-id="61153-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="61153-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="61153-172">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="61153-172">NOTES</span></span>

## <span data-ttu-id="61153-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61153-173">RELATED LINKS</span></span>

[<span data-ttu-id="61153-174">Get-AzRecoveryServicesBackupServiceDetail</span><span class="sxs-lookup"><span data-stu-id="61153-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="61153-175">Stop-AzRecoveryServicesBackupService</span><span class="sxs-lookup"><span data-stu-id="61153-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="61153-176">Wait-AzRecoveryServicesBackupService</span><span class="sxs-lookup"><span data-stu-id="61153-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
