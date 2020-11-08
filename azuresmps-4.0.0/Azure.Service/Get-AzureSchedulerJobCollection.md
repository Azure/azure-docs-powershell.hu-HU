---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015612"
---
# <span data-ttu-id="f862a-101">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f862a-101">Get-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="f862a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f862a-102">SYNOPSIS</span></span>
<span data-ttu-id="f862a-103">Beilleszti a Scheduler Job Collectiont.</span><span class="sxs-lookup"><span data-stu-id="f862a-103">Gets scheduler job collections.</span></span>

## <span data-ttu-id="f862a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f862a-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f862a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f862a-105">DESCRIPTION</span></span>
<span data-ttu-id="f862a-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="f862a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f862a-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f862a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f862a-108">A **Get-AzureSchedulerJobCollection** parancsmag egy vagy több Feladatütemezőt kap.</span><span class="sxs-lookup"><span data-stu-id="f862a-108">The **Get-AzureSchedulerJobCollection** cmdlet gets one or more scheduler job collections.</span></span>

## <span data-ttu-id="f862a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f862a-109">EXAMPLES</span></span>

### <span data-ttu-id="f862a-110">Példa 1: az összes gyűjtemény beolvasása</span><span class="sxs-lookup"><span data-stu-id="f862a-110">Example 1: Get all collections</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection
```

<span data-ttu-id="f862a-111">Ez a parancs az aktuális előfizetésben lévő összes helyről beilleszti az összes Scheduler-munkagyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="f862a-111">This command gets all scheduler job collections across all locations in the current subscription.</span></span>

### <span data-ttu-id="f862a-112">2. példa: a helyek minden gyűjteményének beolvasása</span><span class="sxs-lookup"><span data-stu-id="f862a-112">Example 2: Get all collections for a location</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

<span data-ttu-id="f862a-113">A parancs az észak-közép-amerikai (észak-közép-amerikai) helyen kapja meg az összes ütemező-feladatot.</span><span class="sxs-lookup"><span data-stu-id="f862a-113">This command gets all scheduler job collections in the location named North Central US.</span></span>

### <span data-ttu-id="f862a-114">3. példa: gyűjtemény beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="f862a-114">Example 3: Get a collection by using a name</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="f862a-115">Ez a parancs beolvassa a JobCollection01 nevű Scheduler Job Collectiont.</span><span class="sxs-lookup"><span data-stu-id="f862a-115">This command gets the scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="f862a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f862a-116">PARAMETERS</span></span>

### <span data-ttu-id="f862a-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f862a-117">-JobCollectionName</span></span>
<span data-ttu-id="f862a-118">A beolvasott ütemező-webhelycsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f862a-118">Specifies the name of the scheduler job collection to get.</span></span>

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

### <span data-ttu-id="f862a-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="f862a-119">-Location</span></span>
<span data-ttu-id="f862a-120">Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.</span><span class="sxs-lookup"><span data-stu-id="f862a-120">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="f862a-121">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="f862a-121">Valid values are:</span></span> 

- <span data-ttu-id="f862a-122">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="f862a-122">Anywhere Asia</span></span>
- <span data-ttu-id="f862a-123">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="f862a-123">Anywhere Europe</span></span>
- <span data-ttu-id="f862a-124">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="f862a-124">Anywhere US</span></span>
- <span data-ttu-id="f862a-125">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="f862a-125">East Asia</span></span>
- <span data-ttu-id="f862a-126">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="f862a-126">East US</span></span>
- <span data-ttu-id="f862a-127">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="f862a-127">North Central US</span></span>
- <span data-ttu-id="f862a-128">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="f862a-128">North Europe</span></span>
- <span data-ttu-id="f862a-129">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="f862a-129">South Central US</span></span>
- <span data-ttu-id="f862a-130">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="f862a-130">Southeast Asia</span></span>
- <span data-ttu-id="f862a-131">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="f862a-131">West Europe</span></span>
- <span data-ttu-id="f862a-132">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="f862a-132">West US</span></span>

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

### <span data-ttu-id="f862a-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="f862a-133">-Profile</span></span>
<span data-ttu-id="f862a-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f862a-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f862a-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f862a-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f862a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f862a-136">CommonParameters</span></span>
<span data-ttu-id="f862a-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f862a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f862a-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f862a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f862a-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f862a-139">INPUTS</span></span>

## <span data-ttu-id="f862a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f862a-140">OUTPUTS</span></span>

## <span data-ttu-id="f862a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f862a-141">NOTES</span></span>

## <span data-ttu-id="f862a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f862a-142">RELATED LINKS</span></span>

[<span data-ttu-id="f862a-143">Új – AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f862a-143">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="f862a-144">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f862a-144">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="f862a-145">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f862a-145">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


