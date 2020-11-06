---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 740077def0ba0eccb1d962b88317fadb3c5c897c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492878"
---
# <span data-ttu-id="56882-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="56882-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="56882-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56882-102">SYNOPSIS</span></span>
<span data-ttu-id="56882-103">Biztonsági adatmegőrzési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="56882-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56882-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56882-104">SYNTAX</span></span>

### <span data-ttu-id="56882-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="56882-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56882-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="56882-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56882-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="56882-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56882-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="56882-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56882-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="56882-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56882-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="56882-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56882-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="56882-111">DESCRIPTION</span></span>
<span data-ttu-id="56882-112">A **New-AzureRmBackupRetentionPolicyObject** parancsmag egy Azure Backup adatmegőrzési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="56882-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="56882-113">Az adatmegőrzési házirend azt határozza meg, hogy a biztonsági mentés mennyi ideig tart a helyreállítási pont.</span><span class="sxs-lookup"><span data-stu-id="56882-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="56882-114">Az adatmegőrzés típusai a következők:</span><span class="sxs-lookup"><span data-stu-id="56882-114">The types of retention are the following:</span></span> 
- <span data-ttu-id="56882-115">Napi</span><span class="sxs-lookup"><span data-stu-id="56882-115">Daily</span></span> 
- <span data-ttu-id="56882-116">Heti</span><span class="sxs-lookup"><span data-stu-id="56882-116">Weekly</span></span> 
- <span data-ttu-id="56882-117">Havi</span><span class="sxs-lookup"><span data-stu-id="56882-117">Monthly</span></span> 
- <span data-ttu-id="56882-118">Évente hozzon létre egy adatmegőrzési házirendet a használni kívánt adatmegőrzési típusokhoz.</span><span class="sxs-lookup"><span data-stu-id="56882-118">Yearly Create one retention policy for each type of retention that you plan to use.</span></span>
<span data-ttu-id="56882-119">A biztonságimásolat-házirend legalább egy adatmegőrzési házirendhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="56882-119">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="56882-120">Biztonsági házirend létrehozásához használja az New-AzureRmBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="56882-120">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="56882-121">Ehelyett adatmegőrzési házirendet adhat meg az Enable-AzureRmBackupProtection parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="56882-121">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="56882-122">Példák</span><span class="sxs-lookup"><span data-stu-id="56882-122">EXAMPLES</span></span>

### <span data-ttu-id="56882-123">Példa 1: adatmegőrzési szabály létrehozása a napi adatmegőrzéshez</span><span class="sxs-lookup"><span data-stu-id="56882-123">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="56882-124">Az első parancs adatmegőrzési házirendet hoz létre a napi adatmegőrzési 30 napra, majd a $Daily változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="56882-124">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>
<span data-ttu-id="56882-125">A második parancs a $Daily tartalmát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="56882-125">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="56882-126">2. példa: havi adatmegőrzési házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="56882-126">Example 2: Create a monthly retention policy</span></span>
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

<span data-ttu-id="56882-127">Az első parancs olyan adatmegőrzési házirendet hoz létre, amely minden hónap tizedik és huszadik részéről tizenkét hónapig őrzi meg a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="56882-127">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="56882-128">A parancs az adatmegőrzési házirendet a $Monthly változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="56882-128">The command stores the retention policy in the $Monthly variable.</span></span>
<span data-ttu-id="56882-129">A második parancs a $Monthly tartalmát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="56882-129">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="56882-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56882-130">PARAMETERS</span></span>

### <span data-ttu-id="56882-131">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="56882-131">-DailyRetention</span></span>
<span data-ttu-id="56882-132">Jelzi, hogy ez a parancsmag napi adatmegőrzési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="56882-132">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-133">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="56882-133">-DaysOfMonth</span></span>
<span data-ttu-id="56882-134">A hónap azon napjait adja meg, amely meghatározza, hogy mely helyreállítási pontok biztonsági mentése megmaradjon és mennyi ideig.</span><span class="sxs-lookup"><span data-stu-id="56882-134">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="56882-135">A paraméter elfogadható értékei a következők: 1 – 28 és az utolsó egész szám.</span><span class="sxs-lookup"><span data-stu-id="56882-135">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="56882-136">Adja meg ezt a paramétert, ha a *DailyRetention* , az *MonthlyRetentionInDailyFormat* és a *YearlyRetentionInDailyFormat* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="56882-136">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases:
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-137">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="56882-137">-DaysOfWeek</span></span>
<span data-ttu-id="56882-138">A hét napjainak tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56882-138">Specifies an array of days of the week.</span></span>
<span data-ttu-id="56882-139">A parancsmag azon napjai, amelyek meghatározzák, hogy mely helyreállítási pontok őrzik meg a biztonsági mentést és mennyi ideig.</span><span class="sxs-lookup"><span data-stu-id="56882-139">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="56882-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="56882-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56882-141">Hétfő</span><span class="sxs-lookup"><span data-stu-id="56882-141">Monday</span></span> 
- <span data-ttu-id="56882-142">Kedd</span><span class="sxs-lookup"><span data-stu-id="56882-142">Tuesday</span></span> 
- <span data-ttu-id="56882-143">Szerda</span><span class="sxs-lookup"><span data-stu-id="56882-143">Wednesday</span></span> 
- <span data-ttu-id="56882-144">Csütörtök</span><span class="sxs-lookup"><span data-stu-id="56882-144">Thursday</span></span> 
- <span data-ttu-id="56882-145">Péntek</span><span class="sxs-lookup"><span data-stu-id="56882-145">Friday</span></span> 
- <span data-ttu-id="56882-146">Szombat</span><span class="sxs-lookup"><span data-stu-id="56882-146">Saturday</span></span> 
- <span data-ttu-id="56882-147">Vasárnap: ezt a paramétert akkor adja meg, ha a *WeeklyRetention* , az *MonthlyRetentionInWeeklyFormat* és a *YearlyRetentionInWeeklyFormat* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="56882-147">Sunday Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>
<span data-ttu-id="56882-148">Győződjön meg arról, hogy a hét napja a biztonsági mentéshez és a visszatartás beállításhoz van igazítva.</span><span class="sxs-lookup"><span data-stu-id="56882-148">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="56882-149">Ha például a biztonsági másolat szombaton van beállítva, az adatmegőrzési házirendeknek a szombaton is szerepelniük kell.</span><span class="sxs-lookup"><span data-stu-id="56882-149">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56882-150">-DefaultProfile</span></span>
<span data-ttu-id="56882-151">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="56882-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56882-152">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="56882-152">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="56882-153">Azt jelzi, hogy ez a parancsmag napi formátumban hoz létre havi házirendet.</span><span class="sxs-lookup"><span data-stu-id="56882-153">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-154">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="56882-154">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="56882-155">Jelzi, hogy ez a parancsmag havi szabályokat hoz létre heti formátumban.</span><span class="sxs-lookup"><span data-stu-id="56882-155">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-156">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="56882-156">-MonthsOfYear</span></span>
<span data-ttu-id="56882-157">Itt adhatja meg, hogy az év mely hónapjaiban legyenek a biztonsági másolatok évente megmaradó helyreállítási pontok.</span><span class="sxs-lookup"><span data-stu-id="56882-157">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="56882-158">A paraméter elfogadható értékei a következők: hónapok (például január vagy február) nevei.</span><span class="sxs-lookup"><span data-stu-id="56882-158">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-159">-Adatmegőrzés</span><span class="sxs-lookup"><span data-stu-id="56882-159">-Retention</span></span>
<span data-ttu-id="56882-160">Az adatmegőrzési időszakot napokban, hónapokban vagy években adja meg, hogy mely biztonsági másolat tárolja a biztonsági mentési pontot.</span><span class="sxs-lookup"><span data-stu-id="56882-160">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="56882-161">Az egység attól függ, hogy az adott parancsmag napi, havi vagy éves adatmegőrzési beállítást jelöl-e ki.</span><span class="sxs-lookup"><span data-stu-id="56882-161">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="56882-162">Ha például a *DailyRetention* paramétert adja meg, a parancsmag a jelenlegi paramétert több napra értelmezi.</span><span class="sxs-lookup"><span data-stu-id="56882-162">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-163">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="56882-163">-WeeklyRetention</span></span>
<span data-ttu-id="56882-164">Jelzi, hogy ez a parancsmag heti adatmegőrzési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="56882-164">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-165">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="56882-165">-WeekNumber</span></span>
<span data-ttu-id="56882-166">Itt adhatja meg a hónap hetet, amely meghatározza, hogy mely helyreállítási pontok biztonsági mentése megmaradjon és mennyi ideig.</span><span class="sxs-lookup"><span data-stu-id="56882-166">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="56882-167">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="56882-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56882-168">Első</span><span class="sxs-lookup"><span data-stu-id="56882-168">First</span></span> 
- <span data-ttu-id="56882-169">Második</span><span class="sxs-lookup"><span data-stu-id="56882-169">Second</span></span> 
- <span data-ttu-id="56882-170">Harmadik</span><span class="sxs-lookup"><span data-stu-id="56882-170">Third</span></span> 
- <span data-ttu-id="56882-171">Negyedik</span><span class="sxs-lookup"><span data-stu-id="56882-171">Fourth</span></span> 
- <span data-ttu-id="56882-172">Utolsó</span><span class="sxs-lookup"><span data-stu-id="56882-172">Last</span></span>

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-173">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="56882-173">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="56882-174">Jelzi, hogy ez a parancsmag éves adatmegőrzési házirendet hoz létre napi formátumban.</span><span class="sxs-lookup"><span data-stu-id="56882-174">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-175">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="56882-175">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="56882-176">Jelzi, hogy ez a parancsmag éves adatmegőrzési szabályt hoz létre heti formátumban.</span><span class="sxs-lookup"><span data-stu-id="56882-176">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56882-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56882-177">CommonParameters</span></span>
<span data-ttu-id="56882-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56882-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56882-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56882-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56882-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56882-180">INPUTS</span></span>

### <span data-ttu-id="56882-181">Nincs</span><span class="sxs-lookup"><span data-stu-id="56882-181">None</span></span>

## <span data-ttu-id="56882-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56882-182">OUTPUTS</span></span>

### <span data-ttu-id="56882-183">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="56882-183">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy</span></span>

## <span data-ttu-id="56882-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56882-184">NOTES</span></span>
* <span data-ttu-id="56882-185">Nincs</span><span class="sxs-lookup"><span data-stu-id="56882-185">None</span></span>

## <span data-ttu-id="56882-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56882-186">RELATED LINKS</span></span>

[<span data-ttu-id="56882-187">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="56882-187">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="56882-188">Új – AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="56882-188">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


