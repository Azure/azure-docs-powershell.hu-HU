---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015773"
---
# <span data-ttu-id="cd9aa-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="cd9aa-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="cd9aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd9aa-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9aa-103">Elindítja az áttelepítési terv létrehozását.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-103">Starts the creation of a migration plan.</span></span>

## <span data-ttu-id="cd9aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd9aa-104">SYNTAX</span></span>

### <span data-ttu-id="cd9aa-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="cd9aa-105">MigrateSpecificContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cd9aa-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="cd9aa-106">MigrateAllContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cd9aa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd9aa-107">DESCRIPTION</span></span>
<span data-ttu-id="cd9aa-108">A **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** parancsmag az áttelepítési terv létrehozását indítja el.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-108">The **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet starts the creation of a migration plan.</span></span>
<span data-ttu-id="cd9aa-109">Az áttelepítési terv létrehozása aszinkron.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-109">The creation of a migration plan is asynchronous.</span></span>
<span data-ttu-id="cd9aa-110">Az áttelepítési terv állapotának megtekintéséhez használja a **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-110">To see the status of the migration plan, use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet.</span></span>

## <span data-ttu-id="cd9aa-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cd9aa-111">EXAMPLES</span></span>

### <span data-ttu-id="cd9aa-112">1. példa: áttelepítési terv indítása</span><span class="sxs-lookup"><span data-stu-id="cd9aa-112">Example 1: Start a migration plan</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="cd9aa-113">Ez a parancs elindítja a OneSDKAzureCloud nevű régi tároló áttelepítési tervének létrehozását.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-113">This command starts creation of a migration plan for the legacy container named OneSDKAzureCloud.</span></span>
<span data-ttu-id="cd9aa-114">A parancs a terv állapotára vonatkozó üzenetet ad eredményül, és a **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** parancsmagot a naprakész adatokhoz használja.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-114">The command returns a message about the status of the plan, and to use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet for up to date information.</span></span>

### <span data-ttu-id="cd9aa-115">2. példa: az áttelepítési terv elindítása az összes mennyiségi tárolóban</span><span class="sxs-lookup"><span data-stu-id="cd9aa-115">Example 2: Start migration plan for all volume containers</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="cd9aa-116">Ez a parancs elindítja az áttelepítési terv létrehozását az összes örökölt kötet-tároló számára az importált konfigurációs fájlban.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-116">This command starts creation of migration plan for all legacy volume containers in the configuration file that is imported.</span></span>

## <span data-ttu-id="cd9aa-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd9aa-117">PARAMETERS</span></span>

### <span data-ttu-id="cd9aa-118">-All (mind)</span><span class="sxs-lookup"><span data-stu-id="cd9aa-118">-All</span></span>
<span data-ttu-id="cd9aa-119">Azt jelzi, hogy a parancsmag az importált konfigurációs fájlban az összes mennyiségi tárolóra vonatkozóan elindítja az áttelepítés időpontját.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-119">Indicates that this cmdlet starts migration time estimates for all volume containers in the imported configuration file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9aa-120">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="cd9aa-120">-LegacyConfigId</span></span>
<span data-ttu-id="cd9aa-121">A régi készülék konfigurációjának egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-121">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="cd9aa-122">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="cd9aa-122">-LegacyContainerNames</span></span>
<span data-ttu-id="cd9aa-123">A kötet-tárolók neveinek tömbjét adja meg, amelybe áttelepítési tervet szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-123">Specifies an array of volume container names for which to create a migration plan.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9aa-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="cd9aa-124">-Profile</span></span>
<span data-ttu-id="cd9aa-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd9aa-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd9aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9aa-127">CommonParameters</span></span>
<span data-ttu-id="cd9aa-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd9aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9aa-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9aa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9aa-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd9aa-130">INPUTS</span></span>

### <span data-ttu-id="cd9aa-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="cd9aa-131">None</span></span>

## <span data-ttu-id="cd9aa-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd9aa-132">OUTPUTS</span></span>

### <span data-ttu-id="cd9aa-133">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="cd9aa-133">String</span></span>
<span data-ttu-id="cd9aa-134">Ez a parancsmag az áttelepítési terv feladatának állapotát számítja ki, ha az a készüléken sikeresen elindult.</span><span class="sxs-lookup"><span data-stu-id="cd9aa-134">This cmdlet returns the status of the migration plan job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="cd9aa-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd9aa-135">NOTES</span></span>

## <span data-ttu-id="cd9aa-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd9aa-136">RELATED LINKS</span></span>

[<span data-ttu-id="cd9aa-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="cd9aa-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


