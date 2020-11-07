---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 6aaf7fcd32ae7d50f273d69835f9131032b68c21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839057"
---
# <span data-ttu-id="ad345-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad345-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="ad345-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad345-102">SYNOPSIS</span></span>
<span data-ttu-id="ad345-103">Biztonságimásolat-védelmi házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ad345-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="ad345-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad345-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad345-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad345-105">DESCRIPTION</span></span>
<span data-ttu-id="ad345-106">A **New-AzRecoveryServicesBackupProtectionPolicy** parancsmag biztonsági mentési házirendet hoz létre egy boltozatban.</span><span class="sxs-lookup"><span data-stu-id="ad345-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="ad345-107">A védelmi házirend legalább egy adatmegőrzési házirendhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="ad345-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="ad345-108">Az adatmegőrzési házirend azt határozza meg, hogy mennyi ideig tart a helyreállítási pont az Azure Backup szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="ad345-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="ad345-109">Az alapértelmezett adatmegőrzési házirend beszerzéséhez használhatja az Get-AzRecoveryServicesBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ad345-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="ad345-110">Az alapértelmezett ütemezési házirend beszerzéséhez használhatja a Get-AzRecoveryServicesBackupSchedulePolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ad345-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="ad345-111">A **SchedulePolicy** és az **RetentionPolicy** objektum a **New-AzRecoveryServicesBackupProtectionPolicy** parancsmag bemenetéhez használatos.</span><span class="sxs-lookup"><span data-stu-id="ad345-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="ad345-112">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="ad345-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ad345-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ad345-113">EXAMPLES</span></span>

### <span data-ttu-id="ad345-114">Példa 1: biztonsági mentést biztosító házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="ad345-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="ad345-115">Az első parancs megkapja a bázis **SchedulePolicyObject** , majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ad345-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="ad345-116">A második parancs eltávolítja az összes ütemezett futtatási időpontot a $SchPol ütemezési házirendjéből.</span><span class="sxs-lookup"><span data-stu-id="ad345-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="ad345-117">A harmadik parancs az Get-Date parancsmagot használja az aktuális dátum és idő beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="ad345-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="ad345-118">A negyedik parancs hozzáadja az aktuális dátumot és időpontot $Dt az ütemezési házirendhez ütemezett futási időpontként.</span><span class="sxs-lookup"><span data-stu-id="ad345-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="ad345-119">Az ötödik parancs beolvassa a bázis **RetentionPolicy** objektumot, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ad345-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="ad345-120">A hatodik parancs a retenciós idő házirendjét 365 napra állítja be.</span><span class="sxs-lookup"><span data-stu-id="ad345-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="ad345-121">A végleges parancs az előző parancsok által létrehozott ütemezési és adatmegőrzési szabályok alapján hoz létre **BackupProtectionPolicy** objektumot.</span><span class="sxs-lookup"><span data-stu-id="ad345-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="ad345-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad345-122">PARAMETERS</span></span>

### <span data-ttu-id="ad345-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ad345-123">-BackupManagementType</span></span>
<span data-ttu-id="ad345-124">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad345-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="ad345-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ad345-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad345-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad345-126">AzureVM</span></span> 
- <span data-ttu-id="ad345-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="ad345-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad345-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad345-128">-DefaultProfile</span></span>
<span data-ttu-id="ad345-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad345-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad345-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad345-130">-Name</span></span>
<span data-ttu-id="ad345-131">A házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad345-131">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="ad345-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad345-132">-RetentionPolicy</span></span>
<span data-ttu-id="ad345-133">Az alap **RetentionPolicy** objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad345-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="ad345-134">A Get-AzRecoveryServicesBackupRetentionPolicyObject parancsmaggal **RetentionPolicy** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="ad345-134">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="ad345-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="ad345-135">-SchedulePolicy</span></span>
<span data-ttu-id="ad345-136">Az alap **SchedulePolicy** objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad345-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="ad345-137">A Get-AzRecoveryServicesBackupSchedulePolicyObject parancsmaggal **SchedulePolicy** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="ad345-137">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="ad345-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ad345-138">-VaultId</span></span>
<span data-ttu-id="ad345-139">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="ad345-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ad345-140">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="ad345-140">-WorkloadType</span></span>
<span data-ttu-id="ad345-141">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad345-141">Specifies the workload type.</span></span>
<span data-ttu-id="ad345-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ad345-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad345-143">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad345-143">AzureVM</span></span> 
- <span data-ttu-id="ad345-144">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="ad345-144">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad345-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad345-145">-Confirm</span></span>
<span data-ttu-id="ad345-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad345-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad345-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad345-147">-WhatIf</span></span>
<span data-ttu-id="ad345-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad345-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad345-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad345-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad345-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad345-150">CommonParameters</span></span>
<span data-ttu-id="ad345-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad345-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad345-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad345-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad345-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad345-153">INPUTS</span></span>

### <span data-ttu-id="ad345-154">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. WorkloadType</span><span class="sxs-lookup"><span data-stu-id="ad345-154">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="ad345-155">System. nulla ' 1 [[Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. BackupManagementType, Microsoft. Azure. PowerShell. parancsmagok. RecoveryServices. backup. models, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ad345-155">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ad345-156">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="ad345-156">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="ad345-157">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="ad345-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="ad345-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ad345-158">System.String</span></span>

## <span data-ttu-id="ad345-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad345-159">OUTPUTS</span></span>

### <span data-ttu-id="ad345-160">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="ad345-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="ad345-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad345-161">NOTES</span></span>

## <span data-ttu-id="ad345-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad345-162">RELATED LINKS</span></span>

[<span data-ttu-id="ad345-163">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ad345-163">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="ad345-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad345-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ad345-165">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ad345-165">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="ad345-166">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="ad345-166">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="ad345-167">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad345-167">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ad345-168">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad345-168">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


