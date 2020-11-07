---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: d82e63d21e18b7fb75282da9ac12be7644b0535a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672885"
---
# <span data-ttu-id="cc65e-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cc65e-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="cc65e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc65e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc65e-103">Automatizálási ütemtervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cc65e-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc65e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc65e-104">SYNTAX</span></span>

### <span data-ttu-id="cc65e-105">ByDaily (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc65e-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc65e-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="cc65e-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc65e-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="cc65e-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc65e-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="cc65e-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc65e-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="cc65e-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc65e-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="cc65e-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc65e-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc65e-111">DESCRIPTION</span></span>
<span data-ttu-id="cc65e-112">A **New-AzureRmAutomationSchedule** parancsmag ütemtervet hoz létre az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="cc65e-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="cc65e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="cc65e-113">EXAMPLES</span></span>

### <span data-ttu-id="cc65e-114">1. példa: egyszeri ütemezés létrehozása helyi időpontban</span><span class="sxs-lookup"><span data-stu-id="cc65e-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="cc65e-115">Az első parancs beolvassa az időzóna AZONOSÍTÓját a rendszerből, és a $TimeZone változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cc65e-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="cc65e-116">A második parancs olyan ütemtervet hoz létre, amely egyszer az aktuális dátumon fut a 11:00 ÓRAKOR a megadott időzónában.</span><span class="sxs-lookup"><span data-stu-id="cc65e-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="cc65e-117">2. példa: ismétlődő ütemezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="cc65e-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cc65e-118">Az első parancs a Date-objektumot a **Get-Date** parancsmag segítségével hozza létre, majd a $StartDate változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="cc65e-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="cc65e-119">Adja meg a jövőben legalább öt percet tartalmazó időpontot.</span><span class="sxs-lookup"><span data-stu-id="cc65e-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="cc65e-120">A második parancs a Date-objektumot a **Get-Date** parancsmag segítségével hozza létre, majd a $EndDate változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="cc65e-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="cc65e-121">A parancs a jövőbeli időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-121">The command specifies a future time.</span></span>

<span data-ttu-id="cc65e-122">A végleges parancs a Schedule01 nevű napi ütemtervet hozza létre a $StartDate-ban tárolt időponttól kezdődően, és a $EndDateban tárolt időpontban lejár.</span><span class="sxs-lookup"><span data-stu-id="cc65e-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="cc65e-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc65e-123">PARAMETERS</span></span>

### <span data-ttu-id="cc65e-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cc65e-124">-AutomationAccountName</span></span>
<span data-ttu-id="cc65e-125">Annak az automatizálási fióknak a neve, amelyhez a parancsmag létrehoz egy ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="cc65e-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="cc65e-126">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="cc65e-126">-DayInterval</span></span>
<span data-ttu-id="cc65e-127">Az ütemtervben a napokban megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="cc65e-128">Ha nem adja meg ezt a paramétert, és nem adja meg az *egykori* paramétert, az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="cc65e-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="cc65e-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="cc65e-129">-DayOfWeek</span></span>
<span data-ttu-id="cc65e-130">A heti ütemtervhez tartozó hét napjainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-130">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="cc65e-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="cc65e-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="cc65e-132">A hét előfordulását adja meg az ütemezés szerinti hónapon belül.</span><span class="sxs-lookup"><span data-stu-id="cc65e-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="cc65e-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="cc65e-133">psdx_paramvalues</span></span>

- <span data-ttu-id="cc65e-134">1</span><span class="sxs-lookup"><span data-stu-id="cc65e-134">1</span></span>
- <span data-ttu-id="cc65e-135">2</span><span class="sxs-lookup"><span data-stu-id="cc65e-135">2</span></span>
- <span data-ttu-id="cc65e-136">3</span><span class="sxs-lookup"><span data-stu-id="cc65e-136">3</span></span>
- <span data-ttu-id="cc65e-137">4</span><span class="sxs-lookup"><span data-stu-id="cc65e-137">4</span></span>
- <span data-ttu-id="cc65e-138">-1</span><span class="sxs-lookup"><span data-stu-id="cc65e-138">-1</span></span>
- <span data-ttu-id="cc65e-139">Első</span><span class="sxs-lookup"><span data-stu-id="cc65e-139">First</span></span>
- <span data-ttu-id="cc65e-140">Második</span><span class="sxs-lookup"><span data-stu-id="cc65e-140">Second</span></span>
- <span data-ttu-id="cc65e-141">Harmadik</span><span class="sxs-lookup"><span data-stu-id="cc65e-141">Third</span></span>
- <span data-ttu-id="cc65e-142">Negyedik</span><span class="sxs-lookup"><span data-stu-id="cc65e-142">Fourth</span></span>
- <span data-ttu-id="cc65e-143">LastDay</span><span class="sxs-lookup"><span data-stu-id="cc65e-143">LastDay</span></span>

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

### <span data-ttu-id="cc65e-144">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="cc65e-144">-DaysOfMonth</span></span>
<span data-ttu-id="cc65e-145">A havi ütemtervhez tartozó hónap napjainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-145">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="cc65e-146">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="cc65e-146">-DaysOfWeek</span></span>
<span data-ttu-id="cc65e-147">A heti ütemtervhez tartozó hét napjainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-147">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="cc65e-148">-Leírás</span><span class="sxs-lookup"><span data-stu-id="cc65e-148">-Description</span></span>
<span data-ttu-id="cc65e-149">Az ütemezés leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-149">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="cc65e-150">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cc65e-150">-ExpiryTime</span></span>
<span data-ttu-id="cc65e-151">Az ütemezés lejárati időpontját adja meg **DateTimeOffest** -objektumként.</span><span class="sxs-lookup"><span data-stu-id="cc65e-151">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="cc65e-152">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="cc65e-152">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="cc65e-153">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="cc65e-153">-HourInterval</span></span>
<span data-ttu-id="cc65e-154">Az ütemezéshez az órákban megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-154">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="cc65e-155">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="cc65e-155">-MonthInterval</span></span>
<span data-ttu-id="cc65e-156">A naptárban az ütemterv intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-156">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="cc65e-157">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc65e-157">-Name</span></span>
<span data-ttu-id="cc65e-158">Az ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-158">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="cc65e-159">-Egykori</span><span class="sxs-lookup"><span data-stu-id="cc65e-159">-OneTime</span></span>
<span data-ttu-id="cc65e-160">Azt adja meg, hogy a parancsmag egyszeres ütemtervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cc65e-160">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="cc65e-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc65e-161">-ResourceGroupName</span></span>
<span data-ttu-id="cc65e-162">Annak a csoportnak a neve, amelyhez a parancsmag létrehoz egy ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="cc65e-162">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="cc65e-163">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="cc65e-163">-StartTime</span></span>
<span data-ttu-id="cc65e-164">Az ütemezés kezdési időpontját **DateTimeOffset** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-164">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="cc65e-165">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="cc65e-165">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="cc65e-166">.</span><span class="sxs-lookup"><span data-stu-id="cc65e-166">.</span></span> <span data-ttu-id="cc65e-167">Ha meg van adva az *timezone* paraméter, a program figyelmen kívül hagyja az eltolást, és a megadott időzónát használja.</span><span class="sxs-lookup"><span data-stu-id="cc65e-167">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="cc65e-168">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="cc65e-168">-TimeZone</span></span>
<span data-ttu-id="cc65e-169">Az ütemterv időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-169">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="cc65e-170">Ez a karakterlánc lehet az IANA-azonosító vagy a Windows időzóna azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cc65e-170">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="cc65e-171">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="cc65e-171">-WeekInterval</span></span>
<span data-ttu-id="cc65e-172">Az ütemezésben a hetekben megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc65e-172">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="cc65e-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc65e-173">-DefaultProfile</span></span>
<span data-ttu-id="cc65e-174">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc65e-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc65e-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc65e-175">CommonParameters</span></span>
<span data-ttu-id="cc65e-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc65e-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc65e-177">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc65e-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc65e-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc65e-178">INPUTS</span></span>

## <span data-ttu-id="cc65e-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc65e-179">OUTPUTS</span></span>

### <span data-ttu-id="cc65e-180">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="cc65e-180">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="cc65e-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc65e-181">NOTES</span></span>

## <span data-ttu-id="cc65e-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc65e-182">RELATED LINKS</span></span>

[<span data-ttu-id="cc65e-183">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cc65e-183">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="cc65e-184">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cc65e-184">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="cc65e-185">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cc65e-185">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


