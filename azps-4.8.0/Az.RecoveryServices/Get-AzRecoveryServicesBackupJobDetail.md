---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025087"
---
# <span data-ttu-id="d6ad3-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="d6ad3-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="d6ad3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6ad3-102">SYNOPSIS</span></span>

<span data-ttu-id="d6ad3-103">Megkeresi a biztonsági mentési feladatok részleteit.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="d6ad3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6ad3-104">SYNTAX</span></span>

### <span data-ttu-id="d6ad3-105">JobFilterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6ad3-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6ad3-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="d6ad3-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6ad3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6ad3-107">DESCRIPTION</span></span>

<span data-ttu-id="d6ad3-108">A **Get-AzRecoveryServicesBackupJobDetail** parancsmag az Azure Backup Job részleteit kapja meg egy adott feladathoz.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="d6ad3-109">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="d6ad3-110">Figyelmeztetés: a **Get-AzRecoveryServicesBackupJobDetails** alias törlődni fog egy jövőbeli változtatási kiadásban.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="d6ad3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d6ad3-111">EXAMPLES</span></span>

### <span data-ttu-id="d6ad3-112">Példa 1: a sikertelen feladatok biztonsági mentési feladatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="d6ad3-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="d6ad3-113">Az első parancs beolvassa a megfelelő boltozatot.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="d6ad3-114">A második parancs a boltozatban nem szereplő sikertelen feladatok tömbjét kapja, majd a $Jobs tömbben tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="d6ad3-115">A harmadik parancs a $Jobs első sikertelen munkájának részleteit kapja meg, majd a $JobDetails változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="d6ad3-116">A végleges parancs a hibás feladatok részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="d6ad3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6ad3-117">PARAMETERS</span></span>

### <span data-ttu-id="d6ad3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ad3-118">-DefaultProfile</span></span>

<span data-ttu-id="d6ad3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6ad3-120">-Job</span><span class="sxs-lookup"><span data-stu-id="d6ad3-120">-Job</span></span>

<span data-ttu-id="d6ad3-121">A beolvasás feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-121">Specifies the job to get.</span></span>
<span data-ttu-id="d6ad3-122">Ha **BackupJob** objektumot szeretne beolvasni, használja a **Get-AzRecoveryServicesBackupJob** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="d6ad3-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="d6ad3-123">-JobId</span></span>

<span data-ttu-id="d6ad3-124">A biztonságimásolat-feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="d6ad3-125">Az azonosító a **Microsoft. Azure. commands. RecoveryServices. backup. parancsmags. models. JobBase** objektum JobId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="d6ad3-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d6ad3-126">-VaultId</span></span>

<span data-ttu-id="d6ad3-127">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="d6ad3-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d6ad3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ad3-128">CommonParameters</span></span>
<span data-ttu-id="d6ad3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6ad3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ad3-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6ad3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ad3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6ad3-131">INPUTS</span></span>

### <span data-ttu-id="d6ad3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d6ad3-132">System.String</span></span>

## <span data-ttu-id="d6ad3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6ad3-133">OUTPUTS</span></span>

### <span data-ttu-id="d6ad3-134">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d6ad3-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d6ad3-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6ad3-135">NOTES</span></span>

## <span data-ttu-id="d6ad3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6ad3-136">RELATED LINKS</span></span>

[<span data-ttu-id="d6ad3-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d6ad3-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
