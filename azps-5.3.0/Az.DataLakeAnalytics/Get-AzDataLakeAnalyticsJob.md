---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477017"
---
# <span data-ttu-id="478be-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="478be-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="478be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="478be-102">SYNOPSIS</span></span>
<span data-ttu-id="478be-103">Data Lake Analytics-feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="478be-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="478be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="478be-104">SYNTAX</span></span>

### <span data-ttu-id="478be-105">GetAllInResourceGroupAndAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="478be-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="478be-106">GetBySpecificFeladatInformation</span><span class="sxs-lookup"><span data-stu-id="478be-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="478be-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="478be-107">DESCRIPTION</span></span>
<span data-ttu-id="478be-108">A **Get-AzDataLakeAnalytics Job** parancsmag azure Data Lake Analytics-feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="478be-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="478be-109">Ha nem ad meg feladatot, ez a parancsmag kapja meg az összes feladatot.</span><span class="sxs-lookup"><span data-stu-id="478be-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="478be-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="478be-110">EXAMPLES</span></span>

### <span data-ttu-id="478be-111">1. példa: Egy adott feladat lekérte</span><span class="sxs-lookup"><span data-stu-id="478be-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="478be-112">Ez a parancs a megadott azonosítóval kapja meg a feladatot.</span><span class="sxs-lookup"><span data-stu-id="478be-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="478be-113">2. példa: Az elmúlt egy hétben beküldött feladatok lekérte</span><span class="sxs-lookup"><span data-stu-id="478be-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="478be-114">Ez a parancs az elmúlt héten beküldött feladatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="478be-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="478be-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="478be-115">PARAMETERS</span></span>

### <span data-ttu-id="478be-116">-Account</span><span class="sxs-lookup"><span data-stu-id="478be-116">-Account</span></span>
<span data-ttu-id="478be-117">Egy Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="478be-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="478be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478be-118">-DefaultProfile</span></span>
<span data-ttu-id="478be-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="478be-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="478be-120">-Include</span><span class="sxs-lookup"><span data-stu-id="478be-120">-Include</span></span>
<span data-ttu-id="478be-121">Megadja azokat a beállításokat, amelyek a feladatról lekérni kívánt további információk típusát jelzik.</span><span class="sxs-lookup"><span data-stu-id="478be-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="478be-122">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="478be-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="478be-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="478be-123">None</span></span>
- <span data-ttu-id="478be-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="478be-124">DebugInfo</span></span>
- <span data-ttu-id="478be-125">Statisztika</span><span class="sxs-lookup"><span data-stu-id="478be-125">Statistics</span></span>
- <span data-ttu-id="478be-126">Mind</span><span class="sxs-lookup"><span data-stu-id="478be-126">All</span></span>

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

### <span data-ttu-id="478be-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="478be-127">-JobId</span></span>
<span data-ttu-id="478be-128">A lekért feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="478be-128">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="478be-129">-Name</span><span class="sxs-lookup"><span data-stu-id="478be-129">-Name</span></span>
<span data-ttu-id="478be-130">Megadja a feladatlista eredményeinek szűréséhez használható nevet.</span><span class="sxs-lookup"><span data-stu-id="478be-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="478be-131">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="478be-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="478be-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="478be-132">None</span></span>
- <span data-ttu-id="478be-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="478be-133">DebugInfo</span></span>
- <span data-ttu-id="478be-134">Statisztika</span><span class="sxs-lookup"><span data-stu-id="478be-134">Statistics</span></span>
- <span data-ttu-id="478be-135">Mind</span><span class="sxs-lookup"><span data-stu-id="478be-135">All</span></span>

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

### <span data-ttu-id="478be-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="478be-136">-PipelineId</span></span>
<span data-ttu-id="478be-137">A megadott folyamatnak csak egy részét jelző opcionális azonosítót kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="478be-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

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

### <span data-ttu-id="478be-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="478be-138">-RecurrenceId</span></span>
<span data-ttu-id="478be-139">A megadott ismétlődésnek csak egy részét jelző opcionális azonosítót kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="478be-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

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

### <span data-ttu-id="478be-140">-Result</span><span class="sxs-lookup"><span data-stu-id="478be-140">-Result</span></span>
<span data-ttu-id="478be-141">Egy eredményszűrőt ad meg a feladat eredményéhez.</span><span class="sxs-lookup"><span data-stu-id="478be-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="478be-142">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="478be-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="478be-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="478be-143">None</span></span>
- <span data-ttu-id="478be-144">Megszakítva</span><span class="sxs-lookup"><span data-stu-id="478be-144">Cancelled</span></span>
- <span data-ttu-id="478be-145">Nem sikerült</span><span class="sxs-lookup"><span data-stu-id="478be-145">Failed</span></span>
- <span data-ttu-id="478be-146">Sikeres</span><span class="sxs-lookup"><span data-stu-id="478be-146">Succeeded</span></span>

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

### <span data-ttu-id="478be-147">-State</span><span class="sxs-lookup"><span data-stu-id="478be-147">-State</span></span>
<span data-ttu-id="478be-148">Egy állapotszűrőt ad meg a feladat eredményéhez.</span><span class="sxs-lookup"><span data-stu-id="478be-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="478be-149">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="478be-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="478be-150">Elfogadva</span><span class="sxs-lookup"><span data-stu-id="478be-150">Accepted</span></span>
- <span data-ttu-id="478be-151">Új</span><span class="sxs-lookup"><span data-stu-id="478be-151">New</span></span>
- <span data-ttu-id="478be-152">Összeállítás</span><span class="sxs-lookup"><span data-stu-id="478be-152">Compiling</span></span>
- <span data-ttu-id="478be-153">Ütemezés</span><span class="sxs-lookup"><span data-stu-id="478be-153">Scheduling</span></span>
- <span data-ttu-id="478be-154">Várólistán</span><span class="sxs-lookup"><span data-stu-id="478be-154">Queued</span></span>
- <span data-ttu-id="478be-155">Indítás</span><span class="sxs-lookup"><span data-stu-id="478be-155">Starting</span></span>
- <span data-ttu-id="478be-156">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="478be-156">Paused</span></span>
- <span data-ttu-id="478be-157">Fut</span><span class="sxs-lookup"><span data-stu-id="478be-157">Running</span></span>
- <span data-ttu-id="478be-158">Ended</span><span class="sxs-lookup"><span data-stu-id="478be-158">Ended</span></span>

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

### <span data-ttu-id="478be-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="478be-159">-SubmittedAfter</span></span>
<span data-ttu-id="478be-160">Dátumszűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="478be-160">Specifies a date filter.</span></span>
<span data-ttu-id="478be-161">Ezzel a paraméterrel szűrheti a feladatlista eredményét a megadott dátum után elküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="478be-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

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

### <span data-ttu-id="478be-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="478be-162">-SubmittedBefore</span></span>
<span data-ttu-id="478be-163">Dátumszűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="478be-163">Specifies a date filter.</span></span>
<span data-ttu-id="478be-164">Ezzel a paraméterrel szűrheti a feladatlista eredményét a megadott dátum előtt elküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="478be-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

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

### <span data-ttu-id="478be-165">-Submitter</span><span class="sxs-lookup"><span data-stu-id="478be-165">-Submitter</span></span>
<span data-ttu-id="478be-166">Egy felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="478be-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="478be-167">Ezzel a paraméterrel szűrheti a feladatlista eredményeit a megadott felhasználó által beküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="478be-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

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

### <span data-ttu-id="478be-168">-Top</span><span class="sxs-lookup"><span data-stu-id="478be-168">-Top</span></span>
<span data-ttu-id="478be-169">Nem kötelező érték, amely a visszaadni szükséges feladatok számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="478be-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="478be-170">Az alapértelmezett érték 500</span><span class="sxs-lookup"><span data-stu-id="478be-170">Default value is 500</span></span>

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

### <span data-ttu-id="478be-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478be-171">CommonParameters</span></span>
<span data-ttu-id="478be-172">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="478be-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478be-173">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478be-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478be-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="478be-174">INPUTS</span></span>

### <span data-ttu-id="478be-175">System.String</span><span class="sxs-lookup"><span data-stu-id="478be-175">System.String</span></span>

### <span data-ttu-id="478be-176">System.Guid</span><span class="sxs-lookup"><span data-stu-id="478be-176">System.Guid</span></span>

### <span data-ttu-id="478be-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedDataData</span><span class="sxs-lookup"><span data-stu-id="478be-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="478be-178">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="478be-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="478be-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span><span class="sxs-lookup"><span data-stu-id="478be-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="478be-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span><span class="sxs-lookup"><span data-stu-id="478be-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="478be-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="478be-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="478be-182">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="478be-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="478be-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="478be-183">OUTPUTS</span></span>

### <span data-ttu-id="478be-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="478be-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="478be-185">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="478be-185">NOTES</span></span>

## <span data-ttu-id="478be-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="478be-186">RELATED LINKS</span></span>

[<span data-ttu-id="478be-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="478be-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="478be-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="478be-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="478be-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="478be-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


