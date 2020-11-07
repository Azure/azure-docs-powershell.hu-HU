---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 295cb5bad09584c16e1217e68d3fc80c5ebf8598
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838581"
---
# <span data-ttu-id="d51ff-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d51ff-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="d51ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d51ff-102">SYNOPSIS</span></span>
<span data-ttu-id="d51ff-103">Biztonsági mentési házirendek készülnek a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="d51ff-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="d51ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d51ff-104">SYNTAX</span></span>

### <span data-ttu-id="d51ff-105">NoParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d51ff-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d51ff-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="d51ff-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d51ff-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="d51ff-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d51ff-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="d51ff-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d51ff-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d51ff-109">DESCRIPTION</span></span>
<span data-ttu-id="d51ff-110">A **Get-AzRecoveryServicesBackupProtectionPolicy** parancsmag az Azure Backup Protection házirendjeit kapja a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="d51ff-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="d51ff-111">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="d51ff-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d51ff-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d51ff-112">EXAMPLES</span></span>

### <span data-ttu-id="d51ff-113">Példa 1: az összes házirend beolvasása a boltozaton</span><span class="sxs-lookup"><span data-stu-id="d51ff-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="d51ff-114">Ez a parancs a boltozattal létrehozott összes védelmi házirendet megkapja.</span><span class="sxs-lookup"><span data-stu-id="d51ff-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="d51ff-115">2. példa: speciális házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="d51ff-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="d51ff-116">Ez a parancs a DefaultPolicy nevű védelmi házirendet kapja meg, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d51ff-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="d51ff-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d51ff-117">PARAMETERS</span></span>

### <span data-ttu-id="d51ff-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d51ff-118">-BackupManagementType</span></span>
<span data-ttu-id="d51ff-119">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ff-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="d51ff-120">Jelenleg csak a AzureVM és a AzureStorage támogatott.</span><span class="sxs-lookup"><span data-stu-id="d51ff-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d51ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51ff-121">-DefaultProfile</span></span>
<span data-ttu-id="d51ff-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d51ff-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d51ff-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d51ff-123">-Name</span></span>
<span data-ttu-id="d51ff-124">A házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ff-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="d51ff-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d51ff-125">-VaultId</span></span>
<span data-ttu-id="d51ff-126">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="d51ff-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d51ff-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d51ff-127">-WorkloadType</span></span>
<span data-ttu-id="d51ff-128">A munkaterhelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ff-128">Specifies the workload type.</span></span>
<span data-ttu-id="d51ff-129">Jelenleg csak a AzureVM és a AzureFiles támogatott.</span><span class="sxs-lookup"><span data-stu-id="d51ff-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d51ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51ff-130">CommonParameters</span></span>
<span data-ttu-id="d51ff-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d51ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51ff-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d51ff-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51ff-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d51ff-133">INPUTS</span></span>

### <span data-ttu-id="d51ff-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d51ff-134">System.String</span></span>

## <span data-ttu-id="d51ff-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d51ff-135">OUTPUTS</span></span>

### <span data-ttu-id="d51ff-136">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="d51ff-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="d51ff-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d51ff-137">NOTES</span></span>

## <span data-ttu-id="d51ff-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d51ff-138">RELATED LINKS</span></span>

[<span data-ttu-id="d51ff-139">Új – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d51ff-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d51ff-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d51ff-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d51ff-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d51ff-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


