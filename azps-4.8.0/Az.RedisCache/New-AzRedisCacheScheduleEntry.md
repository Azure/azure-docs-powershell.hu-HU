---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182704"
---
# <span data-ttu-id="b896a-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b896a-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="b896a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b896a-102">SYNOPSIS</span></span>
<span data-ttu-id="b896a-103">Ütemezési bejegyzés létrehozása</span><span class="sxs-lookup"><span data-stu-id="b896a-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="b896a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b896a-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b896a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b896a-105">DESCRIPTION</span></span>
<span data-ttu-id="b896a-106">A **New-AzRedisCacheScheduleEntry** parancsmag létrehoz egy **PSScheduleEntry** objektumot.</span><span class="sxs-lookup"><span data-stu-id="b896a-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="b896a-107">Az Azure Redis-gyorsítótár-javítás ütemezési parancsmagjai (például az New-AzRedisCachePatchSchedule parancsmag) az ütemezési bejegyzés objektumait igénylik.</span><span class="sxs-lookup"><span data-stu-id="b896a-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="b896a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b896a-108">EXAMPLES</span></span>

### <span data-ttu-id="b896a-109">Példa 1: Ütemezési bejegyzés létrehozása hétvégekhez</span><span class="sxs-lookup"><span data-stu-id="b896a-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="b896a-110">Ez a parancs létrehoz egy **PSScheduleEntry** -objektumot, amely egy, a megadott kezdési időpontot és ablakot tartalmazó hétvégi ütemtervet képvisel.</span><span class="sxs-lookup"><span data-stu-id="b896a-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="b896a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b896a-111">PARAMETERS</span></span>

### <span data-ttu-id="b896a-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="b896a-112">-DayOfWeek</span></span>
<span data-ttu-id="b896a-113">Az ütemezési bejegyzéshez tartozó hét napját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b896a-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="b896a-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b896a-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b896a-115">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="b896a-115">Everyday</span></span> 
- <span data-ttu-id="b896a-116">Hétvégén</span><span class="sxs-lookup"><span data-stu-id="b896a-116">Weekend</span></span> 
- <span data-ttu-id="b896a-117">Hétfő</span><span class="sxs-lookup"><span data-stu-id="b896a-117">Monday</span></span> 
- <span data-ttu-id="b896a-118">Kedd</span><span class="sxs-lookup"><span data-stu-id="b896a-118">Tuesday</span></span> 
- <span data-ttu-id="b896a-119">Szerda</span><span class="sxs-lookup"><span data-stu-id="b896a-119">Wednesday</span></span> 
- <span data-ttu-id="b896a-120">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="b896a-120">Thursday</span></span> 
- <span data-ttu-id="b896a-121">Péntek</span><span class="sxs-lookup"><span data-stu-id="b896a-121">Friday</span></span> 
- <span data-ttu-id="b896a-122">Szombat</span><span class="sxs-lookup"><span data-stu-id="b896a-122">Saturday</span></span> 
- <span data-ttu-id="b896a-123">Vasárnap</span><span class="sxs-lookup"><span data-stu-id="b896a-123">Sunday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b896a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b896a-124">-DefaultProfile</span></span>
<span data-ttu-id="b896a-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b896a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b896a-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="b896a-126">-MaintenanceWindow</span></span>
<span data-ttu-id="b896a-127">A frissítésekhez engedélyezett időmennyiséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="b896a-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b896a-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="b896a-128">-StartHourUtc</span></span>
<span data-ttu-id="b896a-129">Az ütemterv kezdési napját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b896a-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b896a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b896a-130">CommonParameters</span></span>
<span data-ttu-id="b896a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b896a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b896a-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b896a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b896a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b896a-133">INPUTS</span></span>

### <span data-ttu-id="b896a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b896a-134">System.String</span></span>

### <span data-ttu-id="b896a-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b896a-135">System.Int32</span></span>

### <span data-ttu-id="b896a-136">System. null ' 1 [[System. időszak, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b896a-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b896a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b896a-137">OUTPUTS</span></span>

### <span data-ttu-id="b896a-138">Microsoft. Azure. Command. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b896a-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="b896a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b896a-139">NOTES</span></span>
* <span data-ttu-id="b896a-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="b896a-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="b896a-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b896a-141">RELATED LINKS</span></span>

[<span data-ttu-id="b896a-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b896a-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="b896a-143">Új – AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b896a-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="b896a-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b896a-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


