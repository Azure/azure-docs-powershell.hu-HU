---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505076"
---
# <span data-ttu-id="6f244-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6f244-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="6f244-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f244-102">SYNOPSIS</span></span>
<span data-ttu-id="6f244-103">Beolvashatja az adat-tó Analytics-munkáját.</span><span class="sxs-lookup"><span data-stu-id="6f244-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f244-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f244-104">SYNTAX</span></span>

### <span data-ttu-id="6f244-105">Az összes erőforrás-csoport és fiók (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f244-105">All In Resource Group and Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f244-106">Adott JobInformation</span><span class="sxs-lookup"><span data-stu-id="6f244-106">Specific JobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f244-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f244-107">DESCRIPTION</span></span>
<span data-ttu-id="6f244-108">A **Get-AzureRmDataLakeAnalyticsJob** parancsmag Azure Data-tó elemzési feladatát kapja.</span><span class="sxs-lookup"><span data-stu-id="6f244-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="6f244-109">Ha nem ad meg feladatot, ez a parancsmag minden feladatot beilleszt.</span><span class="sxs-lookup"><span data-stu-id="6f244-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="6f244-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6f244-110">EXAMPLES</span></span>

### <span data-ttu-id="6f244-111">1. példa: meghatározott feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="6f244-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="6f244-112">Ez a parancs a megadott AZONOSÍTÓval kapja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="6f244-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="6f244-113">2. példa: a múlt héten benyújtott feladatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="6f244-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="6f244-114">Ez a parancs a múlt héten benyújtott feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="6f244-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="6f244-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f244-115">PARAMETERS</span></span>

### <span data-ttu-id="6f244-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="6f244-116">-Account</span></span>
<span data-ttu-id="6f244-117">Az adattó-Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f244-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-118">-Include (include)</span><span class="sxs-lookup"><span data-stu-id="6f244-118">-Include</span></span>
<span data-ttu-id="6f244-119">Azokat a beállításokat adja meg, amelyek jelzik, hogy milyen típusú további információkat kell beolvasni a feladatról.</span><span class="sxs-lookup"><span data-stu-id="6f244-119">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="6f244-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6f244-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f244-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="6f244-121">None</span></span>
- <span data-ttu-id="6f244-122">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="6f244-122">DebugInfo</span></span>
- <span data-ttu-id="6f244-123">Statisztikák</span><span class="sxs-lookup"><span data-stu-id="6f244-123">Statistics</span></span>
- <span data-ttu-id="6f244-124">Minden</span><span class="sxs-lookup"><span data-stu-id="6f244-124">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="6f244-125">-JobId</span></span>
<span data-ttu-id="6f244-126">A beolvasott feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f244-126">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f244-127">-Name</span></span>
<span data-ttu-id="6f244-128">A Feladatlista eredményének szűrésére használható nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f244-128">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="6f244-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6f244-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f244-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="6f244-130">None</span></span>
- <span data-ttu-id="6f244-131">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="6f244-131">DebugInfo</span></span>
- <span data-ttu-id="6f244-132">Statisztikák</span><span class="sxs-lookup"><span data-stu-id="6f244-132">Statistics</span></span>
- <span data-ttu-id="6f244-133">Minden</span><span class="sxs-lookup"><span data-stu-id="6f244-133">All</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-134">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="6f244-134">-PipelineId</span></span>
<span data-ttu-id="6f244-135">Egy olyan opcionális azonosító, amely csak a megadott csővezeték munkamennyiség részét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6f244-135">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-136">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="6f244-136">-RecurrenceId</span></span>
<span data-ttu-id="6f244-137">Egy olyan opcionális azonosító, amely csak a megadott ismétlődéshez tartozó feladatokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="6f244-137">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-138">-Result (eredmény)</span><span class="sxs-lookup"><span data-stu-id="6f244-138">-Result</span></span>
<span data-ttu-id="6f244-139">A projekt eredményéhez tartozó eredményhalmaz-szűrőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f244-139">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="6f244-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6f244-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f244-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="6f244-141">None</span></span>
- <span data-ttu-id="6f244-142">Lemondott</span><span class="sxs-lookup"><span data-stu-id="6f244-142">Cancelled</span></span>
- <span data-ttu-id="6f244-143">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="6f244-143">Failed</span></span>
- <span data-ttu-id="6f244-144">Sikerességéről</span><span class="sxs-lookup"><span data-stu-id="6f244-144">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-145">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="6f244-145">-State</span></span>
<span data-ttu-id="6f244-146">A projekt eredményéhez tartozó állapot-szűrőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f244-146">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="6f244-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6f244-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f244-148">Elfogadott</span><span class="sxs-lookup"><span data-stu-id="6f244-148">Accepted</span></span>
- <span data-ttu-id="6f244-149">Új</span><span class="sxs-lookup"><span data-stu-id="6f244-149">New</span></span>
- <span data-ttu-id="6f244-150">Összeállítása</span><span class="sxs-lookup"><span data-stu-id="6f244-150">Compiling</span></span>
- <span data-ttu-id="6f244-151">Ütemezés</span><span class="sxs-lookup"><span data-stu-id="6f244-151">Scheduling</span></span>
- <span data-ttu-id="6f244-152">Várólistán töltött</span><span class="sxs-lookup"><span data-stu-id="6f244-152">Queued</span></span>
- <span data-ttu-id="6f244-153">Kezdve</span><span class="sxs-lookup"><span data-stu-id="6f244-153">Starting</span></span>
- <span data-ttu-id="6f244-154">Szünetel</span><span class="sxs-lookup"><span data-stu-id="6f244-154">Paused</span></span>
- <span data-ttu-id="6f244-155">Fut</span><span class="sxs-lookup"><span data-stu-id="6f244-155">Running</span></span>
- <span data-ttu-id="6f244-156">Véget</span><span class="sxs-lookup"><span data-stu-id="6f244-156">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-157">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="6f244-157">-SubmittedAfter</span></span>
<span data-ttu-id="6f244-158">A Dátumszűrő értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f244-158">Specifies a date filter.</span></span>
<span data-ttu-id="6f244-159">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét a megadott dátum után elküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="6f244-159">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-160">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="6f244-160">-SubmittedBefore</span></span>
<span data-ttu-id="6f244-161">A Dátumszűrő értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f244-161">Specifies a date filter.</span></span>
<span data-ttu-id="6f244-162">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét a megadott dátum előtt elküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="6f244-162">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-163">-Beküldő</span><span class="sxs-lookup"><span data-stu-id="6f244-163">-Submitter</span></span>
<span data-ttu-id="6f244-164">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f244-164">Specifies the email address of a user.</span></span>
<span data-ttu-id="6f244-165">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét egy adott felhasználó által elküldött munkákra.</span><span class="sxs-lookup"><span data-stu-id="6f244-165">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-166">-Top</span><span class="sxs-lookup"><span data-stu-id="6f244-166">-Top</span></span>
<span data-ttu-id="6f244-167">Egy tetszőleges érték, amely a visszaadott feladatok számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="6f244-167">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="6f244-168">Az alapértelmezett érték a 500</span><span class="sxs-lookup"><span data-stu-id="6f244-168">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f244-169">-DefaultProfile</span></span>
<span data-ttu-id="6f244-170">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f244-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f244-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f244-171">CommonParameters</span></span>
<span data-ttu-id="6f244-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f244-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f244-173">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f244-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f244-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f244-174">INPUTS</span></span>

### <span data-ttu-id="6f244-175">GUID</span><span class="sxs-lookup"><span data-stu-id="6f244-175">Guid</span></span>
<span data-ttu-id="6f244-176">A ' JobId ' paraméter a pipeline "GUID" típusú értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f244-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="6f244-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f244-177">OUTPUTS</span></span>

### <span data-ttu-id="6f244-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="6f244-178">JobInformation</span></span>
<span data-ttu-id="6f244-179">A megadott projektfeladat adatai</span><span class="sxs-lookup"><span data-stu-id="6f244-179">The specified job information details</span></span>

### <span data-ttu-id="6f244-180">Lista<JobInformation></span><span class="sxs-lookup"><span data-stu-id="6f244-180">List<JobInformation></span></span>
<span data-ttu-id="6f244-181">A megadott adattó-fiókban lévő feladatok listája.</span><span class="sxs-lookup"><span data-stu-id="6f244-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="6f244-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f244-182">NOTES</span></span>

## <span data-ttu-id="6f244-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f244-183">RELATED LINKS</span></span>

[<span data-ttu-id="6f244-184">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6f244-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="6f244-185">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6f244-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="6f244-186">Várjon-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6f244-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


