---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: d426cd18aaf3382939e55668b1c19938319a3c51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183361"
---
# <span data-ttu-id="84e7a-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="84e7a-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="84e7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="84e7a-103">Adatmegőrzési házirend-objektumot kap.</span><span class="sxs-lookup"><span data-stu-id="84e7a-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="84e7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84e7a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84e7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="84e7a-106">A **Get-AzRecoveryServicesBackupRetentionPolicyObject** parancsmag alap **AzureRMRecoveryServicesRetentionPolicyObject** kap.</span><span class="sxs-lookup"><span data-stu-id="84e7a-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="84e7a-107">Ez az objektum nem marad fenn a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="84e7a-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="84e7a-108">Ez egy ideiglenes objektum, amelyet az New-AzRecoveryServicesBackupProtectionPolicy parancsmaggal kezelheti és használhat új biztonsági házirend létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="84e7a-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="84e7a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="84e7a-109">EXAMPLES</span></span>

### <span data-ttu-id="84e7a-110">Példa 1: biztonsági mentést biztosító házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="84e7a-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="84e7a-111">Az első parancs megkapja az adatmegőrzési házirend objektumot, majd a $RetPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="84e7a-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="84e7a-112">A második parancs az adatmegőrzési házirend-objektum időtartamát 365 napra állítja be.</span><span class="sxs-lookup"><span data-stu-id="84e7a-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="84e7a-113">A harmadik parancs megkapja az ütemezési házirend-objektumot, majd a $SchPol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="84e7a-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="84e7a-114">Az utolsó parancs biztonsági mentési házirendet hoz létre az előző parancsokkal létrehozott adatmegőrzési házirend és ütemezési házirend használatával.</span><span class="sxs-lookup"><span data-stu-id="84e7a-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="84e7a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84e7a-115">PARAMETERS</span></span>

### <span data-ttu-id="84e7a-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="84e7a-116">-BackupManagementType</span></span>
<span data-ttu-id="84e7a-117">A védelemmel ellátott erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="84e7a-117">The class of resources being protected.</span></span> <span data-ttu-id="84e7a-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="84e7a-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84e7a-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="84e7a-119">AzureVM</span></span> 
- <span data-ttu-id="84e7a-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="84e7a-120">AzureWorkload</span></span>
- <span data-ttu-id="84e7a-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="84e7a-121">AzureStorage</span></span>

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

### <span data-ttu-id="84e7a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e7a-122">-DefaultProfile</span></span>
<span data-ttu-id="84e7a-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84e7a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84e7a-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="84e7a-124">-WorkloadType</span></span>
<span data-ttu-id="84e7a-125">Az erőforrás terhelési típusa.</span><span class="sxs-lookup"><span data-stu-id="84e7a-125">Workload type of the resource.</span></span> <span data-ttu-id="84e7a-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="84e7a-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84e7a-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="84e7a-127">AzureVM</span></span> 
- <span data-ttu-id="84e7a-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="84e7a-128">AzureFiles</span></span>
- <span data-ttu-id="84e7a-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="84e7a-129">MSSQL</span></span>

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

### <span data-ttu-id="84e7a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e7a-130">CommonParameters</span></span>
<span data-ttu-id="84e7a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84e7a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e7a-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="84e7a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e7a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84e7a-133">INPUTS</span></span>

### <span data-ttu-id="84e7a-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="84e7a-134">None</span></span>

## <span data-ttu-id="84e7a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84e7a-135">OUTPUTS</span></span>

### <span data-ttu-id="84e7a-136">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="84e7a-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="84e7a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84e7a-137">NOTES</span></span>

## <span data-ttu-id="84e7a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84e7a-138">RELATED LINKS</span></span>

[<span data-ttu-id="84e7a-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="84e7a-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="84e7a-140">Új – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="84e7a-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


