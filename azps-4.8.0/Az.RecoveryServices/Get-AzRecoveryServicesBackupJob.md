---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025088"
---
# <span data-ttu-id="69e32-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="69e32-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="69e32-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69e32-102">SYNOPSIS</span></span>

<span data-ttu-id="69e32-103">Biztonsági mentési feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="69e32-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="69e32-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69e32-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69e32-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69e32-105">DESCRIPTION</span></span>

<span data-ttu-id="69e32-106">A **Get-AzRecoveryServicesBackupJob** parancsmag Azure biztonságimásolat-készítési feladatokat kap egy adott boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="69e32-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="69e32-107">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="69e32-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="69e32-108">Példák</span><span class="sxs-lookup"><span data-stu-id="69e32-108">EXAMPLES</span></span>

### <span data-ttu-id="69e32-109">Példa 1: minden folyamatban lévő feladat beolvasása</span><span class="sxs-lookup"><span data-stu-id="69e32-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="69e32-110">Az első parancs a folyamatban lévő munkák állapotát tömbként kapja, majd a $Joblist változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="69e32-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="69e32-111">A második parancs a $Joblist tömb első elemét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="69e32-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="69e32-112">2. példa: az összes sikertelen feladat beolvasása az elmúlt 7 napban</span><span class="sxs-lookup"><span data-stu-id="69e32-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="69e32-113">Ez a parancs a boltozat utolsó hetében sikertelen feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="69e32-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="69e32-114">A *from* paraméter egy, az UTC által megadott időpontban hét napot ad meg.</span><span class="sxs-lookup"><span data-stu-id="69e32-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="69e32-115">A parancs nem adja meg *a paraméter értékét* .</span><span class="sxs-lookup"><span data-stu-id="69e32-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="69e32-116">Ennek megfelelően az aktuális idő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="69e32-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="69e32-117">3. példa: folyamatban lévő munka beszerzése és várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="69e32-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="69e32-118">Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="69e32-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="69e32-119">Megjegyzés: a **WAIT-AzRecoveryServicesBackupJob** parancsmaggal megvárhatja, hogy egy Azure biztonsági mentési feladat a hurok helyett a befejezéshez legyen használható.</span><span class="sxs-lookup"><span data-stu-id="69e32-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="69e32-120">Példa 4: az összes AzureVM-feladat beszerzése az elmúlt két napon sikeres befejezés után</span><span class="sxs-lookup"><span data-stu-id="69e32-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="69e32-121">Az első parancsmag beolvassa a boltozat objektumát.</span><span class="sxs-lookup"><span data-stu-id="69e32-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="69e32-122">A második parancsmag minden olyan AzureVM-feladatot tárol az adott Vault-ban, amely a $jobs utolsó két napján befejeződött.</span><span class="sxs-lookup"><span data-stu-id="69e32-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="69e32-123">Módosítsa a BackupManagementType paraméter értékét a Mohácsi értékre a Mohácsi-ügynök munkahelyeinek beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="69e32-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="69e32-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69e32-124">PARAMETERS</span></span>

### <span data-ttu-id="69e32-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="69e32-125">-BackupManagementType</span></span>

<span data-ttu-id="69e32-126">A védelemmel ellátott erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="69e32-126">The class of resources being protected.</span></span> <span data-ttu-id="69e32-127">Jelenleg a parancsmag által támogatott értékek: AzureVM, AzureStorage, AzureWorkload, Mohácsi.</span><span class="sxs-lookup"><span data-stu-id="69e32-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

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

### <span data-ttu-id="69e32-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e32-128">-DefaultProfile</span></span>

<span data-ttu-id="69e32-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69e32-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69e32-130">-From</span><span class="sxs-lookup"><span data-stu-id="69e32-130">-From</span></span>

<span data-ttu-id="69e32-131">A parancsmag által beolvasott feladatok időtartományának kezdetét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="69e32-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="69e32-132">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="69e32-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="69e32-133">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="69e32-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="69e32-134">A dátumok esetében az UTC formátumot használhatja.</span><span class="sxs-lookup"><span data-stu-id="69e32-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="69e32-135">-Job</span><span class="sxs-lookup"><span data-stu-id="69e32-135">-Job</span></span>

<span data-ttu-id="69e32-136">A beolvasás feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="69e32-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="69e32-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="69e32-137">-JobId</span></span>

<span data-ttu-id="69e32-138">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="69e32-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="69e32-139">Az azonosító a **Microsoft. Azure. commands. RecoveryServices. backup. parancsmags. models. JobBase** objektum JobId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="69e32-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="69e32-140">-Művelet</span><span class="sxs-lookup"><span data-stu-id="69e32-140">-Operation</span></span>

<span data-ttu-id="69e32-141">A parancsmag által kapott feladatok működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="69e32-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="69e32-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="69e32-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69e32-143">Hát</span><span class="sxs-lookup"><span data-stu-id="69e32-143">Backup</span></span>
- <span data-ttu-id="69e32-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="69e32-144">ConfigureBackup</span></span>
- <span data-ttu-id="69e32-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="69e32-145">DeleteBackupData</span></span>
- <span data-ttu-id="69e32-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="69e32-146">DisableBackup</span></span>
- <span data-ttu-id="69e32-147">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="69e32-147">Restore</span></span>
- <span data-ttu-id="69e32-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="69e32-148">BackupDataMove</span></span>

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

### <span data-ttu-id="69e32-149">-Állapot</span><span class="sxs-lookup"><span data-stu-id="69e32-149">-Status</span></span>

<span data-ttu-id="69e32-150">A parancsmag által kapott feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="69e32-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="69e32-151">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="69e32-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69e32-152">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="69e32-152">InProgress</span></span>
- <span data-ttu-id="69e32-153">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="69e32-153">Failed</span></span>
- <span data-ttu-id="69e32-154">Lemondott</span><span class="sxs-lookup"><span data-stu-id="69e32-154">Cancelled</span></span>
- <span data-ttu-id="69e32-155">Értekezletének lemondása</span><span class="sxs-lookup"><span data-stu-id="69e32-155">Cancelling</span></span>
- <span data-ttu-id="69e32-156">Kész</span><span class="sxs-lookup"><span data-stu-id="69e32-156">Completed</span></span>
- <span data-ttu-id="69e32-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="69e32-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="69e32-158">-To</span><span class="sxs-lookup"><span data-stu-id="69e32-158">-To</span></span>

<span data-ttu-id="69e32-159">Annak a projektnek az időtartományának a végét adja meg **datetime** -objektumként, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="69e32-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="69e32-160">Az alapértelmezett érték az aktuális rendszer idő.</span><span class="sxs-lookup"><span data-stu-id="69e32-160">The default value is the current system time.</span></span>
<span data-ttu-id="69e32-161">Ha ezt a paramétert adja meg, a **-from** paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="69e32-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="69e32-162">A dátumok esetében az UTC formátumot használhatja.</span><span class="sxs-lookup"><span data-stu-id="69e32-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="69e32-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="69e32-163">-VaultId</span></span>

<span data-ttu-id="69e32-164">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="69e32-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="69e32-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e32-165">CommonParameters</span></span>
<span data-ttu-id="69e32-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69e32-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e32-167">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="69e32-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e32-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69e32-168">INPUTS</span></span>

### <span data-ttu-id="69e32-169">System. String</span><span class="sxs-lookup"><span data-stu-id="69e32-169">System.String</span></span>

## <span data-ttu-id="69e32-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69e32-170">OUTPUTS</span></span>

### <span data-ttu-id="69e32-171">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="69e32-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="69e32-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69e32-172">NOTES</span></span>

## <span data-ttu-id="69e32-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69e32-173">RELATED LINKS</span></span>

[<span data-ttu-id="69e32-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="69e32-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="69e32-175">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="69e32-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="69e32-176">Várjon-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="69e32-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
