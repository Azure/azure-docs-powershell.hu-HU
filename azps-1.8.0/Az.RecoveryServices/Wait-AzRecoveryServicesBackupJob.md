---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 10131025768b93fd1bbd692b07a22a03d8a88726
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669565"
---
# <span data-ttu-id="c534e-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="c534e-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="c534e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c534e-102">SYNOPSIS</span></span>
<span data-ttu-id="c534e-103">Várakozás a biztonsági mentési feladat befejezésére.</span><span class="sxs-lookup"><span data-stu-id="c534e-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="c534e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c534e-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c534e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c534e-105">DESCRIPTION</span></span>
<span data-ttu-id="c534e-106">A **WAIT-AzRecoveryServicesBackupJob** parancsmag megvárja az Azure biztonsági mentési feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="c534e-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="c534e-107">A biztonságimásolat-feladatok hosszú időt vehetnek igénybe.</span><span class="sxs-lookup"><span data-stu-id="c534e-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="c534e-108">Ha egy parancsfájl részeként biztonsági mentési feladatot futtat, előfordulhat, hogy a parancsfájlt úgy kell megvárnia, hogy a feladat befejezését követően továbbra is megmaradjon az egyéb tevékenységekre.</span><span class="sxs-lookup"><span data-stu-id="c534e-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="c534e-109">Az e parancsmagot tartalmazó parancsfájlok egyszerűbbek, mint a biztonsági mentési szolgáltatás a munkahelyi állapothoz.</span><span class="sxs-lookup"><span data-stu-id="c534e-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="c534e-110">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="c534e-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c534e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c534e-111">EXAMPLES</span></span>

### <span data-ttu-id="c534e-112">1. példa: várjon egy feladatot a befejezéshez.</span><span class="sxs-lookup"><span data-stu-id="c534e-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="c534e-113">Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="c534e-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="c534e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c534e-114">PARAMETERS</span></span>

### <span data-ttu-id="c534e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c534e-115">-DefaultProfile</span></span>
<span data-ttu-id="c534e-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c534e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c534e-117">-Job</span><span class="sxs-lookup"><span data-stu-id="c534e-117">-Job</span></span>
<span data-ttu-id="c534e-118">Azt a feladatot adja meg, amelyre várni szeretne.</span><span class="sxs-lookup"><span data-stu-id="c534e-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="c534e-119">**BackupJob** objektum beolvasásához használja az Get-AzRecoveryServicesBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c534e-119">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c534e-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="c534e-120">-Timeout</span></span>
<span data-ttu-id="c534e-121">Annak a maximális időpontnak a száma, másodpercben kifejezve, hogy ez a parancsmag várja a feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="c534e-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="c534e-122">Az időtúllépési érték meghatározása ajánlott.</span><span class="sxs-lookup"><span data-stu-id="c534e-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c534e-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c534e-123">-VaultId</span></span>
<span data-ttu-id="c534e-124">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="c534e-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c534e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c534e-125">CommonParameters</span></span>
<span data-ttu-id="c534e-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c534e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c534e-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c534e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c534e-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c534e-128">INPUTS</span></span>

### <span data-ttu-id="c534e-129">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="c534e-129">System.Object</span></span>

### <span data-ttu-id="c534e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c534e-130">System.String</span></span>

## <span data-ttu-id="c534e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c534e-131">OUTPUTS</span></span>

### <span data-ttu-id="c534e-132">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="c534e-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c534e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c534e-133">NOTES</span></span>

## <span data-ttu-id="c534e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c534e-134">RELATED LINKS</span></span>

[<span data-ttu-id="c534e-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="c534e-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)


