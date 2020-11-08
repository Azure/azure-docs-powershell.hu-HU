---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016311"
---
# <span data-ttu-id="d5273-101">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="d5273-101">Get-AzureSchedulerJob</span></span>

## <span data-ttu-id="d5273-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5273-102">SYNOPSIS</span></span>
<span data-ttu-id="d5273-103">A Scheduler-feladatok listáját vagy egy adott ütemező feladatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5273-103">Gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="d5273-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5273-104">SYNTAX</span></span>

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d5273-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5273-105">DESCRIPTION</span></span>
<span data-ttu-id="d5273-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="d5273-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d5273-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d5273-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d5273-108">A **Get-AzureSchedulerJobCollection** parancsmag a Scheduler-feladatok listáját, vagy egy adott ütemező feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="d5273-108">The **Get-AzureSchedulerJobCollection** cmdlet gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="d5273-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d5273-109">EXAMPLES</span></span>

### <span data-ttu-id="d5273-110">Példa 1: a gyűjtemény összes feladatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d5273-110">Example 1: Get all jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="d5273-111">Ez a parancs a JobCollection01 nevű begyűjtő feladatok részét képezi a Feladatütemezőben.</span><span class="sxs-lookup"><span data-stu-id="d5273-111">This command gets scheduler jobs that are part of the job collection named JobCollection01.</span></span>

### <span data-ttu-id="d5273-112">2. példa: elnevezett feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="d5273-112">Example 2: Get a named job</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="d5273-113">Ez a parancs a Job01 nevű feladatot a megadott helyen lévő JobCollection01 nevű gyűjteményből kapja.</span><span class="sxs-lookup"><span data-stu-id="d5273-113">This command gets the job named Job01 from the collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="d5273-114">3. példa: letiltott feladatok lekérése egy gyűjteményben</span><span class="sxs-lookup"><span data-stu-id="d5273-114">Example 3: Get disabled jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

<span data-ttu-id="d5273-115">Ez a parancs a megadott helyen található JobCollection01 részét képező, letiltott Scheduler-feladatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5273-115">This command gets all disabled scheduler jobs that are part of JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="d5273-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5273-116">PARAMETERS</span></span>

### <span data-ttu-id="d5273-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d5273-117">-JobCollectionName</span></span>
<span data-ttu-id="d5273-118">Annak a gyűjteménynek a nevét adja meg, amely a beolvasás ütemező feladatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d5273-118">Specifies the name of the collection that contains the scheduler job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5273-119">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="d5273-119">-JobName</span></span>
<span data-ttu-id="d5273-120">A beolvasott ütemező feladatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5273-120">Specifies the name of a scheduler job to get.</span></span>

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

### <span data-ttu-id="d5273-121">-JobState</span><span class="sxs-lookup"><span data-stu-id="d5273-121">-JobState</span></span>
<span data-ttu-id="d5273-122">A beolvasott ütemező-feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5273-122">Specifies the state of scheduler jobs to get.</span></span>
<span data-ttu-id="d5273-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d5273-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5273-124">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="d5273-124">Enabled</span></span>
- <span data-ttu-id="d5273-125">Tiltva</span><span class="sxs-lookup"><span data-stu-id="d5273-125">Disabled</span></span>
- <span data-ttu-id="d5273-126">Hibázott</span><span class="sxs-lookup"><span data-stu-id="d5273-126">Faulted</span></span>
- <span data-ttu-id="d5273-127">Kész</span><span class="sxs-lookup"><span data-stu-id="d5273-127">Completed</span></span>

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

### <span data-ttu-id="d5273-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="d5273-128">-Location</span></span>
<span data-ttu-id="d5273-129">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="d5273-129">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="d5273-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d5273-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5273-131">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="d5273-131">Anywhere Asia</span></span>
- <span data-ttu-id="d5273-132">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="d5273-132">Anywhere Europe</span></span>
- <span data-ttu-id="d5273-133">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="d5273-133">Anywhere US</span></span>
- <span data-ttu-id="d5273-134">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="d5273-134">East Asia</span></span>
- <span data-ttu-id="d5273-135">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="d5273-135">East US</span></span>
- <span data-ttu-id="d5273-136">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="d5273-136">North Central US</span></span>
- <span data-ttu-id="d5273-137">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="d5273-137">North Europe</span></span>
- <span data-ttu-id="d5273-138">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="d5273-138">South Central US</span></span>
- <span data-ttu-id="d5273-139">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="d5273-139">Southeast Asia</span></span>
- <span data-ttu-id="d5273-140">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="d5273-140">West Europe</span></span>
- <span data-ttu-id="d5273-141">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="d5273-141">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5273-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="d5273-142">-Profile</span></span>
<span data-ttu-id="d5273-143">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d5273-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d5273-144">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d5273-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5273-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5273-145">CommonParameters</span></span>
<span data-ttu-id="d5273-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5273-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5273-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5273-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5273-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5273-148">INPUTS</span></span>

## <span data-ttu-id="d5273-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5273-149">OUTPUTS</span></span>

## <span data-ttu-id="d5273-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5273-150">NOTES</span></span>

## <span data-ttu-id="d5273-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5273-151">RELATED LINKS</span></span>

[<span data-ttu-id="d5273-152">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="d5273-152">Remove-AzureSchedulerJob</span></span>](./Remove-AzureSchedulerJob.md)


