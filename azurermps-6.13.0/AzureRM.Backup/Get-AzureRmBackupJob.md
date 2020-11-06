---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: cbdb60fb4ec139b1dae92b7dd8e2e54675ae1f90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495169"
---
# <span data-ttu-id="ef66a-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ef66a-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="ef66a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef66a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef66a-103">Biztonsági mentési feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="ef66a-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef66a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef66a-104">SYNTAX</span></span>

### <span data-ttu-id="ef66a-105">FiltersSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef66a-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef66a-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="ef66a-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef66a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef66a-107">DESCRIPTION</span></span>
<span data-ttu-id="ef66a-108">A **Get-AzureRmBackupJob** parancsmag Azure biztonságimásolat-készítési feladatokat kap egy adott boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="ef66a-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="ef66a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ef66a-109">EXAMPLES</span></span>

### <span data-ttu-id="ef66a-110">Példa 1: a biztonságimásolat-tároló minden feladatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ef66a-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="ef66a-111">Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="ef66a-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ef66a-112">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ef66a-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="ef66a-113">A második parancs a boltozat összes feladatát a $Vault-ban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ef66a-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="ef66a-114">2. példa: Befejezett feladatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="ef66a-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="ef66a-115">Ennek a parancsnak a kitöltése a $Vault boltozatán keresztül végezhető el.</span><span class="sxs-lookup"><span data-stu-id="ef66a-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="ef66a-116">3. példa: Sikertelen feladatok beolvasása a múlt héten</span><span class="sxs-lookup"><span data-stu-id="ef66a-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="ef66a-117">Ez a parancs nem működik a múlt héten a $Vault a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="ef66a-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="ef66a-118">A *from* paraméter a múltbeli hét napos időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef66a-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="ef66a-119">A parancs nem adja meg *a paraméter értékét* .</span><span class="sxs-lookup"><span data-stu-id="ef66a-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="ef66a-120">Ennek megfelelően az aktuális idő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="ef66a-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="ef66a-121">4. példa: egy folyamatban lévő projekt szavazás biztonsági másolata, amely befejeződött</span><span class="sxs-lookup"><span data-stu-id="ef66a-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="ef66a-122">Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="ef66a-122">This script polls the first job that is currently in progress until the job has completed.</span></span>
<span data-ttu-id="ef66a-123">A parancsfájl első sora megkapja a folyamatban lévő $Vault összes feladatát, majd a $Jobs tömbképlet tárolja ezeket a feladatokat.</span><span class="sxs-lookup"><span data-stu-id="ef66a-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>
<span data-ttu-id="ef66a-124">A második sor az első feladatot az $Job változó $Jobs tömbből tárolja.</span><span class="sxs-lookup"><span data-stu-id="ef66a-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>
<span data-ttu-id="ef66a-125">A harmadik sorba egy **while** ciklust indít, amely a feladat aktuális állapotát vizsgálja, amíg a feladat el nem készül.</span><span class="sxs-lookup"><span data-stu-id="ef66a-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="ef66a-126">A **while** kulcsszóval kapcsolatos további tudnivalókért írja be a következőt: `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="ef66a-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>
<span data-ttu-id="ef66a-127">A **while** ciklusban egy üzenet jelenik meg a konzolon, tíz másodpercig alszik, majd frissíti a $Job változót.</span><span class="sxs-lookup"><span data-stu-id="ef66a-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="ef66a-128">A parancsfájl a $Job meglévő értékével frissíti a $Job változót, és a jelenlegi parancsmagot használva beolvassa a feladat aktuális állapotát.</span><span class="sxs-lookup"><span data-stu-id="ef66a-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="ef66a-129">A Windows PowerShell-parancsmagokról a és a következő témakörben olvashat bővebben `Get-Help Write-Host` `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="ef66a-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>
<span data-ttu-id="ef66a-130">A parancsfájl utolsó sora közli, hogy a parancsfájl elkészült.</span><span class="sxs-lookup"><span data-stu-id="ef66a-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="ef66a-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef66a-131">PARAMETERS</span></span>

### <span data-ttu-id="ef66a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef66a-132">-DefaultProfile</span></span>
<span data-ttu-id="ef66a-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ef66a-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef66a-134">-From</span><span class="sxs-lookup"><span data-stu-id="ef66a-134">-From</span></span>
<span data-ttu-id="ef66a-135">A parancsmag által beolvasott feladatok időtartományának kezdetét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef66a-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ef66a-136">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ef66a-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="ef66a-137">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ef66a-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef66a-138">-Job</span><span class="sxs-lookup"><span data-stu-id="ef66a-138">-Job</span></span>
<span data-ttu-id="ef66a-139">A parancsmag által kapott feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef66a-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="ef66a-140">**AzureRmBackupJob** objektum beolvasásához használja az Get-AzureRmBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ef66a-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef66a-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="ef66a-141">-JobId</span></span>
<span data-ttu-id="ef66a-142">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="ef66a-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="ef66a-143">Az azonosító egy **AzureRmBackupJob** objektum **InstanceId** tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="ef66a-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="ef66a-144">**AzureRmBackupJob** -objektum beszerzéséhez használja a Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="ef66a-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef66a-145">-Művelet</span><span class="sxs-lookup"><span data-stu-id="ef66a-145">-Operation</span></span>
<span data-ttu-id="ef66a-146">A parancsmag által kapott feladatok működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef66a-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ef66a-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ef66a-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef66a-148">Hát</span><span class="sxs-lookup"><span data-stu-id="ef66a-148">Backup</span></span> 
- <span data-ttu-id="ef66a-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="ef66a-149">ConfigureBackup</span></span> 
- <span data-ttu-id="ef66a-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="ef66a-150">DeleteBackupData</span></span> 
- <span data-ttu-id="ef66a-151">Regisztráció</span><span class="sxs-lookup"><span data-stu-id="ef66a-151">Register</span></span> 
- <span data-ttu-id="ef66a-152">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="ef66a-152">Restore</span></span> 
- <span data-ttu-id="ef66a-153">Védtelen</span><span class="sxs-lookup"><span data-stu-id="ef66a-153">UnProtect</span></span> 
- <span data-ttu-id="ef66a-154">Regisztrációját</span><span class="sxs-lookup"><span data-stu-id="ef66a-154">Unregister</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef66a-155">-Állapot</span><span class="sxs-lookup"><span data-stu-id="ef66a-155">-Status</span></span>
<span data-ttu-id="ef66a-156">A parancsmag által kapott feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef66a-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ef66a-157">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ef66a-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef66a-158">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="ef66a-158">InProgress</span></span>
- <span data-ttu-id="ef66a-159">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="ef66a-159">Failed</span></span>
- <span data-ttu-id="ef66a-160">Lemondott</span><span class="sxs-lookup"><span data-stu-id="ef66a-160">Cancelled</span></span>
- <span data-ttu-id="ef66a-161">Értekezletének lemondása</span><span class="sxs-lookup"><span data-stu-id="ef66a-161">Cancelling</span></span>
- <span data-ttu-id="ef66a-162">Kész</span><span class="sxs-lookup"><span data-stu-id="ef66a-162">Completed</span></span>
- <span data-ttu-id="ef66a-163">CompletedWithWarnings: ezt a paramétert megadhatja az összes folyamatban lévő feladatban vagy az összes sikertelen munkalapon.</span><span class="sxs-lookup"><span data-stu-id="ef66a-163">CompletedWithWarnings You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef66a-164">-To</span><span class="sxs-lookup"><span data-stu-id="ef66a-164">-To</span></span>
<span data-ttu-id="ef66a-165">Annak a projektnek az időtartományának a végét adja meg **datetime** -objektumként, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="ef66a-165">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ef66a-166">Az alapértelmezett érték az aktuális rendszer idő.</span><span class="sxs-lookup"><span data-stu-id="ef66a-166">The default value is the current system time.</span></span>
<span data-ttu-id="ef66a-167">Ha ezt a paramétert adja meg, a *from* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="ef66a-167">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef66a-168">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="ef66a-168">-Type</span></span>
<span data-ttu-id="ef66a-169">Annak a tárolónak a típusa, amelyre a parancsmag biztonsági mentési feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="ef66a-169">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="ef66a-170">Jelenleg az egyetlen támogatott érték a AzureVM.</span><span class="sxs-lookup"><span data-stu-id="ef66a-170">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef66a-171">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="ef66a-171">-Vault</span></span>
<span data-ttu-id="ef66a-172">Annak a biztonságimásolat-tárolónak a megadása, amelyhez ez a parancsmag feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="ef66a-172">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="ef66a-173">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ef66a-173">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef66a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef66a-174">CommonParameters</span></span>
<span data-ttu-id="ef66a-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef66a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef66a-176">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef66a-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef66a-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef66a-177">INPUTS</span></span>

### <span data-ttu-id="ef66a-178">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef66a-178">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="ef66a-179">Paraméterek: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef66a-179">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="ef66a-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef66a-180">OUTPUTS</span></span>

### <span data-ttu-id="ef66a-181">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="ef66a-181">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="ef66a-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef66a-182">NOTES</span></span>
* <span data-ttu-id="ef66a-183">Nincs</span><span class="sxs-lookup"><span data-stu-id="ef66a-183">None</span></span>

## <span data-ttu-id="ef66a-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef66a-184">RELATED LINKS</span></span>

[<span data-ttu-id="ef66a-185">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef66a-185">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ef66a-186">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ef66a-186">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="ef66a-187">Várjon-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ef66a-187">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


