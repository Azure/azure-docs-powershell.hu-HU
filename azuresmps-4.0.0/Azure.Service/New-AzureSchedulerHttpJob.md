---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C608BBDD-DC2B-4BEF-812D-0BAE94FB4395
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f5332c18d2d47096f246485ac0d811548f70aa9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015904"
---
# <span data-ttu-id="2ed99-101">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2ed99-101">New-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="2ed99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ed99-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed99-103">HTTP-műveleteket tartalmazó ütemező feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2ed99-103">Creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="2ed99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ed99-104">SYNTAX</span></span>

### <span data-ttu-id="2ed99-105">Szükséges</span><span class="sxs-lookup"><span data-stu-id="2ed99-105">Required</span></span>
```
New-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> -Method <String>
 -URI <Uri> [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ed99-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="2ed99-106">PutPost</span></span>
```
New-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2ed99-107">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="2ed99-107">Recurring</span></span>
```
New-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2ed99-108">Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="2ed99-108">Authentication</span></span>
```
New-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2ed99-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ed99-109">DESCRIPTION</span></span>
<span data-ttu-id="2ed99-110">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="2ed99-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2ed99-111">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2ed99-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2ed99-112">A **New-AzureSchedulerHttpJob** parancsmag olyan Feladatütemezőt hoz létre, amely http-művelettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="2ed99-112">The **New-AzureSchedulerHttpJob** cmdlet creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="2ed99-113">Példák</span><span class="sxs-lookup"><span data-stu-id="2ed99-113">EXAMPLES</span></span>

### <span data-ttu-id="2ed99-114">Példa 1: HTTP-feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="2ed99-114">Example 1: Create an HTTP job</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -Method "GET" -URI http://www.contoso.com
```

<span data-ttu-id="2ed99-115">Ez a parancs létrehoz egy Scheduler HTTP-feladatot a JobCollection01 nevű munkagyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="2ed99-115">This command creates a scheduler HTTP job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="2ed99-116">A parancs egy URI-azonosítót ad meg, és a GET metódust adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-116">The command specifies a URI and specifies GET as the method.</span></span>

### <span data-ttu-id="2ed99-117">2. példa: HTTP-feladat létrehozása adott futási számhoz</span><span class="sxs-lookup"><span data-stu-id="2ed99-117">Example 2: Create an HTTP job for a specific run count</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01 -JobName "Job23" -Location "North Central US" -Method "GET" -URI http://www.contoso.com -ExecutionCount 20
```

<span data-ttu-id="2ed99-118">Ez a parancs a JobCollection01 nevű munkagyűjteményben létrehozza az ütemező http-feladatot.</span><span class="sxs-lookup"><span data-stu-id="2ed99-118">This command creates scheduler http job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="2ed99-119">A parancs egy URI-azonosítót ad meg, és a GET metódust adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-119">The command specifies a URI and specifies GET as the method.</span></span>
<span data-ttu-id="2ed99-120">A parancs hatására a feladat 20 időpontot futtat.</span><span class="sxs-lookup"><span data-stu-id="2ed99-120">This command causes the job to run 20 times.</span></span>

## <span data-ttu-id="2ed99-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ed99-121">PARAMETERS</span></span>

### <span data-ttu-id="2ed99-122">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="2ed99-122">-ClientCertificatePassword</span></span>
```yaml
Type: String
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed99-123">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="2ed99-123">-ClientCertificatePfx</span></span>
```yaml
Type: Object
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed99-124">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="2ed99-124">-EndTime</span></span>
<span data-ttu-id="2ed99-125">Időpontot ad meg **datetime** -objektumként a Feladatütemező számára a feladatok kezdeményezésének befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="2ed99-125">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="2ed99-126">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2ed99-126">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="2ed99-127">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="2ed99-127">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed99-128">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="2ed99-128">-ErrorActionHeaders</span></span>
<span data-ttu-id="2ed99-129">A fejléceket Hashtable adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-129">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="2ed99-130">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="2ed99-130">-ErrorActionMethod</span></span>
<span data-ttu-id="2ed99-131">A HTTP-és HTTPS-műveletek típusának megfelelő módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-131">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="2ed99-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="2ed99-132">Valid values are:</span></span> 

- <span data-ttu-id="2ed99-133">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="2ed99-133">GET</span></span>
- <span data-ttu-id="2ed99-134">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="2ed99-134">PUT</span></span>
- <span data-ttu-id="2ed99-135">POST</span><span class="sxs-lookup"><span data-stu-id="2ed99-135">POST</span></span>
- <span data-ttu-id="2ed99-136">FEJ</span><span class="sxs-lookup"><span data-stu-id="2ed99-136">HEAD</span></span>
- <span data-ttu-id="2ed99-137">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="2ed99-137">DELETE</span></span>

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

### <span data-ttu-id="2ed99-138">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="2ed99-138">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="2ed99-139">A tárolási feladatok szövegtörzsét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-139">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="2ed99-140">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="2ed99-140">-ErrorActionRequestBody</span></span>
<span data-ttu-id="2ed99-141">A feladatok elvégzésére és KÖZZÉTÉTELére szolgáló szövegtörzset adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-141">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="2ed99-142">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="2ed99-142">-ErrorActionSASToken</span></span>
<span data-ttu-id="2ed99-143">Megadja a tárterület-várólistához tartozó megosztott hozzáférés-aláírási (SA) tokent.</span><span class="sxs-lookup"><span data-stu-id="2ed99-143">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="2ed99-144">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2ed99-144">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="2ed99-145">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-145">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="2ed99-146">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2ed99-146">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="2ed99-147">A tárolási várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-147">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="2ed99-148">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="2ed99-148">-ErrorActionURI</span></span>
<span data-ttu-id="2ed99-149">A hiba-feladathoz tartozó URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-149">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="2ed99-150">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="2ed99-150">-ExecutionCount</span></span>
<span data-ttu-id="2ed99-151">A futtatott feladat előfordulásainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-151">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="2ed99-152">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="2ed99-152">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed99-153">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="2ed99-153">-Frequency</span></span>
<span data-ttu-id="2ed99-154">A Feladatütemező maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-154">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed99-155">– Fejlécek</span><span class="sxs-lookup"><span data-stu-id="2ed99-155">-Headers</span></span>
<span data-ttu-id="2ed99-156">A fejléceket Hashtable adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-156">Specifies the headers as a hashtable.</span></span>

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

### <span data-ttu-id="2ed99-157">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="2ed99-157">-HttpAuthenticationType</span></span>
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

```yaml
Type: String
Parameter Sets: Authentication
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed99-158">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="2ed99-158">-Interval</span></span>
<span data-ttu-id="2ed99-159">A *gyakoriság* paraméterrel megadott gyakoriságú ismétlődési intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-159">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed99-160">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2ed99-160">-JobCollectionName</span></span>
<span data-ttu-id="2ed99-161">Annak a gyűjteménynek a nevét adja meg, amely a Feladatütemező feladatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2ed99-161">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="2ed99-162">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="2ed99-162">-JobName</span></span>
<span data-ttu-id="2ed99-163">A Feladatütemező feladatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-163">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="2ed99-164">-JobState</span><span class="sxs-lookup"><span data-stu-id="2ed99-164">-JobState</span></span>
<span data-ttu-id="2ed99-165">A Feladatütemező feladatához tartozó állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-165">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="2ed99-166">-Hely</span><span class="sxs-lookup"><span data-stu-id="2ed99-166">-Location</span></span>
<span data-ttu-id="2ed99-167">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="2ed99-167">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="2ed99-168">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="2ed99-168">Valid values are:</span></span> 

- <span data-ttu-id="2ed99-169">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="2ed99-169">Anywhere Asia</span></span>
- <span data-ttu-id="2ed99-170">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="2ed99-170">Anywhere Europe</span></span>
- <span data-ttu-id="2ed99-171">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="2ed99-171">Anywhere US</span></span>
- <span data-ttu-id="2ed99-172">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="2ed99-172">East Asia</span></span>
- <span data-ttu-id="2ed99-173">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="2ed99-173">East US</span></span>
- <span data-ttu-id="2ed99-174">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="2ed99-174">North Central US</span></span>
- <span data-ttu-id="2ed99-175">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="2ed99-175">North Europe</span></span>
- <span data-ttu-id="2ed99-176">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="2ed99-176">South Central US</span></span>
- <span data-ttu-id="2ed99-177">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="2ed99-177">Southeast Asia</span></span>
- <span data-ttu-id="2ed99-178">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="2ed99-178">West Europe</span></span>
- <span data-ttu-id="2ed99-179">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="2ed99-179">West US</span></span>

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

### <span data-ttu-id="2ed99-180">-Módszer</span><span class="sxs-lookup"><span data-stu-id="2ed99-180">-Method</span></span>
<span data-ttu-id="2ed99-181">A HTTP-és HTTPS-műveletek típusának megfelelő módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-181">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="2ed99-182">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="2ed99-182">Valid values are:</span></span> 

- <span data-ttu-id="2ed99-183">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="2ed99-183">GET</span></span>
- <span data-ttu-id="2ed99-184">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="2ed99-184">PUT</span></span>
- <span data-ttu-id="2ed99-185">POST</span><span class="sxs-lookup"><span data-stu-id="2ed99-185">POST</span></span>
- <span data-ttu-id="2ed99-186">FEJ</span><span class="sxs-lookup"><span data-stu-id="2ed99-186">HEAD</span></span>
- <span data-ttu-id="2ed99-187">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="2ed99-187">DELETE</span></span>

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

### <span data-ttu-id="2ed99-188">-Profil</span><span class="sxs-lookup"><span data-stu-id="2ed99-188">-Profile</span></span>
<span data-ttu-id="2ed99-189">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="2ed99-189">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ed99-190">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="2ed99-190">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ed99-191">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="2ed99-191">-RequestBody</span></span>
<span data-ttu-id="2ed99-192">A feladatok elvégzésére és KÖZZÉTÉTELére szolgáló szövegtörzset adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-192">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required, PutPost
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed99-193">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="2ed99-193">-StartTime</span></span>
<span data-ttu-id="2ed99-194">Időpontot ad meg **datetime** objektumként a kezdéshez.</span><span class="sxs-lookup"><span data-stu-id="2ed99-194">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="2ed99-195">-URI</span><span class="sxs-lookup"><span data-stu-id="2ed99-195">-URI</span></span>
<span data-ttu-id="2ed99-196">A projektfeladat URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ed99-196">Specifies a URI for a job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed99-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed99-197">CommonParameters</span></span>
<span data-ttu-id="2ed99-198">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ed99-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed99-199">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed99-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed99-200">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ed99-200">INPUTS</span></span>

## <span data-ttu-id="2ed99-201">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ed99-201">OUTPUTS</span></span>

## <span data-ttu-id="2ed99-202">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ed99-202">NOTES</span></span>

## <span data-ttu-id="2ed99-203">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ed99-203">RELATED LINKS</span></span>

[<span data-ttu-id="2ed99-204">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2ed99-204">Set-AzureSchedulerHttpJob</span></span>](./Set-AzureSchedulerHttpJob.md)


