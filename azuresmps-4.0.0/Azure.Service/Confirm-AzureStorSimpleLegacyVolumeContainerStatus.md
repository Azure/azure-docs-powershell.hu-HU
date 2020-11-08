---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015700"
---
# <span data-ttu-id="a46a4-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="a46a4-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="a46a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a46a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a46a4-103">Kezdeményezi az áttelepített kötet-tárolók véglegesítését vagy visszagörgetését.</span><span class="sxs-lookup"><span data-stu-id="a46a4-103">Initiates the commit or rollback of the volume containers that are migrated.</span></span>

## <span data-ttu-id="a46a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a46a4-104">SYNTAX</span></span>

### <span data-ttu-id="a46a4-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="a46a4-105">MigrateSpecificContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a46a4-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="a46a4-106">MigrateAllContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a46a4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a46a4-107">DESCRIPTION</span></span>
<span data-ttu-id="a46a4-108">A **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** parancsmag a régi áttelepítés részeként áttelepített mennyiségi tárolók véglegesítését vagy visszagörgetését kezdeményezi.</span><span class="sxs-lookup"><span data-stu-id="a46a4-108">The **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet initiates the commit or rollback of the volume containers that are migrated as part of a legacy migration.</span></span>
<span data-ttu-id="a46a4-109">A visszagörgetés visszaállítja a készülék eredeti tulajdonjogát.</span><span class="sxs-lookup"><span data-stu-id="a46a4-109">The rollback restores the appliance to the original ownership.</span></span>
<span data-ttu-id="a46a4-110">A véglegesítés a tulajdonost a cél készülékhez rendeli.</span><span class="sxs-lookup"><span data-stu-id="a46a4-110">The commit assigns the ownership to the target appliance.</span></span>

## <span data-ttu-id="a46a4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a46a4-111">EXAMPLES</span></span>

### <span data-ttu-id="a46a4-112">Példa 1: véglegesítési művelet kezdeményezése meghatározott mennyiségi tárolón</span><span class="sxs-lookup"><span data-stu-id="a46a4-112">Example 1: Initiate a commit operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="a46a4-113">A parancs véglegesítési műveletet kezdeményez a megadott mennyiségi tárolón a megadott örökölt konfiguráció-AZONOSÍTÓhoz.</span><span class="sxs-lookup"><span data-stu-id="a46a4-113">This command initiates a commit operation on the specified volume container for the specified legacy configuration ID.</span></span>
<span data-ttu-id="a46a4-114">A művelet állapotának megtekintéséhez használja a **Get-AzureStorSimpleLegacyVolumeContainerStatus** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a46a4-114">To see the status of the operation, use the **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet.</span></span>

### <span data-ttu-id="a46a4-115">2. példa: visszagörgetési művelet kezdeményezése adott mennyiségi tárolón</span><span class="sxs-lookup"><span data-stu-id="a46a4-115">Example 2: Initiate a rollback operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="a46a4-116">Ez a parancs visszagörgetési műveletet kezdeményezett a megadott kötet-tárolóban a megadott örökölt konfiguráció-AZONOSÍTÓhoz.</span><span class="sxs-lookup"><span data-stu-id="a46a4-116">This command initiates a rollback operation on the specified volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="a46a4-117">3. példa: véglegesítési művelet kezdeményezése az összes mennyiségi tárolón</span><span class="sxs-lookup"><span data-stu-id="a46a4-117">Example 3: Initiate a commit operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="a46a4-118">Ez a parancs véglegesítési műveletet kezdeményez a megadott örökölt konfigurációs AZONOSÍTÓhoz tartozó összes mennyiségi tárolóban.</span><span class="sxs-lookup"><span data-stu-id="a46a4-118">This command initiates a commit operation on all volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="a46a4-119">Példa 4: visszagörgetési művelet kezdeményezése az összes mennyiségi tárolón</span><span class="sxs-lookup"><span data-stu-id="a46a4-119">Example 4: Initiate a rollback operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="a46a4-120">Ez a parancs a megadott örökölt konfigurációs AZONOSÍTÓhoz tartozó összes mennyiségi tárolóban visszagörgetési műveletet kezdeményez.</span><span class="sxs-lookup"><span data-stu-id="a46a4-120">This command initiates a rollback operation on all volume containers for the specified legacy configuration ID.</span></span>

## <span data-ttu-id="a46a4-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a46a4-121">PARAMETERS</span></span>

### <span data-ttu-id="a46a4-122">-All (mind)</span><span class="sxs-lookup"><span data-stu-id="a46a4-122">-All</span></span>
<span data-ttu-id="a46a4-123">Azt jelzi, hogy ez a parancsmag visszalépési vagy véglegesítési műveletet kezdeményez az importált konfigurációs fájlban lévő összes mennyiségi tárolóban.</span><span class="sxs-lookup"><span data-stu-id="a46a4-123">Indicates that this cmdlet initiates a roll back or commit operation on all volume containers in the imported configuration file.</span></span>

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

### <span data-ttu-id="a46a4-124">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="a46a4-124">-LegacyConfigId</span></span>
<span data-ttu-id="a46a4-125">A régi készülék konfigurációjának egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a46a4-125">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="a46a4-126">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="a46a4-126">-LegacyContainerNames</span></span>
<span data-ttu-id="a46a4-127">Az áttelepítési terv által érintett mennyiségi tárolók neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a46a4-127">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="a46a4-128">-MigrationOperation</span><span class="sxs-lookup"><span data-stu-id="a46a4-128">-MigrationOperation</span></span>
<span data-ttu-id="a46a4-129">Meghatározza, hogy a parancsmag végrehajt-e egy véglegesítést vagy visszagörgetést.</span><span class="sxs-lookup"><span data-stu-id="a46a4-129">Specifies whether this cmdlet performs a commit or rollback.</span></span>
<span data-ttu-id="a46a4-130">Az érvényes értékek a következők: véglegesítés és visszagörgetés.</span><span class="sxs-lookup"><span data-stu-id="a46a4-130">Valid values are: Commit and Rollback.</span></span>

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

### <span data-ttu-id="a46a4-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="a46a4-131">-Profile</span></span>
<span data-ttu-id="a46a4-132">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a46a4-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a46a4-133">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a46a4-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a46a4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46a4-134">CommonParameters</span></span>
<span data-ttu-id="a46a4-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a46a4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46a4-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a46a4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46a4-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a46a4-137">INPUTS</span></span>

## <span data-ttu-id="a46a4-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a46a4-138">OUTPUTS</span></span>

## <span data-ttu-id="a46a4-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a46a4-139">NOTES</span></span>

## <span data-ttu-id="a46a4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a46a4-140">RELATED LINKS</span></span>

[<span data-ttu-id="a46a4-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="a46a4-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="a46a4-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="a46a4-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[<span data-ttu-id="a46a4-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="a46a4-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


