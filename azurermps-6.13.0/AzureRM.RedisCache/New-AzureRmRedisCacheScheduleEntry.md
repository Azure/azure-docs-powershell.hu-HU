---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 8364a3a8b9d88bfd3ce34f2e70f8fcae80e9b612
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501092"
---
# <span data-ttu-id="40e32-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="40e32-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="40e32-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40e32-102">SYNOPSIS</span></span>
<span data-ttu-id="40e32-103">Ütemezési bejegyzés létrehozása</span><span class="sxs-lookup"><span data-stu-id="40e32-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40e32-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40e32-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40e32-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40e32-105">DESCRIPTION</span></span>
<span data-ttu-id="40e32-106">A **New-AzureRmRedisCacheScheduleEntry** parancsmag létrehoz egy **PSScheduleEntry** objektumot.</span><span class="sxs-lookup"><span data-stu-id="40e32-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="40e32-107">Az Azure Redis-gyorsítótár-javítás ütemezési parancsmagjai (például az New-AzureRmRedisCachePatchSchedule parancsmag) az ütemezési bejegyzés objektumait igénylik.</span><span class="sxs-lookup"><span data-stu-id="40e32-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="40e32-108">Példák</span><span class="sxs-lookup"><span data-stu-id="40e32-108">EXAMPLES</span></span>

### <span data-ttu-id="40e32-109">Példa 1: Ütemezési bejegyzés létrehozása hétvégekhez</span><span class="sxs-lookup"><span data-stu-id="40e32-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="40e32-110">Ez a parancs létrehoz egy **PSScheduleEntry** -objektumot, amely egy, a megadott kezdési időpontot és ablakot tartalmazó hétvégi ütemtervet képvisel.</span><span class="sxs-lookup"><span data-stu-id="40e32-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="40e32-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40e32-111">PARAMETERS</span></span>

### <span data-ttu-id="40e32-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="40e32-112">-DayOfWeek</span></span>
<span data-ttu-id="40e32-113">Az ütemezési bejegyzéshez tartozó hét napját adja meg.</span><span class="sxs-lookup"><span data-stu-id="40e32-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="40e32-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="40e32-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="40e32-115">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="40e32-115">Everyday</span></span> 
- <span data-ttu-id="40e32-116">Hétvégén</span><span class="sxs-lookup"><span data-stu-id="40e32-116">Weekend</span></span> 
- <span data-ttu-id="40e32-117">Hétfő</span><span class="sxs-lookup"><span data-stu-id="40e32-117">Monday</span></span> 
- <span data-ttu-id="40e32-118">Kedd</span><span class="sxs-lookup"><span data-stu-id="40e32-118">Tuesday</span></span> 
- <span data-ttu-id="40e32-119">Szerda</span><span class="sxs-lookup"><span data-stu-id="40e32-119">Wednesday</span></span> 
- <span data-ttu-id="40e32-120">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="40e32-120">Thursday</span></span> 
- <span data-ttu-id="40e32-121">Péntek</span><span class="sxs-lookup"><span data-stu-id="40e32-121">Friday</span></span> 
- <span data-ttu-id="40e32-122">Szombat</span><span class="sxs-lookup"><span data-stu-id="40e32-122">Saturday</span></span> 
- <span data-ttu-id="40e32-123">Vasárnap</span><span class="sxs-lookup"><span data-stu-id="40e32-123">Sunday</span></span>

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

### <span data-ttu-id="40e32-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e32-124">-DefaultProfile</span></span>
<span data-ttu-id="40e32-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40e32-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40e32-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="40e32-126">-MaintenanceWindow</span></span>
<span data-ttu-id="40e32-127">A frissítésekhez engedélyezett időmennyiséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="40e32-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="40e32-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="40e32-128">-StartHourUtc</span></span>
<span data-ttu-id="40e32-129">Az ütemterv kezdési napját adja meg.</span><span class="sxs-lookup"><span data-stu-id="40e32-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="40e32-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e32-130">CommonParameters</span></span>
<span data-ttu-id="40e32-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40e32-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e32-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e32-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e32-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e32-133">INPUTS</span></span>

### <span data-ttu-id="40e32-134">System. String</span><span class="sxs-lookup"><span data-stu-id="40e32-134">System.String</span></span>

### <span data-ttu-id="40e32-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="40e32-135">System.Int32</span></span>

### <span data-ttu-id="40e32-136">System. null ' 1 [[System. időszak, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="40e32-136">System.Nullable\`1[[System.TimeSpan, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="40e32-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e32-137">OUTPUTS</span></span>

### <span data-ttu-id="40e32-138">Microsoft. Azure. Command. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="40e32-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="40e32-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40e32-139">NOTES</span></span>
* <span data-ttu-id="40e32-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="40e32-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="40e32-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40e32-141">RELATED LINKS</span></span>

[<span data-ttu-id="40e32-142">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="40e32-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="40e32-143">Új – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="40e32-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="40e32-144">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="40e32-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


