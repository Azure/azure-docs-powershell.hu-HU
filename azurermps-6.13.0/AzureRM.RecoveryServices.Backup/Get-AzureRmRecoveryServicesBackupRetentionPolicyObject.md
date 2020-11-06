---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 83eeeec861452407dae1a9d92e5bc900b98d6512
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498196"
---
# <span data-ttu-id="a5474-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="a5474-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="a5474-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5474-102">SYNOPSIS</span></span>
<span data-ttu-id="a5474-103">Adatmegőrzési házirend-objektumot kap.</span><span class="sxs-lookup"><span data-stu-id="a5474-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5474-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5474-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5474-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5474-105">DESCRIPTION</span></span>
<span data-ttu-id="a5474-106">A **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** parancsmag alap **AzureRMRecoveryServicesRetentionPolicyObject** kap.</span><span class="sxs-lookup"><span data-stu-id="a5474-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="a5474-107">Ez az objektum nem marad fenn a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="a5474-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="a5474-108">Ez egy ideiglenes objektum, amelyet az New-AzureRmRecoveryServicesBackupProtectionPolicy parancsmaggal kezelheti és használhat új biztonsági házirend létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="a5474-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="a5474-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a5474-109">EXAMPLES</span></span>

### <span data-ttu-id="a5474-110">Példa 1: biztonsági mentést biztosító házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="a5474-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="a5474-111">Az első parancs megkapja az adatmegőrzési házirend objektumot, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a5474-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="a5474-112">A második parancs az adatmegőrzési házirend-objektum időtartamát 365 napra állítja be.</span><span class="sxs-lookup"><span data-stu-id="a5474-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="a5474-113">A harmadik parancs megkapja az ütemezési házirend-objektumot, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a5474-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="a5474-114">Az utolsó parancs biztonsági mentési házirendet hoz létre az előző parancsokkal létrehozott adatmegőrzési házirend és ütemezési házirend használatával.</span><span class="sxs-lookup"><span data-stu-id="a5474-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="a5474-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5474-115">PARAMETERS</span></span>

### <span data-ttu-id="a5474-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="a5474-116">-BackupManagementType</span></span>
<span data-ttu-id="a5474-117">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5474-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="a5474-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a5474-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a5474-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="a5474-119">AzureVM</span></span> 
- <span data-ttu-id="a5474-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="a5474-120">AzureSQLDatabase</span></span>
- <span data-ttu-id="a5474-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="a5474-121">AzureStorage</span></span>

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

### <span data-ttu-id="a5474-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5474-122">-DefaultProfile</span></span>
<span data-ttu-id="a5474-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5474-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5474-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="a5474-124">-WorkloadType</span></span>
<span data-ttu-id="a5474-125">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5474-125">Specifies the workload type.</span></span>
<span data-ttu-id="a5474-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a5474-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a5474-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="a5474-127">AzureVM</span></span> 
- <span data-ttu-id="a5474-128">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="a5474-128">AzureSQLDatabase</span></span>
- <span data-ttu-id="a5474-129">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="a5474-129">AzureFiles</span></span>

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

### <span data-ttu-id="a5474-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5474-130">CommonParameters</span></span>
<span data-ttu-id="a5474-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5474-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5474-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5474-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5474-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5474-133">INPUTS</span></span>

### <span data-ttu-id="a5474-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="a5474-134">None</span></span>

## <span data-ttu-id="a5474-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5474-135">OUTPUTS</span></span>

### <span data-ttu-id="a5474-136">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="a5474-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="a5474-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5474-137">NOTES</span></span>

## <span data-ttu-id="a5474-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5474-138">RELATED LINKS</span></span>

[<span data-ttu-id="a5474-139">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="a5474-139">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="a5474-140">Új – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a5474-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


