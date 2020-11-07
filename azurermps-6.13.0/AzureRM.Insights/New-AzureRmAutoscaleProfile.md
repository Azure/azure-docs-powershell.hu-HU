---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: 1d860c713c29fd10ba502150561e041c46a213aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680113"
---
# <span data-ttu-id="e0322-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="e0322-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="e0322-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0322-102">SYNOPSIS</span></span>
<span data-ttu-id="e0322-103">Automéretarányos profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e0322-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0322-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0322-104">SYNTAX</span></span>

### <span data-ttu-id="e0322-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="e0322-105">CreateWithoutScheduledTimes</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0322-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="e0322-106">CreateWithFixedDateScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0322-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="e0322-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0322-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0322-108">DESCRIPTION</span></span>
<span data-ttu-id="e0322-109">A **New-AzureRmAutoscaleProfile** parancsmag automéretarányos profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e0322-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="e0322-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e0322-110">EXAMPLES</span></span>

### <span data-ttu-id="e0322-111">1. példa: egyetlen profil létrehozása rögzített dátummal</span><span class="sxs-lookup"><span data-stu-id="e0322-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="e0322-112">Az első parancs létrehozza a kérések nevű automéretarányos szabályt, majd a $Rule változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0322-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="e0322-113">A második parancs egy Profile01 nevű profilt hoz létre rögzített dátummal az $Rule szabály használatával.</span><span class="sxs-lookup"><span data-stu-id="e0322-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="e0322-114">2. példa: profil létrehozása ütemtervvel</span><span class="sxs-lookup"><span data-stu-id="e0322-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="e0322-115">Az első parancs létrehozza a kérések nevű automéretarányos szabályt, majd a $Rule változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0322-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="e0322-116">A második parancs egy SecondProfileName nevű profilt hoz létre egy ismétlődő ütemezéssel a $Rule szabály segítségével.</span><span class="sxs-lookup"><span data-stu-id="e0322-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="e0322-117">3. példa: profilok létrehozása két szabállyal</span><span class="sxs-lookup"><span data-stu-id="e0322-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="e0322-118">Az első két parancs szabályokat hoz létre, és azokat a változók $Rule 1 és $Rule 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0322-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="e0322-119">A harmadik parancs a Szabály1 és a Rule2 szabályok segítségével hoz létre egy "fájlnév" nevű profilt, majd a $Profile 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0322-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="e0322-120">A végleges parancs létrehozza a SecondProfileName nevű profilt a Szabály1 és a Rule2 szabályait használva, majd a $Profile 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0322-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="e0322-121">Példa 4: profil létrehozása ütemezés vagy rögzített dátum nélkül</span><span class="sxs-lookup"><span data-stu-id="e0322-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="e0322-122">Az első parancs létrehozza a kérések nevű automéretarányos szabályt, majd a $Rule változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0322-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="e0322-123">A második parancs ütemterv vagy rögzített dátum nélkül hoz létre profilt, majd a $Profile változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0322-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="e0322-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0322-124">PARAMETERS</span></span>

### <span data-ttu-id="e0322-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="e0322-125">-DefaultCapacity</span></span>
<span data-ttu-id="e0322-126">Az alapértelmezett kapacitást adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="e0322-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0322-127">-DefaultProfile</span></span>
<span data-ttu-id="e0322-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e0322-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0322-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="e0322-129">-EndTimeWindow</span></span>
<span data-ttu-id="e0322-130">Az időpont ablakának végét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0322-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="e0322-131">-MaximumCapacity</span></span>
<span data-ttu-id="e0322-132">A maximális kapacitást adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-132">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="e0322-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="e0322-133">-MinimumCapacity</span></span>
<span data-ttu-id="e0322-134">A minimális kapacitást adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-134">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="e0322-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0322-135">-Name</span></span>
<span data-ttu-id="e0322-136">A létrehozandó profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-136">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="e0322-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="e0322-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="e0322-138">Az ismétlődés gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="e0322-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e0322-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e0322-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="e0322-140">None</span></span>
- <span data-ttu-id="e0322-141">Második</span><span class="sxs-lookup"><span data-stu-id="e0322-141">Second</span></span>
- <span data-ttu-id="e0322-142">Perces</span><span class="sxs-lookup"><span data-stu-id="e0322-142">Minute</span></span>
- <span data-ttu-id="e0322-143">Óra</span><span class="sxs-lookup"><span data-stu-id="e0322-143">Hour</span></span>
- <span data-ttu-id="e0322-144">Nap</span><span class="sxs-lookup"><span data-stu-id="e0322-144">Day</span></span>
- <span data-ttu-id="e0322-145">Héten</span><span class="sxs-lookup"><span data-stu-id="e0322-145">Week</span></span>
- <span data-ttu-id="e0322-146">Hónap</span><span class="sxs-lookup"><span data-stu-id="e0322-146">Month</span></span>
- <span data-ttu-id="e0322-147">Az év nem minden érték támogatott.</span><span class="sxs-lookup"><span data-stu-id="e0322-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0322-148">-Szabály</span><span class="sxs-lookup"><span data-stu-id="e0322-148">-Rule</span></span>
<span data-ttu-id="e0322-149">A profilhoz hozzáadni kívánt szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0322-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="e0322-150">-ScheduleDay</span></span>
<span data-ttu-id="e0322-151">Az ütemezett napokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0322-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="e0322-152">-ScheduleHour</span></span>
<span data-ttu-id="e0322-153">Az ütemezett órákat adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0322-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="e0322-154">-ScheduleMinute</span></span>
<span data-ttu-id="e0322-155">Az ütemezett perceket adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0322-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="e0322-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="e0322-157">Az ütemterv időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0322-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="e0322-158">-StartTimeWindow</span></span>
<span data-ttu-id="e0322-159">Az időpont ablak kezdetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0322-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="e0322-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="e0322-161">Az időpont ablak időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0322-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0322-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0322-162">CommonParameters</span></span>
<span data-ttu-id="e0322-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0322-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0322-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0322-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0322-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0322-165">INPUTS</span></span>

### <span data-ttu-id="e0322-166">System. String</span><span class="sxs-lookup"><span data-stu-id="e0322-166">System.String</span></span>

### <span data-ttu-id="e0322-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="e0322-167">System.DateTime</span></span>

### <span data-ttu-id="e0322-168">Microsoft. Azure. Management. monitor. Management. models. RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="e0322-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="e0322-169">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e0322-169">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e0322-170">System. Collections. Generic. list `1[[System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]], mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e0322-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]], mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e0322-171">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. models. ScaleRule, Microsoft. Azure. commands. ininsights, Version = 5.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e0322-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e0322-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0322-172">OUTPUTS</span></span>

### <span data-ttu-id="e0322-173">Microsoft. Azure. Management. monitor. Management. models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="e0322-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="e0322-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0322-174">NOTES</span></span>

## <span data-ttu-id="e0322-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0322-175">RELATED LINKS</span></span>

[<span data-ttu-id="e0322-176">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e0322-176">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="e0322-177">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="e0322-177">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="e0322-178">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e0322-178">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="e0322-179">Új – AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="e0322-179">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="e0322-180">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e0322-180">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


