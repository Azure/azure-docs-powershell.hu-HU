---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492286"
---
# <span data-ttu-id="5beb1-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5beb1-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="5beb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5beb1-102">SYNOPSIS</span></span>
<span data-ttu-id="5beb1-103">Beolvashatja az adat-tó Analytics-munkáját.</span><span class="sxs-lookup"><span data-stu-id="5beb1-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5beb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5beb1-104">SYNTAX</span></span>

### <span data-ttu-id="5beb1-105">GetAllInResourceGroupAndAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5beb1-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5beb1-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="5beb1-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5beb1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5beb1-107">DESCRIPTION</span></span>
<span data-ttu-id="5beb1-108">A **Get-AzureRmDataLakeAnalyticsJob** parancsmag Azure Data-tó elemzési feladatát kapja.</span><span class="sxs-lookup"><span data-stu-id="5beb1-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="5beb1-109">Ha nem ad meg feladatot, ez a parancsmag minden feladatot beilleszt.</span><span class="sxs-lookup"><span data-stu-id="5beb1-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="5beb1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5beb1-110">EXAMPLES</span></span>

### <span data-ttu-id="5beb1-111">1. példa: meghatározott feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="5beb1-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="5beb1-112">Ez a parancs a megadott AZONOSÍTÓval kapja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="5beb1-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="5beb1-113">2. példa: a múlt héten benyújtott feladatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="5beb1-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="5beb1-114">Ez a parancs a múlt héten benyújtott feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="5beb1-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="5beb1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5beb1-115">PARAMETERS</span></span>

### <span data-ttu-id="5beb1-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="5beb1-116">-Account</span></span>
<span data-ttu-id="5beb1-117">Az adattó-Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5beb1-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5beb1-118">-DefaultProfile</span></span>
<span data-ttu-id="5beb1-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5beb1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-120">-Include (include)</span><span class="sxs-lookup"><span data-stu-id="5beb1-120">-Include</span></span>
<span data-ttu-id="5beb1-121">Azokat a beállításokat adja meg, amelyek jelzik, hogy milyen típusú további információkat kell beolvasni a feladatról.</span><span class="sxs-lookup"><span data-stu-id="5beb1-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="5beb1-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5beb1-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5beb1-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="5beb1-123">None</span></span>
- <span data-ttu-id="5beb1-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="5beb1-124">DebugInfo</span></span>
- <span data-ttu-id="5beb1-125">Statisztikák</span><span class="sxs-lookup"><span data-stu-id="5beb1-125">Statistics</span></span>
- <span data-ttu-id="5beb1-126">Minden</span><span class="sxs-lookup"><span data-stu-id="5beb1-126">All</span></span>

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="5beb1-127">-JobId</span></span>
<span data-ttu-id="5beb1-128">A beolvasott feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5beb1-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5beb1-129">-Name</span></span>
<span data-ttu-id="5beb1-130">A Feladatlista eredményének szűrésére használható nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="5beb1-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="5beb1-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5beb1-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5beb1-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="5beb1-132">None</span></span>
- <span data-ttu-id="5beb1-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="5beb1-133">DebugInfo</span></span>
- <span data-ttu-id="5beb1-134">Statisztikák</span><span class="sxs-lookup"><span data-stu-id="5beb1-134">Statistics</span></span>
- <span data-ttu-id="5beb1-135">Minden</span><span class="sxs-lookup"><span data-stu-id="5beb1-135">All</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="5beb1-136">-PipelineId</span></span>
<span data-ttu-id="5beb1-137">Egy olyan opcionális azonosító, amely csak a megadott csővezeték munkamennyiség részét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="5beb1-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="5beb1-138">-RecurrenceId</span></span>
<span data-ttu-id="5beb1-139">Egy olyan opcionális azonosító, amely csak a megadott ismétlődéshez tartozó feladatokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="5beb1-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-140">-Result (eredmény)</span><span class="sxs-lookup"><span data-stu-id="5beb1-140">-Result</span></span>
<span data-ttu-id="5beb1-141">A projekt eredményéhez tartozó eredményhalmaz-szűrőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="5beb1-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="5beb1-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5beb1-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5beb1-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="5beb1-143">None</span></span>
- <span data-ttu-id="5beb1-144">Lemondott</span><span class="sxs-lookup"><span data-stu-id="5beb1-144">Cancelled</span></span>
- <span data-ttu-id="5beb1-145">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="5beb1-145">Failed</span></span>
- <span data-ttu-id="5beb1-146">Sikerességéről</span><span class="sxs-lookup"><span data-stu-id="5beb1-146">Succeeded</span></span>

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-147">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="5beb1-147">-State</span></span>
<span data-ttu-id="5beb1-148">A projekt eredményéhez tartozó állapot-szűrőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="5beb1-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="5beb1-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5beb1-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5beb1-150">Elfogadott</span><span class="sxs-lookup"><span data-stu-id="5beb1-150">Accepted</span></span>
- <span data-ttu-id="5beb1-151">Új</span><span class="sxs-lookup"><span data-stu-id="5beb1-151">New</span></span>
- <span data-ttu-id="5beb1-152">Összeállítása</span><span class="sxs-lookup"><span data-stu-id="5beb1-152">Compiling</span></span>
- <span data-ttu-id="5beb1-153">Ütemezés</span><span class="sxs-lookup"><span data-stu-id="5beb1-153">Scheduling</span></span>
- <span data-ttu-id="5beb1-154">Várólistán töltött</span><span class="sxs-lookup"><span data-stu-id="5beb1-154">Queued</span></span>
- <span data-ttu-id="5beb1-155">Kezdve</span><span class="sxs-lookup"><span data-stu-id="5beb1-155">Starting</span></span>
- <span data-ttu-id="5beb1-156">Szünetel</span><span class="sxs-lookup"><span data-stu-id="5beb1-156">Paused</span></span>
- <span data-ttu-id="5beb1-157">Fut</span><span class="sxs-lookup"><span data-stu-id="5beb1-157">Running</span></span>
- <span data-ttu-id="5beb1-158">Véget</span><span class="sxs-lookup"><span data-stu-id="5beb1-158">Ended</span></span>

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="5beb1-159">-SubmittedAfter</span></span>
<span data-ttu-id="5beb1-160">A Dátumszűrő értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5beb1-160">Specifies a date filter.</span></span>
<span data-ttu-id="5beb1-161">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét a megadott dátum után elküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="5beb1-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="5beb1-162">-SubmittedBefore</span></span>
<span data-ttu-id="5beb1-163">A Dátumszűrő értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5beb1-163">Specifies a date filter.</span></span>
<span data-ttu-id="5beb1-164">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét a megadott dátum előtt elküldött feladatokra.</span><span class="sxs-lookup"><span data-stu-id="5beb1-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-165">-Beküldő</span><span class="sxs-lookup"><span data-stu-id="5beb1-165">-Submitter</span></span>
<span data-ttu-id="5beb1-166">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5beb1-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="5beb1-167">Ezzel a paraméterrel szűrheti a tevékenységlista eredményét egy adott felhasználó által elküldött munkákra.</span><span class="sxs-lookup"><span data-stu-id="5beb1-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-168">-Top</span><span class="sxs-lookup"><span data-stu-id="5beb1-168">-Top</span></span>
<span data-ttu-id="5beb1-169">Egy tetszőleges érték, amely a visszaadott feladatok számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="5beb1-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="5beb1-170">Az alapértelmezett érték a 500</span><span class="sxs-lookup"><span data-stu-id="5beb1-170">Default value is 500</span></span>

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5beb1-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5beb1-171">CommonParameters</span></span>
<span data-ttu-id="5beb1-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5beb1-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5beb1-173">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5beb1-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5beb1-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5beb1-174">INPUTS</span></span>

### <span data-ttu-id="5beb1-175">GUID</span><span class="sxs-lookup"><span data-stu-id="5beb1-175">Guid</span></span>
<span data-ttu-id="5beb1-176">A ' JobId ' paraméter a pipeline "GUID" típusú értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5beb1-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="5beb1-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5beb1-177">OUTPUTS</span></span>

### <span data-ttu-id="5beb1-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="5beb1-178">JobInformation</span></span>
<span data-ttu-id="5beb1-179">A megadott projektfeladat adatai</span><span class="sxs-lookup"><span data-stu-id="5beb1-179">The specified job information details</span></span>

### <span data-ttu-id="5beb1-180">Lista<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="5beb1-180">List<PSJobInformationBasic></span></span>
<span data-ttu-id="5beb1-181">A megadott adattó-fiókban lévő feladatok listája.</span><span class="sxs-lookup"><span data-stu-id="5beb1-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="5beb1-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5beb1-182">NOTES</span></span>

## <span data-ttu-id="5beb1-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5beb1-183">RELATED LINKS</span></span>

[<span data-ttu-id="5beb1-184">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5beb1-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="5beb1-185">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5beb1-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="5beb1-186">Várjon-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5beb1-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


