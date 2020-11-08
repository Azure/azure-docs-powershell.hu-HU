---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015443"
---
# <span data-ttu-id="0f5ba-101">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0f5ba-101">Set-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="0f5ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5ba-103">Ütemező webhelycsoporthoz frissít.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-103">Updates a scheduler job collection.</span></span>

## <span data-ttu-id="0f5ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f5ba-104">SYNTAX</span></span>

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f5ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f5ba-105">DESCRIPTION</span></span>
<span data-ttu-id="0f5ba-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0f5ba-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0f5ba-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0f5ba-108">A **set-AzureSchedulerJobCollection** parancsmag frissíti a Feladatütemező-beosztást.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-108">The **Set-AzureSchedulerJobCollection** cmdlet updates a scheduler job collection.</span></span>

## <span data-ttu-id="0f5ba-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0f5ba-109">EXAMPLES</span></span>

### <span data-ttu-id="0f5ba-110">1. példa: egy adott gyűjtemény maximális mennyiségének módosítása</span><span class="sxs-lookup"><span data-stu-id="0f5ba-110">Example 1: Change the maximum job count for a collection</span></span>
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

<span data-ttu-id="0f5ba-111">Ez a parancs a JobCollection01 nevű, meglévő Scheduler-feladatban a maximálisan 30 értéket módosítja.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-111">This command changes the maximum job count to 30 on the existing scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="0f5ba-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f5ba-112">PARAMETERS</span></span>

### <span data-ttu-id="0f5ba-113">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="0f5ba-113">-Frequency</span></span>
<span data-ttu-id="0f5ba-114">A Feladatütemezőben a munkafolyamatban bármely feladatban megadható maximális frekvenciát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-114">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>
<span data-ttu-id="0f5ba-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0f5ba-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f5ba-116">Perces</span><span class="sxs-lookup"><span data-stu-id="0f5ba-116">Minute</span></span>
- <span data-ttu-id="0f5ba-117">Óra</span><span class="sxs-lookup"><span data-stu-id="0f5ba-117">Hour</span></span>
- <span data-ttu-id="0f5ba-118">Nap</span><span class="sxs-lookup"><span data-stu-id="0f5ba-118">Day</span></span>
- <span data-ttu-id="0f5ba-119">Héten</span><span class="sxs-lookup"><span data-stu-id="0f5ba-119">Week</span></span>
- <span data-ttu-id="0f5ba-120">Hónap</span><span class="sxs-lookup"><span data-stu-id="0f5ba-120">Month</span></span>
- <span data-ttu-id="0f5ba-121">Év</span><span class="sxs-lookup"><span data-stu-id="0f5ba-121">Year</span></span>

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

### <span data-ttu-id="0f5ba-122">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="0f5ba-122">-Interval</span></span>
<span data-ttu-id="0f5ba-123">A *gyakoriság* paraméterrel megadott gyakoriságú ismétlődési intervallumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-123">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="0f5ba-124">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0f5ba-124">-JobCollectionName</span></span>
<span data-ttu-id="0f5ba-125">A frissítendő Scheduler-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-125">Specifies the name of scheduler job collection to update.</span></span>

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

### <span data-ttu-id="0f5ba-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="0f5ba-126">-Location</span></span>
<span data-ttu-id="0f5ba-127">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-127">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="0f5ba-128">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="0f5ba-128">Valid values are:</span></span> 

- <span data-ttu-id="0f5ba-129">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="0f5ba-129">Anywhere Asia</span></span>
- <span data-ttu-id="0f5ba-130">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="0f5ba-130">Anywhere Europe</span></span>
- <span data-ttu-id="0f5ba-131">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="0f5ba-131">Anywhere US</span></span>
- <span data-ttu-id="0f5ba-132">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="0f5ba-132">East Asia</span></span>
- <span data-ttu-id="0f5ba-133">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="0f5ba-133">East US</span></span>
- <span data-ttu-id="0f5ba-134">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="0f5ba-134">North Central US</span></span>
- <span data-ttu-id="0f5ba-135">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="0f5ba-135">North Europe</span></span>
- <span data-ttu-id="0f5ba-136">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="0f5ba-136">South Central US</span></span>
- <span data-ttu-id="0f5ba-137">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="0f5ba-137">Southeast Asia</span></span>
- <span data-ttu-id="0f5ba-138">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="0f5ba-138">West Europe</span></span>
- <span data-ttu-id="0f5ba-139">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="0f5ba-139">West US</span></span>

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

### <span data-ttu-id="0f5ba-140">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="0f5ba-140">-MaxJobCount</span></span>
<span data-ttu-id="0f5ba-141">A Feladatütemezőben létrehozható feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-141">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="0f5ba-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f5ba-142">-PassThru</span></span>
<span data-ttu-id="0f5ba-143">Azt jelzi, hogy ez a parancsmag egy olyan objektumot ad eredményül, amely a működéséhez szükséges elemet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-143">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="0f5ba-144">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f5ba-145">-Terv</span><span class="sxs-lookup"><span data-stu-id="0f5ba-145">-Plan</span></span>
<span data-ttu-id="0f5ba-146">A Scheduler Job Collection Plant adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-146">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="0f5ba-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="0f5ba-147">-Profile</span></span>
<span data-ttu-id="0f5ba-148">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f5ba-149">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f5ba-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5ba-150">CommonParameters</span></span>
<span data-ttu-id="0f5ba-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f5ba-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5ba-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f5ba-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5ba-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f5ba-153">INPUTS</span></span>

## <span data-ttu-id="0f5ba-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f5ba-154">OUTPUTS</span></span>

## <span data-ttu-id="0f5ba-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f5ba-155">NOTES</span></span>

## <span data-ttu-id="0f5ba-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f5ba-156">RELATED LINKS</span></span>

[<span data-ttu-id="0f5ba-157">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0f5ba-157">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="0f5ba-158">Új – AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0f5ba-158">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="0f5ba-159">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0f5ba-159">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)


