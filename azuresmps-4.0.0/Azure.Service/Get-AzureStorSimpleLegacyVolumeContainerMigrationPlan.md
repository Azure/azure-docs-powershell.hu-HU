---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015556"
---
# <span data-ttu-id="dea92-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="dea92-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="dea92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dea92-102">SYNOPSIS</span></span>
<span data-ttu-id="dea92-103">A régebbi tárolók áttelepítési terveit kapja.</span><span class="sxs-lookup"><span data-stu-id="dea92-103">Gets migration plans for legacy containers.</span></span>

## <span data-ttu-id="dea92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dea92-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dea92-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dea92-105">DESCRIPTION</span></span>
<span data-ttu-id="dea92-106">A **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** parancsmag a régi tárolók áttelepítési terveit kapja.</span><span class="sxs-lookup"><span data-stu-id="dea92-106">The **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet gets migration plans for legacy containers.</span></span>
<span data-ttu-id="dea92-107">Adja meg az áttelepítési tervet a régi konfiguráció AZONOSÍTÓjának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="dea92-107">Specify a migration plan by its legacy configuration ID.</span></span>
<span data-ttu-id="dea92-108">Ha az áttelepítési terv még folyamatban van, ez a parancsmag az áttelepítési terv állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dea92-108">If creation of the migration plan is still in progress, this cmdlet gets the status of the migration plan.</span></span>
<span data-ttu-id="dea92-109">Ha az áttelepítési terv befejeződött, ez a parancsmag a régi tárolók készletének tényleges áttelepítési tervét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="dea92-109">If the migration plan is completed, this cmdlet returns the actual migration plan for the set of legacy containers.</span></span>
<span data-ttu-id="dea92-110">Ha nem adja meg a *LegacyConfigId* paramétert, ez a parancsmag a konfigurációs azonosítók listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="dea92-110">If you do not specify the *LegacyConfigId* parameter, this cmdlet returns a list of configuration IDs.</span></span>

## <span data-ttu-id="dea92-111">Példák</span><span class="sxs-lookup"><span data-stu-id="dea92-111">EXAMPLES</span></span>

### <span data-ttu-id="dea92-112">Példa 1: a terv állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="dea92-112">Example 1: Get the status of a plan</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

<span data-ttu-id="dea92-113">Ez a parancs megkapja az áttelepítési terv állapotát.</span><span class="sxs-lookup"><span data-stu-id="dea92-113">This command gets the status of the migration plan.</span></span>
<span data-ttu-id="dea92-114">Az állapot a feltételezett sávszélességet, a becsült időt és a kapcsolódó információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dea92-114">The status includes assumed bandwidth, estimated time and, related information.</span></span>

### <span data-ttu-id="dea92-115">2. példa: meglévő csomagok azonosítóinak beolvasása</span><span class="sxs-lookup"><span data-stu-id="dea92-115">Example 2: Get the IDs of existing plans</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

<span data-ttu-id="dea92-116">Ez a parancs az áttelepítési tervek minden konfigurációs azonosítóját megkapja.</span><span class="sxs-lookup"><span data-stu-id="dea92-116">This command gets all the configuration IDs of migration plans.</span></span>

## <span data-ttu-id="dea92-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dea92-117">PARAMETERS</span></span>

### <span data-ttu-id="dea92-118">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="dea92-118">-LegacyConfigId</span></span>
<span data-ttu-id="dea92-119">A régi készülék konfigurációjának egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dea92-119">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea92-120">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="dea92-120">-LegacyContainerNames</span></span>
<span data-ttu-id="dea92-121">A kötet-tárolók azon neveinek tömbje, amelyekhez ez a parancsmag áttelepítési tervet kap.</span><span class="sxs-lookup"><span data-stu-id="dea92-121">Specifies an array of volume container names for which this cmdlet gets a migration plan.</span></span>

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

### <span data-ttu-id="dea92-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="dea92-122">-Profile</span></span>
<span data-ttu-id="dea92-123">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="dea92-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="dea92-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea92-124">CommonParameters</span></span>
<span data-ttu-id="dea92-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dea92-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea92-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dea92-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea92-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dea92-127">INPUTS</span></span>

### <span data-ttu-id="dea92-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="dea92-128">None</span></span>

## <span data-ttu-id="dea92-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dea92-129">OUTPUTS</span></span>

### <span data-ttu-id="dea92-130">MigrationPlanMsg</span><span class="sxs-lookup"><span data-stu-id="dea92-130">MigrationPlanMsg</span></span>
<span data-ttu-id="dea92-131">Ez a parancsmag egy olyan **MigrationPlanMsg** -objektumot ad eredményül, amely az áttelepítési terv feladatának állapotát tartalmazza, a sávszélességet a másodpercenként megabitben, a becsült időt percekben jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="dea92-131">This cmdlet returns a **MigrationPlanMsg** object that contains the status of the migration plan job, assumed bandwidth in megabits per second, and estimated time in minutes.</span></span>

## <span data-ttu-id="dea92-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dea92-132">NOTES</span></span>

## <span data-ttu-id="dea92-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dea92-133">RELATED LINKS</span></span>

[<span data-ttu-id="dea92-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="dea92-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


