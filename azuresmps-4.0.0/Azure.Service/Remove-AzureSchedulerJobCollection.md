---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016128"
---
# <span data-ttu-id="8d9d1-101">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8d9d1-101">Remove-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="8d9d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d9d1-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9d1-103">Ütemező webhelycsoport törlése</span><span class="sxs-lookup"><span data-stu-id="8d9d1-103">Deletes a scheduler job collection.</span></span>

## <span data-ttu-id="8d9d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d9d1-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8d9d1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d9d1-105">DESCRIPTION</span></span>
<span data-ttu-id="8d9d1-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8d9d1-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8d9d1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8d9d1-108">A **Remove-AzureSchedulerJobCollection** parancsmag az adott gyűjteményben szereplő összes feladatot törli.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-108">The **Remove-AzureSchedulerJobCollection** cmdlet deletes a scheduler job collection and any jobs under that collection.</span></span>

## <span data-ttu-id="8d9d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8d9d1-109">EXAMPLES</span></span>

### <span data-ttu-id="8d9d1-110">Példa 1: webhelycsoport törlése a helyhez</span><span class="sxs-lookup"><span data-stu-id="8d9d1-110">Example 1: Delete a job collection for a location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="8d9d1-111">Ez a parancs törli a JobCollection01 nevű Feladatütemezőt az észak-közép-amerikai helyről.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-111">This command deletes the scheduler job collection named JobCollection01 in the North Central US location.</span></span>
<span data-ttu-id="8d9d1-112">A parancs a JobCollection01 alatti feladatokat is törli.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-112">The command also deletes the jobs under JobCollection01.</span></span>

### <span data-ttu-id="8d9d1-113">2. példa: a munkahely helyének törlése</span><span class="sxs-lookup"><span data-stu-id="8d9d1-113">Example 2: Delete a job location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

<span data-ttu-id="8d9d1-114">Ez a parancs törli a JobCollection02 nevű Scheduler Job Collectiont.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-114">This command deletes the scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="8d9d1-115">A parancs a JobCollection02 alatti feladatokat is törli.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-115">The command also deletes the jobs under JobCollection02.</span></span>

## <span data-ttu-id="8d9d1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d9d1-116">PARAMETERS</span></span>

### <span data-ttu-id="8d9d1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8d9d1-117">-Force</span></span>
<span data-ttu-id="8d9d1-118">Jelzi, hogy ez a parancsmag eltávolítja a Feladatütemezőt, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-118">Indicates that this cmdlet removes the scheduler job collection without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8d9d1-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8d9d1-119">-JobCollectionName</span></span>
<span data-ttu-id="8d9d1-120">A törölni kívánt ütemező-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-120">Specifies the name of the scheduler job collection to delete.</span></span>

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

### <span data-ttu-id="8d9d1-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="8d9d1-121">-Location</span></span>
<span data-ttu-id="8d9d1-122">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-122">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="8d9d1-123">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="8d9d1-123">Valid values are:</span></span> 

- <span data-ttu-id="8d9d1-124">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="8d9d1-124">Anywhere Asia</span></span>
- <span data-ttu-id="8d9d1-125">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="8d9d1-125">Anywhere Europe</span></span>
- <span data-ttu-id="8d9d1-126">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="8d9d1-126">Anywhere US</span></span>
- <span data-ttu-id="8d9d1-127">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="8d9d1-127">East Asia</span></span>
- <span data-ttu-id="8d9d1-128">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="8d9d1-128">East US</span></span>
- <span data-ttu-id="8d9d1-129">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="8d9d1-129">North Central US</span></span>
- <span data-ttu-id="8d9d1-130">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="8d9d1-130">North Europe</span></span>
- <span data-ttu-id="8d9d1-131">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="8d9d1-131">South Central US</span></span>
- <span data-ttu-id="8d9d1-132">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="8d9d1-132">Southeast Asia</span></span>
- <span data-ttu-id="8d9d1-133">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="8d9d1-133">West Europe</span></span>
- <span data-ttu-id="8d9d1-134">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="8d9d1-134">West US</span></span>

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

### <span data-ttu-id="8d9d1-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="8d9d1-135">-Profile</span></span>
<span data-ttu-id="8d9d1-136">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d9d1-137">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d9d1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9d1-138">CommonParameters</span></span>
<span data-ttu-id="8d9d1-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d9d1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9d1-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d9d1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9d1-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d9d1-141">INPUTS</span></span>

## <span data-ttu-id="8d9d1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d9d1-142">OUTPUTS</span></span>

## <span data-ttu-id="8d9d1-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d9d1-143">NOTES</span></span>

## <span data-ttu-id="8d9d1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d9d1-144">RELATED LINKS</span></span>

[<span data-ttu-id="8d9d1-145">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8d9d1-145">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="8d9d1-146">Új – AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8d9d1-146">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="8d9d1-147">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8d9d1-147">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


