---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: bb1c63b41d27f92991a3504cdd5c2fd8fe547298
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921641"
---
# <span data-ttu-id="cc712-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="cc712-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="cc712-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc712-102">SYNOPSIS</span></span>
<span data-ttu-id="cc712-103">Alap adatmegőrzési házirend-objektumot kap.</span><span class="sxs-lookup"><span data-stu-id="cc712-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="cc712-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cc712-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc712-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cc712-105">DESCRIPTION</span></span>
<span data-ttu-id="cc712-106">A **Get-AzRecoveryServicesBackupRetentionPolicyObject** parancsmag egy alap **AzureRMRecoveryServicesRetentionPolicyObject** parancsmagot kap.</span><span class="sxs-lookup"><span data-stu-id="cc712-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="cc712-107">Ez az objektum nem marad meg a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="cc712-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="cc712-108">Ez egy ideiglenes objektum, amely a New-AzRecoveryServicesBackupProtectionPolicy segítségével új biztonságimásolat-házirendet hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="cc712-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="cc712-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cc712-109">EXAMPLES</span></span>

### <span data-ttu-id="cc712-110">1. példa: Biztonságimásolat-védelmi házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="cc712-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="cc712-111">Az első parancs megkapja az adatmegőrzési házirend-objektumot, majd a $RetPol tárolja.</span><span class="sxs-lookup"><span data-stu-id="cc712-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="cc712-112">A második parancs 365 napra állítja az adatmegőrzési házirend-objektum időtartamát.</span><span class="sxs-lookup"><span data-stu-id="cc712-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="cc712-113">A harmadik parancs megkapja az ütemezési házirendobjektumot, majd a $SchPol tárolja.</span><span class="sxs-lookup"><span data-stu-id="cc712-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="cc712-114">Az utolsó parancs egy biztonságimásolat-védelmi házirendet hoz létre az adatmegőrzési házirend és az előző parancsokkal létrehozott ütemezési házirend használatával.</span><span class="sxs-lookup"><span data-stu-id="cc712-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="cc712-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc712-115">PARAMETERS</span></span>

### <span data-ttu-id="cc712-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="cc712-116">-BackupManagementType</span></span>
<span data-ttu-id="cc712-117">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="cc712-117">The class of resources being protected.</span></span> <span data-ttu-id="cc712-118">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="cc712-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc712-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="cc712-119">AzureVM</span></span> 
- <span data-ttu-id="cc712-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="cc712-120">AzureWorkload</span></span>
- <span data-ttu-id="cc712-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="cc712-121">AzureStorage</span></span>

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

### <span data-ttu-id="cc712-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc712-122">-DefaultProfile</span></span>
<span data-ttu-id="cc712-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc712-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc712-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="cc712-124">-WorkloadType</span></span>
<span data-ttu-id="cc712-125">Az erőforrás terheléstípusa.</span><span class="sxs-lookup"><span data-stu-id="cc712-125">Workload type of the resource.</span></span> <span data-ttu-id="cc712-126">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="cc712-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc712-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="cc712-127">AzureVM</span></span> 
- <span data-ttu-id="cc712-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="cc712-128">AzureFiles</span></span>
- <span data-ttu-id="cc712-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="cc712-129">MSSQL</span></span>

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

### <span data-ttu-id="cc712-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc712-130">CommonParameters</span></span>
<span data-ttu-id="cc712-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc712-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc712-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc712-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc712-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc712-133">INPUTS</span></span>

### <span data-ttu-id="cc712-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="cc712-134">None</span></span>

## <span data-ttu-id="cc712-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc712-135">OUTPUTS</span></span>

### <span data-ttu-id="cc712-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="cc712-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="cc712-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cc712-137">NOTES</span></span>

## <span data-ttu-id="cc712-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc712-138">RELATED LINKS</span></span>

[<span data-ttu-id="cc712-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="cc712-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="cc712-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cc712-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


