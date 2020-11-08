---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BBB1A0B7-2F5A-4799-8375-1D775C9D6E2F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 935d9ace51144cdd54cbcf3348ed9fc6b9b4ea02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015799"
---
# <span data-ttu-id="750dc-101">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="750dc-101">Set-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="750dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="750dc-102">SYNOPSIS</span></span>
<span data-ttu-id="750dc-103">Egy HTTP-művelettel rendelkező ütemező-feladatot frissít.</span><span class="sxs-lookup"><span data-stu-id="750dc-103">Updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="750dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="750dc-104">SYNTAX</span></span>

### <span data-ttu-id="750dc-105">Szükséges</span><span class="sxs-lookup"><span data-stu-id="750dc-105">Required</span></span>
```
Set-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> [-Method <String>]
 [-URI <Uri>] [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="750dc-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="750dc-106">PutPost</span></span>
```
Set-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="750dc-107">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="750dc-107">Recurring</span></span>
```
Set-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="750dc-108">Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="750dc-108">Authentication</span></span>
```
Set-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="750dc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="750dc-109">DESCRIPTION</span></span>
<span data-ttu-id="750dc-110">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="750dc-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="750dc-111">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="750dc-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="750dc-112">A **set-AzureSchedulerHttpJob** parancsmag olyan Feladatütemező-feladatot frissít, amely http-művelettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="750dc-112">The **Set-AzureSchedulerHttpJob** cmdlet updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="750dc-113">Példák</span><span class="sxs-lookup"><span data-stu-id="750dc-113">EXAMPLES</span></span>

### <span data-ttu-id="750dc-114">Példa 1: a feladat állapotának módosítása letiltva</span><span class="sxs-lookup"><span data-stu-id="750dc-114">Example 1: Change the state of a job to Disabled</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01" -JobState "Disabled"
```

<span data-ttu-id="750dc-115">A parancs a Job01 nevű feladat állapotát letiltva változtatja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-115">This command changes the state of the job named Job01 to Disabled.</span></span>
<span data-ttu-id="750dc-116">Ez a feladat a megadott helyhez tartozó JobColleciton01 nevű Job Collection része.</span><span class="sxs-lookup"><span data-stu-id="750dc-116">That job is part of the job collection named JobColleciton01 for the specified location.</span></span>

### <span data-ttu-id="750dc-117">2. példa: a feladat URI-ja frissítése</span><span class="sxs-lookup"><span data-stu-id="750dc-117">Example 2: Update the URI of a job</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job37" -URI http://www.contoso.com
```

<span data-ttu-id="750dc-118">Ez a parancs frissíti a Job01 nevű feladat URI-azonosítóját http://www.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="750dc-118">This command updates the URI of the job named Job01 to be http://www.contoso.com.</span></span>

## <span data-ttu-id="750dc-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="750dc-119">PARAMETERS</span></span>

### <span data-ttu-id="750dc-120">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="750dc-120">-ClientCertificatePassword</span></span>
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

### <span data-ttu-id="750dc-121">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="750dc-121">-ClientCertificatePfx</span></span>
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

### <span data-ttu-id="750dc-122">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="750dc-122">-EndTime</span></span>
<span data-ttu-id="750dc-123">Időpontot ad meg **datetime** -objektumként a Feladatütemező számára a feladatok kezdeményezésének befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="750dc-123">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="750dc-124">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="750dc-124">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="750dc-125">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="750dc-125">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="750dc-126">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="750dc-126">-ErrorActionHeaders</span></span>
<span data-ttu-id="750dc-127">A fejléceket Hashtable adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-127">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="750dc-128">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="750dc-128">-ErrorActionMethod</span></span>
<span data-ttu-id="750dc-129">A HTTP-és HTTPS-műveletek típusának megfelelő módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-129">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="750dc-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="750dc-130">Valid values are:</span></span> 

- <span data-ttu-id="750dc-131">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="750dc-131">GET</span></span>
- <span data-ttu-id="750dc-132">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="750dc-132">PUT</span></span>
- <span data-ttu-id="750dc-133">POST</span><span class="sxs-lookup"><span data-stu-id="750dc-133">POST</span></span>
- <span data-ttu-id="750dc-134">FEJ</span><span class="sxs-lookup"><span data-stu-id="750dc-134">HEAD</span></span>
- <span data-ttu-id="750dc-135">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="750dc-135">DELETE</span></span>

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

### <span data-ttu-id="750dc-136">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="750dc-136">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="750dc-137">A tárolási feladatok szövegtörzsét adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-137">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="750dc-138">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="750dc-138">-ErrorActionRequestBody</span></span>
<span data-ttu-id="750dc-139">A feladatok elvégzésére és KÖZZÉTÉTELére szolgáló szövegtörzset adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-139">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="750dc-140">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="750dc-140">-ErrorActionSASToken</span></span>
<span data-ttu-id="750dc-141">Megadja a tárterület-várólistához tartozó megosztott hozzáférés-aláírási (SA) tokent.</span><span class="sxs-lookup"><span data-stu-id="750dc-141">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="750dc-142">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="750dc-142">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="750dc-143">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-143">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="750dc-144">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="750dc-144">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="750dc-145">A tárolási várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-145">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="750dc-146">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="750dc-146">-ErrorActionURI</span></span>
<span data-ttu-id="750dc-147">A hiba-feladathoz tartozó URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-147">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="750dc-148">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="750dc-148">-ExecutionCount</span></span>
<span data-ttu-id="750dc-149">A futtatott feladat előfordulásainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-149">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="750dc-150">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="750dc-150">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="750dc-151">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="750dc-151">-Frequency</span></span>
<span data-ttu-id="750dc-152">A Feladatütemező maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-152">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="750dc-153">– Fejlécek</span><span class="sxs-lookup"><span data-stu-id="750dc-153">-Headers</span></span>
<span data-ttu-id="750dc-154">A fejléceket kivonatoló táblázatként adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-154">Specifies the headers as a hash table.</span></span>

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

### <span data-ttu-id="750dc-155">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="750dc-155">-HttpAuthenticationType</span></span>
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

### <span data-ttu-id="750dc-156">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="750dc-156">-Interval</span></span>
<span data-ttu-id="750dc-157">A *gyakoriság* paraméterrel megadott gyakoriságú ismétlődési intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-157">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="750dc-158">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="750dc-158">-JobCollectionName</span></span>
<span data-ttu-id="750dc-159">Annak a gyűjteménynek a nevét adja meg, amely a módosítani kívánt ütemező feladatot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="750dc-159">Specifies the name of the collection that contains the scheduler job to modify.</span></span>

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

### <span data-ttu-id="750dc-160">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="750dc-160">-JobName</span></span>
<span data-ttu-id="750dc-161">A módosítani kívánt ütemező-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-161">Specifies the name of scheduler job to modify.</span></span>

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

### <span data-ttu-id="750dc-162">-JobState</span><span class="sxs-lookup"><span data-stu-id="750dc-162">-JobState</span></span>
<span data-ttu-id="750dc-163">A Feladatütemező feladatához tartozó állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-163">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="750dc-164">-Hely</span><span class="sxs-lookup"><span data-stu-id="750dc-164">-Location</span></span>
<span data-ttu-id="750dc-165">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="750dc-165">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="750dc-166">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="750dc-166">Valid values are:</span></span> 

- <span data-ttu-id="750dc-167">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="750dc-167">Anywhere Asia</span></span>
- <span data-ttu-id="750dc-168">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="750dc-168">Anywhere Europe</span></span>
- <span data-ttu-id="750dc-169">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="750dc-169">Anywhere US</span></span>
- <span data-ttu-id="750dc-170">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="750dc-170">East Asia</span></span>
- <span data-ttu-id="750dc-171">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="750dc-171">East US</span></span>
- <span data-ttu-id="750dc-172">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="750dc-172">North Central US</span></span>
- <span data-ttu-id="750dc-173">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="750dc-173">North Europe</span></span>
- <span data-ttu-id="750dc-174">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="750dc-174">South Central US</span></span>
- <span data-ttu-id="750dc-175">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="750dc-175">Southeast Asia</span></span>
- <span data-ttu-id="750dc-176">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="750dc-176">West Europe</span></span>
- <span data-ttu-id="750dc-177">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="750dc-177">West US</span></span>

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

### <span data-ttu-id="750dc-178">-Módszer</span><span class="sxs-lookup"><span data-stu-id="750dc-178">-Method</span></span>
<span data-ttu-id="750dc-179">A HTTP-és HTTPS-műveletek típusának megfelelő módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-179">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="750dc-180">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="750dc-180">Valid values are:</span></span> 

- <span data-ttu-id="750dc-181">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="750dc-181">GET</span></span>
- <span data-ttu-id="750dc-182">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="750dc-182">PUT</span></span>
- <span data-ttu-id="750dc-183">POST</span><span class="sxs-lookup"><span data-stu-id="750dc-183">POST</span></span>
- <span data-ttu-id="750dc-184">FEJ</span><span class="sxs-lookup"><span data-stu-id="750dc-184">HEAD</span></span>
- <span data-ttu-id="750dc-185">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="750dc-185">DELETE</span></span>

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

### <span data-ttu-id="750dc-186">-PassThru</span><span class="sxs-lookup"><span data-stu-id="750dc-186">-PassThru</span></span>
<span data-ttu-id="750dc-187">Azt jelzi, hogy ez a parancsmag egy olyan objektumot ad eredményül, amely a működéséhez szükséges elemet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="750dc-187">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="750dc-188">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="750dc-188">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="750dc-189">-Profil</span><span class="sxs-lookup"><span data-stu-id="750dc-189">-Profile</span></span>
<span data-ttu-id="750dc-190">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="750dc-190">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="750dc-191">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="750dc-191">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="750dc-192">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="750dc-192">-RequestBody</span></span>
<span data-ttu-id="750dc-193">A feladatok elvégzésére és KÖZZÉTÉTELére szolgáló szövegtörzset adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-193">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="750dc-194">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="750dc-194">-StartTime</span></span>
<span data-ttu-id="750dc-195">Időpontot ad meg **datetime** objektumként a kezdéshez.</span><span class="sxs-lookup"><span data-stu-id="750dc-195">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="750dc-196">-URI</span><span class="sxs-lookup"><span data-stu-id="750dc-196">-URI</span></span>
<span data-ttu-id="750dc-197">A projektfeladat URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="750dc-197">Specifies a URI for a job action.</span></span>

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

### <span data-ttu-id="750dc-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="750dc-198">CommonParameters</span></span>
<span data-ttu-id="750dc-199">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="750dc-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="750dc-200">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="750dc-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="750dc-201">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="750dc-201">INPUTS</span></span>

## <span data-ttu-id="750dc-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="750dc-202">OUTPUTS</span></span>

## <span data-ttu-id="750dc-203">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="750dc-203">NOTES</span></span>

## <span data-ttu-id="750dc-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="750dc-204">RELATED LINKS</span></span>

[<span data-ttu-id="750dc-205">Új – AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="750dc-205">New-AzureSchedulerHttpJob</span></span>](./New-AzureSchedulerHttpJob.md)


