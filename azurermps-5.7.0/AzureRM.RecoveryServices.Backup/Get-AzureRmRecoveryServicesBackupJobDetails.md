---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493075"
---
# <span data-ttu-id="81b34-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="81b34-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="81b34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81b34-102">SYNOPSIS</span></span>
<span data-ttu-id="81b34-103">Megkeresi a biztonsági mentési feladatok részleteit.</span><span class="sxs-lookup"><span data-stu-id="81b34-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81b34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81b34-104">SYNTAX</span></span>

### <span data-ttu-id="81b34-105">JobFilterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81b34-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81b34-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="81b34-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81b34-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="81b34-107">DESCRIPTION</span></span>
<span data-ttu-id="81b34-108">A **Get-AzureRmRecoveryServicesBackupJobDetails** parancsmag az Azure Backup Job részleteit kapja meg egy adott feladathoz.</span><span class="sxs-lookup"><span data-stu-id="81b34-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="81b34-109">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="81b34-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="81b34-110">Példák</span><span class="sxs-lookup"><span data-stu-id="81b34-110">EXAMPLES</span></span>

### <span data-ttu-id="81b34-111">Példa 1: a sikertelen feladatok biztonsági mentési feladatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="81b34-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="81b34-112">Az első parancs a boltozat során sikertelen feladatok tömbjét kapja, majd a $Jobs tömbben tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="81b34-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="81b34-113">A második parancs beolvassa a $Jobs sikertelen munkafolyamatok adatait, majd a $JobDetails változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="81b34-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="81b34-114">A végleges parancs a hibás feladatok részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="81b34-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="81b34-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81b34-115">PARAMETERS</span></span>

### <span data-ttu-id="81b34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b34-116">-DefaultProfile</span></span>
<span data-ttu-id="81b34-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81b34-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81b34-118">-Job</span><span class="sxs-lookup"><span data-stu-id="81b34-118">-Job</span></span>
<span data-ttu-id="81b34-119">A beolvasás feladatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="81b34-119">Specifies the job to get.</span></span>
<span data-ttu-id="81b34-120">**BackupJob** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="81b34-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="81b34-121">-JobId</span></span>
<span data-ttu-id="81b34-122">A biztonságimásolat-feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="81b34-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="81b34-123">Az azonosító a **BackupJob** -objektum InstanceId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="81b34-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b34-124">CommonParameters</span></span>
<span data-ttu-id="81b34-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81b34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b34-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b34-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b34-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81b34-127">INPUTS</span></span>

### <span data-ttu-id="81b34-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="81b34-128">None</span></span>
<span data-ttu-id="81b34-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="81b34-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="81b34-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81b34-130">OUTPUTS</span></span>

### <span data-ttu-id="81b34-131">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="81b34-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="81b34-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81b34-132">NOTES</span></span>

## <span data-ttu-id="81b34-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81b34-133">RELATED LINKS</span></span>

[<span data-ttu-id="81b34-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="81b34-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


