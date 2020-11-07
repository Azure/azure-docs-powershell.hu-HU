---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1f7dcd013bb91b8ba209cf3f7b031a90f7bb49cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839031"
---
# <span data-ttu-id="a91dc-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a91dc-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="a91dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a91dc-102">SYNOPSIS</span></span>
<span data-ttu-id="a91dc-103">Módosította a biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="a91dc-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="a91dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a91dc-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a91dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a91dc-105">DESCRIPTION</span></span>
<span data-ttu-id="a91dc-106">A **set-AzBackupProtectionPolicy** parancsmag módosította a meglévő Azure Backup Protection házirendet.</span><span class="sxs-lookup"><span data-stu-id="a91dc-106">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="a91dc-107">Módosíthatja a biztonsági ütemterv és a adatmegőrzési házirend összetevőit.</span><span class="sxs-lookup"><span data-stu-id="a91dc-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="a91dc-108">A módosítások akkor befolyásolják a házirendhez társított elemek biztonsági mentését és megőrzését.</span><span class="sxs-lookup"><span data-stu-id="a91dc-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="a91dc-109">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="a91dc-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a91dc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a91dc-110">EXAMPLES</span></span>

### <span data-ttu-id="a91dc-111">Példa 1: biztonsági mentési házirend módosítása</span><span class="sxs-lookup"><span data-stu-id="a91dc-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="a91dc-112">Az első parancs a bázis SchedulePolicy objektumot kapja, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a91dc-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="a91dc-113">A második parancs eltávolítja az összes ütemezett futtatási időpontot a $SchPol ütemezési házirendjéből.</span><span class="sxs-lookup"><span data-stu-id="a91dc-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="a91dc-114">A harmadik parancs az Get-Date parancsmagot használja az aktuális dátum és idő beolvasásához, majd a $DT változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a91dc-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="a91dc-115">A negyedik parancs hozzáadja a dátumot és az időpontot $DT az ütemezési házirend időbeosztási időpontjához.</span><span class="sxs-lookup"><span data-stu-id="a91dc-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="a91dc-116">Az ötödik parancs beolvassa a bázis adatmegőrzési házirend-objektumát, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a91dc-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="a91dc-117">A hatodik parancs a retenciós időtartamot 365 napra állítja be.</span><span class="sxs-lookup"><span data-stu-id="a91dc-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="a91dc-118">A hetedik parancs beolvassa a NewPolicy nevű biztonsági mentési házirendet, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a91dc-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="a91dc-119">A végleges parancs módosítja a biztonsági házirendet $Pol a $SchPol ütemezési házirendje és a $RetPol adatmegőrzési házirend segítségével.</span><span class="sxs-lookup"><span data-stu-id="a91dc-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="a91dc-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a91dc-120">PARAMETERS</span></span>

### <span data-ttu-id="a91dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a91dc-121">-DefaultProfile</span></span>
<span data-ttu-id="a91dc-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a91dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a91dc-123">-Házirend</span><span class="sxs-lookup"><span data-stu-id="a91dc-123">-Policy</span></span>
<span data-ttu-id="a91dc-124">A parancsmag által módosított biztonsági mentési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a91dc-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="a91dc-125">**BackupProtectionPolicy** objektum beolvasásához használja az Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a91dc-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="a91dc-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a91dc-126">-RetentionPolicy</span></span>
<span data-ttu-id="a91dc-127">Az alapszintű adatmegőrzési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a91dc-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="a91dc-128">**RetentionPolicy** objektum beolvasásához használja az Get-AzRecoveryServicesBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a91dc-128">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="a91dc-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="a91dc-129">-SchedulePolicy</span></span>
<span data-ttu-id="a91dc-130">A bázis ütemezési házirend-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a91dc-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="a91dc-131">**SchedulePolicy** objektum beolvasásához használja a Get-AzRecoveryServicesBackupSchedulePolicyObject objektumot.</span><span class="sxs-lookup"><span data-stu-id="a91dc-131">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="a91dc-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a91dc-132">-VaultId</span></span>
<span data-ttu-id="a91dc-133">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="a91dc-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a91dc-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a91dc-134">-Confirm</span></span>
<span data-ttu-id="a91dc-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a91dc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a91dc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a91dc-136">-WhatIf</span></span>
<span data-ttu-id="a91dc-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a91dc-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a91dc-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a91dc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a91dc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a91dc-139">CommonParameters</span></span>
<span data-ttu-id="a91dc-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a91dc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a91dc-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a91dc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a91dc-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a91dc-142">INPUTS</span></span>

### <span data-ttu-id="a91dc-143">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="a91dc-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="a91dc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a91dc-144">System.String</span></span>

## <span data-ttu-id="a91dc-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a91dc-145">OUTPUTS</span></span>

### <span data-ttu-id="a91dc-146">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a91dc-146">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a91dc-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a91dc-147">NOTES</span></span>

## <span data-ttu-id="a91dc-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a91dc-148">RELATED LINKS</span></span>

[<span data-ttu-id="a91dc-149">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a91dc-149">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="a91dc-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="a91dc-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="a91dc-151">Új – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a91dc-151">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="a91dc-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a91dc-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


