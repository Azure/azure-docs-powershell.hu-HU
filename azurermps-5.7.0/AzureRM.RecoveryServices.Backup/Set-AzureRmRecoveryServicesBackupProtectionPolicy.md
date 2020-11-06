---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 5a60320736e65fae83547bbf9b2825979f73601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493056"
---
# <span data-ttu-id="d385d-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d385d-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="d385d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d385d-102">SYNOPSIS</span></span>
<span data-ttu-id="d385d-103">Módosította a biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="d385d-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d385d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d385d-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d385d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d385d-105">DESCRIPTION</span></span>
<span data-ttu-id="d385d-106">A **set-AzureRmBackupProtectionPolicy** parancsmag módosította a meglévő Azure Backup Protection házirendet.</span><span class="sxs-lookup"><span data-stu-id="d385d-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="d385d-107">Módosíthatja a biztonsági ütemterv és a adatmegőrzési házirend összetevőit.</span><span class="sxs-lookup"><span data-stu-id="d385d-107">You can modify the Backup schedule and retention policy components.</span></span>

<span data-ttu-id="d385d-108">A módosítások akkor befolyásolják a házirendhez társított elemek biztonsági mentését és megőrzését.</span><span class="sxs-lookup"><span data-stu-id="d385d-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>

<span data-ttu-id="d385d-109">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="d385d-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d385d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d385d-110">EXAMPLES</span></span>

### <span data-ttu-id="d385d-111">Példa 1: biztonsági mentési házirend módosítása</span><span class="sxs-lookup"><span data-stu-id="d385d-111">Example 1: Modify a Backup protection policy</span></span>
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

<span data-ttu-id="d385d-112">Az első parancs a bázis SchedulePolicy objektumot kapja, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d385d-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="d385d-113">A második parancs eltávolítja az összes ütemezett futtatási időpontot a $SchPol ütemezési házirendjéből.</span><span class="sxs-lookup"><span data-stu-id="d385d-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="d385d-114">A harmadik parancs az Get-Date parancsmagot használja az aktuális dátum és idő beolvasásához, majd a $DT változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d385d-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="d385d-115">A negyedik parancs hozzáadja a dátumot és az időpontot $DT az ütemezési házirend időbeosztási időpontjához.</span><span class="sxs-lookup"><span data-stu-id="d385d-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>

<span data-ttu-id="d385d-116">Az ötödik parancs beolvassa a bázis adatmegőrzési házirend-objektumát, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d385d-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="d385d-117">A hatodik parancs a retenciós időtartamot 365 napra állítja be.</span><span class="sxs-lookup"><span data-stu-id="d385d-117">The sixth command sets the retention duration to 365 days.</span></span>

<span data-ttu-id="d385d-118">A hetedik parancs beolvassa a NewPolicy nevű biztonsági mentési házirendet, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d385d-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="d385d-119">A végleges parancs módosítja a biztonsági házirendet $Pol a $SchPol ütemezési házirendje és a $RetPol adatmegőrzési házirend segítségével.</span><span class="sxs-lookup"><span data-stu-id="d385d-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="d385d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d385d-120">PARAMETERS</span></span>

### <span data-ttu-id="d385d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d385d-121">-DefaultProfile</span></span>
<span data-ttu-id="d385d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d385d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d385d-123">-Házirend</span><span class="sxs-lookup"><span data-stu-id="d385d-123">-Policy</span></span>
<span data-ttu-id="d385d-124">A parancsmag által módosított biztonsági mentési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d385d-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="d385d-125">**BackupProtectionPolicy** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d385d-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d385d-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d385d-126">-RetentionPolicy</span></span>
<span data-ttu-id="d385d-127">Az alapszintű adatmegőrzési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d385d-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="d385d-128">**RetentionPolicy** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d385d-128">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d385d-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="d385d-129">-SchedulePolicy</span></span>
<span data-ttu-id="d385d-130">A bázis ütemezési házirend-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d385d-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="d385d-131">**SchedulePolicy** objektum beolvasásához használja a Get-AzureRmRecoveryServicesBackupSchedulePolicyObject objektumot.</span><span class="sxs-lookup"><span data-stu-id="d385d-131">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d385d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d385d-132">-Confirm</span></span>
<span data-ttu-id="d385d-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d385d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d385d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d385d-134">-WhatIf</span></span>
<span data-ttu-id="d385d-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d385d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d385d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d385d-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d385d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d385d-137">CommonParameters</span></span>
<span data-ttu-id="d385d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d385d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d385d-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d385d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d385d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d385d-140">INPUTS</span></span>

### <span data-ttu-id="d385d-141">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="d385d-141">PolicyBase</span></span>
<span data-ttu-id="d385d-142">A ' Policy ' paraméter az "PolicyBase" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d385d-142">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="d385d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d385d-143">OUTPUTS</span></span>

### <span data-ttu-id="d385d-144">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="d385d-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="d385d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d385d-145">NOTES</span></span>

## <span data-ttu-id="d385d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d385d-146">RELATED LINKS</span></span>

[<span data-ttu-id="d385d-147">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d385d-147">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d385d-148">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d385d-148">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="d385d-149">Új – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d385d-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d385d-150">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d385d-150">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


