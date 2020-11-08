---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025248"
---
# <span data-ttu-id="cdee0-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="cdee0-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="cdee0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdee0-102">SYNOPSIS</span></span>
<span data-ttu-id="cdee0-103">Tevékenység-naplózási események beolvasása</span><span class="sxs-lookup"><span data-stu-id="cdee0-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="cdee0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdee0-104">SYNTAX</span></span>

### <span data-ttu-id="cdee0-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="cdee0-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdee0-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cdee0-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdee0-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cdee0-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdee0-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="cdee0-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdee0-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="cdee0-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdee0-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdee0-110">DESCRIPTION</span></span>
<span data-ttu-id="cdee0-111">Az Get-AzActivityLog parancsmag tevékenység-naplózási eseményeket olvas be.</span><span class="sxs-lookup"><span data-stu-id="cdee0-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="cdee0-112">Az események az aktuális előfizetési AZONOSÍTÓval, korrelációs AZONOSÍTÓval, erőforrás csoporttal, erőforrás-AZONOSÍTÓval vagy erőforrás-szolgáltatóval kapcsolhatók be.</span><span class="sxs-lookup"><span data-stu-id="cdee0-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="cdee0-113">Példák</span><span class="sxs-lookup"><span data-stu-id="cdee0-113">EXAMPLES</span></span>

### <span data-ttu-id="cdee0-114">Példa 1: esemény naplójának beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="cdee0-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="cdee0-115">Ez a parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, az aktuális dátumtól/időponttól számított 7 napot tartalmazó legtöbb 1000-eseményben szerepel.</span><span class="sxs-lookup"><span data-stu-id="cdee0-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-116">2. példa: az esemény naplójának beszerzése előfizetés-AZONOSÍTÓval maximális számú eseménnyel</span><span class="sxs-lookup"><span data-stu-id="cdee0-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="cdee0-117">Ez a parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, az aktuális dátumtól/időponttól számított 7 napot tartalmazó legtöbb 100-eseményben szerepel.</span><span class="sxs-lookup"><span data-stu-id="cdee0-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-118">3. példa: az előfizetési AZONOSÍTÓval beolvashatja az eseménynaplót kezdési időponttal.</span><span class="sxs-lookup"><span data-stu-id="cdee0-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="cdee0-119">Ez a parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, a 2017-06-01T10:30 helyi időpontra, illetve az aktuális dátumtól/időponttól számított 30 napnál nem régebbi 90 verzió esetén jeleníti meg a legtöbb 1000-eseményt.</span><span class="sxs-lookup"><span data-stu-id="cdee0-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-120">Példa 4: az esemény naplójának beszerzése előfizetéses AZONOSÍTÓval a kezdési és befejezési időponttal.</span><span class="sxs-lookup"><span data-stu-id="cdee0-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="cdee0-121">Ez a 1000 parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, a 2017-04-01T10:30 helyi idő, illetve 2017-04-14T11:30 helyi idő, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz a megtartási időszakból.</span><span class="sxs-lookup"><span data-stu-id="cdee0-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="cdee0-122">Példa 5: esemény naplójának beszerzése korrelációs AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="cdee0-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="cdee0-123">Ez a parancs a megadott korrelációs AZONOSÍTÓval társított legtöbb 1000-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot.</span><span class="sxs-lookup"><span data-stu-id="cdee0-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="cdee0-124">**Megjegyzés** : ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="cdee0-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="cdee0-125">6. példa: a korrelációs AZONOSÍTÓval beolvashatja az eseménynaplót az események maximális számával.</span><span class="sxs-lookup"><span data-stu-id="cdee0-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="cdee0-126">Ez a parancs a megadott korrelációs AZONOSÍTÓval társított legtöbb 100-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot.</span><span class="sxs-lookup"><span data-stu-id="cdee0-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="cdee0-127">**Megjegyzés** : ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="cdee0-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="cdee0-128">7. példa: események naplózása a korrelációs AZONOSÍTÓval és a kezdési időponttal</span><span class="sxs-lookup"><span data-stu-id="cdee0-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="cdee0-129">Ez a parancs a 1000-es számú, a 2017-05-22T04:30:00 helyi idő alatt vagy azt követően a megadott korrelációs AZONOSÍTÓval társított legtöbb-eseményen szerepel, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="cdee0-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="cdee0-130">**Megjegyzés** : ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="cdee0-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="cdee0-131">8. példa: esemény naplójának beszerzése korrelációs AZONOSÍTÓval a kezdési és befejezési időponttal</span><span class="sxs-lookup"><span data-stu-id="cdee0-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="cdee0-132">Ez a parancs a megadott korrelációs AZONOSÍTÓval társított legtöbb 1000-eseményen (2017-04-15T04:30 helyi időpontban) vagy a 2017-04-25T12:30 helyi idő alatt, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz: a retenciós időszak.</span><span class="sxs-lookup"><span data-stu-id="cdee0-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="cdee0-133">Példa 9: erőforrás-csoport eseménynaplójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="cdee0-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="cdee0-134">Ez a parancs az aktuális dátumtól/időponttól számított 7 napon belül a megadott erőforráscsoporthoz tartozó eseményeket a legtöbb 1000 jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="cdee0-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-135">10. példa: erőforrás-csoport eseménynaplójának beszerzése maximális számú eseménnyel</span><span class="sxs-lookup"><span data-stu-id="cdee0-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="cdee0-136">Ez a parancs az aktuális dátumtól/időponttól számított 7 napig lezajlott, a megadott erőforráscsoporthoz tartozó 100-eseményekre vonatkozóan jeleníti meg a legtöbbet.</span><span class="sxs-lookup"><span data-stu-id="cdee0-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-137">11-es példa: az erőforráscsoport eseménynaplójának beszerzése kezdési időponttal</span><span class="sxs-lookup"><span data-stu-id="cdee0-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="cdee0-138">Ez a 1000 parancs a megadott erőforráscsoporthoz tartozó, a 2017-05-22T04:30:00 helyi idő alatt vagy azt követően, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="cdee0-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-139">12 példa: az erőforráscsoport eseménynaplójának beszerzése kezdési és befejezési időponttal</span><span class="sxs-lookup"><span data-stu-id="cdee0-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="cdee0-140">Ez a 1000 parancs a megadott erőforráscsoporthoz tartozó, a 2017-04-15T04:30 helyi idő után vagy a 2017-04-25T12:30 helyi idő, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz a megtartási időszakból.</span><span class="sxs-lookup"><span data-stu-id="cdee0-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="cdee0-141">Példa 13: erőforrás-AZONOSÍTÓval rendelkező esemény naplózása</span><span class="sxs-lookup"><span data-stu-id="cdee0-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="cdee0-142">Ez a parancs a megadott erőforrás-AZONOSÍTÓval társított legtöbb 1000-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot.</span><span class="sxs-lookup"><span data-stu-id="cdee0-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-143">14 példa: erőforrás-AZONOSÍTÓval beolvashatja az eseménynaplót, az események maximális száma</span><span class="sxs-lookup"><span data-stu-id="cdee0-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="cdee0-144">Ez a parancs a megadott erőforrás-AZONOSÍTÓval társított legtöbb 100-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot.</span><span class="sxs-lookup"><span data-stu-id="cdee0-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-145">15. példa: erőforrás-AZONOSÍTÓval rendelkező Eseménynapló beszerzése kezdési időponttal</span><span class="sxs-lookup"><span data-stu-id="cdee0-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="cdee0-146">Ezek a parancsok a megadott erőforrás-AZONOSÍTÓval társított legtöbb 1000-eseményen, illetve 2017-05-22T04:30:00 helyi idő szerint jelennek meg, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="cdee0-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-147">Példa 16: erőforrás-AZONOSÍTÓval rendelkező Eseménynapló beszerzése kezdési és befejezési időponttal</span><span class="sxs-lookup"><span data-stu-id="cdee0-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="cdee0-148">Ebben a parancsban a megadott erőforrás-AZONOSÍTÓval társított legtöbb 1000-eseményen (a 2017-04-15T04:30 helyi időpontban) vagy a 2017-04-25T12:30 helyi idő alatt, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz: a retenciós időszak.</span><span class="sxs-lookup"><span data-stu-id="cdee0-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="cdee0-149">Példa 17: erőforrás-szolgáltató eseménynaplójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="cdee0-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="cdee0-150">Ebben a parancsban a megadott erőforrás-szolgáltatóval társított legtöbb 1000-eseményen, az aktuális dátumtól és időponttól számított 7 nap volt látható.</span><span class="sxs-lookup"><span data-stu-id="cdee0-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-151">18. példa: az erőforrás-szolgáltató eseménynaplójának beszerzése maximális számú eseménnyel</span><span class="sxs-lookup"><span data-stu-id="cdee0-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="cdee0-152">Ebben a parancsban a megadott erőforrás-szolgáltatóval társított legtöbb 100-eseményen, az aktuális dátumtól és időponttól számított 7 nap volt látható.</span><span class="sxs-lookup"><span data-stu-id="cdee0-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-153">19. példa: erőforrás-szolgáltató eseménynaplójának beszerzése kezdési időponttal</span><span class="sxs-lookup"><span data-stu-id="cdee0-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="cdee0-154">Ez a parancs a megadott erőforrás-szolgáltatóval társított legtöbb 1000-eseményen, illetve 2017-05-22T04:30:00 helyi idő alatt, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="cdee0-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="cdee0-155">20 példa: az erőforrás-szolgáltató eseménynaplójának beszerzése kezdési és befejezési időponttal</span><span class="sxs-lookup"><span data-stu-id="cdee0-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="cdee0-156">Ebben a parancsban a megadott erőforrás-szolgáltatóval társított legtöbb 1000-eseményre vonatkozóan a 2017-04-15T04:30 helyi idő, de a 2017-04-25T12:30 helyi idő, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz: az adatmegőrzési időszak.</span><span class="sxs-lookup"><span data-stu-id="cdee0-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="cdee0-157">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdee0-157">PARAMETERS</span></span>

### <span data-ttu-id="cdee0-158">-Hívó</span><span class="sxs-lookup"><span data-stu-id="cdee0-158">-Caller</span></span>
<span data-ttu-id="cdee0-159">A beolvasni kívánt események hívója</span><span class="sxs-lookup"><span data-stu-id="cdee0-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="cdee0-160">-Verzióhttp://www.skype.com/hu/Business/Skype-for-Business/onedrive</span><span class="sxs-lookup"><span data-stu-id="cdee0-160">-CorrelationId</span></span>
<span data-ttu-id="cdee0-161">A Verzióhttp://www.skype.com/hu/Business/Skype-for-Business/onedrive</span><span class="sxs-lookup"><span data-stu-id="cdee0-161">The CorrelationId</span></span>

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

### <span data-ttu-id="cdee0-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdee0-162">-DefaultProfile</span></span>
<span data-ttu-id="cdee0-163">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdee0-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdee0-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="cdee0-164">-DetailedOutput</span></span>
<span data-ttu-id="cdee0-165">Visszatérési objektum az események összes részletével (az alapértelmezett az, ha csak bizonyos attribútumokat ad vissza, azaz nem részleteket)</span><span class="sxs-lookup"><span data-stu-id="cdee0-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

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

### <span data-ttu-id="cdee0-166">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="cdee0-166">-EndTime</span></span>
<span data-ttu-id="cdee0-167">A lekérdezés befejezési napja</span><span class="sxs-lookup"><span data-stu-id="cdee0-167">The endTime of the query</span></span>

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

### <span data-ttu-id="cdee0-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="cdee0-168">-MaxRecord</span></span>
<span data-ttu-id="cdee0-169">A beolvasni kívánt rekordok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="cdee0-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="cdee0-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="cdee0-170">Alias: MaxRecords, MaxEvents</span></span>

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

### <span data-ttu-id="cdee0-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdee0-171">-ResourceGroupName</span></span>
<span data-ttu-id="cdee0-172">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cdee0-172">The resource group name</span></span>

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

### <span data-ttu-id="cdee0-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdee0-173">-ResourceId</span></span>
<span data-ttu-id="cdee0-174">A ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdee0-174">The ResourceId</span></span>

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

### <span data-ttu-id="cdee0-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="cdee0-175">-ResourceProvider</span></span>
<span data-ttu-id="cdee0-176">A ResourceProvider neve</span><span class="sxs-lookup"><span data-stu-id="cdee0-176">The ResourceProvider name</span></span>

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

### <span data-ttu-id="cdee0-177">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="cdee0-177">-StartTime</span></span>
<span data-ttu-id="cdee0-178">A lekérdezés Verzióhttp://www.skype.com/hu/Business/Skype-for-Business/onedrive</span><span class="sxs-lookup"><span data-stu-id="cdee0-178">The correlationId of the query</span></span>

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

### <span data-ttu-id="cdee0-179">-Állapot</span><span class="sxs-lookup"><span data-stu-id="cdee0-179">-Status</span></span>
<span data-ttu-id="cdee0-180">A beolvasni kívánt események állapota</span><span class="sxs-lookup"><span data-stu-id="cdee0-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="cdee0-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdee0-181">CommonParameters</span></span>
<span data-ttu-id="cdee0-182">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdee0-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdee0-183">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cdee0-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdee0-184">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdee0-184">INPUTS</span></span>

### <span data-ttu-id="cdee0-185">System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cdee0-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cdee0-186">System. String</span><span class="sxs-lookup"><span data-stu-id="cdee0-186">System.String</span></span>

### <span data-ttu-id="cdee0-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cdee0-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="cdee0-188">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cdee0-188">System.Int32</span></span>

## <span data-ttu-id="cdee0-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdee0-189">OUTPUTS</span></span>

### <span data-ttu-id="cdee0-190">Microsoft. Azure. commands. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="cdee0-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="cdee0-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdee0-191">NOTES</span></span>

## <span data-ttu-id="cdee0-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdee0-192">RELATED LINKS</span></span>
