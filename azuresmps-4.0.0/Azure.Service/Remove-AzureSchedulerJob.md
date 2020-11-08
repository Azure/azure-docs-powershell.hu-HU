---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DEC693-32BA-4048-8912-D1626DD511E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c95fb7f79cdb160bf2dd2014cad49d1bc96eb3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016129"
---
# <span data-ttu-id="0965d-101">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="0965d-101">Remove-AzureSchedulerJob</span></span>

## <span data-ttu-id="0965d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0965d-102">SYNOPSIS</span></span>
<span data-ttu-id="0965d-103">Ütemező feladat törlése</span><span class="sxs-lookup"><span data-stu-id="0965d-103">Deletes a scheduler job.</span></span>

## <span data-ttu-id="0965d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0965d-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJob [-Force] [-Location <String>] -JobCollectionName <String> -JobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0965d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0965d-105">DESCRIPTION</span></span>
<span data-ttu-id="0965d-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="0965d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0965d-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0965d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0965d-108">A **Remove-AzureSchedulerJob** parancsmag törli a Feladatütemező feladatát.</span><span class="sxs-lookup"><span data-stu-id="0965d-108">The **Remove-AzureSchedulerJob** cmdlet deletes a scheduler job.</span></span>

## <span data-ttu-id="0965d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0965d-109">EXAMPLES</span></span>

### <span data-ttu-id="0965d-110">Példa 1: ütemező feladat törlése</span><span class="sxs-lookup"><span data-stu-id="0965d-110">Example 1: Delete a scheduler job</span></span>
```
PS C:\> Remove-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job17"
```

<span data-ttu-id="0965d-111">Ez a parancs törli a Job17 nevű feladatot.</span><span class="sxs-lookup"><span data-stu-id="0965d-111">This command deletes the job named Job17.</span></span>
<span data-ttu-id="0965d-112">Ez a feladat a JobCollection01 nevű Job Collection része, és a megadott helyen található.</span><span class="sxs-lookup"><span data-stu-id="0965d-112">That job is part of the job collection named JobCollection01 and is in of the specified location.</span></span>

## <span data-ttu-id="0965d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0965d-113">PARAMETERS</span></span>

### <span data-ttu-id="0965d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="0965d-114">-Force</span></span>
<span data-ttu-id="0965d-115">Jelzi, hogy ez a parancsmag eltávolítja a Feladatütemezőt, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0965d-115">Indicates that this cmdlet removes the scheduler job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0965d-116">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0965d-116">-JobCollectionName</span></span>
<span data-ttu-id="0965d-117">Annak a gyűjteménynek a nevét adja meg, amely a törölni kívánt ütemező feladatot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0965d-117">Specifies the name of the collection that contains the scheduler job to delete.</span></span>

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

### <span data-ttu-id="0965d-118">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="0965d-118">-JobName</span></span>
<span data-ttu-id="0965d-119">A törlendő ütemező feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0965d-119">Specifies the name of a scheduler job to delete.</span></span>

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

### <span data-ttu-id="0965d-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="0965d-120">-Location</span></span>
<span data-ttu-id="0965d-121">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="0965d-121">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="0965d-122">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="0965d-122">Valid values are:</span></span> 

- <span data-ttu-id="0965d-123">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="0965d-123">Anywhere Asia</span></span>
- <span data-ttu-id="0965d-124">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="0965d-124">Anywhere Europe</span></span>
- <span data-ttu-id="0965d-125">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="0965d-125">Anywhere US</span></span>
- <span data-ttu-id="0965d-126">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="0965d-126">East Asia</span></span>
- <span data-ttu-id="0965d-127">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="0965d-127">East US</span></span>
- <span data-ttu-id="0965d-128">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="0965d-128">North Central US</span></span>
- <span data-ttu-id="0965d-129">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="0965d-129">North Europe</span></span>
- <span data-ttu-id="0965d-130">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="0965d-130">South Central US</span></span>
- <span data-ttu-id="0965d-131">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="0965d-131">Southeast Asia</span></span>
- <span data-ttu-id="0965d-132">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="0965d-132">West Europe</span></span>
- <span data-ttu-id="0965d-133">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="0965d-133">West US</span></span>

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

### <span data-ttu-id="0965d-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="0965d-134">-Profile</span></span>
<span data-ttu-id="0965d-135">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0965d-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0965d-136">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0965d-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0965d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0965d-137">CommonParameters</span></span>
<span data-ttu-id="0965d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0965d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0965d-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0965d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0965d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0965d-140">INPUTS</span></span>

## <span data-ttu-id="0965d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0965d-141">OUTPUTS</span></span>

## <span data-ttu-id="0965d-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0965d-142">NOTES</span></span>

## <span data-ttu-id="0965d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0965d-143">RELATED LINKS</span></span>

[<span data-ttu-id="0965d-144">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="0965d-144">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)


