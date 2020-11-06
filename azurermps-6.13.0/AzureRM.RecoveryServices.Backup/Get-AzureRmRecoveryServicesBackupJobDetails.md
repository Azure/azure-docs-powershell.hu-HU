---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 7d39ce49a76d8519f2eacf0649c52051290274f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492798"
---
# <span data-ttu-id="6b863-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="6b863-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="6b863-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b863-102">SYNOPSIS</span></span>
<span data-ttu-id="6b863-103">Megkeresi a biztonsági mentési feladatok részleteit.</span><span class="sxs-lookup"><span data-stu-id="6b863-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b863-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b863-104">SYNTAX</span></span>

### <span data-ttu-id="6b863-105">JobFilterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b863-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b863-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="6b863-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b863-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b863-107">DESCRIPTION</span></span>
<span data-ttu-id="6b863-108">A **Get-AzureRmRecoveryServicesBackupJobDetails** parancsmag az Azure Backup Job részleteit kapja meg egy adott feladathoz.</span><span class="sxs-lookup"><span data-stu-id="6b863-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="6b863-109">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="6b863-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6b863-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6b863-110">EXAMPLES</span></span>

### <span data-ttu-id="6b863-111">Példa 1: a sikertelen feladatok biztonsági mentési feladatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="6b863-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="6b863-112">Az első parancs a boltozat során sikertelen feladatok tömbjét kapja, majd a $Jobs tömbben tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="6b863-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="6b863-113">A második parancs beolvassa a $Jobs sikertelen munkafolyamatok adatait, majd a $JobDetails változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="6b863-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="6b863-114">A végleges parancs a hibás feladatok részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="6b863-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="6b863-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b863-115">PARAMETERS</span></span>

### <span data-ttu-id="6b863-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b863-116">-DefaultProfile</span></span>
<span data-ttu-id="6b863-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b863-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b863-118">-Job</span><span class="sxs-lookup"><span data-stu-id="6b863-118">-Job</span></span>
<span data-ttu-id="6b863-119">A beolvasás feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b863-119">Specifies the job to get.</span></span>
<span data-ttu-id="6b863-120">**BackupJob** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6b863-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="6b863-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="6b863-121">-JobId</span></span>
<span data-ttu-id="6b863-122">A biztonságimásolat-feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b863-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="6b863-123">Az azonosító a **BackupJob** -objektum InstanceId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="6b863-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="6b863-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6b863-124">-VaultId</span></span>
<span data-ttu-id="6b863-125">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="6b863-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6b863-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b863-126">CommonParameters</span></span>
<span data-ttu-id="6b863-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b863-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b863-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b863-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b863-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b863-129">INPUTS</span></span>

### <span data-ttu-id="6b863-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6b863-130">System.String</span></span>
<span data-ttu-id="6b863-131">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b863-131">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="6b863-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b863-132">OUTPUTS</span></span>

### <span data-ttu-id="6b863-133">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="6b863-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6b863-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b863-134">NOTES</span></span>

## <span data-ttu-id="6b863-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b863-135">RELATED LINKS</span></span>

[<span data-ttu-id="6b863-136">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b863-136">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


