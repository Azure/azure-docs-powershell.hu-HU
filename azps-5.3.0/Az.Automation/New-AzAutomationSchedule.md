---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 9f9cd5b779fcc4e1b9dd6f3df7ed0255adeaa3af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478613"
---
# <span data-ttu-id="9fa73-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9fa73-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="9fa73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fa73-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa73-103">Automatizálási ütemezést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9fa73-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="9fa73-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9fa73-104">SYNTAX</span></span>

### <span data-ttu-id="9fa73-105">ByDaily (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9fa73-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fa73-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="9fa73-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fa73-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="9fa73-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fa73-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="9fa73-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fa73-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="9fa73-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fa73-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="9fa73-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fa73-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9fa73-111">DESCRIPTION</span></span>
<span data-ttu-id="9fa73-112">A **New-AzAutomationSchedule** parancsmag létrehoz egy ütemezést az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="9fa73-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="9fa73-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9fa73-113">EXAMPLES</span></span>

### <span data-ttu-id="9fa73-114">1. példa: Egyszeres ütemezés létrehozása helyi idő szerint</span><span class="sxs-lookup"><span data-stu-id="9fa73-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="9fa73-115">Az első parancs lekérte az időzóna-azonosítót a rendszerből, és a $TimeZone tárolja.</span><span class="sxs-lookup"><span data-stu-id="9fa73-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="9fa73-116">A második parancs létrehoz egy ütemezést, amely egyszer fut az aktuális dátumon 11:00 órakor a megadott időzónában.</span><span class="sxs-lookup"><span data-stu-id="9fa73-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="9fa73-117">2. példa: Ismétlődő ütemezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="9fa73-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9fa73-118">Az első parancs a **Get-Date** parancsmag használatával létrehoz egy dátumobjektumot, majd az objektumot a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9fa73-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="9fa73-119">Adjon meg egy olyan időt, amely a jövőben legalább öt perc.</span><span class="sxs-lookup"><span data-stu-id="9fa73-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="9fa73-120">A második parancs a **Get-Date** parancsmag használatával hoz létre dátumobjektumot, majd az objektumot a $EndDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="9fa73-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="9fa73-121">A parancs egy jövőbeli időt ad meg.</span><span class="sxs-lookup"><span data-stu-id="9fa73-121">The command specifies a future time.</span></span>
<span data-ttu-id="9fa73-122">Az utolsó parancs létrehoz egy Schedule02 nevű napi ütemezést, amely a $StartDate tárolt időpontban kezdődik, és a $EndDate.</span><span class="sxs-lookup"><span data-stu-id="9fa73-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="9fa73-123">3. példa: Heti ismétlődő ütemezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="9fa73-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9fa73-124">Az első parancs a **Get-Date** parancsmag használatával létrehoz egy dátumobjektumot, majd az objektumot a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9fa73-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="9fa73-125">A második parancs létrehozza a hét napjainak tömbét, amely tartalmazza a hétfőt, keddet, szerdát, csütörtököt és pénteket.</span><span class="sxs-lookup"><span data-stu-id="9fa73-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="9fa73-126">Az utolsó parancs létrehoz egy Schedule03 nevű napi ütemezést, amely minden héten 13:00-kor hétfőtől péntekig tart.</span><span class="sxs-lookup"><span data-stu-id="9fa73-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="9fa73-127">Az ütemezés soha nem jár le.</span><span class="sxs-lookup"><span data-stu-id="9fa73-127">The schedule will never expire.</span></span>

## <span data-ttu-id="9fa73-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fa73-128">PARAMETERS</span></span>

### <span data-ttu-id="9fa73-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9fa73-129">-AutomationAccountName</span></span>
<span data-ttu-id="9fa73-130">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag ütemezést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9fa73-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="9fa73-131">-DayInterval</span></span>
<span data-ttu-id="9fa73-132">Az ütemezés intervallumát adja meg napokban.</span><span class="sxs-lookup"><span data-stu-id="9fa73-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="9fa73-133">Ha nem adja meg ezt a paramétert, és nem adja meg a *OneTime* paramétert, az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="9fa73-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByDaily
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="9fa73-134">-DayOfWeek</span></span>
<span data-ttu-id="9fa73-135">A hét napjainak listáját adja meg a heti ütemezéshez.</span><span class="sxs-lookup"><span data-stu-id="9fa73-135">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.Nullable`1[System.DayOfWeek]
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="9fa73-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="9fa73-137">A hétnek az ütemezés szerinti hónapon belüli előfordulását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fa73-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="9fa73-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="9fa73-138">psdx_paramvalues</span></span>
- <span data-ttu-id="9fa73-139">1</span><span class="sxs-lookup"><span data-stu-id="9fa73-139">1</span></span>
- <span data-ttu-id="9fa73-140">2</span><span class="sxs-lookup"><span data-stu-id="9fa73-140">2</span></span>
- <span data-ttu-id="9fa73-141">3</span><span class="sxs-lookup"><span data-stu-id="9fa73-141">3</span></span>
- <span data-ttu-id="9fa73-142">4</span><span class="sxs-lookup"><span data-stu-id="9fa73-142">4</span></span>
- <span data-ttu-id="9fa73-143">-1</span><span class="sxs-lookup"><span data-stu-id="9fa73-143">-1</span></span>
- <span data-ttu-id="9fa73-144">Első</span><span class="sxs-lookup"><span data-stu-id="9fa73-144">First</span></span>
- <span data-ttu-id="9fa73-145">Másodperc</span><span class="sxs-lookup"><span data-stu-id="9fa73-145">Second</span></span>
- <span data-ttu-id="9fa73-146">Harmadik</span><span class="sxs-lookup"><span data-stu-id="9fa73-146">Third</span></span>
- <span data-ttu-id="9fa73-147">Negyedik</span><span class="sxs-lookup"><span data-stu-id="9fa73-147">Fourth</span></span>
- <span data-ttu-id="9fa73-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="9fa73-148">LastDay</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="9fa73-149">-DaysOfMonth</span></span>
<span data-ttu-id="9fa73-150">A havi ütemezés hónap napjainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fa73-150">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases:
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="9fa73-151">-DaysOfWeek</span></span>
<span data-ttu-id="9fa73-152">A hét napjainak listáját adja meg a heti ütemezéshez.</span><span class="sxs-lookup"><span data-stu-id="9fa73-152">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: ByWeekly
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa73-153">-DefaultProfile</span></span>
<span data-ttu-id="9fa73-154">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9fa73-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fa73-155">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9fa73-155">-Description</span></span>
<span data-ttu-id="9fa73-156">Megadja az ütemterv leírását.</span><span class="sxs-lookup"><span data-stu-id="9fa73-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="9fa73-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9fa73-157">-ExpiryTime</span></span>
<span data-ttu-id="9fa73-158">Az ütemezés lejárati idejét adja meg **DateTimeOffset** objektumként.</span><span class="sxs-lookup"><span data-stu-id="9fa73-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="9fa73-159">Megadhat egy olyan karakterláncot, amely érvényes **DateTimeOffset** formátumra konvertálható.</span><span class="sxs-lookup"><span data-stu-id="9fa73-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fa73-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="9fa73-161">Azt jelzi, hogy ezt az ütemezési objektumot szoftverfrissítés-konfiguráció ütemezéséhez fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="9fa73-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="9fa73-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="9fa73-162">-HourInterval</span></span>
<span data-ttu-id="9fa73-163">Az ütemezés intervallumát adja meg órában.</span><span class="sxs-lookup"><span data-stu-id="9fa73-163">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByHourly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="9fa73-164">-MonthInterval</span></span>
<span data-ttu-id="9fa73-165">Az ütemezés intervallumát adja meg a Hónapok mezőben.</span><span class="sxs-lookup"><span data-stu-id="9fa73-165">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-166">-Name</span><span class="sxs-lookup"><span data-stu-id="9fa73-166">-Name</span></span>
<span data-ttu-id="9fa73-167">Az ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fa73-167">Specifies a name for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="9fa73-168">-OneTime</span></span>
<span data-ttu-id="9fa73-169">Azt adja meg, hogy a parancsmag egyszeres ütemezést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9fa73-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByOneTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa73-170">-ResourceGroupName</span></span>
<span data-ttu-id="9fa73-171">Annak az erőforráscsoportnak a nevét adja meg, amelyhez ez a parancsmag ütemezést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9fa73-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9fa73-172">-StartTime</span></span>
<span data-ttu-id="9fa73-173">Az ütemezés kezdési idejét adja meg **DateTimeOffset** objektumként.</span><span class="sxs-lookup"><span data-stu-id="9fa73-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="9fa73-174">Megadhat egy olyan karakterláncot, amely érvényes **DateTimeOffset** formátumra konvertálható.</span><span class="sxs-lookup"><span data-stu-id="9fa73-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="9fa73-175">Ha a *TimeZone* paraméter meg van adva, a program figyelmen kívül hagyja az eltolást, és a megadott időzónát használja.</span><span class="sxs-lookup"><span data-stu-id="9fa73-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="9fa73-176">-TimeZone</span></span>
<span data-ttu-id="9fa73-177">Az ütemezés időzónáját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="9fa73-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="9fa73-178">Ez a karakterlánc lehet az IANA-azonosító vagy a Windows időzóna-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9fa73-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="9fa73-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="9fa73-179">-WeekInterval</span></span>
<span data-ttu-id="9fa73-180">Az ütemezés intervallumát adja meg hetekben.</span><span class="sxs-lookup"><span data-stu-id="9fa73-180">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByWeekly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa73-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa73-181">CommonParameters</span></span>
<span data-ttu-id="9fa73-182">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa73-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa73-183">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa73-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa73-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fa73-184">INPUTS</span></span>

### <span data-ttu-id="9fa73-185">System.String</span><span class="sxs-lookup"><span data-stu-id="9fa73-185">System.String</span></span>

### <span data-ttu-id="9fa73-186">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9fa73-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="9fa73-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9fa73-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9fa73-188">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fa73-188">OUTPUTS</span></span>

### <span data-ttu-id="9fa73-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="9fa73-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="9fa73-190">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9fa73-190">NOTES</span></span>

## <span data-ttu-id="9fa73-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fa73-191">RELATED LINKS</span></span>

[<span data-ttu-id="9fa73-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9fa73-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="9fa73-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9fa73-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="9fa73-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9fa73-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


