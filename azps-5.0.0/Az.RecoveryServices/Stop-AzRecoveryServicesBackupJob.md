---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 41234c91d5c833f15a4914d2af2de93c9c5bf288
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186847"
---
# <span data-ttu-id="99c07-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="99c07-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="99c07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99c07-102">SYNOPSIS</span></span>
<span data-ttu-id="99c07-103">Lemond egy futó feladatot.</span><span class="sxs-lookup"><span data-stu-id="99c07-103">Cancels a running job.</span></span>

## <span data-ttu-id="99c07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99c07-104">SYNTAX</span></span>

### <span data-ttu-id="99c07-105">JobFilterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99c07-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99c07-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="99c07-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99c07-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="99c07-107">DESCRIPTION</span></span>
<span data-ttu-id="99c07-108">A **stop-AzRecoveryServicesBackupJob** parancsmag lemond egy meglévő Azure biztonsági mentési feladatról.</span><span class="sxs-lookup"><span data-stu-id="99c07-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="99c07-109">Ezzel a parancsmaggal leállíthat egy olyan feladatot, amely túl hosszú időt vesz igénybe, és blokkolja az egyéb tevékenységeket.</span><span class="sxs-lookup"><span data-stu-id="99c07-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="99c07-110">Csak biztonsági mentési és visszaállítási munkatípusokat törölhet.</span><span class="sxs-lookup"><span data-stu-id="99c07-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="99c07-111">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="99c07-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="99c07-112">Példák</span><span class="sxs-lookup"><span data-stu-id="99c07-112">EXAMPLES</span></span>

### <span data-ttu-id="99c07-113">Példa 1: biztonsági mentési feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="99c07-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="99c07-114">Az első parancs biztonsági mentési feladatot kap, majd a $Job változóban tárolja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="99c07-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="99c07-115">Az utolsó parancs a feladatot a $Job biztonsági mentési feladat példány-AZONOSÍTÓjának megadásával szünteti meg.</span><span class="sxs-lookup"><span data-stu-id="99c07-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="99c07-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99c07-116">PARAMETERS</span></span>

### <span data-ttu-id="99c07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c07-117">-DefaultProfile</span></span>
<span data-ttu-id="99c07-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99c07-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c07-119">-Job</span><span class="sxs-lookup"><span data-stu-id="99c07-119">-Job</span></span>
<span data-ttu-id="99c07-120">A parancsmag által lemondott feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="99c07-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="99c07-121">**BackupJob** objektum beolvasásához használja az Get-AzRecoveryServicesBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="99c07-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="99c07-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="99c07-122">-JobId</span></span>
<span data-ttu-id="99c07-123">A lemondani kívánt feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="99c07-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="99c07-124">Az azonosító a **BackupJob** -objektum InstanceId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="99c07-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="99c07-125">**BackupJob** -objektum beszerzéséhez használja a Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="99c07-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="99c07-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="99c07-126">-VaultId</span></span>
<span data-ttu-id="99c07-127">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="99c07-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="99c07-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99c07-128">-Confirm</span></span>
<span data-ttu-id="99c07-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99c07-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c07-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c07-130">-WhatIf</span></span>
<span data-ttu-id="99c07-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99c07-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="99c07-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c07-132">CommonParameters</span></span>
<span data-ttu-id="99c07-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99c07-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c07-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="99c07-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c07-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99c07-135">INPUTS</span></span>

### <span data-ttu-id="99c07-136">System. String</span><span class="sxs-lookup"><span data-stu-id="99c07-136">System.String</span></span>

## <span data-ttu-id="99c07-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99c07-137">OUTPUTS</span></span>

### <span data-ttu-id="99c07-138">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="99c07-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="99c07-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99c07-139">NOTES</span></span>

## <span data-ttu-id="99c07-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99c07-140">RELATED LINKS</span></span>

[<span data-ttu-id="99c07-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="99c07-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="99c07-142">Várjon-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="99c07-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


