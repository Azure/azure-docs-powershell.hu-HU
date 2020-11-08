---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016258"
---
# <span data-ttu-id="0ba0c-101">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="0ba0c-101">Import-AzureStorSimpleLegacyVolumeContainer</span></span>

## <span data-ttu-id="0ba0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ba0c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba0c-103">Elindítja a kötet-tárolók áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-103">Starts the migration of volume containers.</span></span>

## <span data-ttu-id="0ba0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ba0c-104">SYNTAX</span></span>

### <span data-ttu-id="0ba0c-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="0ba0c-105">MigrateSpecificContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0ba0c-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="0ba0c-106">MigrateAllContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ba0c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ba0c-107">DESCRIPTION</span></span>
<span data-ttu-id="0ba0c-108">Az **import-AzureStorSimpleLegacyVolumeContainer** parancsmag a kötet-tárolók áttelepítését egy régi készülékről a cél készülékre indítja.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-108">The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.</span></span>

## <span data-ttu-id="0ba0c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0ba0c-109">EXAMPLES</span></span>

### <span data-ttu-id="0ba0c-110">1. példa: örökölt kötet-tároló importálása</span><span class="sxs-lookup"><span data-stu-id="0ba0c-110">Example 1: Import a legacy volume container</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="0ba0c-111">A parancs a megnevezett tároló örökölt kötet tárolóját importálja.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-111">This command imports a legacy volume container for the named container.</span></span>
<span data-ttu-id="0ba0c-112">A parancsmag elindítja az importálást, majd egy üzenetet ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-112">The cmdlet starts the import, and then returns a message.</span></span>

### <span data-ttu-id="0ba0c-113">2. példa: az összes régi mennyiségi tároló importálása</span><span class="sxs-lookup"><span data-stu-id="0ba0c-113">Example 2: Import all legacy volume containers</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="0ba0c-114">Ezzel a paranccsal importálhatja az összes örökölt mennyiségi tárolót a konfigurációs fájlból.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-114">This command imports all legacy volume containers from configuration file imported.</span></span>
<span data-ttu-id="0ba0c-115">A parancsmag elindítja az importálást, majd egy üzenetet ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-115">The cmdlet starts the import, and then returns a message.</span></span>

## <span data-ttu-id="0ba0c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ba0c-116">PARAMETERS</span></span>

### <span data-ttu-id="0ba0c-117">-All (mind)</span><span class="sxs-lookup"><span data-stu-id="0ba0c-117">-All</span></span>
<span data-ttu-id="0ba0c-118">Jelzi, hogy ez a parancsmag az importált konfigurációs fájlban lévő összes mennyiségi tárolót importálja a céleszköz.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-118">Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.</span></span>

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

### <span data-ttu-id="0ba0c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0ba0c-119">-Force</span></span>
<span data-ttu-id="0ba0c-120">Jelzi, hogy ez a parancsmag mennyiségi tárolót importál egy másik eszközre, még akkor is, ha a kötet tárolóját egy másik eszközön importálta.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-120">Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ba0c-121">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="0ba0c-121">-LegacyConfigId</span></span>
<span data-ttu-id="0ba0c-122">A régi készülék konfigurációjának egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-122">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="0ba0c-123">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="0ba0c-123">-LegacyContainerNames</span></span>
<span data-ttu-id="0ba0c-124">Az áttelepítési terv által érintett mennyiségi tárolók neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-124">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="0ba0c-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="0ba0c-125">-Profile</span></span>
<span data-ttu-id="0ba0c-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ba0c-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ba0c-128">-SkipACRs</span><span class="sxs-lookup"><span data-stu-id="0ba0c-128">-SkipACRs</span></span>
<span data-ttu-id="0ba0c-129">Jelzi, hogy az importálási folyamat kihagyja a hozzáférés-vezérlési rekordokat az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-129">Indicates that the import process skips access control records for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ba0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba0c-130">CommonParameters</span></span>
<span data-ttu-id="0ba0c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ba0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba0c-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ba0c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba0c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ba0c-133">INPUTS</span></span>

## <span data-ttu-id="0ba0c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ba0c-134">OUTPUTS</span></span>

### <span data-ttu-id="0ba0c-135">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="0ba0c-135">String</span></span>
<span data-ttu-id="0ba0c-136">Ez a parancs az áttelepítési mennyiség tárolójának állapotát jeleníti meg, ha az sikeresen elindult a készüléken.</span><span class="sxs-lookup"><span data-stu-id="0ba0c-136">This command returns the status of the migration import volume container job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="0ba0c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ba0c-137">NOTES</span></span>

## <span data-ttu-id="0ba0c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ba0c-138">RELATED LINKS</span></span>

[<span data-ttu-id="0ba0c-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="0ba0c-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="0ba0c-140">Importálás – AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="0ba0c-140">Import-AzureStorSimpleLegacyApplianceConfig</span></span>](./Import-AzureStorSimpleLegacyApplianceConfig.md)


