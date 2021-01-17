---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329658"
---
# <span data-ttu-id="f62af-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f62af-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="f62af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f62af-102">SYNOPSIS</span></span>

<span data-ttu-id="f62af-103">Megvárja, amíg befejeződik a biztonsági mentési feladat.</span><span class="sxs-lookup"><span data-stu-id="f62af-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="f62af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f62af-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f62af-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f62af-105">DESCRIPTION</span></span>

<span data-ttu-id="f62af-106">A **Wait-AzRecoveryServicesBackup Job** parancsmag megvárja, amíg befejeződik az Azure Biztonsági másolat parancsmag.</span><span class="sxs-lookup"><span data-stu-id="f62af-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="f62af-107">A biztonsági mentési feladatok hosszú ideig is el tudnak tartani.</span><span class="sxs-lookup"><span data-stu-id="f62af-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="f62af-108">Ha egy parancsfájl részeként futtat biztonságimásolat-feladatot, előfordulhat, hogy kényszeríteni szeretné, hogy a parancsfájl várja meg, amíg befejeződik a feladat, mielőtt az más feladatokra folytatódik.</span><span class="sxs-lookup"><span data-stu-id="f62af-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="f62af-109">A parancsmagot tartalmazó parancsmag egyszerűbb lehet, mint az, amely a biztonsági másolat szolgáltatásban lekérdezi a feladat állapotát.</span><span class="sxs-lookup"><span data-stu-id="f62af-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="f62af-110">Állítsa be a tároló környezetét a -VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="f62af-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f62af-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f62af-111">EXAMPLES</span></span>

### <span data-ttu-id="f62af-112">1. példa: Várjon, amíg befejeződik egy feladat</span><span class="sxs-lookup"><span data-stu-id="f62af-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="f62af-113">Ez a parancsprogram lekérdezi az első folyamatban lévő feladatot, amíg a feladat be nem fejeződik, vagy amíg az 1 órás időkorlát el nem jár.</span><span class="sxs-lookup"><span data-stu-id="f62af-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="f62af-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f62af-114">PARAMETERS</span></span>

### <span data-ttu-id="f62af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62af-115">-DefaultProfile</span></span>

<span data-ttu-id="f62af-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f62af-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f62af-117">-Job</span><span class="sxs-lookup"><span data-stu-id="f62af-117">-Job</span></span>

<span data-ttu-id="f62af-118">Azt a feladatot adja meg, amelyig várni kell.</span><span class="sxs-lookup"><span data-stu-id="f62af-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="f62af-119">**Biztonságimásolat-objektum** beszerzéséhez használja a **Get-AzRecoveryServicesBackupServicesBackupService** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f62af-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="f62af-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="f62af-120">-Timeout</span></span>

<span data-ttu-id="f62af-121">Ez a parancsmag másodpercben megadott maximális idejét adja meg, amíg a feladat befejeződik.</span><span class="sxs-lookup"><span data-stu-id="f62af-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="f62af-122">Javasoljuk, hogy adjon meg egy időkorrektaértéket.</span><span class="sxs-lookup"><span data-stu-id="f62af-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="f62af-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f62af-123">-VaultId</span></span>

<span data-ttu-id="f62af-124">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f62af-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f62af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62af-125">CommonParameters</span></span>
<span data-ttu-id="f62af-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f62af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62af-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f62af-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62af-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f62af-128">INPUTS</span></span>

### <span data-ttu-id="f62af-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="f62af-129">System.Object</span></span>

### <span data-ttu-id="f62af-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f62af-130">System.String</span></span>

## <span data-ttu-id="f62af-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f62af-131">OUTPUTS</span></span>

### <span data-ttu-id="f62af-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="f62af-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f62af-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f62af-133">NOTES</span></span>

## <span data-ttu-id="f62af-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f62af-134">RELATED LINKS</span></span>

[<span data-ttu-id="f62af-135">Get-AzRecoveryServicesBackupService</span><span class="sxs-lookup"><span data-stu-id="f62af-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
