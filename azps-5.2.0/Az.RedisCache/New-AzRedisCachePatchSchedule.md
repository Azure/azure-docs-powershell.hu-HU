---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 4215cf8450922a03f061abcc04022ee4e20950b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336426"
---
# <span data-ttu-id="f84f3-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f84f3-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="f84f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f84f3-102">SYNOPSIS</span></span>
<span data-ttu-id="f84f3-103">Javításütemtervet ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="f84f3-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="f84f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f84f3-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f84f3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f84f3-105">DESCRIPTION</span></span>
<span data-ttu-id="f84f3-106">A **New-AzRedisCachePatchSchedule** parancsmag hozzáad egy javításütemtervet az Azure Redis Cache gyorsítótárában lévő gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="f84f3-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="f84f3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f84f3-107">EXAMPLES</span></span>

### <span data-ttu-id="f84f3-108">1. példa: Javításütemterv létrehozása és hozzáadása gyorsítótárhoz</span><span class="sxs-lookup"><span data-stu-id="f84f3-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="f84f3-109">Ez a parancs hozzáad egy javításütemtervet a RedisCache06 nevű gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="f84f3-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="f84f3-110">Az Entries paraméter értékeként egy olyan parancsot használ, amely a **New-AzRedisCacheScheduleEntry** segítségével hoz létre ütemezést.</span><span class="sxs-lookup"><span data-stu-id="f84f3-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="f84f3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f84f3-111">PARAMETERS</span></span>

### <span data-ttu-id="f84f3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84f3-112">-DefaultProfile</span></span>
<span data-ttu-id="f84f3-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f84f3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f84f3-114">-Entries</span><span class="sxs-lookup"><span data-stu-id="f84f3-114">-Entries</span></span>
<span data-ttu-id="f84f3-115">Ez a parancsmag által egy gyorsítótárban megadott ütemezéstömböt ad meg.</span><span class="sxs-lookup"><span data-stu-id="f84f3-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="f84f3-116">**PSScheduleEntry** objektum beszerzéséhez használja a New-AzRedisCacheScheduleEntry parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f84f3-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="f84f3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f84f3-117">-Name</span></span>
<span data-ttu-id="f84f3-118">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f84f3-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="f84f3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84f3-119">-ResourceGroupName</span></span>
<span data-ttu-id="f84f3-120">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f84f3-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="f84f3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f84f3-121">-Confirm</span></span>
<span data-ttu-id="f84f3-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f84f3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f84f3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f84f3-123">-WhatIf</span></span>
<span data-ttu-id="f84f3-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f84f3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f84f3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f84f3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f84f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84f3-126">CommonParameters</span></span>
<span data-ttu-id="f84f3-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84f3-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f84f3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84f3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f84f3-129">INPUTS</span></span>

### <span data-ttu-id="f84f3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f84f3-130">System.String</span></span>

### <span data-ttu-id="f84f3-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span><span class="sxs-lookup"><span data-stu-id="f84f3-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="f84f3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f84f3-132">OUTPUTS</span></span>

### <span data-ttu-id="f84f3-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f84f3-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="f84f3-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f84f3-134">NOTES</span></span>
* <span data-ttu-id="f84f3-135">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="f84f3-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f84f3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f84f3-136">RELATED LINKS</span></span>

[<span data-ttu-id="f84f3-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f84f3-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="f84f3-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f84f3-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="f84f3-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f84f3-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


