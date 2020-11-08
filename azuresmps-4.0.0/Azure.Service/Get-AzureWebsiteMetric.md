---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016271"
---
# <span data-ttu-id="5fcb1-101">Get-AzureWebsiteMetric</span><span class="sxs-lookup"><span data-stu-id="5fcb1-101">Get-AzureWebsiteMetric</span></span>

## <span data-ttu-id="5fcb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fcb1-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcb1-103">A jelenlegi előfizetésben az Azure-webhely metrikáit kapja.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-103">Gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="5fcb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fcb1-104">SYNTAX</span></span>

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5fcb1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fcb1-105">DESCRIPTION</span></span>
<span data-ttu-id="5fcb1-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5fcb1-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5fcb1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5fcb1-108">A **Get-AzureWebsiteMetric** parancsmag metrikákat kap az Azure-webhelyhez az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-108">The **Get-AzureWebsiteMetric** cmdlet gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="5fcb1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5fcb1-109">EXAMPLES</span></span>

### <span data-ttu-id="5fcb1-110">Példa 1: mérőszámok beszerzése az elmúlt három órára a webhelyen egy példány szintjén</span><span class="sxs-lookup"><span data-stu-id="5fcb1-110">Example 1: Get metrics for the last three hours on a per-instance level for a website</span></span>
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

<span data-ttu-id="5fcb1-111">Ez a parancs metrikákat kap az elmúlt három órára vonatkozóan egy webhelyre vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-111">This command gets metrics for the last three hours on a per-instance level for a website.</span></span>

## <span data-ttu-id="5fcb1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fcb1-112">PARAMETERS</span></span>

### <span data-ttu-id="5fcb1-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="5fcb1-113">-EndDate</span></span>
<span data-ttu-id="5fcb1-114">Időpontot ad meg **datetime** objektumként a mérőszámok beszerzésének befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-114">Specifies the time, as a **DateTime** object, to stop getting metrics.</span></span>
<span data-ttu-id="5fcb1-115">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="5fcb1-116">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5fcb1-116">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="5fcb1-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="5fcb1-117">-InstanceDetails</span></span>
<span data-ttu-id="5fcb1-118">Azt jelzi, hogy ez a parancsmag a példányok szintjének részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="5fcb1-119">Ha a web-üzemeltetési terv két vagy több számítógépen fut, ez a parancsmag metrikus adatokat ad eredményül az egyes számítógépekhez.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-119">If the web hosting plan runs on two or more computers, this cmdlet returns metrics for each computer.</span></span>

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

### <span data-ttu-id="5fcb1-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="5fcb1-120">-MetricNames</span></span>
<span data-ttu-id="5fcb1-121">A beolvasott mérőszámok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-121">Specifies an array of metrics to get.</span></span>
<span data-ttu-id="5fcb1-122">Ha nem adja meg ezt a paramétert, a parancsmag minden metrikát kap.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-122">If you do not specify this parameter, the cmdlet gets all metrics.</span></span>

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

### <span data-ttu-id="5fcb1-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5fcb1-123">-Name</span></span>
<span data-ttu-id="5fcb1-124">Az előfizetésben lévő webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-124">Specifies the name of a website in the subscription.</span></span>
<span data-ttu-id="5fcb1-125">Ez a paraméter nem támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-125">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="5fcb1-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="5fcb1-126">-Profile</span></span>
<span data-ttu-id="5fcb1-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5fcb1-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5fcb1-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="5fcb1-129">-Slot</span></span>
<span data-ttu-id="5fcb1-130">A Felhőbeli szolgáltatások bevezetésének környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-130">Specifies the environment of a cloud service deployment.</span></span>
<span data-ttu-id="5fcb1-131">Érvényes értékek: a termelés és a megállóhelyek.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-131">Valid values are: Production and Staging.</span></span>

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

### <span data-ttu-id="5fcb1-132">-SlotView</span><span class="sxs-lookup"><span data-stu-id="5fcb1-132">-SlotView</span></span>
<span data-ttu-id="5fcb1-133">Azt jelzi, hogy ez a parancsmag metrikákat kap az aktuális bővítőhelyen forgalmat fogadó állomásnevek számára.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-133">Indicates that this cmdlet gets metrics for the host names that receive traffic at the current slot.</span></span>
<span data-ttu-id="5fcb1-134">Ha az időszak során csere történik, a metrikák egyesítése folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-134">If a swap occurs during the time period, the metrics are merged.</span></span>

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

### <span data-ttu-id="5fcb1-135">-StartDate</span><span class="sxs-lookup"><span data-stu-id="5fcb1-135">-StartDate</span></span>
<span data-ttu-id="5fcb1-136">Itt adhatja meg az időt **datetime** objektumként a mérőszámok kezdéséhez.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-136">Specifies the time, as a **DateTime** object, to start getting metrics.</span></span>

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

### <span data-ttu-id="5fcb1-137">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="5fcb1-137">-TimeGrain</span></span>
<span data-ttu-id="5fcb1-138">A metrikák időegységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-138">Specifies the time unit for metrics.</span></span>
<span data-ttu-id="5fcb1-139">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="5fcb1-139">Valid values are:</span></span> 

- <span data-ttu-id="5fcb1-140">PT1M (perc)</span><span class="sxs-lookup"><span data-stu-id="5fcb1-140">PT1M (Minute)</span></span> 
- <span data-ttu-id="5fcb1-141">PT1H (óra)</span><span class="sxs-lookup"><span data-stu-id="5fcb1-141">PT1H (Hour)</span></span> 
- <span data-ttu-id="5fcb1-142">P1D (nap)</span><span class="sxs-lookup"><span data-stu-id="5fcb1-142">P1D (Day)</span></span>

<span data-ttu-id="5fcb1-143">Az alapértelmezett érték a PT1H.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-143">The default value is PT1H.</span></span>

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

### <span data-ttu-id="5fcb1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcb1-144">CommonParameters</span></span>
<span data-ttu-id="5fcb1-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fcb1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcb1-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fcb1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcb1-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fcb1-147">INPUTS</span></span>

###  
<span data-ttu-id="5fcb1-148">A parancsmagot név szerint, de nem érték szerint is továbbíthatja.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-148">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="5fcb1-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fcb1-149">OUTPUTS</span></span>

### <span data-ttu-id="5fcb1-150">Microsoft. WindowsAzure. Command. Utilities. websites. Services. webentitások. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="5fcb1-150">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>
<span data-ttu-id="5fcb1-151">Alapértelmezés szerint a **Get-AzureWebsiteMetric** a **MetricResponse** -objektumok tömbjét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-151">By default, **Get-AzureWebsiteMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="5fcb1-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fcb1-152">NOTES</span></span>

## <span data-ttu-id="5fcb1-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fcb1-153">RELATED LINKS</span></span>

[<span data-ttu-id="5fcb1-154">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5fcb1-154">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


