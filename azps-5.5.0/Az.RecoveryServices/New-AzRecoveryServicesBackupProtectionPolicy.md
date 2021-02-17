---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156530"
---
# <span data-ttu-id="542a3-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="542a3-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="542a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="542a3-102">SYNOPSIS</span></span>
<span data-ttu-id="542a3-103">Biztonságimásolat-védelmi házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="542a3-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="542a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="542a3-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="542a3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="542a3-105">DESCRIPTION</span></span>
<span data-ttu-id="542a3-106">A **New-AzRecoveryServicesBackupProtectionPolicy** parancsmag biztonsági mentési házirendet hoz létre a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="542a3-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="542a3-107">A védelmi házirendek legalább egy adatmegőrzési házirendhez kapcsolódnak.</span><span class="sxs-lookup"><span data-stu-id="542a3-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="542a3-108">Az adatmegőrzési házirend azt határozza meg, hogy mennyi ideig tart egy helyreállítási pontot az Azure Biztonsági másolat szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="542a3-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="542a3-109">A Get-AzRecoveryServicesBackupRetentionPolicyObject használhatja az alapértelmezett adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="542a3-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="542a3-110">Az alapértelmezett ütemezési házirendet Get-AzRecoveryServicesBackupSchedulePolicyObject a Get-AzRecoveryServicesBackupSchedulePolicyObject parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="542a3-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="542a3-111">A **SchedulePolicy** és **a RetentionPolicy** objektum a **New-AzRecoveryServicesBackupProtectionPolicy** parancsmag bemeneteként használatos.</span><span class="sxs-lookup"><span data-stu-id="542a3-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="542a3-112">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="542a3-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="542a3-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="542a3-113">EXAMPLES</span></span>

### <span data-ttu-id="542a3-114">1. példa: Biztonságimásolat-védelmi házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="542a3-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="542a3-115">Az első parancs egy alap **SchedulePolicyObject** parancsot kap, majd a $SchPol tárolja.</span><span class="sxs-lookup"><span data-stu-id="542a3-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="542a3-116">A második parancs minden ütemezett futási időt eltávolít az ütemezési házirendből a $SchPol.</span><span class="sxs-lookup"><span data-stu-id="542a3-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="542a3-117">A harmadik parancs a Get-Date parancsmag segítségével begyakorlja az aktuális dátumot és időt.</span><span class="sxs-lookup"><span data-stu-id="542a3-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="542a3-118">A negyedik parancs hozzáadja az aktuális dátumot és időt $Dt ütemezési házirendhez ütemezett futási időként.</span><span class="sxs-lookup"><span data-stu-id="542a3-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="542a3-119">Az ötödik parancs egy alap **RetentionPolicy** objektumot kap, majd a helyi $RetPol tárolja.</span><span class="sxs-lookup"><span data-stu-id="542a3-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="542a3-120">A hatodik parancs 365 napra állítja az adatmegőrzési időtartamra vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="542a3-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="542a3-121">Az utolsó parancs létrehoz egy **BackupProtectionPolicy** objektumot az előző parancsok által létrehozott ütemezési és adatmegőrzési házirendek alapján.</span><span class="sxs-lookup"><span data-stu-id="542a3-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="542a3-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="542a3-122">Example 2</span></span>

<span data-ttu-id="542a3-123">Biztonságimásolat-védelmi házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="542a3-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="542a3-124">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="542a3-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="542a3-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="542a3-125">PARAMETERS</span></span>

### <span data-ttu-id="542a3-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="542a3-126">-BackupManagementType</span></span>
<span data-ttu-id="542a3-127">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="542a3-127">The class of resources being protected.</span></span> <span data-ttu-id="542a3-128">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="542a3-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="542a3-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="542a3-129">AzureVM</span></span> 
- <span data-ttu-id="542a3-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="542a3-130">AzureStorage</span></span>
- <span data-ttu-id="542a3-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="542a3-131">AzureWorkload</span></span>

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

### <span data-ttu-id="542a3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542a3-132">-DefaultProfile</span></span>
<span data-ttu-id="542a3-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="542a3-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="542a3-134">-Name</span><span class="sxs-lookup"><span data-stu-id="542a3-134">-Name</span></span>
<span data-ttu-id="542a3-135">A házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="542a3-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="542a3-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="542a3-136">-RetentionPolicy</span></span>
<span data-ttu-id="542a3-137">Az alap **RetentionPolicy objektumot** adja meg.</span><span class="sxs-lookup"><span data-stu-id="542a3-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="542a3-138">A Get-AzRecoveryServicesBackupRetentionPolicyObject parancsmag használatával lekértheti a **RetentionPolicy objektumot.**</span><span class="sxs-lookup"><span data-stu-id="542a3-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="542a3-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="542a3-139">-SchedulePolicy</span></span>
<span data-ttu-id="542a3-140">Az alap **SchedulePolicy objektumot** adja meg.</span><span class="sxs-lookup"><span data-stu-id="542a3-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="542a3-141">A **SchedulePolicy** Get-AzRecoveryServicesBackupSchedulePolicyObject használhatja a Get-AzRecoveryServicesBackupSchedulePolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="542a3-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="542a3-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="542a3-142">-VaultId</span></span>
<span data-ttu-id="542a3-143">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="542a3-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="542a3-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="542a3-144">-WorkloadType</span></span>
<span data-ttu-id="542a3-145">Az erőforrás terheléstípusa.</span><span class="sxs-lookup"><span data-stu-id="542a3-145">Workload type of the resource.</span></span> <span data-ttu-id="542a3-146">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="542a3-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="542a3-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="542a3-147">AzureVM</span></span> 
- <span data-ttu-id="542a3-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="542a3-148">AzureFiles</span></span>
- <span data-ttu-id="542a3-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="542a3-149">MSSQL</span></span>

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

### <span data-ttu-id="542a3-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="542a3-150">-Confirm</span></span>
<span data-ttu-id="542a3-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="542a3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="542a3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="542a3-152">-WhatIf</span></span>
<span data-ttu-id="542a3-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="542a3-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="542a3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542a3-154">CommonParameters</span></span>
<span data-ttu-id="542a3-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="542a3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542a3-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="542a3-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542a3-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="542a3-157">INPUTS</span></span>

### <span data-ttu-id="542a3-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span><span class="sxs-lookup"><span data-stu-id="542a3-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="542a3-159">System.Nullable'1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="542a3-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="542a3-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="542a3-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="542a3-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="542a3-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="542a3-162">System.String</span><span class="sxs-lookup"><span data-stu-id="542a3-162">System.String</span></span>

## <span data-ttu-id="542a3-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="542a3-163">OUTPUTS</span></span>

### <span data-ttu-id="542a3-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="542a3-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="542a3-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="542a3-165">NOTES</span></span>

## <span data-ttu-id="542a3-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="542a3-166">RELATED LINKS</span></span>

[<span data-ttu-id="542a3-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="542a3-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="542a3-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="542a3-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="542a3-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="542a3-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="542a3-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="542a3-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="542a3-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="542a3-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="542a3-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="542a3-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


