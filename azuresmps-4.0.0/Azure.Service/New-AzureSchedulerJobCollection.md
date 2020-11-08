---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015980"
---
# <span data-ttu-id="5ec13-101">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="5ec13-101">New-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="5ec13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ec13-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec13-103">Ütemező begyűjtési feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5ec13-103">Creates a scheduler job collection.</span></span>

## <span data-ttu-id="5ec13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ec13-104">SYNTAX</span></span>

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ec13-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ec13-105">DESCRIPTION</span></span>
<span data-ttu-id="5ec13-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="5ec13-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5ec13-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5ec13-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5ec13-108">A **New-AzureSchedulerJobCollection** parancsmag létrehoz egy Scheduler Job Collectiont.</span><span class="sxs-lookup"><span data-stu-id="5ec13-108">The **New-AzureSchedulerJobCollection** cmdlet creates a scheduler job collection.</span></span>
<span data-ttu-id="5ec13-109">Ha nem ad meg értéket a *terv* paraméterhez, a parancsmag létrehoz egy szabványos begyűjtő feladatot.</span><span class="sxs-lookup"><span data-stu-id="5ec13-109">If you do not specify a value for the *Plan* parameter, the cmdlet creates a standard job collection.</span></span>

## <span data-ttu-id="5ec13-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5ec13-110">EXAMPLES</span></span>

### <span data-ttu-id="5ec13-111">Példa 1: alapértelmezett értékeket tartalmazó Scheduler-gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="5ec13-111">Example 1: Create a scheduler job collection that includes default values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

<span data-ttu-id="5ec13-112">Ez a parancs létrehoz egy JobCollection01 nevű normál Scheduler-munkagyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="5ec13-112">This command creates a standard scheduler job collection named JobCollection01.</span></span>
<span data-ttu-id="5ec13-113">Az új gyűjteményhez tartozik egy alapértelmezett tevékenység száma és a maximális ismétlődési értékek a szokásos ütemező-összegyűjtéshez.</span><span class="sxs-lookup"><span data-stu-id="5ec13-113">The new collection has a default job count and maximum recurrence values for a standard scheduler job collection.</span></span>

### <span data-ttu-id="5ec13-114">2. példa: a Scheduler-munkagyűjtemény létrehozása megadott értékekkel</span><span class="sxs-lookup"><span data-stu-id="5ec13-114">Example 2: Create a scheduler job collection with specified values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

<span data-ttu-id="5ec13-115">Ez a parancs létrehoz egy JobCollection02 nevű normál Scheduler-munkagyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="5ec13-115">This command creates a standard scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="5ec13-116">Az új gyűjteményben a maximális mennyiség 30, a maximálisan 12 óránként</span><span class="sxs-lookup"><span data-stu-id="5ec13-116">The new collection has a maximum job count of 30 and a maximum recurrence of 12 per hour.</span></span>

## <span data-ttu-id="5ec13-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ec13-117">PARAMETERS</span></span>

### <span data-ttu-id="5ec13-118">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="5ec13-118">-Frequency</span></span>
<span data-ttu-id="5ec13-119">A Feladatütemezőben a munkafolyamatban bármely feladatban megadható maximális frekvenciát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ec13-119">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>

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

### <span data-ttu-id="5ec13-120">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="5ec13-120">-Interval</span></span>
<span data-ttu-id="5ec13-121">A *gyakoriság* paraméterrel megadott gyakoriságú ismétlődési intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ec13-121">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="5ec13-122">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="5ec13-122">-JobCollectionName</span></span>
<span data-ttu-id="5ec13-123">Az új ütemező-beosztáshoz tartozó nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ec13-123">Specifies the name for the new scheduler job collection.</span></span>

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

### <span data-ttu-id="5ec13-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="5ec13-124">-Location</span></span>
<span data-ttu-id="5ec13-125">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ec13-125">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="5ec13-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="5ec13-126">Valid values are:</span></span> 

- <span data-ttu-id="5ec13-127">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="5ec13-127">Anywhere Asia</span></span>
- <span data-ttu-id="5ec13-128">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="5ec13-128">Anywhere Europe</span></span>
- <span data-ttu-id="5ec13-129">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="5ec13-129">Anywhere US</span></span>
- <span data-ttu-id="5ec13-130">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="5ec13-130">East Asia</span></span>
- <span data-ttu-id="5ec13-131">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="5ec13-131">East US</span></span>
- <span data-ttu-id="5ec13-132">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="5ec13-132">North Central US</span></span>
- <span data-ttu-id="5ec13-133">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="5ec13-133">North Europe</span></span>
- <span data-ttu-id="5ec13-134">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="5ec13-134">South Central US</span></span>
- <span data-ttu-id="5ec13-135">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="5ec13-135">Southeast Asia</span></span>
- <span data-ttu-id="5ec13-136">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="5ec13-136">West Europe</span></span>
- <span data-ttu-id="5ec13-137">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="5ec13-137">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ec13-138">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="5ec13-138">-MaxJobCount</span></span>
<span data-ttu-id="5ec13-139">A Feladatütemezőben létrehozható feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ec13-139">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="5ec13-140">-Terv</span><span class="sxs-lookup"><span data-stu-id="5ec13-140">-Plan</span></span>
<span data-ttu-id="5ec13-141">A Scheduler Job Collection Plant adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ec13-141">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="5ec13-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="5ec13-142">-Profile</span></span>
<span data-ttu-id="5ec13-143">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5ec13-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ec13-144">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5ec13-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ec13-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec13-145">CommonParameters</span></span>
<span data-ttu-id="5ec13-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ec13-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec13-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec13-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec13-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ec13-148">INPUTS</span></span>

## <span data-ttu-id="5ec13-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ec13-149">OUTPUTS</span></span>

## <span data-ttu-id="5ec13-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ec13-150">NOTES</span></span>

## <span data-ttu-id="5ec13-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ec13-151">RELATED LINKS</span></span>

[<span data-ttu-id="5ec13-152">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="5ec13-152">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="5ec13-153">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="5ec13-153">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="5ec13-154">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="5ec13-154">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


