---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206127"
---
# <span data-ttu-id="6ac92-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="6ac92-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="6ac92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ac92-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac92-103">Ütemezési bejegyzést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6ac92-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="6ac92-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6ac92-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ac92-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6ac92-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac92-106">A **New-AzRedisCacheScheduleEntry** parancsmag létrehoz egy **PSScheduleEntry objektumot.**</span><span class="sxs-lookup"><span data-stu-id="6ac92-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="6ac92-107">Az Azure Redis Cache javításütemterv-parancsmagja, például a New-AzRedisCachePatchSchedule parancsmag ütemezési belépési objektumokat igényel.</span><span class="sxs-lookup"><span data-stu-id="6ac92-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="6ac92-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6ac92-108">EXAMPLES</span></span>

### <span data-ttu-id="6ac92-109">1. példa: Ütemezési bejegyzés létrehozása hétvégékhez</span><span class="sxs-lookup"><span data-stu-id="6ac92-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="6ac92-110">Ez a parancs létrehoz egy **PSScheduleEntry** objektumot, amely egy hétvégi ütemezést képvisel, amely a megadott kezdési időpontot és ablakot is meg van adva.</span><span class="sxs-lookup"><span data-stu-id="6ac92-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="6ac92-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ac92-111">PARAMETERS</span></span>

### <span data-ttu-id="6ac92-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="6ac92-112">-DayOfWeek</span></span>
<span data-ttu-id="6ac92-113">Az ütemezési bejegyzéshez a hét napját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ac92-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="6ac92-114">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="6ac92-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6ac92-115">Mindennapos</span><span class="sxs-lookup"><span data-stu-id="6ac92-115">Everyday</span></span> 
- <span data-ttu-id="6ac92-116">Hétvége</span><span class="sxs-lookup"><span data-stu-id="6ac92-116">Weekend</span></span> 
- <span data-ttu-id="6ac92-117">Hétfő</span><span class="sxs-lookup"><span data-stu-id="6ac92-117">Monday</span></span> 
- <span data-ttu-id="6ac92-118">Kedd</span><span class="sxs-lookup"><span data-stu-id="6ac92-118">Tuesday</span></span> 
- <span data-ttu-id="6ac92-119">Szerda</span><span class="sxs-lookup"><span data-stu-id="6ac92-119">Wednesday</span></span> 
- <span data-ttu-id="6ac92-120">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="6ac92-120">Thursday</span></span> 
- <span data-ttu-id="6ac92-121">Péntek</span><span class="sxs-lookup"><span data-stu-id="6ac92-121">Friday</span></span> 
- <span data-ttu-id="6ac92-122">Szombat</span><span class="sxs-lookup"><span data-stu-id="6ac92-122">Saturday</span></span> 
- <span data-ttu-id="6ac92-123">vasárnap</span><span class="sxs-lookup"><span data-stu-id="6ac92-123">Sunday</span></span>

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

### <span data-ttu-id="6ac92-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac92-124">-DefaultProfile</span></span>
<span data-ttu-id="6ac92-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ac92-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ac92-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="6ac92-126">-MaintenanceWindow</span></span>
<span data-ttu-id="6ac92-127">A frissítésekhez engedélyezett időkeretet adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ac92-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="6ac92-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="6ac92-128">-StartHourUtc</span></span>
<span data-ttu-id="6ac92-129">Az ütemezés kezdetekor a nap egy óráját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ac92-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="6ac92-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac92-130">CommonParameters</span></span>
<span data-ttu-id="6ac92-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ac92-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac92-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac92-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac92-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ac92-133">INPUTS</span></span>

### <span data-ttu-id="6ac92-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6ac92-134">System.String</span></span>

### <span data-ttu-id="6ac92-135">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6ac92-135">System.Int32</span></span>

### <span data-ttu-id="6ac92-136">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6ac92-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6ac92-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ac92-137">OUTPUTS</span></span>

### <span data-ttu-id="6ac92-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="6ac92-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="6ac92-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6ac92-139">NOTES</span></span>
* <span data-ttu-id="6ac92-140">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="6ac92-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="6ac92-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ac92-141">RELATED LINKS</span></span>

[<span data-ttu-id="6ac92-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6ac92-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="6ac92-143">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6ac92-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="6ac92-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6ac92-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


