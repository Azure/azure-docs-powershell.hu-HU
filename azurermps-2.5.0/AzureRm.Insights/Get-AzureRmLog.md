---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlog
schema: 2.0.0
ms.openlocfilehash: 2c63efe0d22f1582b0828f595ba8a72cd389b435
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848302"
---
# <span data-ttu-id="968e3-101">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="968e3-101">Get-AzureRmLog</span></span>

## <span data-ttu-id="968e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="968e3-102">SYNOPSIS</span></span>
<span data-ttu-id="968e3-103">Naplózza az eseményeket.</span><span class="sxs-lookup"><span data-stu-id="968e3-103">Gets a log of events.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="968e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="968e3-104">SYNTAX</span></span>

### <span data-ttu-id="968e3-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="968e3-105">GetByCorrelationId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="968e3-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="968e3-106">GetByResourceId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="968e3-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="968e3-107">GetByResourceGroup</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="968e3-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="968e3-108">GetByResourceProvider</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="968e3-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="968e3-109">GetBySubscription</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="968e3-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="968e3-110">DESCRIPTION</span></span>
<span data-ttu-id="968e3-111">A **Get-AzureRmLog** parancsmag események naplózását kapja.</span><span class="sxs-lookup"><span data-stu-id="968e3-111">The **Get-AzureRmLog** cmdlet gets a log of events.</span></span>
<span data-ttu-id="968e3-112">Az események az aktuális előfizetési AZONOSÍTÓval, korrelációs AZONOSÍTÓval, erőforrás csoporttal, erőforrás-AZONOSÍTÓval vagy erőforrás-szolgáltatóval kapcsolhatók be.</span><span class="sxs-lookup"><span data-stu-id="968e3-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="968e3-113">Példák</span><span class="sxs-lookup"><span data-stu-id="968e3-113">EXAMPLES</span></span>

### <span data-ttu-id="968e3-114">Példa 1: esemény naplójának beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="968e3-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzureRmLog
```

<span data-ttu-id="968e3-115">Ez a parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, az aktuális dátumtól/időponttól számított 7 napot tartalmazó legtöbb 1000-eseményben szerepel.</span><span class="sxs-lookup"><span data-stu-id="968e3-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-116">2. példa: az esemény naplójának beszerzése előfizetés-AZONOSÍTÓval maximális számú eseménnyel</span><span class="sxs-lookup"><span data-stu-id="968e3-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

<span data-ttu-id="968e3-117">Ez a parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, az aktuális dátumtól/időponttól számított 7 napot tartalmazó legtöbb 100-eseményben szerepel.</span><span class="sxs-lookup"><span data-stu-id="968e3-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-118">3. példa: az előfizetési AZONOSÍTÓval beolvashatja az eseménynaplót kezdési időponttal.</span><span class="sxs-lookup"><span data-stu-id="968e3-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="968e3-119">Ez a parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, a 2017-06-01T10:30 helyi időpontra, illetve az aktuális dátumtól/időponttól számított 30 napnál nem régebbi 90 verzió esetén jeleníti meg a legtöbb 1000-eseményt.</span><span class="sxs-lookup"><span data-stu-id="968e3-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-120">Példa 4: az esemény naplójának beszerzése előfizetéses AZONOSÍTÓval a kezdési és befejezési időponttal.</span><span class="sxs-lookup"><span data-stu-id="968e3-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="968e3-121">Ez a 1000 parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, a 2017-04-01T10:30 helyi idő, illetve 2017-04-14T11:30 helyi idő, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz a megtartási időszakból.</span><span class="sxs-lookup"><span data-stu-id="968e3-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="968e3-122">Példa 5: esemény naplójának beszerzése korrelációs AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="968e3-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="968e3-123">Ez a parancs a megadott korrelációs AZONOSÍTÓval társított legtöbb 1000-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot.</span><span class="sxs-lookup"><span data-stu-id="968e3-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="968e3-124">**Megjegyzés** : ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="968e3-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="968e3-125">6. példa: a korrelációs AZONOSÍTÓval beolvashatja az eseménynaplót az események maximális számával.</span><span class="sxs-lookup"><span data-stu-id="968e3-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

<span data-ttu-id="968e3-126">Ez a parancs a megadott korrelációs AZONOSÍTÓval társított legtöbb 100-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot.</span><span class="sxs-lookup"><span data-stu-id="968e3-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="968e3-127">**Megjegyzés** : ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="968e3-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="968e3-128">7. példa: események naplózása a korrelációs AZONOSÍTÓval és a kezdési időponttal</span><span class="sxs-lookup"><span data-stu-id="968e3-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="968e3-129">Ez a parancs a 1000-es számú, a 2017-05-22T04:30:00 helyi idő alatt vagy azt követően a megadott korrelációs AZONOSÍTÓval társított legtöbb-eseményen szerepel, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="968e3-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="968e3-130">**Megjegyzés** : ez általában csak egy esemény.</span><span class="sxs-lookup"><span data-stu-id="968e3-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="968e3-131">8. példa: esemény naplójának beszerzése korrelációs AZONOSÍTÓval a kezdési és befejezési időponttal</span><span class="sxs-lookup"><span data-stu-id="968e3-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="968e3-132">Ez a parancs a megadott korrelációs AZONOSÍTÓval társított legtöbb 1000-eseményen (2017-04-15T04:30 helyi időpontban) vagy a 2017-04-25T12:30 helyi idő alatt, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz: a retenciós időszak.</span><span class="sxs-lookup"><span data-stu-id="968e3-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="968e3-133">Példa 9: erőforrás-csoport eseménynaplójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="968e3-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="968e3-134">Ez a parancs az aktuális dátumtól/időponttól számított 7 napon belül a megadott erőforráscsoporthoz tartozó eseményeket a legtöbb 1000 jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="968e3-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-135">10. példa: erőforrás-csoport eseménynaplójának beszerzése maximális számú eseménnyel</span><span class="sxs-lookup"><span data-stu-id="968e3-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

<span data-ttu-id="968e3-136">Ez a parancs az aktuális dátumtól/időponttól számított 7 napig lezajlott, a megadott erőforráscsoporthoz tartozó 100-eseményekre vonatkozóan jeleníti meg a legtöbbet.</span><span class="sxs-lookup"><span data-stu-id="968e3-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-137">11-es példa: az erőforráscsoport eseménynaplójának beszerzése kezdési időponttal</span><span class="sxs-lookup"><span data-stu-id="968e3-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="968e3-138">Ez a parancs a megadott erőforráscsoporthoz tartozó, a 2017-05-22T04:30:00-as helyi időponttal társított legtöbb 1000-evetns jeleníti meg, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="968e3-138">This command lists at most 1000 evetns associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-139">12 példa: az erőforráscsoport eseménynaplójának beszerzése kezdési és befejezési időponttal</span><span class="sxs-lookup"><span data-stu-id="968e3-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="968e3-140">Ez a 1000 parancs a megadott erőforráscsoporthoz tartozó, a 2017-04-15T04:30 helyi idő után vagy a 2017-04-25T12:30 helyi idő, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz a megtartási időszakból.</span><span class="sxs-lookup"><span data-stu-id="968e3-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="968e3-141">Példa 13: erőforrás-AZONOSÍTÓval rendelkező esemény naplózása</span><span class="sxs-lookup"><span data-stu-id="968e3-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="968e3-142">Ez a parancs a megadott erőforrás-AZONOSÍTÓval társított legtöbb 1000-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot.</span><span class="sxs-lookup"><span data-stu-id="968e3-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-143">14 példa: erőforrás-AZONOSÍTÓval beolvashatja az eseménynaplót, az események maximális száma</span><span class="sxs-lookup"><span data-stu-id="968e3-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

<span data-ttu-id="968e3-144">Ez a parancs a megadott erőforrás-AZONOSÍTÓval társított legtöbb 100-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot.</span><span class="sxs-lookup"><span data-stu-id="968e3-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-145">15. példa: erőforrás-AZONOSÍTÓval rendelkező Eseménynapló beszerzése kezdési időponttal</span><span class="sxs-lookup"><span data-stu-id="968e3-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="968e3-146">Ezek a parancsok a megadott erőforrás-AZONOSÍTÓval társított legtöbb 1000-eseményen, illetve 2017-05-22T04:30:00 helyi idő szerint jelennek meg, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="968e3-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-147">Példa 16: erőforrás-AZONOSÍTÓval rendelkező Eseménynapló beszerzése kezdési és befejezési időponttal</span><span class="sxs-lookup"><span data-stu-id="968e3-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="968e3-148">Ebben a parancsban a megadott erőforrás-AZONOSÍTÓval társított legtöbb 1000-eseményen (a 2017-04-15T04:30 helyi időpontban) vagy a 2017-04-25T12:30 helyi idő alatt, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz: a retenciós időszak.</span><span class="sxs-lookup"><span data-stu-id="968e3-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="968e3-149">Példa 17: erőforrás-szolgáltató eseménynaplójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="968e3-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="968e3-150">Ebben a parancsban a megadott erőforrás-szolgáltatóval társított legtöbb 1000-eseményen, az aktuális dátumtól és időponttól számított 7 nap volt látható.</span><span class="sxs-lookup"><span data-stu-id="968e3-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-151">18. példa: az erőforrás-szolgáltató eseménynaplójának beszerzése maximális számú eseménnyel</span><span class="sxs-lookup"><span data-stu-id="968e3-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

<span data-ttu-id="968e3-152">Ebben a parancsban a megadott erőforrás-szolgáltatóval társított legtöbb 100-eseményen, az aktuális dátumtól és időponttól számított 7 nap volt látható.</span><span class="sxs-lookup"><span data-stu-id="968e3-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-153">19. példa: erőforrás-szolgáltató eseménynaplójának beszerzése kezdési időponttal</span><span class="sxs-lookup"><span data-stu-id="968e3-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="968e3-154">Ez a parancs a megadott erőforrás-szolgáltatóval társított legtöbb 1000-eseményen, illetve 2017-05-22T04:30:00 helyi idő alatt, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.</span><span class="sxs-lookup"><span data-stu-id="968e3-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="968e3-155">20 példa: az erőforrás-szolgáltató eseménynaplójának beszerzése kezdési és befejezési időponttal</span><span class="sxs-lookup"><span data-stu-id="968e3-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="968e3-156">Ebben a parancsban a megadott erőforrás-szolgáltatóval társított legtöbb 1000-eseményre vonatkozóan a 2017-04-15T04:30 helyi idő, de a 2017-04-25T12:30 helyi idő, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz: az adatmegőrzési időszak.</span><span class="sxs-lookup"><span data-stu-id="968e3-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="968e3-157">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="968e3-157">PARAMETERS</span></span>

### <span data-ttu-id="968e3-158">-Hívó</span><span class="sxs-lookup"><span data-stu-id="968e3-158">-Caller</span></span>
<span data-ttu-id="968e3-159">A hívót adja meg.</span><span class="sxs-lookup"><span data-stu-id="968e3-159">Specifies a caller.</span></span>

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

### <span data-ttu-id="968e3-160">-Verzióhttp://www.skype.com/hu/Business/Skype-for-Business/onedrive</span><span class="sxs-lookup"><span data-stu-id="968e3-160">-CorrelationId</span></span>
<span data-ttu-id="968e3-161">A korrelációs azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="968e3-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="968e3-162">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="968e3-162">This parameter is required.</span></span>

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

### <span data-ttu-id="968e3-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968e3-163">-DefaultProfile</span></span>
<span data-ttu-id="968e3-164">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="968e3-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="968e3-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="968e3-165">-DetailedOutput</span></span>
<span data-ttu-id="968e3-166">Azt jelzi, hogy ez a parancsmag részletes kimenetet jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="968e3-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="968e3-167">A program alapértelmezés szerint összesíti a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="968e3-167">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="968e3-168">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="968e3-168">-EndTime</span></span>
<span data-ttu-id="968e3-169">A lekérdezés befejezési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="968e3-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="968e3-170">Az alapértelmezett érték az aktuális idő.</span><span class="sxs-lookup"><span data-stu-id="968e3-170">The default value is the current time.</span></span>
<span data-ttu-id="968e3-171">Az értéknek a kezdésnél *StartTime* későbbinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="968e3-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="968e3-172">A Get-Date parancsmaggal **datetime** -objektumot is beszerezhet.</span><span class="sxs-lookup"><span data-stu-id="968e3-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="968e3-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="968e3-173">-MaxRecord</span></span>
<span data-ttu-id="968e3-174">A megadott szűrőhöz beolvasott rekordok teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="968e3-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="968e3-175">Az alapértelmezett érték a 1000, a maximálisan elfogadott érték pedig 100000.</span><span class="sxs-lookup"><span data-stu-id="968e3-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="968e3-176">A program figyelmen kívül hagyja a negatív értékeket és a 0 értéket, és az alapértelmezett értéket fogja használni.</span><span class="sxs-lookup"><span data-stu-id="968e3-176">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="968e3-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="968e3-177">-ResourceGroupName</span></span>
<span data-ttu-id="968e3-178">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="968e3-178">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="968e3-179">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="968e3-179">-ResourceId</span></span>
<span data-ttu-id="968e3-180">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="968e3-180">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="968e3-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="968e3-181">-ResourceProvider</span></span>
<span data-ttu-id="968e3-182">Az erőforrás-szolgáltató szerinti szűrést adja meg.</span><span class="sxs-lookup"><span data-stu-id="968e3-182">Specifies a filter by resource provider.</span></span>

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

### <span data-ttu-id="968e3-183">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="968e3-183">-StartTime</span></span>
<span data-ttu-id="968e3-184">A lekérdezés kezdési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="968e3-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="968e3-185">Az alapértelmezett érték a *befejezési* hét napja mínusz.</span><span class="sxs-lookup"><span data-stu-id="968e3-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="968e3-186">A Get-Date parancsmaggal **datetime** -objektumot is beszerezhet.</span><span class="sxs-lookup"><span data-stu-id="968e3-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="968e3-187">-Állapot</span><span class="sxs-lookup"><span data-stu-id="968e3-187">-Status</span></span>
<span data-ttu-id="968e3-188">Az állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="968e3-188">Specifies the status.</span></span>

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

### <span data-ttu-id="968e3-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968e3-189">CommonParameters</span></span>
<span data-ttu-id="968e3-190">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="968e3-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968e3-191">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="968e3-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968e3-192">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="968e3-192">INPUTS</span></span>

### <span data-ttu-id="968e3-193">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="968e3-193">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="968e3-194">System. String</span><span class="sxs-lookup"><span data-stu-id="968e3-194">System.String</span></span>

### <span data-ttu-id="968e3-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="968e3-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="968e3-196">System. Int32</span><span class="sxs-lookup"><span data-stu-id="968e3-196">System.Int32</span></span>

## <span data-ttu-id="968e3-197">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="968e3-197">OUTPUTS</span></span>

### <span data-ttu-id="968e3-198">Microsoft. Azure. commands. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="968e3-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="968e3-199">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="968e3-199">NOTES</span></span>

## <span data-ttu-id="968e3-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="968e3-200">RELATED LINKS</span></span>
