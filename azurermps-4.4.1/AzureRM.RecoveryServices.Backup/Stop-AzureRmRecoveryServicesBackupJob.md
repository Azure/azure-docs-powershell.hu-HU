---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 63d90aa5f98f6710702a70e9609c7625626e34c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503991"
---
# <span data-ttu-id="804c1-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="804c1-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="804c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="804c1-102">SYNOPSIS</span></span>
<span data-ttu-id="804c1-103">Lemond egy futó feladatot.</span><span class="sxs-lookup"><span data-stu-id="804c1-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="804c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="804c1-104">SYNTAX</span></span>

### <span data-ttu-id="804c1-105">JobFilterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="804c1-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="804c1-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="804c1-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="804c1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="804c1-107">DESCRIPTION</span></span>
<span data-ttu-id="804c1-108">A **stop-AzureRmRecoveryServicesBackupJob** parancsmag lemond egy meglévő Azure biztonsági mentési feladatról.</span><span class="sxs-lookup"><span data-stu-id="804c1-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="804c1-109">Ezzel a parancsmaggal leállíthat egy olyan feladatot, amely túl hosszú időt vesz igénybe, és blokkolja az egyéb tevékenységeket.</span><span class="sxs-lookup"><span data-stu-id="804c1-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="804c1-110">Csak biztonsági mentési és visszaállítási munkatípusokat törölhet.</span><span class="sxs-lookup"><span data-stu-id="804c1-110">You can cancel only Backup and Restore job types.</span></span>

<span data-ttu-id="804c1-111">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="804c1-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="804c1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="804c1-112">EXAMPLES</span></span>

### <span data-ttu-id="804c1-113">Példa 1: biztonsági mentési feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="804c1-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="804c1-114">Az első parancs biztonsági mentési feladatot kap, majd a $Job változóban tárolja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="804c1-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>

<span data-ttu-id="804c1-115">Az utolsó parancs a feladatot a $Job biztonsági mentési feladat példány-AZONOSÍTÓjának megadásával szünteti meg.</span><span class="sxs-lookup"><span data-stu-id="804c1-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="804c1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="804c1-116">PARAMETERS</span></span>

### <span data-ttu-id="804c1-117">-Job</span><span class="sxs-lookup"><span data-stu-id="804c1-117">-Job</span></span>
<span data-ttu-id="804c1-118">A parancsmag által lemondott feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="804c1-118">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="804c1-119">**BackupJob** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="804c1-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="804c1-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="804c1-120">-JobId</span></span>
<span data-ttu-id="804c1-121">A lemondani kívánt feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="804c1-121">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="804c1-122">Az azonosító a **BackupJob** -objektum InstanceId tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="804c1-122">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="804c1-123">**BackupJob** -objektum beszerzéséhez használja a Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="804c1-123">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="804c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="804c1-124">-DefaultProfile</span></span>
<span data-ttu-id="804c1-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="804c1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="804c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804c1-126">CommonParameters</span></span>
<span data-ttu-id="804c1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="804c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804c1-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="804c1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804c1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="804c1-129">INPUTS</span></span>

## <span data-ttu-id="804c1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="804c1-130">OUTPUTS</span></span>

### <span data-ttu-id="804c1-131">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="804c1-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="804c1-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="804c1-132">NOTES</span></span>

## <span data-ttu-id="804c1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="804c1-133">RELATED LINKS</span></span>

[<span data-ttu-id="804c1-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="804c1-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="804c1-135">Várjon-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="804c1-135">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


