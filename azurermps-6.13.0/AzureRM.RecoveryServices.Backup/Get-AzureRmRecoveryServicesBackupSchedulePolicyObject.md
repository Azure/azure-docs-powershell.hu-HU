---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: cc65ea2b2f050eb356d5be22c935aebb131f5cfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495760"
---
# <span data-ttu-id="84315-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="84315-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="84315-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84315-102">SYNOPSIS</span></span>
<span data-ttu-id="84315-103">Beolvassa a bázis ütemezése házirend-objektumot.</span><span class="sxs-lookup"><span data-stu-id="84315-103">Gets a base schedule policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84315-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84315-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84315-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84315-105">DESCRIPTION</span></span>
<span data-ttu-id="84315-106">A **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** parancsmag alap **AzureRMRecoveryServicesSchedulePolicyObject** kap.</span><span class="sxs-lookup"><span data-stu-id="84315-106">The **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="84315-107">Ez az objektum nem marad fenn a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="84315-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="84315-108">Az ideiglenes objektum, amelyet az New-AzureRmRecoveryServicesBackupProtectionPolicy parancsmaggal kezelhet és használhat új biztonsági mentési házirend létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="84315-108">It is temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="84315-109">Példák</span><span class="sxs-lookup"><span data-stu-id="84315-109">EXAMPLES</span></span>

### <span data-ttu-id="84315-110">Példa 1: az ütemezés gyakoriságának beállítása hetente</span><span class="sxs-lookup"><span data-stu-id="84315-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="84315-111">Az első parancs megkapja az adatmegőrzési házirend objektumot, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="84315-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="84315-112">A második parancs bekerül az ütemezési házirend-objektumba, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="84315-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="84315-113">A harmadik parancs az ütemezési házirend gyakoriságát hetente módosítja.</span><span class="sxs-lookup"><span data-stu-id="84315-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="84315-114">Az utolsó parancs biztonsági mentési házirendet hoz létre a frissített ütemezéssel.</span><span class="sxs-lookup"><span data-stu-id="84315-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="84315-115">2. példa: a biztonsági mentés időpontjának beállítása</span><span class="sxs-lookup"><span data-stu-id="84315-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="84315-116">Az első parancs megkapja az ütemezési házirend-objektumot, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="84315-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="84315-117">A második parancs eltávolítja az összes ütemezett futási időpontot a $SchPolból.</span><span class="sxs-lookup"><span data-stu-id="84315-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="84315-118">A harmadik parancs az aktuális dátumot és időpontot kapja, majd a $DT változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="84315-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="84315-119">A negyedik parancs a jelenlegi időpontra cseréli az ütemezett futási időpontokat.</span><span class="sxs-lookup"><span data-stu-id="84315-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="84315-120">Csak egyszer lehet biztonsági másolatot készíteni a AzureVM, így a biztonsági mentés időpontjának alaphelyzetbe állításához az eredeti ütemtervet kell cserélnie.</span><span class="sxs-lookup"><span data-stu-id="84315-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="84315-121">Az utolsó parancs az új időbeosztással hozza létre a biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="84315-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="84315-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84315-122">PARAMETERS</span></span>

### <span data-ttu-id="84315-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="84315-123">-BackupManagementType</span></span>
<span data-ttu-id="84315-124">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84315-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="84315-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="84315-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84315-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="84315-126">AzureVM</span></span> 
- <span data-ttu-id="84315-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="84315-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="84315-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="84315-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84315-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84315-129">-DefaultProfile</span></span>
<span data-ttu-id="84315-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84315-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84315-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="84315-131">-WorkloadType</span></span>
<span data-ttu-id="84315-132">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84315-132">Specifies the workload type.</span></span>
<span data-ttu-id="84315-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="84315-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84315-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="84315-134">AzureVM</span></span> 
- <span data-ttu-id="84315-135">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="84315-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="84315-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="84315-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84315-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84315-137">CommonParameters</span></span>
<span data-ttu-id="84315-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84315-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84315-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84315-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84315-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84315-140">INPUTS</span></span>

### <span data-ttu-id="84315-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="84315-141">None</span></span>

## <span data-ttu-id="84315-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84315-142">OUTPUTS</span></span>

### <span data-ttu-id="84315-143">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="84315-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="84315-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84315-144">NOTES</span></span>

## <span data-ttu-id="84315-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84315-145">RELATED LINKS</span></span>

[<span data-ttu-id="84315-146">Új – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="84315-146">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="84315-147">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="84315-147">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


