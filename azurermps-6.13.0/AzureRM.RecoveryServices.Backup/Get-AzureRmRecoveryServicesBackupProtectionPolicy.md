---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d08bd0a02878b1b99b3243e80512df30eca6e1c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495768"
---
# <span data-ttu-id="22d6c-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="22d6c-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="22d6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="22d6c-103">Biztonsági mentési házirendek készülnek a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="22d6c-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22d6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22d6c-104">SYNTAX</span></span>

### <span data-ttu-id="22d6c-105">NoParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22d6c-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d6c-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="22d6c-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d6c-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="22d6c-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d6c-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="22d6c-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22d6c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="22d6c-109">DESCRIPTION</span></span>
<span data-ttu-id="22d6c-110">A **Get-AzureRmRecoveryServicesBackupProtectionPolicy** parancsmag az Azure Backup Protection házirendjeit kapja a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="22d6c-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="22d6c-111">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="22d6c-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="22d6c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="22d6c-112">EXAMPLES</span></span>

### <span data-ttu-id="22d6c-113">Példa 1: az összes házirend beolvasása a boltozaton</span><span class="sxs-lookup"><span data-stu-id="22d6c-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="22d6c-114">Ez a parancs a boltozattal létrehozott összes védelmi házirendet megkapja.</span><span class="sxs-lookup"><span data-stu-id="22d6c-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="22d6c-115">2. példa: speciális házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="22d6c-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="22d6c-116">Ez a parancs a DefaultPolicy nevű védelmi házirendet kapja meg, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="22d6c-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="22d6c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22d6c-117">PARAMETERS</span></span>

### <span data-ttu-id="22d6c-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="22d6c-118">-BackupManagementType</span></span>
<span data-ttu-id="22d6c-119">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d6c-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="22d6c-120">Jelenleg csak a AzureVM és a AzureStorage támogatott.</span><span class="sxs-lookup"><span data-stu-id="22d6c-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d6c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d6c-121">-DefaultProfile</span></span>
<span data-ttu-id="22d6c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22d6c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22d6c-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="22d6c-123">-Name</span></span>
<span data-ttu-id="22d6c-124">A házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d6c-124">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d6c-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="22d6c-125">-VaultId</span></span>
<span data-ttu-id="22d6c-126">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="22d6c-126">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22d6c-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="22d6c-127">-WorkloadType</span></span>
<span data-ttu-id="22d6c-128">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d6c-128">Specifies the workload type.</span></span>
<span data-ttu-id="22d6c-129">Jelenleg csak a AzureVM és a AzureFiles támogatott.</span><span class="sxs-lookup"><span data-stu-id="22d6c-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d6c-130">CommonParameters</span></span>
<span data-ttu-id="22d6c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22d6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d6c-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d6c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d6c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22d6c-133">INPUTS</span></span>

### <span data-ttu-id="22d6c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="22d6c-134">System.String</span></span>
<span data-ttu-id="22d6c-135">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22d6c-135">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="22d6c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22d6c-136">OUTPUTS</span></span>

### <span data-ttu-id="22d6c-137">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="22d6c-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="22d6c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22d6c-138">NOTES</span></span>

## <span data-ttu-id="22d6c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22d6c-139">RELATED LINKS</span></span>

[<span data-ttu-id="22d6c-140">Új – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="22d6c-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="22d6c-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="22d6c-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="22d6c-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="22d6c-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


