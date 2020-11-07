---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc23d8535e7aaca656379811121ed09bad2f64bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838594"
---
# <span data-ttu-id="f7e79-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f7e79-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="f7e79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7e79-102">SYNOPSIS</span></span>

<span data-ttu-id="f7e79-103">Biztonsági mentési feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="f7e79-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="f7e79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7e79-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7e79-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7e79-105">DESCRIPTION</span></span>

<span data-ttu-id="f7e79-106">A **Get-AzRecoveryServicesBackupJob** parancsmag Azure biztonságimásolat-készítési feladatokat kap egy adott boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="f7e79-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="f7e79-107">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="f7e79-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f7e79-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f7e79-108">EXAMPLES</span></span>

### <span data-ttu-id="f7e79-109">Példa 1: minden folyamatban lévő feladat beolvasása</span><span class="sxs-lookup"><span data-stu-id="f7e79-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="f7e79-110">Az első parancs a folyamatban lévő munkák állapotát tömbként kapja, majd a $Joblist változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f7e79-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="f7e79-111">A második parancs a $Joblist tömb első elemét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="f7e79-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="f7e79-112">2. példa: az összes sikertelen feladat beolvasása az elmúlt 7 napban</span><span class="sxs-lookup"><span data-stu-id="f7e79-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="f7e79-113">Ez a parancs a boltozat utolsó hetében sikertelen feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="f7e79-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="f7e79-114">A *from* paraméter egy, az UTC által megadott időpontban hét napot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f7e79-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="f7e79-115">A parancs nem adja meg *a paraméter értékét* .</span><span class="sxs-lookup"><span data-stu-id="f7e79-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="f7e79-116">Ennek megfelelően az aktuális idő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="f7e79-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="f7e79-117">3. példa: folyamatban lévő munka beszerzése és várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="f7e79-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="f7e79-118">Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="f7e79-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="f7e79-119">Megjegyzés: a **WAIT-AzRecoveryServicesBackupJob** parancsmaggal megvárhatja, hogy egy Azure biztonsági mentési feladat a hurok helyett a befejezéshez legyen használható.</span><span class="sxs-lookup"><span data-stu-id="f7e79-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="f7e79-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7e79-120">PARAMETERS</span></span>

### <span data-ttu-id="f7e79-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f7e79-121">-BackupManagementType</span></span>

<span data-ttu-id="f7e79-122">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7e79-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="f7e79-123">Jelenleg csak a AzureVM és a AzureStorage támogatott.</span><span class="sxs-lookup"><span data-stu-id="f7e79-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="f7e79-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e79-124">-DefaultProfile</span></span>

<span data-ttu-id="f7e79-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7e79-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7e79-126">-From</span><span class="sxs-lookup"><span data-stu-id="f7e79-126">-From</span></span>

<span data-ttu-id="f7e79-127">A parancsmag által beolvasott feladatok időtartományának kezdetét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7e79-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f7e79-128">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f7e79-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="f7e79-129">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f7e79-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="f7e79-130">A dátumok esetében az UTC formátumot használhatja.</span><span class="sxs-lookup"><span data-stu-id="f7e79-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="f7e79-131">-Job</span><span class="sxs-lookup"><span data-stu-id="f7e79-131">-Job</span></span>

<span data-ttu-id="f7e79-132">A beolvasás feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7e79-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="f7e79-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="f7e79-133">-JobId</span></span>

<span data-ttu-id="f7e79-134">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="f7e79-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="f7e79-135">Az azonosító a **Microsoft. Azure. commands. RecoveryServices. backup. parancsmags. models. JobBase** objektum JobId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="f7e79-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="f7e79-136">-Művelet</span><span class="sxs-lookup"><span data-stu-id="f7e79-136">-Operation</span></span>

<span data-ttu-id="f7e79-137">A parancsmag által kapott feladatok működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7e79-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f7e79-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f7e79-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7e79-139">Hát</span><span class="sxs-lookup"><span data-stu-id="f7e79-139">Backup</span></span>
- <span data-ttu-id="f7e79-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="f7e79-140">ConfigureBackup</span></span>
- <span data-ttu-id="f7e79-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="f7e79-141">DeleteBackupData</span></span>
- <span data-ttu-id="f7e79-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="f7e79-142">DisableBackup</span></span>
- <span data-ttu-id="f7e79-143">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="f7e79-143">Restore</span></span>

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

### <span data-ttu-id="f7e79-144">-Állapot</span><span class="sxs-lookup"><span data-stu-id="f7e79-144">-Status</span></span>

<span data-ttu-id="f7e79-145">A parancsmag által kapott feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7e79-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f7e79-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f7e79-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7e79-147">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="f7e79-147">InProgress</span></span>
- <span data-ttu-id="f7e79-148">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="f7e79-148">Failed</span></span>
- <span data-ttu-id="f7e79-149">Lemondott</span><span class="sxs-lookup"><span data-stu-id="f7e79-149">Cancelled</span></span>
- <span data-ttu-id="f7e79-150">Értekezletének lemondása</span><span class="sxs-lookup"><span data-stu-id="f7e79-150">Cancelling</span></span>
- <span data-ttu-id="f7e79-151">Kész</span><span class="sxs-lookup"><span data-stu-id="f7e79-151">Completed</span></span>
- <span data-ttu-id="f7e79-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="f7e79-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="f7e79-153">-To</span><span class="sxs-lookup"><span data-stu-id="f7e79-153">-To</span></span>

<span data-ttu-id="f7e79-154">Annak a projektnek az időtartományának a végét adja meg **datetime** -objektumként, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="f7e79-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f7e79-155">Az alapértelmezett érték az aktuális rendszer idő.</span><span class="sxs-lookup"><span data-stu-id="f7e79-155">The default value is the current system time.</span></span>
<span data-ttu-id="f7e79-156">Ha ezt a paramétert adja meg, a **-from** paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="f7e79-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="f7e79-157">A dátumok esetében az UTC formátumot használhatja.</span><span class="sxs-lookup"><span data-stu-id="f7e79-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="f7e79-158">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f7e79-158">-VaultId</span></span>

<span data-ttu-id="f7e79-159">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="f7e79-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f7e79-160">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e79-160">-CommonParameters</span></span>

<span data-ttu-id="f7e79-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7e79-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e79-162">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f7e79-162">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e79-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7e79-163">INPUTS</span></span>

### <span data-ttu-id="f7e79-164">System. String</span><span class="sxs-lookup"><span data-stu-id="f7e79-164">System.String</span></span>

## <span data-ttu-id="f7e79-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7e79-165">OUTPUTS</span></span>

### <span data-ttu-id="f7e79-166">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="f7e79-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f7e79-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7e79-167">NOTES</span></span>

## <span data-ttu-id="f7e79-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7e79-168">RELATED LINKS</span></span>

[<span data-ttu-id="f7e79-169">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="f7e79-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="f7e79-170">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f7e79-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="f7e79-171">Várjon-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f7e79-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
