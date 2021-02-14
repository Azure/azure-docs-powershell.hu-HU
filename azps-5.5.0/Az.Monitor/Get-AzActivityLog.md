---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154627"
---
# <span data-ttu-id="59aa9-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="59aa9-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="59aa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="59aa9-103">Tevékenységnapló-események beolvasása.</span><span class="sxs-lookup"><span data-stu-id="59aa9-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="59aa9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59aa9-104">SYNTAX</span></span>

### <span data-ttu-id="59aa9-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="59aa9-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59aa9-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="59aa9-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59aa9-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="59aa9-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59aa9-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="59aa9-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59aa9-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="59aa9-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59aa9-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59aa9-110">DESCRIPTION</span></span>
<span data-ttu-id="59aa9-111">A Get-AzActivityLog parancsmag beolvassa a tevékenységnapló eseményeit.</span><span class="sxs-lookup"><span data-stu-id="59aa9-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="59aa9-112">Az események az aktuális előfizetés-azonosítóhoz, korrelációs azonosítóhoz, erőforráscsoporthoz, erőforrás-azonosítóhoz vagy erőforrás-szolgáltatóhoz társíthatók.</span><span class="sxs-lookup"><span data-stu-id="59aa9-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="59aa9-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59aa9-113">EXAMPLES</span></span>

### <span data-ttu-id="59aa9-114">1. példa: Eseménynapló lekérte előfizetésazonosító szerint</span><span class="sxs-lookup"><span data-stu-id="59aa9-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="59aa9-115">Ez a parancs a felhasználó előfizetés-azonosítójával társított 1000 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="59aa9-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-116">2. példa: Eseménynapló lekérte az előfizetésazonosítót, amely maximális számú eseményt adott meg</span><span class="sxs-lookup"><span data-stu-id="59aa9-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="59aa9-117">Ez a parancs a felhasználó előfizetés-azonosítójával társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="59aa9-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-118">3. példa: Eseménynapló lekérte az előfizetés azonosítóját kezdési időpontban.</span><span class="sxs-lookup"><span data-stu-id="59aa9-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="59aa9-119">Ez a parancs a 2017-06-01T10:30 időpontban helyi idő szerint 2017-06-01T10:30 időpontban történt vagy azt követően a felhasználó előfizetés-azonosítójával társított 1000 eseményt sorolja fel, ha az adott dátum/idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="59aa9-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-120">4. példa: Eseménynapló lekérte előfizetésazonosító alapján kezdési és záró időpontra.</span><span class="sxs-lookup"><span data-stu-id="59aa9-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="59aa9-121">Ez a parancs a 2017–04-01T10:30 helyi időpontban, illetve a 2017-04-01T10:30 időpontban, illetve a 2017-04-14T11:30 időpontig helyi idő előtt, ha a teljes dátum/időtartomány nem régebbi, mint 90 nap az aktuális dátumtól/időponttól ( például a megőrzési idő) helyi időig.</span><span class="sxs-lookup"><span data-stu-id="59aa9-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="59aa9-122">5. példa: Eseménynapló lekérte korrelációs azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="59aa9-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="59aa9-123">Ez a parancs a legtöbb 1000 eseményt sorolja fel a megadott korrelációs azonosítóval, amely az aktuális dátumtól/időponttól 7 nappal történt.</span><span class="sxs-lookup"><span data-stu-id="59aa9-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="59aa9-124">**MEGJEGYZÉS:** ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="59aa9-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="59aa9-125">6. példa: Eseménynapló lekérte korrelációs azonosító alapján, maximális számú esemény esetén</span><span class="sxs-lookup"><span data-stu-id="59aa9-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="59aa9-126">Ez a parancs a megadott korrelációs azonosítóval társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="59aa9-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="59aa9-127">**MEGJEGYZÉS:** ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="59aa9-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="59aa9-128">7. példa: Eseménynapló lekérte korrelációs azonosító és kezdési időpont alapján</span><span class="sxs-lookup"><span data-stu-id="59aa9-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="59aa9-129">Ez a parancs a 2017–05–22T04:30:00 időpontban megadott korrelációs azonosítóval társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="59aa9-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="59aa9-130">**MEGJEGYZÉS:** ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="59aa9-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="59aa9-131">8. példa: Eseménynapló lekérte korrelációs azonosító alapján a kezdési és a záró időpontmal</span><span class="sxs-lookup"><span data-stu-id="59aa9-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="59aa9-132">Ez a parancs a 2017–04–15T04:30 helyi időtartományon vagy azt követően lekért korrelációs azonosítóval társított legtöbb 1000 eseményt sorolja fel, de a 2017-04-25T12:30 időpont előtt, ha a teljes dátum/időtartomány nem régebbi 90 napnál az aktuális dátumtól/időponttól( vagyis a megőrzési időszaktól).</span><span class="sxs-lookup"><span data-stu-id="59aa9-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="59aa9-133">9. példa: Erőforráscsoport eseménynaplója</span><span class="sxs-lookup"><span data-stu-id="59aa9-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="59aa9-134">Ez a parancs legalább 1000 olyan eseményt sorol fel, amely a megadott erőforráscsoporthoz tartozik, és az aktuális dátumtól/időponttól 7 nappal történt.</span><span class="sxs-lookup"><span data-stu-id="59aa9-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-135">10. példa: Eseménynapló lekérte egy legfeljebb eseményszámú erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="59aa9-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="59aa9-136">Ez a parancs a megadott erőforráscsoporttal társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="59aa9-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-137">11. példa: Erőforráscsoport eseménynaplója kezdési időpontra</span><span class="sxs-lookup"><span data-stu-id="59aa9-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="59aa9-138">Ez a parancs a 2017–05–22T04:30:00 időpontban megadott erőforráscsoporttal társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="59aa9-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-139">12. példa: Eseménynapló lekérte egy kezdési és a záró időponttal egy erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="59aa9-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="59aa9-140">Ez a parancs a 2017-04-15T04:30 helyi időtartományon vagy azt követően a megadott erőforráscsoporttal társított legtöbb 1000 eseményt sorolja fel, de a 2017-04-25T12:30 időpont előtt, ha a teljes dátum/időtartomány nem régebbi 90 napnál az aktuális dátumtól/időponttól( vagyis a megőrzési időszaktól).</span><span class="sxs-lookup"><span data-stu-id="59aa9-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="59aa9-141">13. példa: Eseménynapló lekérte erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="59aa9-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="59aa9-142">Ez a parancs a megadott erőforrás-azonosítóhoz tartozó 1000 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="59aa9-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-143">14. példa: Eseménynapló lekérte erőforrás-azonosító szerint, maximális számú esemény esetén</span><span class="sxs-lookup"><span data-stu-id="59aa9-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="59aa9-144">Ez a parancs a megadott erőforrás-azonosítóhoz tartozó 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="59aa9-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-145">15. példa: Eseménynapló lekérte erőforrás-azonosító szerint kezdési időpontban</span><span class="sxs-lookup"><span data-stu-id="59aa9-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="59aa9-146">Ez a parancs a 2017–05–22T04:30:00 időpontban megadott erőforrás-azonosítóhoz tartozó legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="59aa9-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-147">16. példa: Eseménynapló lekérte erőforrás-azonosító szerint kezdési és záró időpont esetén</span><span class="sxs-lookup"><span data-stu-id="59aa9-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="59aa9-148">Ez a parancs a 2017–04–15T04:30 helyi időtartományon vagy azt követően lekért erőforrás-azonosítóval társított legtöbb 1000 eseményt sorolja fel, de a 2017-04-25T12:30 időpont előtt, ha a teljes dátum/időtartomány nem régebbi 90 napnál az aktuális dátumtól/időponttól( vagyis a megőrzési időszaktól).</span><span class="sxs-lookup"><span data-stu-id="59aa9-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="59aa9-149">17. példa: Eseménynapló lekérte az erőforrás-szolgáltató</span><span class="sxs-lookup"><span data-stu-id="59aa9-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="59aa9-150">Ez a parancs a megadott erőforrás-szolgáltatóval társított 1000 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="59aa9-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-151">18. példa: Eseménynapló lekérte az erőforrás-szolgáltató által, amely maximális számú eseményt tud behozni</span><span class="sxs-lookup"><span data-stu-id="59aa9-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="59aa9-152">Ez a parancs a megadott erőforrás-szolgáltatóval társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="59aa9-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-153">19. példa: Eseménynapló lekérte az erőforrás-szolgáltatótól kezdési időpontban</span><span class="sxs-lookup"><span data-stu-id="59aa9-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="59aa9-154">Ez a parancs a 2017–05–22T04:30:00 időpontban megadott erőforrás-szolgáltatóval társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="59aa9-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="59aa9-155">20. példa: Eseménynapló lekérte az erőforrás-szolgáltatótól a kezdési és a záró időpontra</span><span class="sxs-lookup"><span data-stu-id="59aa9-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="59aa9-156">Ez a parancs a 2017–2017–04–15T04:30 helyi időtartományon, de a 2017-04-25T12:30 időpontig helyi idő előtt, ha a teljes dátum/időtartomány nem régebbi, mint 90 nap az aktuális dátumtól/időponttól (vagyis a megőrzési időszaktól) társított 1000 esemény.</span><span class="sxs-lookup"><span data-stu-id="59aa9-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="59aa9-157">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59aa9-157">PARAMETERS</span></span>

### <span data-ttu-id="59aa9-158">-Hívó</span><span class="sxs-lookup"><span data-stu-id="59aa9-158">-Caller</span></span>
<span data-ttu-id="59aa9-159">A lehívni megfelelő események hívója</span><span class="sxs-lookup"><span data-stu-id="59aa9-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="59aa9-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="59aa9-160">-CorrelationId</span></span>
<span data-ttu-id="59aa9-161">The CorrelationId</span><span class="sxs-lookup"><span data-stu-id="59aa9-161">The CorrelationId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aa9-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59aa9-162">-DefaultProfile</span></span>
<span data-ttu-id="59aa9-163">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59aa9-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59aa9-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="59aa9-164">-DetailedOutput</span></span>
<span data-ttu-id="59aa9-165">A Return objektum az események összes adatával együtt (az alapértelmezett érték az, hogy csak bizonyos attribútumokat ad vissza, azaz nem ad részletes adatokat)</span><span class="sxs-lookup"><span data-stu-id="59aa9-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aa9-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="59aa9-166">-EndTime</span></span>
<span data-ttu-id="59aa9-167">The endTime of the query</span><span class="sxs-lookup"><span data-stu-id="59aa9-167">The endTime of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aa9-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="59aa9-168">-MaxRecord</span></span>
<span data-ttu-id="59aa9-169">A lehívni megfelelő rekordok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="59aa9-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="59aa9-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="59aa9-170">Alias: MaxRecords, MaxEvents</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aa9-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59aa9-171">-ResourceGroupName</span></span>
<span data-ttu-id="59aa9-172">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="59aa9-172">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aa9-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59aa9-173">-ResourceId</span></span>
<span data-ttu-id="59aa9-174">A ResourceId</span><span class="sxs-lookup"><span data-stu-id="59aa9-174">The ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aa9-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="59aa9-175">-ResourceProvider</span></span>
<span data-ttu-id="59aa9-176">A ResourceProvider neve</span><span class="sxs-lookup"><span data-stu-id="59aa9-176">The ResourceProvider name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aa9-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="59aa9-177">-StartTime</span></span>
<span data-ttu-id="59aa9-178">A lekérdezés korrelációsazonosítója</span><span class="sxs-lookup"><span data-stu-id="59aa9-178">The correlationId of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aa9-179">-Állapot</span><span class="sxs-lookup"><span data-stu-id="59aa9-179">-Status</span></span>
<span data-ttu-id="59aa9-180">A lehívni megfelelő események állapota</span><span class="sxs-lookup"><span data-stu-id="59aa9-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="59aa9-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59aa9-181">CommonParameters</span></span>
<span data-ttu-id="59aa9-182">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59aa9-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59aa9-183">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59aa9-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59aa9-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59aa9-184">INPUTS</span></span>

### <span data-ttu-id="59aa9-185">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="59aa9-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="59aa9-186">System.String</span><span class="sxs-lookup"><span data-stu-id="59aa9-186">System.String</span></span>

### <span data-ttu-id="59aa9-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="59aa9-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="59aa9-188">System.Int32</span><span class="sxs-lookup"><span data-stu-id="59aa9-188">System.Int32</span></span>

## <span data-ttu-id="59aa9-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59aa9-189">OUTPUTS</span></span>

### <span data-ttu-id="59aa9-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="59aa9-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="59aa9-191">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59aa9-191">NOTES</span></span>

## <span data-ttu-id="59aa9-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59aa9-192">RELATED LINKS</span></span>
