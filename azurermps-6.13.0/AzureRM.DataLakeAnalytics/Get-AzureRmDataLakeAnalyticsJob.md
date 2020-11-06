---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 59ec07b253b30d9cc7f03153706afba20331022c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502139"
---
# <span data-ttu-id="0b236-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0b236-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="0b236-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b236-102">SYNOPSIS</span></span>
<span data-ttu-id="0b236-103">Beolvashatja az adat-tó Analytics-munkáját.</span><span class="sxs-lookup"><span data-stu-id="0b236-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b236-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b236-104">SYNTAX</span></span>

### <span data-ttu-id="0b236-105">GetAllInResourceGroupAndAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b236-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b236-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="0b236-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b236-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b236-107">DESCRIPTION</span></span>
<span data-ttu-id="0b236-108">A **Get-AzureRmDataLakeAnalyticsJob** parancsmag Azure Data-tó elemzési feladatát kapja.</span><span class="sxs-lookup"><span data-stu-id="0b236-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="0b236-109">Ha nem ad meg feladatot, ez a parancsmag minden feladatot beilleszt.</span><span class="sxs-lookup"><span data-stu-id="0b236-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="0b236-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0b236-110">EXAMPLES</span></span>

### <span data-ttu-id="0b236-111">1. példa: meghatározott feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="0b236-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="0b236-112">Ez a parancs a megadott AZONOSÍTÓval kapja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="0b236-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="0b236-113">2. példa: a múlt héten benyújtott feladatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="0b236-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="0b236-114">Ez a parancs a múlt héten benyújtott feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="0b236-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="0b236-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b236-115">PARAMETERS</span></span>

### <span data-ttu-id="0b236-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="0b236-116">-Account</span></span>
<span data-ttu-id="0b236-117">Az adattó-Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b236-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0b236-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b236-118">-DefaultProfile</span></span>
<span data-ttu-id="0b236-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0b236-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b236-120">-Include (include)</span><span class="sxs-lookup"><span data-stu-id="0b236-120">-Include</span></span>
<span data-ttu-id="0b236-121">Azokat a beállításokat adja meg, amelyek jelzik, hogy milyen típusú további információkat kell beolvasni a feladatról.</span><span class="sxs-lookup"><span data-stu-id="0b236-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="0b236-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b236-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b236-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="0b236-123">None</span></span>
- <span data-ttu-id="0b236-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="0b236-124">DebugInfo</span></span>
- <span data-ttu-id="0b236-125">Statisztikák</span><span class="sxs-lookup"><span data-stu-id="0b236-125">Statistics</span></span>
- <span data-ttu-id="0b236-126">Minden</span><span class="sxs-lookup"><span data-stu-id="0b236-126">All</span></span>

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

### <span data-ttu-id="0b236-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="0b236-127">-JobId</span></span>
<span data-ttu-id="0b236-128">A beolvasott feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b236-128">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="0b236-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0b236-129">-Name</span></span>
<span data-ttu-id="0b236-130">A Feladatlista eredményének szűrésére használható nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b236-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="0b236-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b236-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b236-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="0b236-132">None</span></span>
- <span data-ttu-id="0b236-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="0b236-133">DebugInfo</span></span>
- <span data-ttu-id="0b236-134">Statisztikák</span><span class="sxs-lookup"><span data-stu-id="0b236-134">Statistics</span></span>
- <span data-ttu-id="0b236-135">Minden</span><span class="sxs-lookup"><span data-stu-id="0b236-135">All</span></span>

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

### <span data-ttu-id="0b236-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="0b236-136">-PipelineId</span></span>
<span data-ttu-id="0b236-137">Egy olyan opcionális azonosító, amely csak a megadott csővezeték munkamennyiség részét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0b236-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

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

### <span data-ttu-id="0b236-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="0b236-138">-RecurrenceId</span></span>
<span data-ttu-id="0b236-139">Egy olyan opcionális azonosító, amely csak a megadott ismétlődéshez tartozó feladatokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0b236-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

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

### <span data-ttu-id="0b236-140">-Result (eredmény)</span><span class="sxs-lookup"><span data-stu-id="0b236-140">-Result</span></span>
<span data-ttu-id="0b236-141">A projekt eredményéhez tartozó eredményhalmaz-szűrőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b236-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="0b236-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b236-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b236-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="0b236-143">None</span></span>
- <span data-ttu-id="0b236-144">Lemondott</span><span class="sxs-lookup"><span data-stu-id="0b236-144">Cancelled</span></span>
- <span data-ttu-id="0b236-145">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="0b236-145">Failed</span></span>
- <span data-ttu-id="0b236-146">Sikerességéről</span><span class="sxs-lookup"><span data-stu-id="0b236-146">Succeeded</span></span>

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

### <span data-ttu-id="0b236-147">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="0b236-147">-State</span></span>
<span data-ttu-id="0b236-148">A projekt eredményéhez tartozó állapot-szűrőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b236-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="0b236-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b236-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b236-150">Elfogadott</span><span class="sxs-lookup"><span data-stu-id="0b236-150">Accepted</span></span>
- <span data-ttu-id="0b236-151">Új</span><span class="sxs-lookup"><span data-stu-id="0b236-151">New</span></span>
- <span data-ttu-id="0b236-152">Összeállítása</span><span class="sxs-lookup"><span data-stu-id="0b236-152">Compiling</span></span>
- <span data-ttu-id="0b236-153">Ütemezés</span><span class="sxs-lookup"><span data-stu-id="0b236-153">Scheduling</span></span>
- <span data-ttu-id="0b236-154">Várólistán töltött</span><span class="sxs-lookup"><span data-stu-id="0b236-154">Queued</span></span>
- <span data-ttu-id="0b236-155">Kezdve</span><span class="sxs-lookup"><span data-stu-id="0b236-155">Starting</span></span>
- <span data-ttu-id="0b236-156">Szünetel</span><span class="sxs-lookup"><span data-stu-id="0b236-156">Paused</span></span>
- <span data-ttu-id="0b236-157">Fut</span><span class="sxs-lookup"><span data-stu-id="0b236-157">Running</span></span>
- <span data-ttu-id="0b236-158">Véget</span><span class="sxs-lookup"><span data-stu-id="0b236-158">Ended</span></span>

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

### <span data-ttu-id="0b236-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="0b236-159">-SubmittedAfter</span></span>
<span data-ttu-id="0b236-160">A Dátumszűrő értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b236-160">Specifies a date filter.</span></span>
<span data-ttu-id="0b236-161">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét a megadott dátum után elküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="0b236-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

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

### <span data-ttu-id="0b236-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="0b236-162">-SubmittedBefore</span></span>
<span data-ttu-id="0b236-163">A Dátumszűrő értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b236-163">Specifies a date filter.</span></span>
<span data-ttu-id="0b236-164">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét a megadott dátum előtt elküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="0b236-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

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

### <span data-ttu-id="0b236-165">-Beküldő</span><span class="sxs-lookup"><span data-stu-id="0b236-165">-Submitter</span></span>
<span data-ttu-id="0b236-166">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b236-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="0b236-167">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét egy adott felhasználó által elküldött munkákra.</span><span class="sxs-lookup"><span data-stu-id="0b236-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

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

### <span data-ttu-id="0b236-168">-Top</span><span class="sxs-lookup"><span data-stu-id="0b236-168">-Top</span></span>
<span data-ttu-id="0b236-169">Egy tetszőleges érték, amely a visszaadott feladatok számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="0b236-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="0b236-170">Az alapértelmezett érték a 500</span><span class="sxs-lookup"><span data-stu-id="0b236-170">Default value is 500</span></span>

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

### <span data-ttu-id="0b236-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b236-171">CommonParameters</span></span>
<span data-ttu-id="0b236-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b236-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b236-173">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b236-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b236-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b236-174">INPUTS</span></span>

### <span data-ttu-id="0b236-175">System. String</span><span class="sxs-lookup"><span data-stu-id="0b236-175">System.String</span></span>

### <span data-ttu-id="0b236-176">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0b236-176">System.Guid</span></span>

### <span data-ttu-id="0b236-177">Microsoft. Azure. Command. DataLakeAnalytics. modellek. DataLakeAnalyticsEnums + ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="0b236-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="0b236-178">System. null ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0b236-178">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0b236-179">Microsoft. Azure. Management. DataLake. Analytics. models. JobState []</span><span class="sxs-lookup"><span data-stu-id="0b236-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="0b236-180">Microsoft. Azure. Management. DataLake. Analytics. models. JobResult []</span><span class="sxs-lookup"><span data-stu-id="0b236-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="0b236-181">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0b236-181">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0b236-182">System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0b236-182">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0b236-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b236-183">OUTPUTS</span></span>

### <span data-ttu-id="0b236-184">Microsoft. Azure. Management. DataLake. Analytics. models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="0b236-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="0b236-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b236-185">NOTES</span></span>

## <span data-ttu-id="0b236-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b236-186">RELATED LINKS</span></span>

[<span data-ttu-id="0b236-187">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0b236-187">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="0b236-188">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0b236-188">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="0b236-189">Várjon-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0b236-189">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


