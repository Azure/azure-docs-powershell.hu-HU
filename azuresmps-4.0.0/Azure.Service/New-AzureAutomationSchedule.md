---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D28DD808-E8EF-4C71-A353-8BF1E458DF6F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9fcae4a0232331a020a716b3f7284b8f6dfc3212
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016219"
---
# <span data-ttu-id="15402-101">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="15402-101">New-AzureAutomationSchedule</span></span>

## <span data-ttu-id="15402-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15402-102">SYNOPSIS</span></span>

<span data-ttu-id="15402-103">Automatizálási ütemtervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="15402-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="15402-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15402-104">SYNTAX</span></span>

### <span data-ttu-id="15402-105">ByDaily (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15402-105">ByDaily (Default)</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="15402-106">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="15402-106">ByOneTime</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>] [-OneTime]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="15402-107">ByHourly</span><span class="sxs-lookup"><span data-stu-id="15402-107">ByHourly</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="15402-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="15402-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="15402-109">A **New-AzureAutomationSchedule** parancsmag ütemtervet hoz létre a Microsoft Azure automatizálási szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="15402-109">The **New-AzureAutomationSchedule** cmdlet creates a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="15402-110">Példák</span><span class="sxs-lookup"><span data-stu-id="15402-110">EXAMPLES</span></span>

### <span data-ttu-id="15402-111">Példa 1: egyszeri ütemezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="15402-111">Example 1: Create a one-time schedule</span></span>
```
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime
```

<span data-ttu-id="15402-112">A következő parancs olyan ütemtervet hoz létre, amely egy időben fut az aktuális napon a 11:00 PM-ben.</span><span class="sxs-lookup"><span data-stu-id="15402-112">The following command creates a schedule that runs one time on the current date at 11:00 PM.</span></span>

### <span data-ttu-id="15402-113">2. példa: ismétlődő ütemezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="15402-113">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1
```

<span data-ttu-id="15402-114">Az alábbi parancsok olyan új ütemtervet hoznak létre, amely a 1:00 PM-nél minden nap az aktuális napi naptól kezdődően fut.</span><span class="sxs-lookup"><span data-stu-id="15402-114">The following commands create a new schedule that runs at 1:00 PM every day for one year starting on the current day.</span></span>

## <span data-ttu-id="15402-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15402-115">PARAMETERS</span></span>

### <span data-ttu-id="15402-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="15402-116">-AutomationAccountName</span></span>
<span data-ttu-id="15402-117">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15402-117">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15402-118">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="15402-118">-DayInterval</span></span>
<span data-ttu-id="15402-119">Az ütemtervben a napokban megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="15402-119">Specifies an interval, in days, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15402-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="15402-120">-Description</span></span>
<span data-ttu-id="15402-121">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="15402-121">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15402-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="15402-122">-ExpiryTime</span></span>
<span data-ttu-id="15402-123">Az ütemterv lejárati időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="15402-123">Specifies the expiry time of a schedule.</span></span>
<span data-ttu-id="15402-124">Karakterláncot akkor lehet megadni, ha az érvényes **datetime** értékké alakul.</span><span class="sxs-lookup"><span data-stu-id="15402-124">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15402-125">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="15402-125">-HourInterval</span></span>
<span data-ttu-id="15402-126">Az ütemezéshez az órákban megadott intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="15402-126">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15402-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15402-127">-Name</span></span>
<span data-ttu-id="15402-128">Az ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15402-128">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15402-129">-Egykori</span><span class="sxs-lookup"><span data-stu-id="15402-129">-OneTime</span></span>
<span data-ttu-id="15402-130">Jelzi, hogy ez a művelet egyszeri ütemtervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="15402-130">Indicates that this operation creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15402-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="15402-131">-Profile</span></span>
<span data-ttu-id="15402-132">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="15402-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="15402-133">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="15402-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15402-134">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="15402-134">-StartTime</span></span>
<span data-ttu-id="15402-135">Az ütemterv kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="15402-135">Specifies the start time of a schedule.</span></span>
<span data-ttu-id="15402-136">Karakterláncot akkor lehet megadni, ha az érvényes **datetime** értékké alakul.</span><span class="sxs-lookup"><span data-stu-id="15402-136">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15402-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15402-137">CommonParameters</span></span>
<span data-ttu-id="15402-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15402-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15402-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15402-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15402-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15402-140">INPUTS</span></span>

## <span data-ttu-id="15402-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15402-141">OUTPUTS</span></span>

### <span data-ttu-id="15402-142">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="15402-142">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="15402-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15402-143">NOTES</span></span>

## <span data-ttu-id="15402-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15402-144">RELATED LINKS</span></span>

[<span data-ttu-id="15402-145">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="15402-145">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="15402-146">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="15402-146">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="15402-147">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="15402-147">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


