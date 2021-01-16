---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476813"
---
# <span data-ttu-id="feee8-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="feee8-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="feee8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feee8-102">SYNOPSIS</span></span>
<span data-ttu-id="feee8-103">Tevékenységnapló-események beolvasása.</span><span class="sxs-lookup"><span data-stu-id="feee8-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="feee8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="feee8-104">SYNTAX</span></span>

### <span data-ttu-id="feee8-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="feee8-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="feee8-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="feee8-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="feee8-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="feee8-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feee8-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="feee8-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="feee8-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="feee8-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feee8-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="feee8-110">DESCRIPTION</span></span>
<span data-ttu-id="feee8-111">A Get-AzActivityLog parancsmag beolvassa a tevékenységnapló eseményeit.</span><span class="sxs-lookup"><span data-stu-id="feee8-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="feee8-112">Az események az aktuális előfizetés-azonosítóhoz, korrelációs azonosítóhoz, erőforráscsoporthoz, erőforrás-azonosítóhoz vagy erőforrás-szolgáltatóhoz társíthatók.</span><span class="sxs-lookup"><span data-stu-id="feee8-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="feee8-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="feee8-113">EXAMPLES</span></span>

### <span data-ttu-id="feee8-114">1. példa: Eseménynapló lekérte előfizetésazonosító szerint</span><span class="sxs-lookup"><span data-stu-id="feee8-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="feee8-115">Ez a parancs a felhasználó előfizetés-azonosítójával társított legtöbb 1000 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="feee8-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-116">2. példa: Eseménynapló lekérte az előfizetésazonosítót, amely maximális számú eseményt adott meg</span><span class="sxs-lookup"><span data-stu-id="feee8-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="feee8-117">Ez a parancs a felhasználó előfizetés-azonosítójával társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="feee8-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-118">3. példa: Eseménynapló lekérte az előfizetés azonosítóját kezdési időpontban.</span><span class="sxs-lookup"><span data-stu-id="feee8-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="feee8-119">Ez a parancs a 2017-06-06-01T10:30 időpontban helyi idő szerint 2017-06-01T10:30 időpontban megadott felhasználó előfizetés-azonosítójával társított legtöbb 1000 eseményt sorolja fel, ha az adott dátum/idő nem régebbi az aktuális dátumtól/időponttól 90 napnál.</span><span class="sxs-lookup"><span data-stu-id="feee8-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-120">4. példa: Eseménynapló lekérte előfizetésazonosító alapján kezdési és záró időpontra.</span><span class="sxs-lookup"><span data-stu-id="feee8-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="feee8-121">Ez a parancs a 2017-04-04-01T10:30 helyi időpontban, illetve a 2017-04-14T11:30 időpontban, illetve a 2017-04-14T11:30 időpontig helyi idő előtt, ha a teljes dátum/időtartomány nem régebbi az aktuális dátumtól/időponttól ( például a megőrzési időtől) 1000-ig.</span><span class="sxs-lookup"><span data-stu-id="feee8-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="feee8-122">5. példa: Eseménynapló lekérte korrelációs azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="feee8-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="feee8-123">Ez a parancs a legtöbb 1000 eseményt sorolja fel a megadott korrelációs azonosítóval, amely az aktuális dátumtól/időponttól 7 nappal történt.</span><span class="sxs-lookup"><span data-stu-id="feee8-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="feee8-124">**MEGJEGYZÉS:** ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="feee8-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="feee8-125">6. példa: Eseménynapló lekérte korrelációs azonosító alapján, maximális számú esemény esetén</span><span class="sxs-lookup"><span data-stu-id="feee8-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="feee8-126">Ez a parancs a megadott korrelációs azonosítóval társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="feee8-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="feee8-127">**MEGJEGYZÉS:** ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="feee8-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="feee8-128">7. példa: Eseménynapló lekérte korrelációs azonosító és kezdési időpont alapján</span><span class="sxs-lookup"><span data-stu-id="feee8-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="feee8-129">Ez a parancs a 2017–05–22T04:30:00 időpontban megadott korrelációs azonosítóval társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="feee8-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="feee8-130">**MEGJEGYZÉS:** ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="feee8-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="feee8-131">8. példa: Eseménynapló lekérte korrelációs azonosító alapján a kezdési és a záró időpontmal</span><span class="sxs-lookup"><span data-stu-id="feee8-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="feee8-132">Ez a parancs a 2017–04–15T04:30 helyi időtartományon vagy azt követően lekért korrelációs azonosítóval társított legtöbb 1000 eseményt sorolja fel, de a 2017-04-25T12:30 időpont előtt, ha a teljes dátum/időtartomány nem régebbi 90 napnál az aktuális dátumtól/időponttól( vagyis a megőrzési időszaktól).</span><span class="sxs-lookup"><span data-stu-id="feee8-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="feee8-133">9. példa: Erőforráscsoport eseménynaplója</span><span class="sxs-lookup"><span data-stu-id="feee8-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="feee8-134">Ez a parancs legalább 1000 olyan eseményt sorol fel, amely a megadott erőforráscsoporthoz tartozik, és az aktuális dátumtól/időponttól 7 nappal történt.</span><span class="sxs-lookup"><span data-stu-id="feee8-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-135">10. példa: Eseménynapló bejedése egy legfeljebb eseményszámú erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="feee8-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="feee8-136">Ez a parancs a megadott erőforráscsoporttal társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="feee8-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-137">11. példa: Erőforráscsoport eseménynaplója kezdési időpontra</span><span class="sxs-lookup"><span data-stu-id="feee8-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="feee8-138">Ez a parancs a 2017–05–22T04:30:00 időpontban megadott erőforráscsoporttal társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="feee8-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-139">12. példa: Eseménynapló lekérte egy kezdési és a záró időponttal egy erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="feee8-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="feee8-140">Ez a parancs a 2017-04-15T04:30 helyi időtartományon vagy azt követően a megadott erőforráscsoporttal társított legtöbb 1000 eseményt sorolja fel, de a 2017-04-25T12:30 időpont előtt, ha a teljes dátum/időtartomány nem régebbi 90 napnál az aktuális dátumtól/időponttól( vagyis a megőrzési időszaktól).</span><span class="sxs-lookup"><span data-stu-id="feee8-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="feee8-141">13. példa: Eseménynapló lekérte erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="feee8-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="feee8-142">Ez a parancs a megadott erőforrás-azonosítóhoz tartozó 1000 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="feee8-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-143">14. példa: Eseménynapló lekérte erőforrás-azonosító szerint, maximális számú esemény esetén</span><span class="sxs-lookup"><span data-stu-id="feee8-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="feee8-144">Ez a parancs a megadott erőforrás-azonosítóhoz tartozó 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="feee8-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-145">15. példa: Eseménynapló lekérte erőforrás-azonosítója alapján kezdési időpont esetén</span><span class="sxs-lookup"><span data-stu-id="feee8-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="feee8-146">Ez a parancs a 2017–05–22T04:30:00 helyi időtartományban megadott erőforrás-azonosítóval társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="feee8-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-147">16. példa: Eseménynapló lekérte erőforrás-azonosító szerint kezdési és záró időpont esetén</span><span class="sxs-lookup"><span data-stu-id="feee8-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="feee8-148">Ez a parancs a 2017–04–15T04:30 helyi időtartományon vagy azt követően lekért erőforrás-azonosítóval társított legtöbb 1000 eseményt sorolja fel, de a 2017-04-25T12:30 időpont előtt, ha a teljes dátum/időtartomány nem régebbi 90 napnál az aktuális dátumtól/időponttól( vagyis a megőrzési időszaktól).</span><span class="sxs-lookup"><span data-stu-id="feee8-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="feee8-149">17. példa: Eseménynapló lekérte az erőforrás-szolgáltató</span><span class="sxs-lookup"><span data-stu-id="feee8-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="feee8-150">Ez a parancs a megadott erőforrás-szolgáltatóval társított 1000 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="feee8-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-151">18. példa: Eseménynapló lekérte az erőforrás-szolgáltató által, amely maximális számú eseményt tud behozni</span><span class="sxs-lookup"><span data-stu-id="feee8-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="feee8-152">Ez a parancs a megadott erőforrás-szolgáltatóval társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.</span><span class="sxs-lookup"><span data-stu-id="feee8-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-153">19. példa: Eseménynapló lekérte az erőforrás-szolgáltatótól kezdési időpontban</span><span class="sxs-lookup"><span data-stu-id="feee8-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="feee8-154">Ez a parancs a 2017–05–22T04:30:00 időpontban megadott erőforrás-szolgáltatóval társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="feee8-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="feee8-155">20. példa: Eseménynapló beása erőforrás-szolgáltató szerint kezdési és záró időpontban</span><span class="sxs-lookup"><span data-stu-id="feee8-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="feee8-156">Ez a parancs a 2017–2017–04–15T04:30 helyi időtartományon, de a 2017-04-25T12:30 időpontig helyi idő előtt, ha a teljes dátum/időtartomány nem régebbi, mint 90 nap az aktuális dátumtól/időponttól (vagyis a megőrzési időszaktól) társított 1000 esemény.</span><span class="sxs-lookup"><span data-stu-id="feee8-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="feee8-157">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feee8-157">PARAMETERS</span></span>

### <span data-ttu-id="feee8-158">-Hívó</span><span class="sxs-lookup"><span data-stu-id="feee8-158">-Caller</span></span>
<span data-ttu-id="feee8-159">A lehívni megfelelő események hívója</span><span class="sxs-lookup"><span data-stu-id="feee8-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="feee8-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="feee8-160">-CorrelationId</span></span>
<span data-ttu-id="feee8-161">The CorrelationId</span><span class="sxs-lookup"><span data-stu-id="feee8-161">The CorrelationId</span></span>

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

### <span data-ttu-id="feee8-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feee8-162">-DefaultProfile</span></span>
<span data-ttu-id="feee8-163">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="feee8-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feee8-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="feee8-164">-DetailedOutput</span></span>
<span data-ttu-id="feee8-165">A Return objektum az események összes adatával együtt (az alapértelmezett érték az, hogy csak bizonyos attribútumokat ad vissza, azaz nem ad részletes adatokat)</span><span class="sxs-lookup"><span data-stu-id="feee8-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

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

### <span data-ttu-id="feee8-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="feee8-166">-EndTime</span></span>
<span data-ttu-id="feee8-167">The endTime of the query</span><span class="sxs-lookup"><span data-stu-id="feee8-167">The endTime of the query</span></span>

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

### <span data-ttu-id="feee8-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="feee8-168">-MaxRecord</span></span>
<span data-ttu-id="feee8-169">A lehívni megfelelő rekordok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="feee8-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="feee8-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="feee8-170">Alias: MaxRecords, MaxEvents</span></span>

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

### <span data-ttu-id="feee8-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feee8-171">-ResourceGroupName</span></span>
<span data-ttu-id="feee8-172">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="feee8-172">The resource group name</span></span>

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

### <span data-ttu-id="feee8-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="feee8-173">-ResourceId</span></span>
<span data-ttu-id="feee8-174">A ResourceId</span><span class="sxs-lookup"><span data-stu-id="feee8-174">The ResourceId</span></span>

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

### <span data-ttu-id="feee8-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="feee8-175">-ResourceProvider</span></span>
<span data-ttu-id="feee8-176">A ResourceProvider neve</span><span class="sxs-lookup"><span data-stu-id="feee8-176">The ResourceProvider name</span></span>

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

### <span data-ttu-id="feee8-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="feee8-177">-StartTime</span></span>
<span data-ttu-id="feee8-178">A lekérdezés korrelációsazonosítója</span><span class="sxs-lookup"><span data-stu-id="feee8-178">The correlationId of the query</span></span>

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

### <span data-ttu-id="feee8-179">-Állapot</span><span class="sxs-lookup"><span data-stu-id="feee8-179">-Status</span></span>
<span data-ttu-id="feee8-180">A lehívni megfelelő események állapota</span><span class="sxs-lookup"><span data-stu-id="feee8-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="feee8-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feee8-181">CommonParameters</span></span>
<span data-ttu-id="feee8-182">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feee8-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feee8-183">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="feee8-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feee8-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="feee8-184">INPUTS</span></span>

### <span data-ttu-id="feee8-185">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="feee8-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="feee8-186">System.String</span><span class="sxs-lookup"><span data-stu-id="feee8-186">System.String</span></span>

### <span data-ttu-id="feee8-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="feee8-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="feee8-188">System.Int32</span><span class="sxs-lookup"><span data-stu-id="feee8-188">System.Int32</span></span>

## <span data-ttu-id="feee8-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="feee8-189">OUTPUTS</span></span>

### <span data-ttu-id="feee8-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="feee8-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="feee8-191">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="feee8-191">NOTES</span></span>

## <span data-ttu-id="feee8-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="feee8-192">RELATED LINKS</span></span>
