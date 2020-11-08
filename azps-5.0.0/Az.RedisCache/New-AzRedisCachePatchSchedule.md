---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 4215cf8450922a03f061abcc04022ee4e20950b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187678"
---
# <span data-ttu-id="46006-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="46006-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="46006-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46006-102">SYNOPSIS</span></span>
<span data-ttu-id="46006-103">Egy javítócsomag-ütemezést ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="46006-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="46006-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46006-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46006-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="46006-105">DESCRIPTION</span></span>
<span data-ttu-id="46006-106">A **New-AzRedisCachePatchSchedule** parancsmag az Azure Redis-gyorsítótárban lévő gyorsítótárba helyezi a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="46006-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="46006-107">Példák</span><span class="sxs-lookup"><span data-stu-id="46006-107">EXAMPLES</span></span>

### <span data-ttu-id="46006-108">1. példa: a javítás ütemezésének létrehozása és hozzáadása a gyorsítótárban</span><span class="sxs-lookup"><span data-stu-id="46006-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="46006-109">A parancs hozzáadja a javítás ütemezését a RedisCache06 nevű gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="46006-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="46006-110">A Entries paraméter az a érték, amely a **New-AzRedisCacheScheduleEntry-** t használja az ütemterv létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="46006-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="46006-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46006-111">PARAMETERS</span></span>

### <span data-ttu-id="46006-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46006-112">-DefaultProfile</span></span>
<span data-ttu-id="46006-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46006-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46006-114">-Bejegyzések</span><span class="sxs-lookup"><span data-stu-id="46006-114">-Entries</span></span>
<span data-ttu-id="46006-115">Az ütemtervek egy olyan tömbjét adja meg, amelyet a parancsmag a gyorsítótárban ad meg.</span><span class="sxs-lookup"><span data-stu-id="46006-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="46006-116">**PSScheduleEntry** objektum beolvasásához használja az New-AzRedisCacheScheduleEntry parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="46006-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46006-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46006-117">-Name</span></span>
<span data-ttu-id="46006-118">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46006-118">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46006-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46006-119">-ResourceGroupName</span></span>
<span data-ttu-id="46006-120">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46006-120">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46006-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46006-121">-Confirm</span></span>
<span data-ttu-id="46006-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46006-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46006-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46006-123">-WhatIf</span></span>
<span data-ttu-id="46006-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46006-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46006-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46006-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46006-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46006-126">CommonParameters</span></span>
<span data-ttu-id="46006-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46006-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46006-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46006-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46006-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46006-129">INPUTS</span></span>

### <span data-ttu-id="46006-130">System. String</span><span class="sxs-lookup"><span data-stu-id="46006-130">System.String</span></span>

### <span data-ttu-id="46006-131">Microsoft. Azure. Command. RedisCache. models. PSScheduleEntry []</span><span class="sxs-lookup"><span data-stu-id="46006-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="46006-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46006-132">OUTPUTS</span></span>

### <span data-ttu-id="46006-133">Microsoft. Azure. Command. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="46006-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="46006-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46006-134">NOTES</span></span>
* <span data-ttu-id="46006-135">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="46006-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="46006-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46006-136">RELATED LINKS</span></span>

[<span data-ttu-id="46006-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="46006-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="46006-138">Új – AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="46006-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="46006-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="46006-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


