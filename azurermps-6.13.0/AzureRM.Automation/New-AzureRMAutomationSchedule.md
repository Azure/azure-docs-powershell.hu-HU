---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: 0672e7ab292046b79ceaad61446c30c210bcb535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502259"
---
# <span data-ttu-id="61c30-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="61c30-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="61c30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61c30-102">SYNOPSIS</span></span>
<span data-ttu-id="61c30-103">Automatizálási ütemtervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="61c30-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61c30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61c30-104">SYNTAX</span></span>

### <span data-ttu-id="61c30-105">ByDaily (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="61c30-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61c30-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="61c30-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61c30-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="61c30-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61c30-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="61c30-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61c30-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="61c30-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61c30-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="61c30-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61c30-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="61c30-111">DESCRIPTION</span></span>
<span data-ttu-id="61c30-112">A **New-AzureRmAutomationSchedule** parancsmag ütemtervet hoz létre az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="61c30-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="61c30-113">Példák</span><span class="sxs-lookup"><span data-stu-id="61c30-113">EXAMPLES</span></span>

### <span data-ttu-id="61c30-114">1. példa: egyszeri ütemezés létrehozása helyi időpontban</span><span class="sxs-lookup"><span data-stu-id="61c30-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="61c30-115">Az első parancs beolvassa az időzóna AZONOSÍTÓját a rendszerből, és a $TimeZone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="61c30-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="61c30-116">A második parancs olyan ütemtervet hoz létre, amely egyszer az aktuális dátumon fut a 11:00 ÓRAKOR a megadott időzónában.</span><span class="sxs-lookup"><span data-stu-id="61c30-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="61c30-117">2. példa: ismétlődő ütemezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="61c30-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="61c30-118">Az első parancs a Date-objektumot a **Get-Date** parancsmag segítségével hozza létre, majd a $StartDate változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="61c30-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="61c30-119">Adja meg a jövőben legalább öt percet tartalmazó időpontot.</span><span class="sxs-lookup"><span data-stu-id="61c30-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="61c30-120">A második parancs a Date-objektumot a **Get-Date** parancsmag segítségével hozza létre, majd a $EndDate változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="61c30-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="61c30-121">A parancs a jövőbeli időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-121">The command specifies a future time.</span></span>
<span data-ttu-id="61c30-122">A végleges parancs a Schedule02 nevű napi ütemtervet hozza létre a $StartDate-ban tárolt időponttól kezdődően, és a $EndDateban tárolt időpontban lejár.</span><span class="sxs-lookup"><span data-stu-id="61c30-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="61c30-123">3. példa: hetente ismétlődő ütemterv létrehozása</span><span class="sxs-lookup"><span data-stu-id="61c30-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="61c30-124">Az első parancs a Date-objektumot a **Get-Date** parancsmag segítségével hozza létre, majd a $StartDate változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="61c30-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="61c30-125">A második parancs a hét napjait a hétfő, kedd, szerda, csütörtök és péntek képletet tartalmazó tömbként hozza létre.</span><span class="sxs-lookup"><span data-stu-id="61c30-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="61c30-126">A végleges parancs létrehoz egy Schedule03 nevű napi ütemtervet, amely minden héten hétfőtől péntekig fog futni az 13:00-ben.</span><span class="sxs-lookup"><span data-stu-id="61c30-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="61c30-127">Az ütemezés sosem jár le.</span><span class="sxs-lookup"><span data-stu-id="61c30-127">The schedule will never expire.</span></span>

## <span data-ttu-id="61c30-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61c30-128">PARAMETERS</span></span>

### <span data-ttu-id="61c30-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="61c30-129">-AutomationAccountName</span></span>
<span data-ttu-id="61c30-130">Annak az automatizálási fióknak a neve, amelyhez a parancsmag létrehoz egy ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="61c30-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="61c30-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="61c30-131">-DayInterval</span></span>
<span data-ttu-id="61c30-132">Az ütemtervben a napokban megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="61c30-133">Ha nem adja meg ezt a paramétert, és nem adja meg az *egykori* paramétert, az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="61c30-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="61c30-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="61c30-134">-DayOfWeek</span></span>
<span data-ttu-id="61c30-135">A heti ütemtervhez tartozó hét napjainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="61c30-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="61c30-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="61c30-137">A hét előfordulását adja meg az ütemezés szerinti hónapon belül.</span><span class="sxs-lookup"><span data-stu-id="61c30-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="61c30-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="61c30-138">psdx_paramvalues</span></span>
- <span data-ttu-id="61c30-139">1</span><span class="sxs-lookup"><span data-stu-id="61c30-139">1</span></span>
- <span data-ttu-id="61c30-140">2</span><span class="sxs-lookup"><span data-stu-id="61c30-140">2</span></span>
- <span data-ttu-id="61c30-141">3</span><span class="sxs-lookup"><span data-stu-id="61c30-141">3</span></span>
- <span data-ttu-id="61c30-142">4</span><span class="sxs-lookup"><span data-stu-id="61c30-142">4</span></span>
- <span data-ttu-id="61c30-143">-1</span><span class="sxs-lookup"><span data-stu-id="61c30-143">-1</span></span>
- <span data-ttu-id="61c30-144">Első</span><span class="sxs-lookup"><span data-stu-id="61c30-144">First</span></span>
- <span data-ttu-id="61c30-145">Második</span><span class="sxs-lookup"><span data-stu-id="61c30-145">Second</span></span>
- <span data-ttu-id="61c30-146">Harmadik</span><span class="sxs-lookup"><span data-stu-id="61c30-146">Third</span></span>
- <span data-ttu-id="61c30-147">Negyedik</span><span class="sxs-lookup"><span data-stu-id="61c30-147">Fourth</span></span>
- <span data-ttu-id="61c30-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="61c30-148">LastDay</span></span>

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

### <span data-ttu-id="61c30-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="61c30-149">-DaysOfMonth</span></span>
<span data-ttu-id="61c30-150">A havi ütemtervhez tartozó hónap napjainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="61c30-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="61c30-151">-DaysOfWeek</span></span>
<span data-ttu-id="61c30-152">A heti ütemtervhez tartozó hét napjainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="61c30-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c30-153">-DefaultProfile</span></span>
<span data-ttu-id="61c30-154">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="61c30-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61c30-155">-Leírás</span><span class="sxs-lookup"><span data-stu-id="61c30-155">-Description</span></span>
<span data-ttu-id="61c30-156">Az ütemezés leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="61c30-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="61c30-157">-ExpiryTime</span></span>
<span data-ttu-id="61c30-158">Az ütemezés lejárati időpontját adja meg **DateTimeOffest** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="61c30-158">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="61c30-159">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="61c30-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="61c30-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="61c30-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="61c30-161">Azt jelzi, hogy ez az ütemezési objektum a szoftverfrissítési konfiguráció ütemezéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="61c30-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="61c30-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="61c30-162">-HourInterval</span></span>
<span data-ttu-id="61c30-163">Az ütemezéshez az órákban megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="61c30-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="61c30-164">-MonthInterval</span></span>
<span data-ttu-id="61c30-165">A naptárban az ütemterv intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="61c30-166">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="61c30-166">-Name</span></span>
<span data-ttu-id="61c30-167">Az ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="61c30-168">-Egykori</span><span class="sxs-lookup"><span data-stu-id="61c30-168">-OneTime</span></span>
<span data-ttu-id="61c30-169">Azt adja meg, hogy a parancsmag egyszeres ütemtervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="61c30-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="61c30-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c30-170">-ResourceGroupName</span></span>
<span data-ttu-id="61c30-171">Annak a csoportnak a neve, amelyhez a parancsmag létrehoz egy ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="61c30-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="61c30-172">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="61c30-172">-StartTime</span></span>
<span data-ttu-id="61c30-173">Az ütemezés kezdési időpontját **DateTimeOffset** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="61c30-174">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="61c30-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="61c30-175">Ha meg van adva az *timezone* paraméter, a program figyelmen kívül hagyja az eltolást, és a megadott időzónát használja.</span><span class="sxs-lookup"><span data-stu-id="61c30-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="61c30-176">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="61c30-176">-TimeZone</span></span>
<span data-ttu-id="61c30-177">Az ütemterv időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="61c30-178">Ez a karakterlánc lehet az IANA-azonosító vagy a Windows időzóna azonosítója.</span><span class="sxs-lookup"><span data-stu-id="61c30-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="61c30-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="61c30-179">-WeekInterval</span></span>
<span data-ttu-id="61c30-180">Az ütemezésben a hetekben megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="61c30-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="61c30-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c30-181">CommonParameters</span></span>
<span data-ttu-id="61c30-182">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61c30-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c30-183">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c30-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c30-184">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61c30-184">INPUTS</span></span>

### <span data-ttu-id="61c30-185">System. String</span><span class="sxs-lookup"><span data-stu-id="61c30-185">System.String</span></span>

### <span data-ttu-id="61c30-186">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61c30-186">System.DateTimeOffset</span></span>

## <span data-ttu-id="61c30-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61c30-187">OUTPUTS</span></span>

### <span data-ttu-id="61c30-188">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="61c30-188">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="61c30-189">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61c30-189">NOTES</span></span>

## <span data-ttu-id="61c30-190">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61c30-190">RELATED LINKS</span></span>

[<span data-ttu-id="61c30-191">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="61c30-191">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="61c30-192">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="61c30-192">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="61c30-193">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="61c30-193">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)

