---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016310"
---
# <span data-ttu-id="fdec5-101">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="fdec5-101">Get-AzureSchedulerJobHistory</span></span>

## <span data-ttu-id="fdec5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdec5-102">SYNOPSIS</span></span>
<span data-ttu-id="fdec5-103">Meglesz az előzmények egy ütemező feladathoz.</span><span class="sxs-lookup"><span data-stu-id="fdec5-103">Gets history for a scheduler job.</span></span>

## <span data-ttu-id="fdec5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdec5-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="fdec5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdec5-105">DESCRIPTION</span></span>
<span data-ttu-id="fdec5-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="fdec5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fdec5-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="fdec5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fdec5-108">A **Get-AzureSchedulerJobHistory** parancsmag a Scheduler-feladatok előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="fdec5-108">The **Get-AzureSchedulerJobHistory** cmdlet gets the history for a scheduler job.</span></span>

## <span data-ttu-id="fdec5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fdec5-109">EXAMPLES</span></span>

### <span data-ttu-id="fdec5-110">Példa 1: a projekt előzményeinek beolvasása a nevével</span><span class="sxs-lookup"><span data-stu-id="fdec5-110">Example 1: Get history for a job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="fdec5-111">Ez a parancs a Job01 nevű feladat előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="fdec5-111">This command gets the history of the job named Job01.</span></span>
<span data-ttu-id="fdec5-112">Ez a feladat a megadott helyen lévő JobCollection01 nevű webhelycsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="fdec5-112">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="fdec5-113">2. példa: a sikertelen munka előzményeinek beolvasása a neve segítségével</span><span class="sxs-lookup"><span data-stu-id="fdec5-113">Example 2: Get history for a failed job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

<span data-ttu-id="fdec5-114">Ez a parancs a Job12 nevű feladat előzményeit kapja meg, amelynek állapota nem sikerült.</span><span class="sxs-lookup"><span data-stu-id="fdec5-114">This command gets the history of the job named Job12 that has a status of Failed.</span></span>
<span data-ttu-id="fdec5-115">Ez a feladat a megadott helyen lévő JobCollection01 nevű webhelycsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="fdec5-115">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="fdec5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdec5-116">PARAMETERS</span></span>

### <span data-ttu-id="fdec5-117">– Első</span><span class="sxs-lookup"><span data-stu-id="fdec5-117">-First</span></span>
<span data-ttu-id="fdec5-118">Csak a megadott számú objektumot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fdec5-118">Gets only the specified number of objects.</span></span>
<span data-ttu-id="fdec5-119">Adja meg a bejutni kívánt objektumok számát.</span><span class="sxs-lookup"><span data-stu-id="fdec5-119">Enter the number of objects to get.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdec5-120">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="fdec5-120">-IncludeTotalCount</span></span>
<span data-ttu-id="fdec5-121">A kijelölt objektumok által követett összes objektum (egész) számát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fdec5-121">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="fdec5-122">Ha a parancsmag nem tudja megállapítani a teljes számlálást, az "ismeretlen összeg száma" szöveget jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="fdec5-122">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="fdec5-123">Az egész számnak van egy pontossági tulajdonsága, amely az összeg megbízhatóságát jelzi.</span><span class="sxs-lookup"><span data-stu-id="fdec5-123">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="fdec5-124">Az 0,0-től 1,0-ig terjedő pontossági értékek értéke, ahol az 0,0 azt jelenti, hogy a parancsmag nem tudta megszámolni az objektumokat, az 1,0 azt jelenti, hogy a darab pontos, és a 0,0 és a 1,0 közötti érték egyre megbízhatóbb becslést ad.</span><span class="sxs-lookup"><span data-stu-id="fdec5-124">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdec5-125">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="fdec5-125">-JobCollectionName</span></span>
<span data-ttu-id="fdec5-126">A Scheduler-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdec5-126">Specifies the name of a scheduler job collection.</span></span>
<span data-ttu-id="fdec5-127">Ez a parancsmag egy olyan projekt előzményeit kapja meg, amely a paraméter által megadott gyűjteményhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="fdec5-127">This cmdlet gets the history for a job that belongs to the collection that this parameter specifies.</span></span>

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

### <span data-ttu-id="fdec5-128">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="fdec5-128">-JobName</span></span>
<span data-ttu-id="fdec5-129">Annak a Scheduler-feladatnak a nevét adja meg, amelynek az előzményeit meg szeretné kapni.</span><span class="sxs-lookup"><span data-stu-id="fdec5-129">Specifies the name of a scheduler job for which to get the history.</span></span>

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

### <span data-ttu-id="fdec5-130">-JobStatus</span><span class="sxs-lookup"><span data-stu-id="fdec5-130">-JobStatus</span></span>
<span data-ttu-id="fdec5-131">Annak a Scheduler-feladatnak a állapotát adja meg, amelynek az előzményeit meg szeretné kapni.</span><span class="sxs-lookup"><span data-stu-id="fdec5-131">Specifies the status of scheduler job for which to get the history.</span></span>
<span data-ttu-id="fdec5-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fdec5-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fdec5-133">Kész</span><span class="sxs-lookup"><span data-stu-id="fdec5-133">Completed</span></span>
- <span data-ttu-id="fdec5-134">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="fdec5-134">Failed</span></span>

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

### <span data-ttu-id="fdec5-135">-Hely</span><span class="sxs-lookup"><span data-stu-id="fdec5-135">-Location</span></span>
<span data-ttu-id="fdec5-136">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="fdec5-136">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="fdec5-137">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="fdec5-137">Valid values are:</span></span> 

- <span data-ttu-id="fdec5-138">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="fdec5-138">Anywhere Asia</span></span>
- <span data-ttu-id="fdec5-139">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="fdec5-139">Anywhere Europe</span></span>
- <span data-ttu-id="fdec5-140">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="fdec5-140">Anywhere US</span></span>
- <span data-ttu-id="fdec5-141">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="fdec5-141">East Asia</span></span>
- <span data-ttu-id="fdec5-142">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="fdec5-142">East US</span></span>
- <span data-ttu-id="fdec5-143">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="fdec5-143">North Central US</span></span>
- <span data-ttu-id="fdec5-144">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="fdec5-144">North Europe</span></span>
- <span data-ttu-id="fdec5-145">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="fdec5-145">South Central US</span></span>
- <span data-ttu-id="fdec5-146">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="fdec5-146">Southeast Asia</span></span>
- <span data-ttu-id="fdec5-147">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="fdec5-147">West Europe</span></span>
- <span data-ttu-id="fdec5-148">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="fdec5-148">West US</span></span>

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

### <span data-ttu-id="fdec5-149">-Profil</span><span class="sxs-lookup"><span data-stu-id="fdec5-149">-Profile</span></span>
<span data-ttu-id="fdec5-150">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="fdec5-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fdec5-151">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="fdec5-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fdec5-152">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="fdec5-152">-Skip</span></span>
<span data-ttu-id="fdec5-153">Figyelmen kívül hagyja a megadott számú objektumot, majd Kinyeri a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="fdec5-153">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="fdec5-154">Adja meg, hogy hány objektum legyen kihagyva.</span><span class="sxs-lookup"><span data-stu-id="fdec5-154">Enter the number of objects to skip.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdec5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdec5-155">CommonParameters</span></span>
<span data-ttu-id="fdec5-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdec5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdec5-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdec5-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdec5-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdec5-158">INPUTS</span></span>

## <span data-ttu-id="fdec5-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdec5-159">OUTPUTS</span></span>

## <span data-ttu-id="fdec5-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdec5-160">NOTES</span></span>

## <span data-ttu-id="fdec5-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdec5-161">RELATED LINKS</span></span>

[<span data-ttu-id="fdec5-162">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="fdec5-162">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="fdec5-163">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fdec5-163">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)


