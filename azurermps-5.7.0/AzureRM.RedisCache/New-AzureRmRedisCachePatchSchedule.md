---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 5c4375b4bb325877ec0520e0641496e8adfafec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492205"
---
# <span data-ttu-id="7fb02-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb02-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="7fb02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7fb02-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb02-103">Egy javítócsomag-ütemezést ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="7fb02-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fb02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7fb02-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb02-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7fb02-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb02-106">A **New-AzureRmRedisCachePatchSchedule** parancsmag az Azure Redis-gyorsítótárban lévő gyorsítótárba helyezi a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="7fb02-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="7fb02-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7fb02-107">EXAMPLES</span></span>

### <span data-ttu-id="7fb02-108">1. példa: a javítás ütemezésének létrehozása és hozzáadása a gyorsítótárban</span><span class="sxs-lookup"><span data-stu-id="7fb02-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="7fb02-109">A parancs hozzáadja a javítás ütemezését a RedisCache06 nevű gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="7fb02-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="7fb02-110">A Entries paraméter az a érték, amely a **New-AzureRmRedisCacheScheduleEntry-** t használja az ütemterv létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7fb02-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="7fb02-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7fb02-111">PARAMETERS</span></span>

### <span data-ttu-id="7fb02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb02-112">-DefaultProfile</span></span>
<span data-ttu-id="7fb02-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fb02-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fb02-114">-Bejegyzések</span><span class="sxs-lookup"><span data-stu-id="7fb02-114">-Entries</span></span>
<span data-ttu-id="7fb02-115">Az ütemtervek egy olyan tömbjét adja meg, amelyet a parancsmag a gyorsítótárban ad meg.</span><span class="sxs-lookup"><span data-stu-id="7fb02-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="7fb02-116">**PSScheduleEntry** objektum beolvasásához használja az New-AzureRmRedisCacheScheduleEntry parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7fb02-116">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb02-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7fb02-117">-Name</span></span>
<span data-ttu-id="7fb02-118">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7fb02-118">Specifies the name of the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb02-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb02-119">-ResourceGroupName</span></span>
<span data-ttu-id="7fb02-120">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7fb02-120">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb02-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7fb02-121">-Confirm</span></span>
<span data-ttu-id="7fb02-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7fb02-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb02-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb02-123">-WhatIf</span></span>
<span data-ttu-id="7fb02-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7fb02-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fb02-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7fb02-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb02-126">CommonParameters</span></span>
<span data-ttu-id="7fb02-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7fb02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb02-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb02-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb02-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fb02-129">INPUTS</span></span>

### <span data-ttu-id="7fb02-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="7fb02-130">None</span></span>
<span data-ttu-id="7fb02-131">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="7fb02-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="7fb02-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fb02-132">OUTPUTS</span></span>

### <span data-ttu-id="7fb02-133">Microsoft. Azure. Command. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="7fb02-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="7fb02-134">Ez a parancsmag a gyorsítótárban beállított javítócsomag-ütemezési bejegyzéseket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7fb02-134">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="7fb02-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7fb02-135">NOTES</span></span>
* <span data-ttu-id="7fb02-136">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="7fb02-136">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="7fb02-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fb02-137">RELATED LINKS</span></span>

[<span data-ttu-id="7fb02-138">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb02-138">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="7fb02-139">Új – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="7fb02-139">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="7fb02-140">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7fb02-140">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


