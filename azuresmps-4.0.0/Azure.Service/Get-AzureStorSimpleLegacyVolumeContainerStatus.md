---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A736738A-C6B3-4E5A-B9BA-D6559A27A667
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95e604c6c3f6766ccfc89bd9018dbe2241fb5b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016550"
---
# <span data-ttu-id="92a78-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="92a78-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="92a78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92a78-102">SYNOPSIS</span></span>
<span data-ttu-id="92a78-103">A kötet-tárolók áttelepítési állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="92a78-103">Gets the migration status of the volume containers.</span></span>

## <span data-ttu-id="92a78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92a78-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> [-LegacyContainerNames <String[]>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="92a78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="92a78-105">DESCRIPTION</span></span>
<span data-ttu-id="92a78-106">A **Get-AzureStorSimpleLegacyVolumeContainerStatus** parancsmag a mennyiségi tárolók áttelepítési állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="92a78-106">The **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet gets the migration status of the volume containers.</span></span>
<span data-ttu-id="92a78-107">Ez a parancsmag azokat az állapotadatokat jeleníti meg, amelyek azt jelzik, hogy a mennyiségi tároló áttelepítése továbbra is folyamatban, befejezett vagy sikertelen.</span><span class="sxs-lookup"><span data-stu-id="92a78-107">This cmdlet returns status information which includes whether the volume container migration is still in progress, completed, or failed.</span></span>

## <span data-ttu-id="92a78-108">Példák</span><span class="sxs-lookup"><span data-stu-id="92a78-108">EXAMPLES</span></span>

### <span data-ttu-id="92a78-109">Példa 1: sikertelen áttelepítés állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="92a78-109">Example 1: Get status for a failed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : No Cloud Configuration(s)  are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : Cloud Configuration Name: OneSDKAzureCloud
                       PercentageCompleted : 0
                       MigrationStatus : Failed
                       No Backup sets found
```

<span data-ttu-id="92a78-110">Ez a parancs beolvassa a régi nevű tároló áttelepítési állapotát.</span><span class="sxs-lookup"><span data-stu-id="92a78-110">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="92a78-111">Az eredmények azt mutatják, hogy az áttelepítés sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="92a78-111">The results show that the migration failed.</span></span>

### <span data-ttu-id="92a78-112">2. példa: állapot beszerzése folyamatban lévő áttelepítés esetén</span><span class="sxs-lookup"><span data-stu-id="92a78-112">Example 2: Get status for a migration in progress</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : CloudConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 10
                       MigrationStatus : InProgress
                       BackupSets : 
                           Policy : OneSDKBackupPolicy, Status : InProgress
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="92a78-113">Ez a parancs beolvassa a régi nevű tároló áttelepítési állapotát.</span><span class="sxs-lookup"><span data-stu-id="92a78-113">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="92a78-114">Az eredmények azt mutatják, hogy az áttelepítés folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="92a78-114">The results show that the migration is in progress.</span></span>

### <span data-ttu-id="92a78-115">3. példa: befejezett áttelepítés állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="92a78-115">Example 3: Get status for a completed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4 -LegacyContainerNames OneSDKAzureCloud
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : Cloud ConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 100
                       MigrationStatus : Completed
                       BackupSets : 
                          Policy : vg1p1, Created On : 04/06/2015 11:22:00, Status : Completed
                          Policy : vg1p1, Created On : 03/30/2015 11:22:00, Status : Completed
                          Policy : c1v1-Auto-Daily-CloudSnapshot, Created On : 03/30/2015 03:30:00, Status : Completed
MigrationInprogress  : No Cloud Configuration(s) are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="92a78-116">Ez a parancs beolvassa a régi nevű tároló áttelepítési állapotát.</span><span class="sxs-lookup"><span data-stu-id="92a78-116">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="92a78-117">Az eredmények azt mutatják, hogy az áttelepítés befejeződött.</span><span class="sxs-lookup"><span data-stu-id="92a78-117">The results show that the migration is completed.</span></span>

## <span data-ttu-id="92a78-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92a78-118">PARAMETERS</span></span>

### <span data-ttu-id="92a78-119">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="92a78-119">-LegacyConfigId</span></span>
<span data-ttu-id="92a78-120">A régi készülék konfigurációjának egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="92a78-120">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a78-121">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="92a78-121">-LegacyContainerNames</span></span>
<span data-ttu-id="92a78-122">Az áttelepítési terv által érintett mennyiségi tárolók neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92a78-122">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a78-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="92a78-123">-Profile</span></span>
<span data-ttu-id="92a78-124">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="92a78-124">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a78-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a78-125">CommonParameters</span></span>
<span data-ttu-id="92a78-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92a78-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a78-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92a78-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a78-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92a78-128">INPUTS</span></span>

## <span data-ttu-id="92a78-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92a78-129">OUTPUTS</span></span>

## <span data-ttu-id="92a78-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92a78-130">NOTES</span></span>

## <span data-ttu-id="92a78-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92a78-131">RELATED LINKS</span></span>

[<span data-ttu-id="92a78-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="92a78-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="92a78-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="92a78-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)


