---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158530"
---
# <span data-ttu-id="13f65-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13f65-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="13f65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13f65-102">SYNOPSIS</span></span>
<span data-ttu-id="13f65-103">Biztonságimásolat-védelmi házirendet módosít.</span><span class="sxs-lookup"><span data-stu-id="13f65-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="13f65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13f65-104">SYNTAX</span></span>

### <span data-ttu-id="13f65-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="13f65-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f65-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="13f65-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13f65-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13f65-107">DESCRIPTION</span></span>
<span data-ttu-id="13f65-108">A **Set-AzRecoveryServicesBackupProtectionPolicy** parancsmag módosít egy meglévő Azure biztonsági mentési védelmi házirendet.</span><span class="sxs-lookup"><span data-stu-id="13f65-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="13f65-109">Módosíthatja a biztonsági mentési ütemezés és az adatmegőrzési házirend összetevőit.</span><span class="sxs-lookup"><span data-stu-id="13f65-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="13f65-110">Az ön által végrehajtott módosítások hatással vannak a házirendhez társított elemek biztonsági mentésére és megőrzésére.</span><span class="sxs-lookup"><span data-stu-id="13f65-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="13f65-111">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="13f65-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="13f65-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13f65-112">EXAMPLES</span></span>

### <span data-ttu-id="13f65-113">1. példa: Biztonságimásolat-védelmi házirend módosítása</span><span class="sxs-lookup"><span data-stu-id="13f65-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Time = Get-Date
PS C:\> $Time1 = Get-Date -Year $Time.Year -Month $Time.Month -Day $Time.Day -Hour $Time.Hour -Minute 0 -Second 0 -Millisecond 0
PS C:\> $Time1 = $Time1.ToUniversalTime()
PS C:\> $SchPol.ScheduleRunTimes.Add($Time1)
PS C:\> $SchPol.ScheduleRunFrequency.Clear
PS C:\> $SchPol.ScheduleRunDays.Add("Monday")
PS C:\> $SchPol.ScheduleRunFrequency="Weekly"
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.IsDailyScheduleEnabled=$false
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 0
PS C:\> $RetPol.IsWeeklyScheduleEnabled=$true 
PS C:\> $RetPol.WeeklySchedule.DaysOfTheWeek.Add("Monday")
PS C:\> $RetPol.WeeklySchedule.DurationCountInWeeks = 365
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "azurefiles" -Name "azurefilesvault"
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "TestPolicy" -VaultId $vault.ID
PS C:\> $Pol.SnapshotRetentionInDays=5
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="13f65-114">A következő lépésekkel módosíthatja a védelmi házirendet:</span><span class="sxs-lookup"><span data-stu-id="13f65-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="13f65-115">Alap SchedulePolicyObject és retentionPolicyObject alaphoz jut.</span><span class="sxs-lookup"><span data-stu-id="13f65-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="13f65-116">Tárolja őket valamilyen változóban.</span><span class="sxs-lookup"><span data-stu-id="13f65-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="13f65-117">Állítsa be az ütemezési és adatmegőrzési házirend objektum különböző paramétereit a követelményeknek megfelelően.</span><span class="sxs-lookup"><span data-stu-id="13f65-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="13f65-118">A fenti mintaprogramban például heti védelmi szabályzatot próbálunk beállítani.</span><span class="sxs-lookup"><span data-stu-id="13f65-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="13f65-119">Ezért az ütemezés gyakoriságát "Hetente" gyakoriságra módosítottuk, és frissítettük az ütemezés futási idejét is.</span><span class="sxs-lookup"><span data-stu-id="13f65-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="13f65-120">Az adatmegőrzési házirend-objektumban frissítettük a heti adatmegőrzési időtartamot, és beállítottuk a "heti ütemezés engedélyezve" jelzőt.</span><span class="sxs-lookup"><span data-stu-id="13f65-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="13f65-121">Ha napi házirendet szeretne beállítani, állítsa a "napi ütemezés engedélyezve" jelzőt igazra, és rendelje hozzá a megfelelő értékeket a többi objektumparaméterhez.</span><span class="sxs-lookup"><span data-stu-id="13f65-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="13f65-122">Szerezze be a módosítani kívánt biztonságimásolat-védelmi házirendet, és tárolja egy változóban.</span><span class="sxs-lookup"><span data-stu-id="13f65-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="13f65-123">A fenti példában a "TestPolicy" nevű biztonságimásolat-házirendet kértük a módosításhoz.</span><span class="sxs-lookup"><span data-stu-id="13f65-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="13f65-124">Módosítsa a 3. lépésben beolvasott biztonságimásolat-védelmi házirendet a módosított ütemezési házirendobjektummal és adatmegőrzési házirend-objektummal.</span><span class="sxs-lookup"><span data-stu-id="13f65-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="13f65-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13f65-125">PARAMETERS</span></span>

### <span data-ttu-id="13f65-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f65-126">-DefaultProfile</span></span>
<span data-ttu-id="13f65-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13f65-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13f65-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="13f65-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="13f65-129">Switch Parameter indicating whether to retry Policy Update for failed items.</span><span class="sxs-lookup"><span data-stu-id="13f65-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13f65-130">-Házirend</span><span class="sxs-lookup"><span data-stu-id="13f65-130">-Policy</span></span>
<span data-ttu-id="13f65-131">A parancsmag által módosított biztonságimásolat-védelmi házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="13f65-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="13f65-132">A **BackupProtectionPolicy** objektum beszerzéséhez használja a Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="13f65-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13f65-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="13f65-133">-RetentionPolicy</span></span>
<span data-ttu-id="13f65-134">Az alap adatmegőrzési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="13f65-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="13f65-135">A **RetentionPolicy objektum** beszerzéséhez használja a Get-AzRecoveryServicesBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="13f65-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13f65-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="13f65-136">-SchedulePolicy</span></span>
<span data-ttu-id="13f65-137">Az alapütemterv-házirendobjektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="13f65-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="13f65-138">**SchedulePolicy-objektum** beszerzéséhez használja a Get-AzRecoveryServicesBackupSchedulePolicyObject objektumot.</span><span class="sxs-lookup"><span data-stu-id="13f65-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13f65-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="13f65-139">-VaultId</span></span>
<span data-ttu-id="13f65-140">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="13f65-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="13f65-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13f65-141">-Confirm</span></span>
<span data-ttu-id="13f65-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13f65-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13f65-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13f65-143">-WhatIf</span></span>
<span data-ttu-id="13f65-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13f65-144">Shows what would happen if the cmdlet runs.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13f65-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f65-145">CommonParameters</span></span>
<span data-ttu-id="13f65-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f65-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f65-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13f65-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f65-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13f65-148">INPUTS</span></span>

### <span data-ttu-id="13f65-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="13f65-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="13f65-150">System.String</span><span class="sxs-lookup"><span data-stu-id="13f65-150">System.String</span></span>

## <span data-ttu-id="13f65-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13f65-151">OUTPUTS</span></span>

### <span data-ttu-id="13f65-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="13f65-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="13f65-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13f65-153">NOTES</span></span>

## <span data-ttu-id="13f65-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13f65-154">RELATED LINKS</span></span>

[<span data-ttu-id="13f65-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13f65-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="13f65-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="13f65-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="13f65-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13f65-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="13f65-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13f65-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


