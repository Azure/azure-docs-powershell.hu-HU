---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: fcf5bec22dffc18d6c4f9950d8dfb3e5b37332a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680238"
---
# <span data-ttu-id="7af8a-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="7af8a-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="7af8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7af8a-102">SYNOPSIS</span></span>
<span data-ttu-id="7af8a-103">Beolvassa a bázis ütemezése házirend-objektumot.</span><span class="sxs-lookup"><span data-stu-id="7af8a-103">Gets a base schedule policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7af8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7af8a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7af8a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7af8a-105">DESCRIPTION</span></span>
<span data-ttu-id="7af8a-106">A **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** parancsmag alap **AzureRMRecoveryServicesSchedulePolicyObject** kap.</span><span class="sxs-lookup"><span data-stu-id="7af8a-106">The **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="7af8a-107">Ez az objektum nem marad fenn a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="7af8a-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="7af8a-108">Az ideiglenes objektum, amelyet az New-AzureRmRecoveryServicesBackupProtectionPolicy parancsmaggal kezelhet és használhat új biztonsági mentési házirend létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7af8a-108">It is temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="7af8a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7af8a-109">EXAMPLES</span></span>

### <span data-ttu-id="7af8a-110">Példa 1: az ütemezés gyakoriságának beállítása hetente</span><span class="sxs-lookup"><span data-stu-id="7af8a-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="7af8a-111">Az első parancs megkapja az adatmegőrzési házirend objektumot, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7af8a-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="7af8a-112">A második parancs bekerül az ütemezési házirend-objektumba, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7af8a-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="7af8a-113">A harmadik parancs az ütemezési házirend gyakoriságát hetente módosítja.</span><span class="sxs-lookup"><span data-stu-id="7af8a-113">The third command changes the frequency for the schedule policy to weekly.</span></span>

<span data-ttu-id="7af8a-114">Az utolsó parancs biztonsági mentési házirendet hoz létre a frissített ütemezéssel.</span><span class="sxs-lookup"><span data-stu-id="7af8a-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="7af8a-115">2. példa: a biztonsági mentés időpontjának beállítása</span><span class="sxs-lookup"><span data-stu-id="7af8a-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="7af8a-116">Az első parancs megkapja az ütemezési házirend-objektumot, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7af8a-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="7af8a-117">A második parancs eltávolítja az összes ütemezett futási időpontot a $SchPolból.</span><span class="sxs-lookup"><span data-stu-id="7af8a-117">The second command removes all scheduled run times from $SchPol.</span></span>

<span data-ttu-id="7af8a-118">A harmadik parancs az aktuális dátumot és időpontot kapja, majd a $DT változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7af8a-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="7af8a-119">A negyedik parancs a jelenlegi időpontra cseréli az ütemezett futási időpontokat.</span><span class="sxs-lookup"><span data-stu-id="7af8a-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="7af8a-120">Csak egyszer lehet biztonsági másolatot készíteni a AzureVM, így a biztonsági mentés időpontjának alaphelyzetbe állításához az eredeti ütemtervet kell cserélnie.</span><span class="sxs-lookup"><span data-stu-id="7af8a-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>

<span data-ttu-id="7af8a-121">Az utolsó parancs az új időbeosztással hozza létre a biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="7af8a-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="7af8a-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7af8a-122">PARAMETERS</span></span>

### <span data-ttu-id="7af8a-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7af8a-123">-BackupManagementType</span></span>
<span data-ttu-id="7af8a-124">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7af8a-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="7af8a-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7af8a-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7af8a-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7af8a-126">AzureVM</span></span> 
- <span data-ttu-id="7af8a-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="7af8a-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af8a-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="7af8a-128">-WorkloadType</span></span>
<span data-ttu-id="7af8a-129">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7af8a-129">Specifies the workload type.</span></span>
<span data-ttu-id="7af8a-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7af8a-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7af8a-131">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7af8a-131">AzureVM</span></span> 
- <span data-ttu-id="7af8a-132">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="7af8a-132">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af8a-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af8a-133">-DefaultProfile</span></span>
<span data-ttu-id="7af8a-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7af8a-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7af8a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af8a-135">CommonParameters</span></span>
<span data-ttu-id="7af8a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7af8a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af8a-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7af8a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af8a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7af8a-138">INPUTS</span></span>

## <span data-ttu-id="7af8a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7af8a-139">OUTPUTS</span></span>

### <span data-ttu-id="7af8a-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="7af8a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="7af8a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7af8a-141">NOTES</span></span>

## <span data-ttu-id="7af8a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7af8a-142">RELATED LINKS</span></span>

[<span data-ttu-id="7af8a-143">Új – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af8a-143">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="7af8a-144">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7af8a-144">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


