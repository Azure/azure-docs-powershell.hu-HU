---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: f38029a85cac1b6771a546b120714823f5b02927
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669704"
---
# <span data-ttu-id="d48d6-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="d48d6-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="d48d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d48d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d48d6-103">Megkeresi a biztonsági mentési feladatok részleteit.</span><span class="sxs-lookup"><span data-stu-id="d48d6-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="d48d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d48d6-104">SYNTAX</span></span>

### <span data-ttu-id="d48d6-105">JobFilterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d48d6-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d48d6-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="d48d6-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d48d6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d48d6-107">DESCRIPTION</span></span>
<span data-ttu-id="d48d6-108">A **Get-AzRecoveryServicesBackupJobDetail** parancsmag az Azure Backup Job részleteit kapja meg egy adott feladathoz.</span><span class="sxs-lookup"><span data-stu-id="d48d6-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="d48d6-109">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="d48d6-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d48d6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d48d6-110">EXAMPLES</span></span>

### <span data-ttu-id="d48d6-111">Példa 1: a sikertelen feladatok biztonsági mentési feladatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="d48d6-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="d48d6-112">Az első parancs a boltozat során sikertelen feladatok tömbjét kapja, majd a $Jobs tömbben tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="d48d6-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="d48d6-113">A második parancs beolvassa a $Jobs sikertelen munkafolyamatok adatait, majd a $JobDetails változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="d48d6-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="d48d6-114">A végleges parancs a hibás feladatok részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="d48d6-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="d48d6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d48d6-115">PARAMETERS</span></span>

### <span data-ttu-id="d48d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d48d6-116">-DefaultProfile</span></span>
<span data-ttu-id="d48d6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d48d6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d48d6-118">-Job</span><span class="sxs-lookup"><span data-stu-id="d48d6-118">-Job</span></span>
<span data-ttu-id="d48d6-119">A beolvasás feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d48d6-119">Specifies the job to get.</span></span>
<span data-ttu-id="d48d6-120">**BackupJob** objektum beolvasásához használja az Get-AzRecoveryServicesBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d48d6-120">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="d48d6-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="d48d6-121">-JobId</span></span>
<span data-ttu-id="d48d6-122">A biztonságimásolat-feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d48d6-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="d48d6-123">Az azonosító a **BackupJob** -objektum InstanceId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="d48d6-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="d48d6-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d48d6-124">-VaultId</span></span>
<span data-ttu-id="d48d6-125">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="d48d6-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d48d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d48d6-126">CommonParameters</span></span>
<span data-ttu-id="d48d6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d48d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d48d6-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d48d6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d48d6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d48d6-129">INPUTS</span></span>

### <span data-ttu-id="d48d6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d48d6-130">System.String</span></span>

## <span data-ttu-id="d48d6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d48d6-131">OUTPUTS</span></span>

### <span data-ttu-id="d48d6-132">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d48d6-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d48d6-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d48d6-133">NOTES</span></span>

## <span data-ttu-id="d48d6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d48d6-134">RELATED LINKS</span></span>

[<span data-ttu-id="d48d6-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d48d6-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)


