---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016510"
---
# <span data-ttu-id="c2ed7-101">Get-AzureWebHostingPlanMetric</span><span class="sxs-lookup"><span data-stu-id="c2ed7-101">Get-AzureWebHostingPlanMetric</span></span>

## <span data-ttu-id="c2ed7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ed7-103">Az Azure webhelyhez tartozó csomagok metrikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-103">Gets metrics for Azure website hosting plans.</span></span>

## <span data-ttu-id="c2ed7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2ed7-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2ed7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2ed7-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ed7-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c2ed7-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c2ed7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c2ed7-108">A **Get-AzureWebHostingPlanMetric** parancsmag metrikákat kap az Azure web hosting csomaghoz egy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-108">The **Get-AzureWebHostingPlanMetric** cmdlet gets metrics for Azure web hosting plans in a subscription.</span></span>

## <span data-ttu-id="c2ed7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c2ed7-109">EXAMPLES</span></span>

### <span data-ttu-id="c2ed7-110">Példa 1: a mérőszámok beszerzése az elmúlt három órában a per-instance szinten</span><span class="sxs-lookup"><span data-stu-id="c2ed7-110">Example 1: Get metrics for the last three hours at a per-instance level</span></span>
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

<span data-ttu-id="c2ed7-111">Ez a parancs a webes üzemeltetési terv metrikáját adja meg az elmúlt három órában a per-instance szinten.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-111">This command gets web hosting plan metrics for last three hours on per-instance level.</span></span>

## <span data-ttu-id="c2ed7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2ed7-112">PARAMETERS</span></span>

### <span data-ttu-id="c2ed7-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c2ed7-113">-EndDate</span></span>
<span data-ttu-id="c2ed7-114">A befejezési időpontot **datetime** -objektumként adja meg, amelyből a program visszaadja a metrikákat.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-114">Specifies the end time, as a **DateTime** object, from which to return metrics.</span></span>
<span data-ttu-id="c2ed7-115">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="c2ed7-116">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c2ed7-116">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ed7-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="c2ed7-117">-InstanceDetails</span></span>
<span data-ttu-id="c2ed7-118">Azt jelzi, hogy ez a parancsmag a példányok szintjének részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="c2ed7-119">Ha a webhely-üzemeltetési terv két vagy több számítógépen fut, ez a parancsmag az egyes gépek részletes metrikáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-119">If the website hosting plan runs on two or more machines, this cmdlet returns details metrics for each machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ed7-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="c2ed7-120">-MetricNames</span></span>
<span data-ttu-id="c2ed7-121">Faj: a mérőszámok tömbje a kezdéshez.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-121">Species an array of metrics to get.</span></span>
<span data-ttu-id="c2ed7-122">Ha nem ad meg értéket ehhez a paraméterhez, ez a parancsmag minden metrikát kap.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-122">If you do not specify a value for this parameter, this cmdlet gets all metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ed7-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2ed7-123">-Name</span></span>
<span data-ttu-id="c2ed7-124">Az előfizetésben szereplő terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-124">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="c2ed7-125">A **Get-AzureWebHostingPlanMetric** alapértelmezés szerint a jelenlegi előfizetés összes webhelyét kapja.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-125">By default, **Get-AzureWebHostingPlanMetric** gets all websites in the current subscription.</span></span>
<span data-ttu-id="c2ed7-126">Ez a paraméter nem támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-126">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="c2ed7-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="c2ed7-127">-Profile</span></span>
<span data-ttu-id="c2ed7-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c2ed7-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2ed7-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c2ed7-130">-StartDate</span></span>
<span data-ttu-id="c2ed7-131">Azt a kezdési időpontot adja meg **datetime** -objektumként, amelyből mérőszámokat szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-131">Specifies the start time, as a **DateTime** object, for which to get metrics.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ed7-132">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="c2ed7-132">-TimeGrain</span></span>
<span data-ttu-id="c2ed7-133">A mérőszámok beszerzéséhez szükséges időegységet adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-133">Specifies the time unit for which to get metrics.</span></span>
<span data-ttu-id="c2ed7-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="c2ed7-134">Valid values are:</span></span> 

- <span data-ttu-id="c2ed7-135">PT1M (perc)</span><span class="sxs-lookup"><span data-stu-id="c2ed7-135">PT1M (Minute)</span></span> 
- <span data-ttu-id="c2ed7-136">PT1H (óra)</span><span class="sxs-lookup"><span data-stu-id="c2ed7-136">PT1H (Hour)</span></span> 
- <span data-ttu-id="c2ed7-137">P1D (nap)</span><span class="sxs-lookup"><span data-stu-id="c2ed7-137">P1D (Day)</span></span>

<span data-ttu-id="c2ed7-138">Az alapértelmezett érték a PT1H.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-138">The default value is PT1H.</span></span>

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

### <span data-ttu-id="c2ed7-139">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="c2ed7-139">-WebSpaceName</span></span>
<span data-ttu-id="c2ed7-140">Az előfizetésben lévő tárhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-140">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="c2ed7-141">A **Get-AzureWebHostingPlanMetric** alapértelmezés szerint az aktuális előfizetéshez tartozó összes csomagot kapja.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-141">By default, **Get-AzureWebHostingPlanMetric** gets all plans in the current subscription.</span></span>
<span data-ttu-id="c2ed7-142">Ez a paraméter nem támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-142">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ed7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ed7-143">CommonParameters</span></span>
<span data-ttu-id="c2ed7-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2ed7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ed7-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ed7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ed7-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2ed7-146">INPUTS</span></span>

###  
<span data-ttu-id="c2ed7-147">A parancsmagot név szerint, de nem érték szerint is továbbíthatja.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-147">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="c2ed7-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2ed7-148">OUTPUTS</span></span>

###  
<span data-ttu-id="c2ed7-149">Microsoft. WindowsAzure. Command. Utilities. websites. Services. webentitások. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="c2ed7-149">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>

<span data-ttu-id="c2ed7-150">Alapértelmezés szerint a **Get-AzureWebHostingPlanMetric** a **MetricResponse** -objektumok tömbjét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c2ed7-150">By default, **Get-AzureWebHostingPlanMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="c2ed7-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2ed7-151">NOTES</span></span>

## <span data-ttu-id="c2ed7-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2ed7-152">RELATED LINKS</span></span>

[<span data-ttu-id="c2ed7-153">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="c2ed7-153">Get-AzureWebHostingPlan</span></span>](./Get-AzureWebHostingPlan.md)


