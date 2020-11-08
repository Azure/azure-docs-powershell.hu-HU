---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015902"
---
# <span data-ttu-id="d304b-101">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d304b-101">New-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="d304b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d304b-102">SYNOPSIS</span></span>
<span data-ttu-id="d304b-103">A tárolási műveleteket tartalmazó ütemező feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d304b-103">Creates a scheduler job that has a Storage action.</span></span>

## <span data-ttu-id="d304b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d304b-104">SYNTAX</span></span>

### <span data-ttu-id="d304b-105">Szükséges</span><span class="sxs-lookup"><span data-stu-id="d304b-105">Required</span></span>
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d304b-106">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="d304b-106">Recurring</span></span>
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d304b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d304b-107">DESCRIPTION</span></span>
<span data-ttu-id="d304b-108">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="d304b-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d304b-109">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d304b-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d304b-110">A **New-AzureSchedulerStorageQueueJob** parancsmag létrehoz egy olyan Feladatütemező-feladatot, amely Azure Storage művelettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="d304b-110">The **New-AzureSchedulerStorageQueueJob** cmdlet creates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="d304b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d304b-111">EXAMPLES</span></span>

### <span data-ttu-id="d304b-112">Példa 1: egyszer futó tárolási feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="d304b-112">Example 1: Create a Storage job that runs once</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

<span data-ttu-id="d304b-113">Ez a parancs létrehoz egy Feladatütemező tárolási feladatot a JobCollection01 nevű gyűjtemény részeként.</span><span class="sxs-lookup"><span data-stu-id="d304b-113">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="d304b-114">A parancs a tárolási fiókot, a várólista nevét és a SAS-tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-114">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="d304b-115">A feladat egyszer, azonnal fut.</span><span class="sxs-lookup"><span data-stu-id="d304b-115">The job runs once, immediately.</span></span>

### <span data-ttu-id="d304b-116">2. példa: adott számú alkalommal futó tárterület létrehozása</span><span class="sxs-lookup"><span data-stu-id="d304b-116">Example 2: Create a Storage job that runs a specified number of times</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

<span data-ttu-id="d304b-117">Ez a parancs létrehoz egy Feladatütemező tárolási feladatot a JobCollection01 nevű gyűjtemény részeként.</span><span class="sxs-lookup"><span data-stu-id="d304b-117">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="d304b-118">A parancs a tárolási fiókot, a várólista nevét és a SAS-tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-118">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="d304b-119">A feladat összesen 20 alkalommal, óránként kétszer fut.</span><span class="sxs-lookup"><span data-stu-id="d304b-119">The job runs 20 times in total, twice every hour.</span></span>

## <span data-ttu-id="d304b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d304b-120">PARAMETERS</span></span>

### <span data-ttu-id="d304b-121">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="d304b-121">-EndTime</span></span>
<span data-ttu-id="d304b-122">Időpontot ad meg **datetime** -objektumként a Feladatütemező számára a feladat kezdeményezésének befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d304b-122">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="d304b-123">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d304b-123">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="d304b-124">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d304b-124">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-125">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="d304b-125">-ErrorActionHeaders</span></span>
<span data-ttu-id="d304b-126">A fejléceket a hash-táblázatként adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-126">Specifies headers as a hash table.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-127">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="d304b-127">-ErrorActionMethod</span></span>
<span data-ttu-id="d304b-128">A HTTP-és HTTPS-műveletek típusának megfelelő módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-128">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="d304b-129">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d304b-129">Valid values are:</span></span> 

- <span data-ttu-id="d304b-130">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="d304b-130">GET</span></span>
- <span data-ttu-id="d304b-131">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="d304b-131">PUT</span></span>
- <span data-ttu-id="d304b-132">POST</span><span class="sxs-lookup"><span data-stu-id="d304b-132">POST</span></span>
- <span data-ttu-id="d304b-133">FEJ</span><span class="sxs-lookup"><span data-stu-id="d304b-133">HEAD</span></span>
- <span data-ttu-id="d304b-134">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="d304b-134">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-135">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="d304b-135">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="d304b-136">A tárolási feladatok szövegtörzsét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-136">Specifies the body for Storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-137">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="d304b-137">-ErrorActionRequestBody</span></span>
<span data-ttu-id="d304b-138">A feladatok elvégzésére és KÖZZÉTÉTELére szolgáló szövegtörzset adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-138">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-139">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="d304b-139">-ErrorActionSASToken</span></span>
<span data-ttu-id="d304b-140">Megadja a tárterület-várólistához tartozó megosztott hozzáférés-aláírási (SA) tokent.</span><span class="sxs-lookup"><span data-stu-id="d304b-140">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-141">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d304b-141">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="d304b-142">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-142">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-143">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d304b-143">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="d304b-144">A tárolási várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-144">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-145">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="d304b-145">-ErrorActionURI</span></span>
<span data-ttu-id="d304b-146">A hiba-feladathoz tartozó URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-146">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-147">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="d304b-147">-ExecutionCount</span></span>
<span data-ttu-id="d304b-148">A futtatott feladat előfordulásainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-148">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="d304b-149">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="d304b-149">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-150">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="d304b-150">-Frequency</span></span>
<span data-ttu-id="d304b-151">A Feladatütemező maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-151">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-152">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="d304b-152">-Interval</span></span>
<span data-ttu-id="d304b-153">A *gyakoriság* paraméterrel megadott gyakoriságú ismétlődési intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-153">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-154">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d304b-154">-JobCollectionName</span></span>
<span data-ttu-id="d304b-155">Annak a gyűjteménynek a nevét adja meg, amely a Feladatütemező feladatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d304b-155">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-156">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="d304b-156">-JobName</span></span>
<span data-ttu-id="d304b-157">A Feladatütemező feladatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-157">Specifies the name for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-158">-JobState</span><span class="sxs-lookup"><span data-stu-id="d304b-158">-JobState</span></span>
<span data-ttu-id="d304b-159">A Feladatütemező feladatához tartozó állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-159">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="d304b-160">-Hely</span><span class="sxs-lookup"><span data-stu-id="d304b-160">-Location</span></span>
<span data-ttu-id="d304b-161">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="d304b-161">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="d304b-162">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d304b-162">Valid values are:</span></span> 

- <span data-ttu-id="d304b-163">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="d304b-163">Anywhere Asia</span></span>
- <span data-ttu-id="d304b-164">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="d304b-164">Anywhere Europe</span></span>
- <span data-ttu-id="d304b-165">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="d304b-165">Anywhere US</span></span>
- <span data-ttu-id="d304b-166">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="d304b-166">East Asia</span></span>
- <span data-ttu-id="d304b-167">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="d304b-167">East US</span></span>
- <span data-ttu-id="d304b-168">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="d304b-168">North Central US</span></span>
- <span data-ttu-id="d304b-169">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="d304b-169">North Europe</span></span>
- <span data-ttu-id="d304b-170">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="d304b-170">South Central US</span></span>
- <span data-ttu-id="d304b-171">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="d304b-171">Southeast Asia</span></span>
- <span data-ttu-id="d304b-172">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="d304b-172">West Europe</span></span>
- <span data-ttu-id="d304b-173">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="d304b-173">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-174">-Profil</span><span class="sxs-lookup"><span data-stu-id="d304b-174">-Profile</span></span>
<span data-ttu-id="d304b-175">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d304b-175">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d304b-176">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d304b-176">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d304b-177">-SASToken</span><span class="sxs-lookup"><span data-stu-id="d304b-177">-SASToken</span></span>
<span data-ttu-id="d304b-178">A tárolási várólista biztonsági társítási jogkivonatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-178">Specifies the SAS token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-179">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="d304b-179">-StartTime</span></span>
<span data-ttu-id="d304b-180">Időpontot ad meg **datetime** objektumként a kezdéshez.</span><span class="sxs-lookup"><span data-stu-id="d304b-180">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-181">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="d304b-181">-StorageQueueAccount</span></span>
<span data-ttu-id="d304b-182">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-182">Specifies the Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-183">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="d304b-183">-StorageQueueMessage</span></span>
<span data-ttu-id="d304b-184">A tárolási feladatok várólistájának üzenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-184">Specifies the queue message for Storage job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-185">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="d304b-185">-StorageQueueName</span></span>
<span data-ttu-id="d304b-186">A tárolási várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d304b-186">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d304b-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d304b-187">CommonParameters</span></span>
<span data-ttu-id="d304b-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d304b-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d304b-189">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d304b-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d304b-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d304b-190">INPUTS</span></span>

## <span data-ttu-id="d304b-191">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d304b-191">OUTPUTS</span></span>

## <span data-ttu-id="d304b-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d304b-192">NOTES</span></span>

## <span data-ttu-id="d304b-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d304b-193">RELATED LINKS</span></span>

[<span data-ttu-id="d304b-194">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d304b-194">Set-AzureSchedulerStorageQueueJob</span></span>](./Set-AzureSchedulerStorageQueueJob.md)


