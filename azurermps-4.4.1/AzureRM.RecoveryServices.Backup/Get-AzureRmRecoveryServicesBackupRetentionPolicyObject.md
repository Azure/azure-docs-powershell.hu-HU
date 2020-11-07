---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 5fd705d38f2deb232c9b62861804eb2830f45999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680239"
---
# <span data-ttu-id="7f0fc-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="7f0fc-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="7f0fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0fc-103">Adatmegőrzési házirend-objektumot kap.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f0fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f0fc-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f0fc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f0fc-105">DESCRIPTION</span></span>
<span data-ttu-id="7f0fc-106">A **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** parancsmag alap **AzureRMRecoveryServicesRetentionPolicyObject** kap.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="7f0fc-107">Ez az objektum nem marad fenn a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="7f0fc-108">Ez egy ideiglenes objektum, amelyet az New-AzureRmRecoveryServicesBackupProtectionPolicy parancsmaggal kezelheti és használhat új biztonsági házirend létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="7f0fc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7f0fc-109">EXAMPLES</span></span>

### <span data-ttu-id="7f0fc-110">Példa 1: biztonsági mentést biztosító házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="7f0fc-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="7f0fc-111">Az első parancs megkapja az adatmegőrzési házirend objektumot, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="7f0fc-112">A második parancs az adatmegőrzési házirend-objektum időtartamát 365 napra állítja be.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-112">The second command sets the duration for the retention policy object to 365 days.</span></span>

<span data-ttu-id="7f0fc-113">A harmadik parancs megkapja az ütemezési házirend-objektumot, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="7f0fc-114">Az utolsó parancs biztonsági mentési házirendet hoz létre az előző parancsokkal létrehozott adatmegőrzési házirend és ütemezési házirend használatával.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="7f0fc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f0fc-115">PARAMETERS</span></span>

### <span data-ttu-id="7f0fc-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7f0fc-116">-BackupManagementType</span></span>
<span data-ttu-id="7f0fc-117">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="7f0fc-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7f0fc-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f0fc-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7f0fc-119">AzureVM</span></span> 
- <span data-ttu-id="7f0fc-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="7f0fc-120">AzureSQLDatabase</span></span>

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

### <span data-ttu-id="7f0fc-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="7f0fc-121">-WorkloadType</span></span>
<span data-ttu-id="7f0fc-122">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-122">Specifies the workload type.</span></span>
<span data-ttu-id="7f0fc-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7f0fc-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f0fc-124">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7f0fc-124">AzureVM</span></span> 
- <span data-ttu-id="7f0fc-125">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="7f0fc-125">AzureSQLDatabase</span></span>

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

### <span data-ttu-id="7f0fc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f0fc-126">-DefaultProfile</span></span>
<span data-ttu-id="7f0fc-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f0fc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f0fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0fc-128">CommonParameters</span></span>
<span data-ttu-id="7f0fc-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f0fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0fc-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f0fc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0fc-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f0fc-131">INPUTS</span></span>

## <span data-ttu-id="7f0fc-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f0fc-132">OUTPUTS</span></span>

### <span data-ttu-id="7f0fc-133">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="7f0fc-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="7f0fc-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f0fc-134">NOTES</span></span>

## <span data-ttu-id="7f0fc-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f0fc-135">RELATED LINKS</span></span>

[<span data-ttu-id="7f0fc-136">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="7f0fc-136">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="7f0fc-137">Új – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7f0fc-137">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


