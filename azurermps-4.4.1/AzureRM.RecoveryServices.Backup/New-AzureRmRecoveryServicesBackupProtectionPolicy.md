---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: a871aa624aaf8b7f24d06bd0ff04a45e29b95468
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494746"
---
# <span data-ttu-id="70af8-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="70af8-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="70af8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70af8-102">SYNOPSIS</span></span>
<span data-ttu-id="70af8-103">Biztonságimásolat-védelmi házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="70af8-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70af8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70af8-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70af8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="70af8-105">DESCRIPTION</span></span>
<span data-ttu-id="70af8-106">A **New-AzureRmRecoveryServicesBackupProtectionPolicy** parancsmag biztonsági mentési házirendet hoz létre egy boltozatban.</span><span class="sxs-lookup"><span data-stu-id="70af8-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="70af8-107">A védelmi házirend legalább egy adatmegőrzési házirendhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="70af8-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="70af8-108">Az adatmegőrzési házirend azt határozza meg, hogy mennyi ideig tart a helyreállítási pont az Azure Backup szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="70af8-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="70af8-109">Az alapértelmezett adatmegőrzési házirend beszerzéséhez használhatja az Get-AzureRmRecoveryServicesBackupRetentionPolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70af8-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="70af8-110">Az alapértelmezett ütemezési házirend beszerzéséhez használhatja a Get-AzureRmRecoveryServicesBackupSchedulePolicyObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70af8-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="70af8-111">A **SchedulePolicy** és az **RetentionPolicy** objektum a **New-AzureRmRecoveryServicesBackupProtectionPolicy** parancsmag bemenetéhez használatos.</span><span class="sxs-lookup"><span data-stu-id="70af8-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="70af8-112">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="70af8-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="70af8-113">Példák</span><span class="sxs-lookup"><span data-stu-id="70af8-113">EXAMPLES</span></span>

### <span data-ttu-id="70af8-114">Példa 1: biztonsági mentést biztosító házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="70af8-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="70af8-115">Az első parancs megkapja a bázis **SchedulePolicyObject** , majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="70af8-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="70af8-116">A második parancs eltávolítja az összes ütemezett futtatási időpontot a $SchPol ütemezési házirendjéből.</span><span class="sxs-lookup"><span data-stu-id="70af8-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="70af8-117">A harmadik parancs az Get-Date parancsmagot használja az aktuális dátum és idő beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="70af8-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="70af8-118">A negyedik parancs hozzáadja az aktuális dátumot és időpontot $Dt az ütemezési házirendhez ütemezett futási időpontként.</span><span class="sxs-lookup"><span data-stu-id="70af8-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="70af8-119">Az ötödik parancs beolvassa a bázis **RetentionPolicy** objektumot, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="70af8-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="70af8-120">A hatodik parancs a retenciós idő házirendjét 365 napra állítja be.</span><span class="sxs-lookup"><span data-stu-id="70af8-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="70af8-121">A végleges parancs az előző parancsok által létrehozott ütemezési és adatmegőrzési szabályok alapján hoz létre **BackupProtectionPolicy** objektumot.</span><span class="sxs-lookup"><span data-stu-id="70af8-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="70af8-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70af8-122">PARAMETERS</span></span>

### <span data-ttu-id="70af8-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="70af8-123">-BackupManagementType</span></span>
<span data-ttu-id="70af8-124">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70af8-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="70af8-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="70af8-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70af8-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="70af8-126">AzureVM</span></span> 
- <span data-ttu-id="70af8-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="70af8-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70af8-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70af8-128">-Name</span></span>
<span data-ttu-id="70af8-129">A házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70af8-129">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="70af8-130">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="70af8-130">-RetentionPolicy</span></span>
<span data-ttu-id="70af8-131">Az alap **RetentionPolicy** objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70af8-131">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="70af8-132">A Get-AzureRmRecoveryServicesBackupRetentionPolicyObject parancsmaggal **RetentionPolicy** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="70af8-132">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="70af8-133">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="70af8-133">-SchedulePolicy</span></span>
<span data-ttu-id="70af8-134">Az alap **SchedulePolicy** objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70af8-134">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="70af8-135">A Get-AzureRmRecoveryServicesBackupSchedulePolicyObject parancsmaggal **SchedulePolicy** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="70af8-135">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="70af8-136">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="70af8-136">-WorkloadType</span></span>
<span data-ttu-id="70af8-137">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70af8-137">Specifies the workload type.</span></span>
<span data-ttu-id="70af8-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="70af8-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70af8-139">AzureVM</span><span class="sxs-lookup"><span data-stu-id="70af8-139">AzureVM</span></span> 
- <span data-ttu-id="70af8-140">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="70af8-140">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70af8-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70af8-141">-DefaultProfile</span></span>
<span data-ttu-id="70af8-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70af8-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70af8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70af8-143">CommonParameters</span></span>
<span data-ttu-id="70af8-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70af8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70af8-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70af8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70af8-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70af8-146">INPUTS</span></span>

## <span data-ttu-id="70af8-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70af8-147">OUTPUTS</span></span>

### <span data-ttu-id="70af8-148">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="70af8-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="70af8-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70af8-149">NOTES</span></span>

## <span data-ttu-id="70af8-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70af8-150">RELATED LINKS</span></span>

[<span data-ttu-id="70af8-151">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="70af8-151">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="70af8-152">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="70af8-152">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="70af8-153">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="70af8-153">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="70af8-154">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="70af8-154">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="70af8-155">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="70af8-155">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="70af8-156">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="70af8-156">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


