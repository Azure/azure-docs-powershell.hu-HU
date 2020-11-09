---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298094"
---
# <span data-ttu-id="8e3e3-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8e3e3-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="8e3e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3e3-103">Beolvashatja az adat-tó Analytics-munkáját.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="8e3e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e3e3-104">SYNTAX</span></span>

### <span data-ttu-id="8e3e3-105">GetAllInResourceGroupAndAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e3e3-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3e3-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="8e3e3-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e3e3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e3e3-107">DESCRIPTION</span></span>
<span data-ttu-id="8e3e3-108">A **Get-AzDataLakeAnalyticsJob** parancsmag Azure Data-tó elemzési feladatát kapja.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="8e3e3-109">Ha nem ad meg feladatot, ez a parancsmag minden feladatot beilleszt.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="8e3e3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8e3e3-110">EXAMPLES</span></span>

### <span data-ttu-id="8e3e3-111">1. példa: meghatározott feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="8e3e3-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="8e3e3-112">Ez a parancs a megadott AZONOSÍTÓval kapja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="8e3e3-113">2. példa: a múlt héten benyújtott feladatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="8e3e3-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="8e3e3-114">Ez a parancs a múlt héten benyújtott feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="8e3e3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e3e3-115">PARAMETERS</span></span>

### <span data-ttu-id="8e3e3-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="8e3e3-116">-Account</span></span>
<span data-ttu-id="8e3e3-117">Az adattó-Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="8e3e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3e3-118">-DefaultProfile</span></span>
<span data-ttu-id="8e3e3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8e3e3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e3e3-120">-Include (include)</span><span class="sxs-lookup"><span data-stu-id="8e3e3-120">-Include</span></span>
<span data-ttu-id="8e3e3-121">Azokat a beállításokat adja meg, amelyek jelzik, hogy milyen típusú további információkat kell beolvasni a feladatról.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="8e3e3-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8e3e3-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e3e3-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e3e3-123">None</span></span>
- <span data-ttu-id="8e3e3-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="8e3e3-124">DebugInfo</span></span>
- <span data-ttu-id="8e3e3-125">Statisztikák</span><span class="sxs-lookup"><span data-stu-id="8e3e3-125">Statistics</span></span>
- <span data-ttu-id="8e3e3-126">Minden</span><span class="sxs-lookup"><span data-stu-id="8e3e3-126">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="8e3e3-127">-JobId</span></span>
<span data-ttu-id="8e3e3-128">A beolvasott feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e3e3-129">-Name</span></span>
<span data-ttu-id="8e3e3-130">A Feladatlista eredményének szűrésére használható nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="8e3e3-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8e3e3-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e3e3-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e3e3-132">None</span></span>
- <span data-ttu-id="8e3e3-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="8e3e3-133">DebugInfo</span></span>
- <span data-ttu-id="8e3e3-134">Statisztikák</span><span class="sxs-lookup"><span data-stu-id="8e3e3-134">Statistics</span></span>
- <span data-ttu-id="8e3e3-135">Minden</span><span class="sxs-lookup"><span data-stu-id="8e3e3-135">All</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="8e3e3-136">-PipelineId</span></span>
<span data-ttu-id="8e3e3-137">Egy olyan opcionális azonosító, amely csak a megadott csővezeték munkamennyiség részét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="8e3e3-138">-RecurrenceId</span></span>
<span data-ttu-id="8e3e3-139">Egy olyan opcionális azonosító, amely csak a megadott ismétlődéshez tartozó feladatokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-140">-Result (eredmény)</span><span class="sxs-lookup"><span data-stu-id="8e3e3-140">-Result</span></span>
<span data-ttu-id="8e3e3-141">A projekt eredményéhez tartozó eredményhalmaz-szűrőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="8e3e3-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8e3e3-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e3e3-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e3e3-143">None</span></span>
- <span data-ttu-id="8e3e3-144">Lemondott</span><span class="sxs-lookup"><span data-stu-id="8e3e3-144">Cancelled</span></span>
- <span data-ttu-id="8e3e3-145">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="8e3e3-145">Failed</span></span>
- <span data-ttu-id="8e3e3-146">Sikerességéről</span><span class="sxs-lookup"><span data-stu-id="8e3e3-146">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-147">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="8e3e3-147">-State</span></span>
<span data-ttu-id="8e3e3-148">A projekt eredményéhez tartozó állapot-szűrőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="8e3e3-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8e3e3-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e3e3-150">Elfogadott</span><span class="sxs-lookup"><span data-stu-id="8e3e3-150">Accepted</span></span>
- <span data-ttu-id="8e3e3-151">Új</span><span class="sxs-lookup"><span data-stu-id="8e3e3-151">New</span></span>
- <span data-ttu-id="8e3e3-152">Összeállítása</span><span class="sxs-lookup"><span data-stu-id="8e3e3-152">Compiling</span></span>
- <span data-ttu-id="8e3e3-153">Ütemezés</span><span class="sxs-lookup"><span data-stu-id="8e3e3-153">Scheduling</span></span>
- <span data-ttu-id="8e3e3-154">Várólistán töltött</span><span class="sxs-lookup"><span data-stu-id="8e3e3-154">Queued</span></span>
- <span data-ttu-id="8e3e3-155">Kezdve</span><span class="sxs-lookup"><span data-stu-id="8e3e3-155">Starting</span></span>
- <span data-ttu-id="8e3e3-156">Szünetel</span><span class="sxs-lookup"><span data-stu-id="8e3e3-156">Paused</span></span>
- <span data-ttu-id="8e3e3-157">Fut</span><span class="sxs-lookup"><span data-stu-id="8e3e3-157">Running</span></span>
- <span data-ttu-id="8e3e3-158">Véget</span><span class="sxs-lookup"><span data-stu-id="8e3e3-158">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="8e3e3-159">-SubmittedAfter</span></span>
<span data-ttu-id="8e3e3-160">A Dátumszűrő értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-160">Specifies a date filter.</span></span>
<span data-ttu-id="8e3e3-161">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét a megadott dátum után elküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="8e3e3-162">-SubmittedBefore</span></span>
<span data-ttu-id="8e3e3-163">A Dátumszűrő értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-163">Specifies a date filter.</span></span>
<span data-ttu-id="8e3e3-164">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét a megadott dátum előtt elküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-165">-Beküldő</span><span class="sxs-lookup"><span data-stu-id="8e3e3-165">-Submitter</span></span>
<span data-ttu-id="8e3e3-166">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="8e3e3-167">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét egy adott felhasználó által elküldött munkákra.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-168">-Top</span><span class="sxs-lookup"><span data-stu-id="8e3e3-168">-Top</span></span>
<span data-ttu-id="8e3e3-169">Egy tetszőleges érték, amely a visszaadott feladatok számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="8e3e3-170">Az alapértelmezett érték a 500</span><span class="sxs-lookup"><span data-stu-id="8e3e3-170">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e3-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3e3-171">CommonParameters</span></span>
<span data-ttu-id="8e3e3-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e3e3-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3e3-173">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e3e3-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3e3-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e3e3-174">INPUTS</span></span>

### <span data-ttu-id="8e3e3-175">System. String</span><span class="sxs-lookup"><span data-stu-id="8e3e3-175">System.String</span></span>

### <span data-ttu-id="8e3e3-176">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8e3e3-176">System.Guid</span></span>

### <span data-ttu-id="8e3e3-177">Microsoft. Azure. Command. DataLakeAnalytics. modellek. DataLakeAnalyticsEnums + ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="8e3e3-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="8e3e3-178">System. null ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e3e3-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8e3e3-179">Microsoft. Azure. Management. DataLake. Analytics. models. JobState []</span><span class="sxs-lookup"><span data-stu-id="8e3e3-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="8e3e3-180">Microsoft. Azure. Management. DataLake. Analytics. models. JobResult []</span><span class="sxs-lookup"><span data-stu-id="8e3e3-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="8e3e3-181">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e3e3-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8e3e3-182">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e3e3-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8e3e3-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e3e3-183">OUTPUTS</span></span>

### <span data-ttu-id="8e3e3-184">Microsoft. Azure. Management. DataLake. Analytics. models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="8e3e3-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="8e3e3-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e3e3-185">NOTES</span></span>

## <span data-ttu-id="8e3e3-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e3e3-186">RELATED LINKS</span></span>

[<span data-ttu-id="8e3e3-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8e3e3-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="8e3e3-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8e3e3-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="8e3e3-189">Várjon-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8e3e3-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


