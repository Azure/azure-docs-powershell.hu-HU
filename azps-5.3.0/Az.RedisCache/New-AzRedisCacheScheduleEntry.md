---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466623"
---
# <span data-ttu-id="f6e1c-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f6e1c-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="f6e1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e1c-103">Ütemezési bejegyzést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="f6e1c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6e1c-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6e1c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6e1c-105">DESCRIPTION</span></span>
<span data-ttu-id="f6e1c-106">A **New-AzRedisCacheScheduleEntry** parancsmag létrehoz egy **PSScheduleEntry objektumot.**</span><span class="sxs-lookup"><span data-stu-id="f6e1c-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="f6e1c-107">Az Azure Redis Cache javításütemterv-parancsmagja, például a New-AzRedisCachePatchSchedule parancsmag ütemezési belépési objektumokat igényel.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="f6e1c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6e1c-108">EXAMPLES</span></span>

### <span data-ttu-id="f6e1c-109">1. példa: Ütemezési bejegyzés létrehozása hétvégékhez</span><span class="sxs-lookup"><span data-stu-id="f6e1c-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="f6e1c-110">Ez a parancs létrehoz egy **PSScheduleEntry** objektumot, amely egy hétvégi ütemezést képvisel, amely a megadott kezdési időpontot és ablakot is meg van adva.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="f6e1c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6e1c-111">PARAMETERS</span></span>

### <span data-ttu-id="f6e1c-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="f6e1c-112">-DayOfWeek</span></span>
<span data-ttu-id="f6e1c-113">Az ütemezési bejegyzéshez a hét napját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="f6e1c-114">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="f6e1c-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6e1c-115">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="f6e1c-115">Everyday</span></span> 
- <span data-ttu-id="f6e1c-116">Hétvége</span><span class="sxs-lookup"><span data-stu-id="f6e1c-116">Weekend</span></span> 
- <span data-ttu-id="f6e1c-117">Hétfő</span><span class="sxs-lookup"><span data-stu-id="f6e1c-117">Monday</span></span> 
- <span data-ttu-id="f6e1c-118">Kedd</span><span class="sxs-lookup"><span data-stu-id="f6e1c-118">Tuesday</span></span> 
- <span data-ttu-id="f6e1c-119">Szerda</span><span class="sxs-lookup"><span data-stu-id="f6e1c-119">Wednesday</span></span> 
- <span data-ttu-id="f6e1c-120">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="f6e1c-120">Thursday</span></span> 
- <span data-ttu-id="f6e1c-121">Péntek</span><span class="sxs-lookup"><span data-stu-id="f6e1c-121">Friday</span></span> 
- <span data-ttu-id="f6e1c-122">Szombat</span><span class="sxs-lookup"><span data-stu-id="f6e1c-122">Saturday</span></span> 
- <span data-ttu-id="f6e1c-123">vasárnap</span><span class="sxs-lookup"><span data-stu-id="f6e1c-123">Sunday</span></span>

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

### <span data-ttu-id="f6e1c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e1c-124">-DefaultProfile</span></span>
<span data-ttu-id="f6e1c-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6e1c-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="f6e1c-126">-MaintenanceWindow</span></span>
<span data-ttu-id="f6e1c-127">A frissítésekhez engedélyezett időkeretet adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="f6e1c-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="f6e1c-128">-StartHourUtc</span></span>
<span data-ttu-id="f6e1c-129">Az ütemezés kezdetekor a nap egy óráját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="f6e1c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e1c-130">CommonParameters</span></span>
<span data-ttu-id="f6e1c-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e1c-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6e1c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e1c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6e1c-133">INPUTS</span></span>

### <span data-ttu-id="f6e1c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f6e1c-134">System.String</span></span>

### <span data-ttu-id="f6e1c-135">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f6e1c-135">System.Int32</span></span>

### <span data-ttu-id="f6e1c-136">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f6e1c-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f6e1c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6e1c-137">OUTPUTS</span></span>

### <span data-ttu-id="f6e1c-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f6e1c-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="f6e1c-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6e1c-139">NOTES</span></span>
* <span data-ttu-id="f6e1c-140">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="f6e1c-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f6e1c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6e1c-141">RELATED LINKS</span></span>

[<span data-ttu-id="f6e1c-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f6e1c-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="f6e1c-143">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f6e1c-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="f6e1c-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f6e1c-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


