---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f9cd7064c1949639526f2e7b84f01fb6355b584f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185702"
---
# <span data-ttu-id="1c445-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c445-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="1c445-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c445-102">SYNOPSIS</span></span>
<span data-ttu-id="1c445-103">Módosította a biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="1c445-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="1c445-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c445-104">SYNTAX</span></span>

### <span data-ttu-id="1c445-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="1c445-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c445-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="1c445-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c445-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c445-107">DESCRIPTION</span></span>
<span data-ttu-id="1c445-108">A **set-AzRecoveryServicesBackupProtectionPolicy** parancsmag módosította a meglévő Azure Backup Protection házirendet.</span><span class="sxs-lookup"><span data-stu-id="1c445-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="1c445-109">Módosíthatja a biztonsági ütemterv és a adatmegőrzési házirend összetevőit.</span><span class="sxs-lookup"><span data-stu-id="1c445-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="1c445-110">A módosítások akkor befolyásolják a házirendhez társított elemek biztonsági mentését és megőrzését.</span><span class="sxs-lookup"><span data-stu-id="1c445-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="1c445-111">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="1c445-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1c445-112">Példák</span><span class="sxs-lookup"><span data-stu-id="1c445-112">EXAMPLES</span></span>

### <span data-ttu-id="1c445-113">Példa 1: biztonsági mentési házirend módosítása</span><span class="sxs-lookup"><span data-stu-id="1c445-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> $Pol.AzureBackupRGName = "RG_prefix"
PS C:\> $Pol.AzureBackupRGNameSuffix = "RG_suffix"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="1c445-114">Az első parancs a bázis SchedulePolicy objektumot kapja, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1c445-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="1c445-115">A második parancs eltávolítja az összes ütemezett futtatási időpontot a $SchPol ütemezési házirendjéből.</span><span class="sxs-lookup"><span data-stu-id="1c445-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="1c445-116">A harmadik parancs az Get-Date parancsmagot használja az aktuális dátum és idő beolvasásához, majd a $DT változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1c445-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="1c445-117">A negyedik parancs hozzáadja a dátumot és az időpontot $DT az ütemezési házirend időbeosztási időpontjához.</span><span class="sxs-lookup"><span data-stu-id="1c445-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="1c445-118">Az ötödik parancs beolvassa a bázis adatmegőrzési házirend-objektumát, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1c445-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="1c445-119">A hatodik parancs a retenciós időtartamot 365 napra állítja be.</span><span class="sxs-lookup"><span data-stu-id="1c445-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="1c445-120">A hetedik parancs beolvassa a NewPolicy nevű biztonsági mentési házirendet, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1c445-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="1c445-121">A nyolcadik és a kilencedik beállítás a visszaállítási pontokat tároló házirenddel társított erőforráscsoport-paramétereket adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c445-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="1c445-122">A végleges parancs módosítja a biztonsági házirendet $Pol a $SchPol ütemezési házirendje és a $RetPol adatmegőrzési házirend segítségével.</span><span class="sxs-lookup"><span data-stu-id="1c445-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="1c445-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c445-123">PARAMETERS</span></span>

### <span data-ttu-id="1c445-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c445-124">-DefaultProfile</span></span>
<span data-ttu-id="1c445-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c445-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c445-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="1c445-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="1c445-127">Kapcsoló paraméter, amely azt jelzi, hogy a sikertelen elemek esetén újra kell-e próbálni a házirend-frissítést.</span><span class="sxs-lookup"><span data-stu-id="1c445-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="1c445-128">-Házirend</span><span class="sxs-lookup"><span data-stu-id="1c445-128">-Policy</span></span>
<span data-ttu-id="1c445-129">A parancsmag által módosított biztonsági mentési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c445-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="1c445-130">**BackupProtectionPolicy** objektum beolvasásához használja az Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1c445-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="1c445-131">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c445-131">-RetentionPolicy</span></span>
<span data-ttu-id="1c445-132">Az alapszintű adatmegőrzési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c445-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="1c445-133">**RetentionPolicy** objektum beolvasásához használja az Get-AzRecoveryServicesBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1c445-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="1c445-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="1c445-134">-SchedulePolicy</span></span>
<span data-ttu-id="1c445-135">A bázis ütemezési házirend-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c445-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="1c445-136">**SchedulePolicy** objektum beolvasásához használja a Get-AzRecoveryServicesBackupSchedulePolicyObject objektumot.</span><span class="sxs-lookup"><span data-stu-id="1c445-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="1c445-137">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1c445-137">-VaultId</span></span>
<span data-ttu-id="1c445-138">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="1c445-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1c445-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1c445-139">-Confirm</span></span>
<span data-ttu-id="1c445-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1c445-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c445-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c445-141">-WhatIf</span></span>
<span data-ttu-id="1c445-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1c445-142">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="1c445-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c445-143">CommonParameters</span></span>
<span data-ttu-id="1c445-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c445-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c445-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1c445-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c445-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c445-146">INPUTS</span></span>

### <span data-ttu-id="1c445-147">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1c445-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="1c445-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1c445-148">System.String</span></span>

## <span data-ttu-id="1c445-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c445-149">OUTPUTS</span></span>

### <span data-ttu-id="1c445-150">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="1c445-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="1c445-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c445-151">NOTES</span></span>

## <span data-ttu-id="1c445-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c445-152">RELATED LINKS</span></span>

[<span data-ttu-id="1c445-153">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c445-153">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1c445-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1c445-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="1c445-155">Új – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c445-155">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1c445-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c445-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


