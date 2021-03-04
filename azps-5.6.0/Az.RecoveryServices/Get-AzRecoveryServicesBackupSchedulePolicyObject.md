---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 5bf91aafffb1c6fd650b5fd88f343897afc6c5d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932330"
---
# <span data-ttu-id="5fab1-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="5fab1-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="5fab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fab1-102">SYNOPSIS</span></span>
<span data-ttu-id="5fab1-103">Alapütemterv-házirendobjektumot kap.</span><span class="sxs-lookup"><span data-stu-id="5fab1-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="5fab1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5fab1-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fab1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5fab1-105">DESCRIPTION</span></span>
<span data-ttu-id="5fab1-106">A **Get-AzRecoveryServicesBackupSchedulePolicyObject** parancsmag egy alap **AzureRMRecoveryServicesSchedulePolicyObject** parancsmagot kap.</span><span class="sxs-lookup"><span data-stu-id="5fab1-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="5fab1-107">Ez az objektum nem marad meg a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="5fab1-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="5fab1-108">Ez egy ideiglenes objektum, amely a New-AzRecoveryServicesBackupProtectionPolicy parancsmaggal egy új biztonságimásolat-védelmi házirend létrehozásához használható.</span><span class="sxs-lookup"><span data-stu-id="5fab1-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="5fab1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5fab1-109">EXAMPLES</span></span>

### <span data-ttu-id="5fab1-110">1. példa: Az ütemezés gyakoriságának beállítása hetente</span><span class="sxs-lookup"><span data-stu-id="5fab1-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="5fab1-111">Az első parancs megkapja az adatmegőrzési házirend-objektumot, majd a $RetPol tárolja.</span><span class="sxs-lookup"><span data-stu-id="5fab1-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="5fab1-112">A második parancs beveszi az ütemezési házirendobjektumot, majd a $SchPol tárolja.</span><span class="sxs-lookup"><span data-stu-id="5fab1-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="5fab1-113">A harmadik parancs heti rendszerességgel módosítja az ütemezési házirend gyakoriságát.</span><span class="sxs-lookup"><span data-stu-id="5fab1-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="5fab1-114">Az utolsó parancs létrehoz egy biztonságimásolat-védelmi házirendet a frissített ütemezéssel.</span><span class="sxs-lookup"><span data-stu-id="5fab1-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="5fab1-115">2. példa: A biztonsági mentés időének beállítása</span><span class="sxs-lookup"><span data-stu-id="5fab1-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="5fab1-116">Az első parancs megkapja az ütemezési házirendobjektumot, majd a $SchPol tárolja.</span><span class="sxs-lookup"><span data-stu-id="5fab1-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="5fab1-117">A második parancs minden ütemezett futási időt eltávolít a $SchPol.</span><span class="sxs-lookup"><span data-stu-id="5fab1-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="5fab1-118">A harmadik parancs bekérte az aktuális dátumot és időpontot, majd tárolja azt a $DT változóban.</span><span class="sxs-lookup"><span data-stu-id="5fab1-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="5fab1-119">A negyedik parancs az ütemezett futtatás idejét az aktuális időpontra cseréli.</span><span class="sxs-lookup"><span data-stu-id="5fab1-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="5fab1-120">Naponta csak egyszer lehet biztonsági másolatot készíteni az AzureVM-ről, így a biztonsági mentés alaphelyzetbe állításának idejét az eredeti ütemezést kell lecserélnie.</span><span class="sxs-lookup"><span data-stu-id="5fab1-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="5fab1-121">Az utolsó parancs egy biztonságimásolat-védelmi házirendet hoz létre az új ütemezés használatával.</span><span class="sxs-lookup"><span data-stu-id="5fab1-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="5fab1-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fab1-122">PARAMETERS</span></span>

### <span data-ttu-id="5fab1-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="5fab1-123">-BackupManagementType</span></span>
<span data-ttu-id="5fab1-124">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="5fab1-124">The class of resources being protected.</span></span> <span data-ttu-id="5fab1-125">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5fab1-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5fab1-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="5fab1-126">AzureVM</span></span> 
- <span data-ttu-id="5fab1-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="5fab1-127">AzureStorage</span></span>
- <span data-ttu-id="5fab1-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="5fab1-128">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fab1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fab1-129">-DefaultProfile</span></span>
<span data-ttu-id="5fab1-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fab1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fab1-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="5fab1-131">-WorkloadType</span></span>
<span data-ttu-id="5fab1-132">Az erőforrás terheléstípusa.</span><span class="sxs-lookup"><span data-stu-id="5fab1-132">Workload type of the resource.</span></span> <span data-ttu-id="5fab1-133">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5fab1-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5fab1-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="5fab1-134">AzureVM</span></span> 
- <span data-ttu-id="5fab1-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="5fab1-135">AzureFiles</span></span>
- <span data-ttu-id="5fab1-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="5fab1-136">MSSQL</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fab1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fab1-137">CommonParameters</span></span>
<span data-ttu-id="5fab1-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fab1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fab1-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fab1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fab1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fab1-140">INPUTS</span></span>

### <span data-ttu-id="5fab1-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="5fab1-141">None</span></span>

## <span data-ttu-id="5fab1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fab1-142">OUTPUTS</span></span>

### <span data-ttu-id="5fab1-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="5fab1-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="5fab1-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5fab1-144">NOTES</span></span>

## <span data-ttu-id="5fab1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fab1-145">RELATED LINKS</span></span>

[<span data-ttu-id="5fab1-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5fab1-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="5fab1-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5fab1-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


