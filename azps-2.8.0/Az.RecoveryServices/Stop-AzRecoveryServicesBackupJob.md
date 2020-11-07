---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 80fbb17d31c37dafd4ba16b059c1dda5a987bea4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838536"
---
# <span data-ttu-id="c5870-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="c5870-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="c5870-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5870-102">SYNOPSIS</span></span>
<span data-ttu-id="c5870-103">Lemond egy futó feladatot.</span><span class="sxs-lookup"><span data-stu-id="c5870-103">Cancels a running job.</span></span>

## <span data-ttu-id="c5870-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5870-104">SYNTAX</span></span>

### <span data-ttu-id="c5870-105">JobFilterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5870-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5870-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="c5870-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5870-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5870-107">DESCRIPTION</span></span>
<span data-ttu-id="c5870-108">A **stop-AzRecoveryServicesBackupJob** parancsmag lemond egy meglévő Azure biztonsági mentési feladatról.</span><span class="sxs-lookup"><span data-stu-id="c5870-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="c5870-109">Ezzel a parancsmaggal leállíthat egy olyan feladatot, amely túl hosszú időt vesz igénybe, és blokkolja az egyéb tevékenységeket.</span><span class="sxs-lookup"><span data-stu-id="c5870-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="c5870-110">Csak biztonsági mentési és visszaállítási munkatípusokat törölhet.</span><span class="sxs-lookup"><span data-stu-id="c5870-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="c5870-111">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="c5870-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c5870-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c5870-112">EXAMPLES</span></span>

### <span data-ttu-id="c5870-113">Példa 1: biztonsági mentési feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="c5870-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="c5870-114">Az első parancs biztonsági mentési feladatot kap, majd a $Job változóban tárolja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="c5870-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="c5870-115">Az utolsó parancs a feladatot a $Job biztonsági mentési feladat példány-AZONOSÍTÓjának megadásával szünteti meg.</span><span class="sxs-lookup"><span data-stu-id="c5870-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="c5870-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5870-116">PARAMETERS</span></span>

### <span data-ttu-id="c5870-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5870-117">-DefaultProfile</span></span>
<span data-ttu-id="c5870-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5870-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5870-119">-Job</span><span class="sxs-lookup"><span data-stu-id="c5870-119">-Job</span></span>
<span data-ttu-id="c5870-120">A parancsmag által lemondott feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5870-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="c5870-121">**BackupJob** objektum beolvasásához használja az Get-AzRecoveryServicesBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c5870-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="c5870-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="c5870-122">-JobId</span></span>
<span data-ttu-id="c5870-123">A lemondani kívánt feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5870-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="c5870-124">Az azonosító a **BackupJob** -objektum InstanceId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="c5870-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="c5870-125">**BackupJob** -objektum beszerzéséhez használja a Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="c5870-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="c5870-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c5870-126">-VaultId</span></span>
<span data-ttu-id="c5870-127">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="c5870-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c5870-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5870-128">-Confirm</span></span>
<span data-ttu-id="c5870-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5870-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5870-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5870-130">-WhatIf</span></span>
<span data-ttu-id="c5870-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5870-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5870-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5870-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5870-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5870-133">CommonParameters</span></span>
<span data-ttu-id="c5870-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5870-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5870-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5870-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5870-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5870-136">INPUTS</span></span>

### <span data-ttu-id="c5870-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c5870-137">System.String</span></span>

## <span data-ttu-id="c5870-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5870-138">OUTPUTS</span></span>

### <span data-ttu-id="c5870-139">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="c5870-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c5870-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5870-140">NOTES</span></span>

## <span data-ttu-id="c5870-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5870-141">RELATED LINKS</span></span>

[<span data-ttu-id="c5870-142">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="c5870-142">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="c5870-143">Várjon-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="c5870-143">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


