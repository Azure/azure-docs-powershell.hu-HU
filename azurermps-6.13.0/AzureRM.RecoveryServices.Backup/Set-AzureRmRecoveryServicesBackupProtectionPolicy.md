---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: fb0373e97d719535c87c01c0a4b53b029cc2a878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500147"
---
# <span data-ttu-id="428d3-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="428d3-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="428d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="428d3-102">SYNOPSIS</span></span>
<span data-ttu-id="428d3-103">Módosította a biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="428d3-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="428d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="428d3-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="428d3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="428d3-105">DESCRIPTION</span></span>
<span data-ttu-id="428d3-106">A **set-AzureRmBackupProtectionPolicy** parancsmag módosította a meglévő Azure Backup Protection házirendet.</span><span class="sxs-lookup"><span data-stu-id="428d3-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="428d3-107">Módosíthatja a biztonsági ütemterv és a adatmegőrzési házirend összetevőit.</span><span class="sxs-lookup"><span data-stu-id="428d3-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="428d3-108">A módosítások akkor befolyásolják a házirendhez társított elemek biztonsági mentését és megőrzését.</span><span class="sxs-lookup"><span data-stu-id="428d3-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="428d3-109">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="428d3-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="428d3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="428d3-110">EXAMPLES</span></span>

### <span data-ttu-id="428d3-111">Példa 1: biztonsági mentési házirend módosítása</span><span class="sxs-lookup"><span data-stu-id="428d3-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="428d3-112">Az első parancs a bázis SchedulePolicy objektumot kapja, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="428d3-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="428d3-113">A második parancs eltávolítja az összes ütemezett futtatási időpontot a $SchPol ütemezési házirendjéből.</span><span class="sxs-lookup"><span data-stu-id="428d3-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="428d3-114">A harmadik parancs az Get-Date parancsmagot használja az aktuális dátum és idő beolvasásához, majd a $DT változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="428d3-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="428d3-115">A negyedik parancs hozzáadja a dátumot és az időpontot $DT az ütemezési házirend időbeosztási időpontjához.</span><span class="sxs-lookup"><span data-stu-id="428d3-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="428d3-116">Az ötödik parancs beolvassa a bázis adatmegőrzési házirend-objektumát, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="428d3-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="428d3-117">A hatodik parancs a retenciós időtartamot 365 napra állítja be.</span><span class="sxs-lookup"><span data-stu-id="428d3-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="428d3-118">A hetedik parancs beolvassa a NewPolicy nevű biztonsági mentési házirendet, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="428d3-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="428d3-119">A végleges parancs módosítja a biztonsági házirendet $Pol a $SchPol ütemezési házirendje és a $RetPol adatmegőrzési házirend segítségével.</span><span class="sxs-lookup"><span data-stu-id="428d3-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="428d3-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="428d3-120">PARAMETERS</span></span>

### <span data-ttu-id="428d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428d3-121">-DefaultProfile</span></span>
<span data-ttu-id="428d3-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="428d3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="428d3-123">-Házirend</span><span class="sxs-lookup"><span data-stu-id="428d3-123">-Policy</span></span>
<span data-ttu-id="428d3-124">A parancsmag által módosított biztonsági mentési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="428d3-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="428d3-125">**BackupProtectionPolicy** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="428d3-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="428d3-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="428d3-126">-RetentionPolicy</span></span>
<span data-ttu-id="428d3-127">Az alapszintű adatmegőrzési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="428d3-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="428d3-128">**RetentionPolicy** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="428d3-128">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428d3-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="428d3-129">-SchedulePolicy</span></span>
<span data-ttu-id="428d3-130">A bázis ütemezési házirend-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="428d3-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="428d3-131">**SchedulePolicy** objektum beolvasásához használja a Get-AzureRmRecoveryServicesBackupSchedulePolicyObject objektumot.</span><span class="sxs-lookup"><span data-stu-id="428d3-131">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428d3-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="428d3-132">-VaultId</span></span>
<span data-ttu-id="428d3-133">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="428d3-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="428d3-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="428d3-134">-Confirm</span></span>
<span data-ttu-id="428d3-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="428d3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="428d3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="428d3-136">-WhatIf</span></span>
<span data-ttu-id="428d3-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="428d3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="428d3-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="428d3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="428d3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428d3-139">CommonParameters</span></span>
<span data-ttu-id="428d3-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="428d3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428d3-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="428d3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428d3-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="428d3-142">INPUTS</span></span>

### <span data-ttu-id="428d3-143">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="428d3-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>
<span data-ttu-id="428d3-144">Paraméterek: házirend (ByValue)</span><span class="sxs-lookup"><span data-stu-id="428d3-144">Parameters: Policy (ByValue)</span></span>

### <span data-ttu-id="428d3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="428d3-145">System.String</span></span>
<span data-ttu-id="428d3-146">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="428d3-146">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="428d3-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="428d3-147">OUTPUTS</span></span>

### <span data-ttu-id="428d3-148">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="428d3-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="428d3-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="428d3-149">NOTES</span></span>

## <span data-ttu-id="428d3-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="428d3-150">RELATED LINKS</span></span>

[<span data-ttu-id="428d3-151">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="428d3-151">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="428d3-152">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="428d3-152">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="428d3-153">Új – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="428d3-153">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="428d3-154">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="428d3-154">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


