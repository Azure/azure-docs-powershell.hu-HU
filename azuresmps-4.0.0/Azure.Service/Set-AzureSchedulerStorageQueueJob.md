---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016050"
---
# <span data-ttu-id="928e8-101">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="928e8-101">Set-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="928e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="928e8-102">SYNOPSIS</span></span>
<span data-ttu-id="928e8-103">A tárolási műveleteket tartalmazó ütemező feladatot frissít.</span><span class="sxs-lookup"><span data-stu-id="928e8-103">Updates a scheduler job that has a storage action.</span></span>

## <span data-ttu-id="928e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="928e8-104">SYNTAX</span></span>

### <span data-ttu-id="928e8-105">Szükséges</span><span class="sxs-lookup"><span data-stu-id="928e8-105">Required</span></span>
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="928e8-106">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="928e8-106">Recurring</span></span>
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="928e8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="928e8-107">DESCRIPTION</span></span>
<span data-ttu-id="928e8-108">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="928e8-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="928e8-109">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="928e8-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="928e8-110">A **set-AzureSchedulerStorageQueueJob** parancsmag olyan ütemező feladatot frissít, amely Azure Storage művelettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="928e8-110">The **Set-AzureSchedulerStorageQueueJob** cmdlet updates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="928e8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="928e8-111">EXAMPLES</span></span>

### <span data-ttu-id="928e8-112">Példa 1: tárterület-várólista üzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="928e8-112">Example 1: Update a Storage queue message</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

<span data-ttu-id="928e8-113">Ez a parancs frissíti a Job12 nevű tárterület várólistájának üzenetét.</span><span class="sxs-lookup"><span data-stu-id="928e8-113">This command updates the queue message for the Storage job named Job12.</span></span>
<span data-ttu-id="928e8-114">A parancs a Job Collection nevét és a helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-114">The command specifies the job collection name and the location.</span></span>

### <span data-ttu-id="928e8-115">2. példa: tárterület-várólista-feladat engedélyezése</span><span class="sxs-lookup"><span data-stu-id="928e8-115">Example 2: Enable a Storage queue job</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

<span data-ttu-id="928e8-116">Ez a parancs engedélyezi a Job16 nevű feladatot.</span><span class="sxs-lookup"><span data-stu-id="928e8-116">This command enables the job named Job16.</span></span>
<span data-ttu-id="928e8-117">A parancs a *JobState* paraméter értékének megadásával módosítja a feladat állapotát.</span><span class="sxs-lookup"><span data-stu-id="928e8-117">The command changes the state of the job to Enabled by specifying that value for the *JobState* parameter.</span></span>

## <span data-ttu-id="928e8-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="928e8-118">PARAMETERS</span></span>

### <span data-ttu-id="928e8-119">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="928e8-119">-EndTime</span></span>
<span data-ttu-id="928e8-120">Időpontot ad meg **datetime** -objektumként a Feladatütemező számára a feladat kezdeményezésének befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="928e8-120">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="928e8-121">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="928e8-121">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="928e8-122">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="928e8-122">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="928e8-123">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="928e8-123">-ErrorActionHeaders</span></span>
<span data-ttu-id="928e8-124">A fejléceket a hash-táblázatként adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-124">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="928e8-125">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="928e8-125">-ErrorActionMethod</span></span>
<span data-ttu-id="928e8-126">A HTTP-és HTTPS-műveletek típusának megfelelő módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-126">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="928e8-127">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="928e8-127">Valid values are:</span></span> 

- <span data-ttu-id="928e8-128">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="928e8-128">GET</span></span>
- <span data-ttu-id="928e8-129">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="928e8-129">PUT</span></span>
- <span data-ttu-id="928e8-130">POST</span><span class="sxs-lookup"><span data-stu-id="928e8-130">POST</span></span>
- <span data-ttu-id="928e8-131">FEJ</span><span class="sxs-lookup"><span data-stu-id="928e8-131">HEAD</span></span>
- <span data-ttu-id="928e8-132">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="928e8-132">DELETE</span></span>

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

### <span data-ttu-id="928e8-133">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="928e8-133">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="928e8-134">A tárolási feladatok szövegtörzsét adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-134">Specifies the body for Storage job actions.</span></span>

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

### <span data-ttu-id="928e8-135">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="928e8-135">-ErrorActionRequestBody</span></span>
<span data-ttu-id="928e8-136">A feladatok elvégzésére és KÖZZÉTÉTELére szolgáló szövegtörzset adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-136">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="928e8-137">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="928e8-137">-ErrorActionSASToken</span></span>
<span data-ttu-id="928e8-138">Megadja a tárterület-várólistához tartozó megosztott hozzáférés-aláírási (SA) tokent.</span><span class="sxs-lookup"><span data-stu-id="928e8-138">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

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

### <span data-ttu-id="928e8-139">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="928e8-139">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="928e8-140">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-140">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="928e8-141">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="928e8-141">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="928e8-142">A tárolási várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-142">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="928e8-143">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="928e8-143">-ErrorActionURI</span></span>
<span data-ttu-id="928e8-144">A hiba-feladathoz tartozó URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-144">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="928e8-145">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="928e8-145">-ExecutionCount</span></span>
<span data-ttu-id="928e8-146">A futtatott feladat előfordulásainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-146">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="928e8-147">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="928e8-147">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="928e8-148">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="928e8-148">-Frequency</span></span>
<span data-ttu-id="928e8-149">A Feladatütemező maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-149">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="928e8-150">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="928e8-150">-Interval</span></span>
<span data-ttu-id="928e8-151">A *gyakoriság* paraméterrel megadott gyakoriságú ismétlődési intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-151">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="928e8-152">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="928e8-152">-JobCollectionName</span></span>
<span data-ttu-id="928e8-153">Annak a gyűjteménynek a nevét adja meg, amely a Feladatütemező feladatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="928e8-153">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="928e8-154">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="928e8-154">-JobName</span></span>
<span data-ttu-id="928e8-155">A frissítendő ütemező-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-155">Specifies the name of the scheduler job to update.</span></span>

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

### <span data-ttu-id="928e8-156">-JobState</span><span class="sxs-lookup"><span data-stu-id="928e8-156">-JobState</span></span>
<span data-ttu-id="928e8-157">A Feladatütemező feladatához tartozó állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-157">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="928e8-158">-Hely</span><span class="sxs-lookup"><span data-stu-id="928e8-158">-Location</span></span>
<span data-ttu-id="928e8-159">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="928e8-159">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="928e8-160">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="928e8-160">Valid values are:</span></span> 

- <span data-ttu-id="928e8-161">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="928e8-161">Anywhere Asia</span></span>
- <span data-ttu-id="928e8-162">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="928e8-162">Anywhere Europe</span></span>
- <span data-ttu-id="928e8-163">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="928e8-163">Anywhere US</span></span>
- <span data-ttu-id="928e8-164">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="928e8-164">East Asia</span></span>
- <span data-ttu-id="928e8-165">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="928e8-165">East US</span></span>
- <span data-ttu-id="928e8-166">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="928e8-166">North Central US</span></span>
- <span data-ttu-id="928e8-167">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="928e8-167">North Europe</span></span>
- <span data-ttu-id="928e8-168">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="928e8-168">South Central US</span></span>
- <span data-ttu-id="928e8-169">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="928e8-169">Southeast Asia</span></span>
- <span data-ttu-id="928e8-170">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="928e8-170">West Europe</span></span>
- <span data-ttu-id="928e8-171">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="928e8-171">West US</span></span>

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

### <span data-ttu-id="928e8-172">-PassThru</span><span class="sxs-lookup"><span data-stu-id="928e8-172">-PassThru</span></span>
<span data-ttu-id="928e8-173">Azt jelzi, hogy ez a parancsmag egy olyan objektumot ad eredményül, amely a működéséhez szükséges elemet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="928e8-173">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="928e8-174">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="928e8-174">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928e8-175">-Profil</span><span class="sxs-lookup"><span data-stu-id="928e8-175">-Profile</span></span>
<span data-ttu-id="928e8-176">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="928e8-176">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="928e8-177">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="928e8-177">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="928e8-178">-SASToken</span><span class="sxs-lookup"><span data-stu-id="928e8-178">-SASToken</span></span>
<span data-ttu-id="928e8-179">A tárolási várólista biztonsági társítási jogkivonatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-179">Specifies the SAS token for the Storage queue.</span></span>

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

### <span data-ttu-id="928e8-180">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="928e8-180">-StartTime</span></span>
<span data-ttu-id="928e8-181">Időpontot ad meg **datetime** objektumként a kezdéshez.</span><span class="sxs-lookup"><span data-stu-id="928e8-181">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="928e8-182">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="928e8-182">-StorageQueueAccount</span></span>
<span data-ttu-id="928e8-183">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-183">Specifies the Storage account name.</span></span>

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

### <span data-ttu-id="928e8-184">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="928e8-184">-StorageQueueMessage</span></span>
<span data-ttu-id="928e8-185">A tárolási feladat várólistájának üzenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-185">Specifies the queue message for the Storage job.</span></span>

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

### <span data-ttu-id="928e8-186">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="928e8-186">-StorageQueueName</span></span>
<span data-ttu-id="928e8-187">A tárolási várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="928e8-187">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="928e8-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928e8-188">CommonParameters</span></span>
<span data-ttu-id="928e8-189">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="928e8-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928e8-190">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928e8-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928e8-191">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="928e8-191">INPUTS</span></span>

## <span data-ttu-id="928e8-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="928e8-192">OUTPUTS</span></span>

## <span data-ttu-id="928e8-193">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="928e8-193">NOTES</span></span>

## <span data-ttu-id="928e8-194">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="928e8-194">RELATED LINKS</span></span>

[<span data-ttu-id="928e8-195">Új – AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="928e8-195">New-AzureSchedulerStorageQueueJob</span></span>](./New-AzureSchedulerStorageQueueJob.md)


