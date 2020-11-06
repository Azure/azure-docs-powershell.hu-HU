---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: a5cea42544f2f24ad6c1f1cc1ce64bf122e53440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504152"
---
# <span data-ttu-id="77df5-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="77df5-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="77df5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77df5-102">SYNOPSIS</span></span>
<span data-ttu-id="77df5-103">Automéretarányos profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="77df5-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77df5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77df5-104">SYNTAX</span></span>

### <span data-ttu-id="77df5-105">New-AzureRmAutoscaleProfile parancsmag paraméterei ütemezett időpontok nélkül</span><span class="sxs-lookup"><span data-stu-id="77df5-105">Parameters for New-AzureRmAutoscaleProfile cmdlet without scheduled times</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77df5-106">New-AzureRmAutoscaleProfile parancsmag paramétereinek beállítása a javítás dátuma ütemezésével</span><span class="sxs-lookup"><span data-stu-id="77df5-106">Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77df5-107">New-AzureRmAutoscaleProfile parancsmag paraméterei ismétlődő ütemezés használatával</span><span class="sxs-lookup"><span data-stu-id="77df5-107">Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDays <System.Collections.Generic.List`1[System.String]>
 -ScheduleHours <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinutes <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77df5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="77df5-108">DESCRIPTION</span></span>
<span data-ttu-id="77df5-109">A **New-AzureRmAutoscaleProfile** parancsmag automéretarányos profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="77df5-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="77df5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="77df5-110">EXAMPLES</span></span>

### <span data-ttu-id="77df5-111">1. példa: egyetlen profil létrehozása rögzített dátummal</span><span class="sxs-lookup"><span data-stu-id="77df5-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="77df5-112">Az első parancs létrehozza a kérések nevű automéretarányos szabályt, majd a $Rule változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="77df5-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="77df5-113">A második parancs egy Profile01 nevű profilt hoz létre rögzített dátummal az $Rule szabály használatával.</span><span class="sxs-lookup"><span data-stu-id="77df5-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="77df5-114">2. példa: profil létrehozása ütemtervvel</span><span class="sxs-lookup"><span data-stu-id="77df5-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="77df5-115">Az első parancs létrehozza a kérések nevű automéretarányos szabályt, majd a $Rule változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="77df5-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="77df5-116">A második parancs egy SecondProfileName nevű profilt hoz létre egy ismétlődő ütemezéssel a $Rule szabály segítségével.</span><span class="sxs-lookup"><span data-stu-id="77df5-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="77df5-117">3. példa: profilok létrehozása két szabállyal</span><span class="sxs-lookup"><span data-stu-id="77df5-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="77df5-118">Az első két parancs szabályokat hoz létre, és azokat a változók $Rule 1 és $Rule 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="77df5-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="77df5-119">A harmadik parancs a Szabály1 és a Rule2 szabályok segítségével hoz létre egy "fájlnév" nevű profilt, majd a $Profile 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="77df5-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="77df5-120">A végleges parancs létrehozza a SecondProfileName nevű profilt a Szabály1 és a Rule2 szabályait használva, majd a $Profile 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="77df5-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="77df5-121">Példa 4: profil létrehozása ütemezés vagy rögzített dátum nélkül</span><span class="sxs-lookup"><span data-stu-id="77df5-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="77df5-122">Az első parancs létrehozza a kérések nevű automéretarányos szabályt, majd a $Rule változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="77df5-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="77df5-123">A második parancs ütemterv vagy rögzített dátum nélkül hoz létre profilt, majd a $Profile változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="77df5-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="77df5-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77df5-124">PARAMETERS</span></span>

### <span data-ttu-id="77df5-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="77df5-125">-DefaultCapacity</span></span>
<span data-ttu-id="77df5-126">Az alapértelmezett kapacitást adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="77df5-127">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="77df5-127">-EndTimeWindow</span></span>
<span data-ttu-id="77df5-128">Az időpont ablakának végét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-128">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77df5-129">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="77df5-129">-MaximumCapacity</span></span>
<span data-ttu-id="77df5-130">A maximális kapacitást adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-130">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="77df5-131">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="77df5-131">-MinimumCapacity</span></span>
<span data-ttu-id="77df5-132">A minimális kapacitást adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-132">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="77df5-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77df5-133">-Name</span></span>
<span data-ttu-id="77df5-134">A létrehozandó profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-134">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="77df5-135">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="77df5-135">-RecurrenceFrequency</span></span>
<span data-ttu-id="77df5-136">Az ismétlődés gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-136">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="77df5-137">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="77df5-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="77df5-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="77df5-138">None</span></span>
- <span data-ttu-id="77df5-139">Második</span><span class="sxs-lookup"><span data-stu-id="77df5-139">Second</span></span>
- <span data-ttu-id="77df5-140">Perces</span><span class="sxs-lookup"><span data-stu-id="77df5-140">Minute</span></span>
- <span data-ttu-id="77df5-141">Óra</span><span class="sxs-lookup"><span data-stu-id="77df5-141">Hour</span></span>
- <span data-ttu-id="77df5-142">Nap</span><span class="sxs-lookup"><span data-stu-id="77df5-142">Day</span></span>
- <span data-ttu-id="77df5-143">Héten</span><span class="sxs-lookup"><span data-stu-id="77df5-143">Week</span></span>
- <span data-ttu-id="77df5-144">Hónap</span><span class="sxs-lookup"><span data-stu-id="77df5-144">Month</span></span>
- <span data-ttu-id="77df5-145">Év</span><span class="sxs-lookup"><span data-stu-id="77df5-145">Year</span></span>

<span data-ttu-id="77df5-146">Nem mindegyik érték támogatott.</span><span class="sxs-lookup"><span data-stu-id="77df5-146">Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77df5-147">-Szabályok</span><span class="sxs-lookup"><span data-stu-id="77df5-147">-Rules</span></span>
<span data-ttu-id="77df5-148">A profilhoz hozzáadni kívánt szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-148">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="77df5-149">-ScheduleDays</span><span class="sxs-lookup"><span data-stu-id="77df5-149">-ScheduleDays</span></span>
<span data-ttu-id="77df5-150">Az ütemezett napokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-150">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77df5-151">-ScheduleHours</span><span class="sxs-lookup"><span data-stu-id="77df5-151">-ScheduleHours</span></span>
<span data-ttu-id="77df5-152">Az ütemezett órákat adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-152">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77df5-153">-ScheduleMinutes</span><span class="sxs-lookup"><span data-stu-id="77df5-153">-ScheduleMinutes</span></span>
<span data-ttu-id="77df5-154">Az ütemezett perceket adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-154">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77df5-155">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="77df5-155">-ScheduleTimeZone</span></span>
<span data-ttu-id="77df5-156">Az ütemterv időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-156">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77df5-157">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="77df5-157">-StartTimeWindow</span></span>
<span data-ttu-id="77df5-158">Az időpont ablak kezdetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-158">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77df5-159">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="77df5-159">-TimeWindowTimeZone</span></span>
<span data-ttu-id="77df5-160">Az időpont ablak időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="77df5-160">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77df5-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77df5-161">-DefaultProfile</span></span>
<span data-ttu-id="77df5-162">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77df5-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77df5-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77df5-163">CommonParameters</span></span>
<span data-ttu-id="77df5-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77df5-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77df5-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77df5-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77df5-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77df5-166">INPUTS</span></span>

## <span data-ttu-id="77df5-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77df5-167">OUTPUTS</span></span>

### <span data-ttu-id="77df5-168">Microsoft. Azure. Management. monitor. Management. models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="77df5-168">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="77df5-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77df5-169">NOTES</span></span>

## <span data-ttu-id="77df5-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77df5-170">RELATED LINKS</span></span>

[<span data-ttu-id="77df5-171">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="77df5-171">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="77df5-172">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="77df5-172">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="77df5-173">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="77df5-173">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="77df5-174">Új – AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="77df5-174">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="77df5-175">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="77df5-175">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


