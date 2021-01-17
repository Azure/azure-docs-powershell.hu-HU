---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467254"
---
# <span data-ttu-id="53520-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="53520-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="53520-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53520-102">SYNOPSIS</span></span>

<span data-ttu-id="53520-103">Részleteket kap a biztonsági másolatok készítéséhez.</span><span class="sxs-lookup"><span data-stu-id="53520-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="53520-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53520-104">SYNTAX</span></span>

### <span data-ttu-id="53520-105">JobFilterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53520-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53520-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="53520-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53520-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53520-107">DESCRIPTION</span></span>

<span data-ttu-id="53520-108">A **Get-AzRecoveryServicesBackup JobDetail** parancsmag az Azure biztonsági mentési feladatának részleteit kapja meg egy adott feladathoz.</span><span class="sxs-lookup"><span data-stu-id="53520-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="53520-109">Állítsa be a tároló környezetét a -VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="53520-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="53520-110">Figyelmeztetés: **A Get-AzRecoveryServicesBackupServicesBackupServiceDetails** aliast a rendszer eltávolítja egy későbbi, friss módosítással kapcsolatos kiadásban.</span><span class="sxs-lookup"><span data-stu-id="53520-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="53520-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53520-111">EXAMPLES</span></span>

### <span data-ttu-id="53520-112">1. példa: Biztonsági mentési feladat részleteinek lekérte a sikertelen feladatok adatait</span><span class="sxs-lookup"><span data-stu-id="53520-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="53520-113">Az első parancs lekéri a megfelelő tárolót.</span><span class="sxs-lookup"><span data-stu-id="53520-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="53520-114">A második parancs egy tömböt kap a sikertelen feladatokból a tárolóban, majd tárolja őket a $Jobs tömbben.</span><span class="sxs-lookup"><span data-stu-id="53520-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="53520-115">A harmadik parancs lekérte az első sikertelen feladat $Jobs, majd tárolja őket a $JobDetails változóban.</span><span class="sxs-lookup"><span data-stu-id="53520-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="53520-116">Az utolsó parancs megjeleníti a sikertelen feladatok hiba részleteit.</span><span class="sxs-lookup"><span data-stu-id="53520-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="53520-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53520-117">PARAMETERS</span></span>

### <span data-ttu-id="53520-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53520-118">-DefaultProfile</span></span>

<span data-ttu-id="53520-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53520-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53520-120">-Job</span><span class="sxs-lookup"><span data-stu-id="53520-120">-Job</span></span>

<span data-ttu-id="53520-121">A lekért feladat megadása.</span><span class="sxs-lookup"><span data-stu-id="53520-121">Specifies the job to get.</span></span>
<span data-ttu-id="53520-122">**Biztonságimásolat-objektum** beszerzéséhez használja a **Get-AzRecoveryServicesBackupServicesBackupService** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="53520-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="53520-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="53520-123">-JobId</span></span>

<span data-ttu-id="53520-124">Egy biztonságimásolat-feladat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53520-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="53520-125">Az azonosító a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase objektum JobId tulajdonsága.**</span><span class="sxs-lookup"><span data-stu-id="53520-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="53520-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="53520-126">-VaultId</span></span>

<span data-ttu-id="53520-127">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="53520-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="53520-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53520-128">CommonParameters</span></span>
<span data-ttu-id="53520-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53520-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53520-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53520-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53520-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53520-131">INPUTS</span></span>

### <span data-ttu-id="53520-132">System.String</span><span class="sxs-lookup"><span data-stu-id="53520-132">System.String</span></span>

## <span data-ttu-id="53520-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53520-133">OUTPUTS</span></span>

### <span data-ttu-id="53520-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="53520-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="53520-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53520-135">NOTES</span></span>

## <span data-ttu-id="53520-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53520-136">RELATED LINKS</span></span>

[<span data-ttu-id="53520-137">Get-AzRecoveryServicesBackupService</span><span class="sxs-lookup"><span data-stu-id="53520-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
