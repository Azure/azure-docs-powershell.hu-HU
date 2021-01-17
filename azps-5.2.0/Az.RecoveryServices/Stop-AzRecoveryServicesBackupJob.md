---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 41234c91d5c833f15a4914d2af2de93c9c5bf288
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331721"
---
# <span data-ttu-id="5ca0d-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5ca0d-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="5ca0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca0d-103">Megszakít egy futó feladatot.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-103">Cancels a running job.</span></span>

## <span data-ttu-id="5ca0d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-104">SYNTAX</span></span>

### <span data-ttu-id="5ca0d-105">JobFilterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ca0d-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ca0d-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="5ca0d-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ca0d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-107">DESCRIPTION</span></span>
<span data-ttu-id="5ca0d-108">A **Stop-AzRecoveryServicesBackup Job** parancsmag megszakít egy meglévő Azure biztonsági mentési feladatot.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="5ca0d-109">Ezzel a parancsmagkal leállíthatja a túl sokáig tartó és egyéb tevékenységeket letiltó feladatot.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="5ca0d-110">Csak a biztonsági mentési és visszaállítási feladattípusokat mondhatja le.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="5ca0d-111">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5ca0d-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ca0d-112">EXAMPLES</span></span>

### <span data-ttu-id="5ca0d-113">1. példa: Biztonsági mentési feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="5ca0d-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="5ca0d-114">Az első parancs kap egy biztonságimásolat-feladatot, majd a feladatot a $Job tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="5ca0d-115">Az utolsó parancs leállítja a feladatot a biztonságimásolat-feladat példányazonosítójának megadásával a $Job.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="5ca0d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-116">PARAMETERS</span></span>

### <span data-ttu-id="5ca0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca0d-117">-DefaultProfile</span></span>
<span data-ttu-id="5ca0d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ca0d-119">-Job</span><span class="sxs-lookup"><span data-stu-id="5ca0d-119">-Job</span></span>
<span data-ttu-id="5ca0d-120">Azt a feladatot adja meg, amely megszakítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="5ca0d-121">**Biztonságimásolat-objektum** beszerzéséhez használja a Get-AzRecoveryServicesBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca0d-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="5ca0d-122">-JobId</span></span>
<span data-ttu-id="5ca0d-123">A megszakítható feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="5ca0d-124">Az azonosító egy Backup Állmán-objektum **InstanceId tulajdonsága.**</span><span class="sxs-lookup"><span data-stu-id="5ca0d-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="5ca0d-125">**Biztonságimásolat-objektum** beszerzéséhez használja a Get-AzRecoveryServicesBackupServicesBackupBacket.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca0d-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5ca0d-126">-VaultId</span></span>
<span data-ttu-id="5ca0d-127">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5ca0d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ca0d-128">-Confirm</span></span>
<span data-ttu-id="5ca0d-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ca0d-130">-WhatIf</span></span>
<span data-ttu-id="5ca0d-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-131">Shows what would happen if the cmdlet runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca0d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca0d-132">CommonParameters</span></span>
<span data-ttu-id="5ca0d-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca0d-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ca0d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca0d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-135">INPUTS</span></span>

### <span data-ttu-id="5ca0d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5ca0d-136">System.String</span></span>

## <span data-ttu-id="5ca0d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ca0d-137">OUTPUTS</span></span>

### <span data-ttu-id="5ca0d-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="5ca0d-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5ca0d-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ca0d-139">NOTES</span></span>

## <span data-ttu-id="5ca0d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ca0d-140">RELATED LINKS</span></span>

[<span data-ttu-id="5ca0d-141">Get-AzRecoveryServicesBackupService</span><span class="sxs-lookup"><span data-stu-id="5ca0d-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="5ca0d-142">Wait-AzRecoveryServicesBackupService</span><span class="sxs-lookup"><span data-stu-id="5ca0d-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


