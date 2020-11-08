---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195192"
---
# <span data-ttu-id="ee476-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ee476-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="ee476-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee476-102">SYNOPSIS</span></span>
<span data-ttu-id="ee476-103">Biztonságimásolat-védelmi házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ee476-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="ee476-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee476-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee476-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee476-105">DESCRIPTION</span></span>
<span data-ttu-id="ee476-106">A **New-AzRecoveryServicesBackupProtectionPolicy** parancsmag biztonsági mentési házirendet hoz létre egy boltozatban.</span><span class="sxs-lookup"><span data-stu-id="ee476-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="ee476-107">A védelmi házirend legalább egy adatmegőrzési házirendhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="ee476-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="ee476-108">Az adatmegőrzési házirend azt határozza meg, hogy mennyi ideig tart a helyreállítási pont az Azure Backup szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="ee476-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="ee476-109">Az alapértelmezett adatmegőrzési házirend beszerzéséhez használhatja az Get-AzRecoveryServicesBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ee476-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="ee476-110">Az alapértelmezett ütemezési házirend beszerzéséhez használhatja a Get-AzRecoveryServicesBackupSchedulePolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ee476-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="ee476-111">A **SchedulePolicy** és az **RetentionPolicy** objektum a **New-AzRecoveryServicesBackupProtectionPolicy** parancsmag bemenetéhez használatos.</span><span class="sxs-lookup"><span data-stu-id="ee476-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="ee476-112">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="ee476-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ee476-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ee476-113">EXAMPLES</span></span>

### <span data-ttu-id="ee476-114">Példa 1: biztonsági mentést biztosító házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="ee476-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="ee476-115">Az első parancs megkapja a bázis **SchedulePolicyObject** , majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ee476-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="ee476-116">A második parancs eltávolítja az összes ütemezett futtatási időpontot a $SchPol ütemezési házirendjéből.</span><span class="sxs-lookup"><span data-stu-id="ee476-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="ee476-117">A harmadik parancs az Get-Date parancsmagot használja az aktuális dátum és idő beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="ee476-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="ee476-118">A negyedik parancs hozzáadja az aktuális dátumot és időpontot $Dt az ütemezési házirendhez ütemezett futási időpontként.</span><span class="sxs-lookup"><span data-stu-id="ee476-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="ee476-119">Az ötödik parancs beolvassa a bázis **RetentionPolicy** objektumot, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ee476-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="ee476-120">A hatodik parancs a retenciós idő házirendjét 365 napra állítja be.</span><span class="sxs-lookup"><span data-stu-id="ee476-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="ee476-121">A végleges parancs az előző parancsok által létrehozott ütemezési és adatmegőrzési szabályok alapján hoz létre **BackupProtectionPolicy** objektumot.</span><span class="sxs-lookup"><span data-stu-id="ee476-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="ee476-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="ee476-122">Example 2</span></span>

<span data-ttu-id="ee476-123">Biztonságimásolat-védelmi házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ee476-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="ee476-124">autogenerated</span><span class="sxs-lookup"><span data-stu-id="ee476-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="ee476-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee476-125">PARAMETERS</span></span>

### <span data-ttu-id="ee476-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ee476-126">-BackupManagementType</span></span>
<span data-ttu-id="ee476-127">A védelemmel ellátott erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="ee476-127">The class of resources being protected.</span></span> <span data-ttu-id="ee476-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ee476-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee476-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee476-129">AzureVM</span></span> 
- <span data-ttu-id="ee476-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="ee476-130">AzureStorage</span></span>
- <span data-ttu-id="ee476-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="ee476-131">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee476-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee476-132">-DefaultProfile</span></span>
<span data-ttu-id="ee476-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee476-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee476-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee476-134">-Name</span></span>
<span data-ttu-id="ee476-135">A házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee476-135">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee476-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ee476-136">-RetentionPolicy</span></span>
<span data-ttu-id="ee476-137">Az alap **RetentionPolicy** objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee476-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="ee476-138">A Get-AzRecoveryServicesBackupRetentionPolicyObject parancsmaggal **RetentionPolicy** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="ee476-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee476-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="ee476-139">-SchedulePolicy</span></span>
<span data-ttu-id="ee476-140">Az alap **SchedulePolicy** objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee476-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="ee476-141">A Get-AzRecoveryServicesBackupSchedulePolicyObject parancsmaggal **SchedulePolicy** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="ee476-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee476-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ee476-142">-VaultId</span></span>
<span data-ttu-id="ee476-143">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="ee476-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ee476-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="ee476-144">-WorkloadType</span></span>
<span data-ttu-id="ee476-145">Az erőforrás terhelési típusa.</span><span class="sxs-lookup"><span data-stu-id="ee476-145">Workload type of the resource.</span></span> <span data-ttu-id="ee476-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ee476-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee476-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ee476-147">AzureVM</span></span> 
- <span data-ttu-id="ee476-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="ee476-148">AzureFiles</span></span>
- <span data-ttu-id="ee476-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="ee476-149">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee476-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee476-150">-Confirm</span></span>
<span data-ttu-id="ee476-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee476-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee476-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee476-152">-WhatIf</span></span>
<span data-ttu-id="ee476-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee476-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="ee476-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee476-154">CommonParameters</span></span>
<span data-ttu-id="ee476-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee476-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee476-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ee476-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee476-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee476-157">INPUTS</span></span>

### <span data-ttu-id="ee476-158">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. WorkloadType</span><span class="sxs-lookup"><span data-stu-id="ee476-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="ee476-159">System. nulla ' 1 [[Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. BackupManagementType, Microsoft. Azure. PowerShell. parancsmagok. RecoveryServices. backup. models, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ee476-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ee476-160">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="ee476-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="ee476-161">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="ee476-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="ee476-162">System. String</span><span class="sxs-lookup"><span data-stu-id="ee476-162">System.String</span></span>

## <span data-ttu-id="ee476-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee476-163">OUTPUTS</span></span>

### <span data-ttu-id="ee476-164">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="ee476-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="ee476-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee476-165">NOTES</span></span>

## <span data-ttu-id="ee476-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee476-166">RELATED LINKS</span></span>

[<span data-ttu-id="ee476-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ee476-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="ee476-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ee476-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ee476-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ee476-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="ee476-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="ee476-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="ee476-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ee476-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ee476-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ee476-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


