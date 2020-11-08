---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 81c1aeded9b4bb40998448d61a5edbf35742bfcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010887"
---
# <span data-ttu-id="04398-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="04398-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="04398-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04398-102">SYNOPSIS</span></span>

<span data-ttu-id="04398-103">Megkeresi a biztonsági mentési feladatok részleteit.</span><span class="sxs-lookup"><span data-stu-id="04398-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="04398-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04398-104">SYNTAX</span></span>

### <span data-ttu-id="04398-105">JobFilterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04398-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04398-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="04398-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04398-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="04398-107">DESCRIPTION</span></span>

<span data-ttu-id="04398-108">A **Get-AzRecoveryServicesBackupJobDetail** parancsmag az Azure Backup Job részleteit kapja meg egy adott feladathoz.</span><span class="sxs-lookup"><span data-stu-id="04398-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="04398-109">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="04398-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="04398-110">Figyelmeztetés: a **Get-AzRecoveryServicesBackupJobDetails** alias törlődni fog egy jövőbeli változtatási kiadásban.</span><span class="sxs-lookup"><span data-stu-id="04398-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="04398-111">Példák</span><span class="sxs-lookup"><span data-stu-id="04398-111">EXAMPLES</span></span>

### <span data-ttu-id="04398-112">Példa 1: a sikertelen feladatok biztonsági mentési feladatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="04398-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="04398-113">Az első parancs a boltozat során sikertelen feladatok tömbjét kapja, majd a $Jobs tömbben tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="04398-113">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="04398-114">A második parancs beolvassa a $Jobs sikertelen munkafolyamatok adatait, majd a $JobDetails változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="04398-114">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="04398-115">A végleges parancs a hibás feladatok részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="04398-115">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="04398-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04398-116">PARAMETERS</span></span>

### <span data-ttu-id="04398-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04398-117">-DefaultProfile</span></span>

<span data-ttu-id="04398-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04398-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04398-119">-Job</span><span class="sxs-lookup"><span data-stu-id="04398-119">-Job</span></span>

<span data-ttu-id="04398-120">A beolvasás feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="04398-120">Specifies the job to get.</span></span>
<span data-ttu-id="04398-121">Ha **BackupJob** objektumot szeretne beolvasni, használja a **Get-AzRecoveryServicesBackupJob** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="04398-121">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="04398-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="04398-122">-JobId</span></span>

<span data-ttu-id="04398-123">A biztonságimásolat-feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="04398-123">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="04398-124">Az azonosító a **Microsoft. Azure. commands. RecoveryServices. backup. parancsmags. models. JobBase** objektum JobId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="04398-124">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="04398-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="04398-125">-VaultId</span></span>

<span data-ttu-id="04398-126">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="04398-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="04398-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04398-127">CommonParameters</span></span>
<span data-ttu-id="04398-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04398-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04398-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="04398-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04398-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04398-130">INPUTS</span></span>

### <span data-ttu-id="04398-131">System. String</span><span class="sxs-lookup"><span data-stu-id="04398-131">System.String</span></span>

## <span data-ttu-id="04398-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04398-132">OUTPUTS</span></span>

### <span data-ttu-id="04398-133">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="04398-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="04398-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04398-134">NOTES</span></span>

## <span data-ttu-id="04398-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04398-135">RELATED LINKS</span></span>

[<span data-ttu-id="04398-136">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="04398-136">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
