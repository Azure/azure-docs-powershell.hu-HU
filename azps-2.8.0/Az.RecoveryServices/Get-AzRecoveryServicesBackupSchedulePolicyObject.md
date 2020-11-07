---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 71650d36c319536db5ad96aa142e2712e229d712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838573"
---
# <span data-ttu-id="37c64-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="37c64-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="37c64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37c64-102">SYNOPSIS</span></span>
<span data-ttu-id="37c64-103">Beolvassa a bázis ütemezése házirend-objektumot.</span><span class="sxs-lookup"><span data-stu-id="37c64-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="37c64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37c64-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37c64-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="37c64-105">DESCRIPTION</span></span>
<span data-ttu-id="37c64-106">A **Get-AzRecoveryServicesBackupSchedulePolicyObject** parancsmag alap **AzureRMRecoveryServicesSchedulePolicyObject** kap.</span><span class="sxs-lookup"><span data-stu-id="37c64-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="37c64-107">Ez az objektum nem marad fenn a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="37c64-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="37c64-108">Az ideiglenes objektum, amelyet az New-AzRecoveryServicesBackupProtectionPolicy parancsmaggal kezelhet és használhat új biztonsági mentési házirend létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="37c64-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="37c64-109">Példák</span><span class="sxs-lookup"><span data-stu-id="37c64-109">EXAMPLES</span></span>

### <span data-ttu-id="37c64-110">Példa 1: az ütemezés gyakoriságának beállítása hetente</span><span class="sxs-lookup"><span data-stu-id="37c64-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="37c64-111">Az első parancs megkapja az adatmegőrzési házirend objektumot, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="37c64-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="37c64-112">A második parancs bekerül az ütemezési házirend-objektumba, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="37c64-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="37c64-113">A harmadik parancs az ütemezési házirend gyakoriságát hetente módosítja.</span><span class="sxs-lookup"><span data-stu-id="37c64-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="37c64-114">Az utolsó parancs biztonsági mentési házirendet hoz létre a frissített ütemezéssel.</span><span class="sxs-lookup"><span data-stu-id="37c64-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="37c64-115">2. példa: a biztonsági mentés időpontjának beállítása</span><span class="sxs-lookup"><span data-stu-id="37c64-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="37c64-116">Az első parancs megkapja az ütemezési házirend-objektumot, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="37c64-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="37c64-117">A második parancs eltávolítja az összes ütemezett futási időpontot a $SchPolból.</span><span class="sxs-lookup"><span data-stu-id="37c64-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="37c64-118">A harmadik parancs az aktuális dátumot és időpontot kapja, majd a $DT változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="37c64-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="37c64-119">A negyedik parancs a jelenlegi időpontra cseréli az ütemezett futási időpontokat.</span><span class="sxs-lookup"><span data-stu-id="37c64-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="37c64-120">Csak egyszer lehet biztonsági másolatot készíteni a AzureVM, így a biztonsági mentés időpontjának alaphelyzetbe állításához az eredeti ütemtervet kell cserélnie.</span><span class="sxs-lookup"><span data-stu-id="37c64-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="37c64-121">Az utolsó parancs az új időbeosztással hozza létre a biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="37c64-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="37c64-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37c64-122">PARAMETERS</span></span>

### <span data-ttu-id="37c64-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="37c64-123">-BackupManagementType</span></span>
<span data-ttu-id="37c64-124">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="37c64-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="37c64-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="37c64-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37c64-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="37c64-126">AzureVM</span></span> 
- <span data-ttu-id="37c64-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="37c64-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="37c64-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="37c64-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c64-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c64-129">-DefaultProfile</span></span>
<span data-ttu-id="37c64-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37c64-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37c64-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="37c64-131">-WorkloadType</span></span>
<span data-ttu-id="37c64-132">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="37c64-132">Specifies the workload type.</span></span>
<span data-ttu-id="37c64-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="37c64-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37c64-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="37c64-134">AzureVM</span></span> 
- <span data-ttu-id="37c64-135">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="37c64-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="37c64-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="37c64-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c64-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c64-137">CommonParameters</span></span>
<span data-ttu-id="37c64-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37c64-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c64-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c64-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c64-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37c64-140">INPUTS</span></span>

### <span data-ttu-id="37c64-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="37c64-141">None</span></span>

## <span data-ttu-id="37c64-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37c64-142">OUTPUTS</span></span>

### <span data-ttu-id="37c64-143">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="37c64-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="37c64-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37c64-144">NOTES</span></span>

## <span data-ttu-id="37c64-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37c64-145">RELATED LINKS</span></span>

[<span data-ttu-id="37c64-146">Új – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="37c64-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="37c64-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="37c64-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


