---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 377250dcc8cbeb3727e7d2bf3f0dd0a8581d6401
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499452"
---
# <span data-ttu-id="3e9cd-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3e9cd-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="3e9cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e9cd-102">SYNOPSIS</span></span>
<span data-ttu-id="3e9cd-103">Várakozás a biztonsági mentési feladat befejezésére.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e9cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e9cd-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e9cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e9cd-105">DESCRIPTION</span></span>
<span data-ttu-id="3e9cd-106">A **WAIT-AzureRmRecoveryServicesBackupJob** parancsmag megvárja az Azure biztonsági mentési feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="3e9cd-107">A biztonságimásolat-feladatok hosszú időt vehetnek igénybe.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="3e9cd-108">Ha egy parancsfájl részeként biztonsági mentési feladatot futtat, előfordulhat, hogy a parancsfájlt úgy kell megvárnia, hogy a feladat befejezését követően továbbra is megmaradjon az egyéb tevékenységekre.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="3e9cd-109">Az e parancsmagot tartalmazó parancsfájlok egyszerűbbek, mint a biztonsági mentési szolgáltatás a munkahelyi állapothoz.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="3e9cd-110">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3e9cd-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3e9cd-111">EXAMPLES</span></span>

### <span data-ttu-id="3e9cd-112">1. példa: várjon egy feladatot a befejezéshez.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="3e9cd-113">Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="3e9cd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e9cd-114">PARAMETERS</span></span>

### <span data-ttu-id="3e9cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e9cd-115">-DefaultProfile</span></span>
<span data-ttu-id="3e9cd-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e9cd-117">-Job</span><span class="sxs-lookup"><span data-stu-id="3e9cd-117">-Job</span></span>
<span data-ttu-id="3e9cd-118">Azt a feladatot adja meg, amelyre várni szeretne.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="3e9cd-119">**BackupJob** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="3e9cd-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="3e9cd-120">-Timeout</span></span>
<span data-ttu-id="3e9cd-121">Annak a maximális időpontnak a száma, másodpercben kifejezve, hogy ez a parancsmag várja a feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="3e9cd-122">Az időtúllépési érték meghatározása ajánlott.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="3e9cd-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3e9cd-123">-VaultId</span></span>
<span data-ttu-id="3e9cd-124">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="3e9cd-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3e9cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9cd-125">CommonParameters</span></span>
<span data-ttu-id="3e9cd-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e9cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9cd-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e9cd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9cd-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e9cd-128">INPUTS</span></span>

### <span data-ttu-id="3e9cd-129">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-129">System.Object</span></span>
<span data-ttu-id="3e9cd-130">Paraméterek: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="3e9cd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3e9cd-131">System.String</span></span>
<span data-ttu-id="3e9cd-132">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-132">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="3e9cd-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e9cd-133">OUTPUTS</span></span>

### <span data-ttu-id="3e9cd-134">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="3e9cd-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3e9cd-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e9cd-135">NOTES</span></span>

## <span data-ttu-id="3e9cd-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e9cd-136">RELATED LINKS</span></span>

[<span data-ttu-id="3e9cd-137">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3e9cd-137">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


