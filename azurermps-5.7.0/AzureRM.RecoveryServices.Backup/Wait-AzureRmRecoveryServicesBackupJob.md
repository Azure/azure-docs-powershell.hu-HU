---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 651c1cd08f8a2c711a4a0cec16ddb965ccfa8211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493053"
---
# <span data-ttu-id="6626b-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6626b-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="6626b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6626b-102">SYNOPSIS</span></span>
<span data-ttu-id="6626b-103">Várakozás a biztonsági mentési feladat befejezésére.</span><span class="sxs-lookup"><span data-stu-id="6626b-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6626b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6626b-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6626b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6626b-105">DESCRIPTION</span></span>
<span data-ttu-id="6626b-106">A **WAIT-AzureRmRecoveryServicesBackupJob** parancsmag megvárja az Azure biztonsági mentési feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="6626b-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="6626b-107">A biztonságimásolat-feladatok hosszú időt vehetnek igénybe.</span><span class="sxs-lookup"><span data-stu-id="6626b-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="6626b-108">Ha egy parancsfájl részeként biztonsági mentési feladatot futtat, előfordulhat, hogy a parancsfájlt úgy kell megvárnia, hogy a feladat befejezését követően továbbra is megmaradjon az egyéb tevékenységekre.</span><span class="sxs-lookup"><span data-stu-id="6626b-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="6626b-109">Az e parancsmagot tartalmazó parancsfájlok egyszerűbbek, mint a biztonsági mentési szolgáltatás a munkahelyi állapothoz.</span><span class="sxs-lookup"><span data-stu-id="6626b-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

<span data-ttu-id="6626b-110">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="6626b-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6626b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6626b-111">EXAMPLES</span></span>

### <span data-ttu-id="6626b-112">1. példa: várjon egy feladatot a befejezéshez.</span><span class="sxs-lookup"><span data-stu-id="6626b-112">Example 1: Wait for a job to finish</span></span>
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

<span data-ttu-id="6626b-113">Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.</span><span class="sxs-lookup"><span data-stu-id="6626b-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="6626b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6626b-114">PARAMETERS</span></span>

### <span data-ttu-id="6626b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6626b-115">-DefaultProfile</span></span>
<span data-ttu-id="6626b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6626b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6626b-117">-Job</span><span class="sxs-lookup"><span data-stu-id="6626b-117">-Job</span></span>
<span data-ttu-id="6626b-118">Azt a feladatot adja meg, amelyre várni szeretne.</span><span class="sxs-lookup"><span data-stu-id="6626b-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="6626b-119">**BackupJob** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6626b-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6626b-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="6626b-120">-Timeout</span></span>
<span data-ttu-id="6626b-121">Annak a maximális időpontnak a száma, másodpercben kifejezve, hogy ez a parancsmag várja a feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="6626b-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="6626b-122">Az időtúllépési érték meghatározása ajánlott.</span><span class="sxs-lookup"><span data-stu-id="6626b-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6626b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6626b-123">CommonParameters</span></span>
<span data-ttu-id="6626b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6626b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6626b-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6626b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6626b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6626b-126">INPUTS</span></span>

### <span data-ttu-id="6626b-127">Objektum</span><span class="sxs-lookup"><span data-stu-id="6626b-127">Object</span></span>
<span data-ttu-id="6626b-128">A ' Job ' paraméter elfogadja az "objektum" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6626b-128">Parameter 'Job' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="6626b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6626b-129">OUTPUTS</span></span>

### <span data-ttu-id="6626b-130">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="6626b-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="6626b-131">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="6626b-131">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="6626b-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6626b-132">NOTES</span></span>

## <span data-ttu-id="6626b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6626b-133">RELATED LINKS</span></span>

[<span data-ttu-id="6626b-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6626b-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


