---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A2CBF963-1FAE-41B0-964E-EFF52076AB32
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c4bb84111b8ec22b1b529622e61ca476cf6081b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016507"
---
# <span data-ttu-id="a7a63-101">Get-AzureWebsiteJobHistory</span><span class="sxs-lookup"><span data-stu-id="a7a63-101">Get-AzureWebsiteJobHistory</span></span>

## <span data-ttu-id="a7a63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7a63-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a63-103">Webes előzményeket kap.</span><span class="sxs-lookup"><span data-stu-id="a7a63-103">Gets a web job history.</span></span>

## <span data-ttu-id="a7a63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7a63-104">SYNTAX</span></span>

### <span data-ttu-id="a7a63-105">HistoryParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a7a63-105">HistoryParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7a63-106">RunIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a7a63-106">RunIdParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> -RunId <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a7a63-107">LatestParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a7a63-107">LatestParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Latest] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a7a63-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7a63-108">DESCRIPTION</span></span>
<span data-ttu-id="a7a63-109">Webes előzményeket kap.</span><span class="sxs-lookup"><span data-stu-id="a7a63-109">Gets a web job history.</span></span>

## <span data-ttu-id="a7a63-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a7a63-110">EXAMPLES</span></span>

### <span data-ttu-id="a7a63-111">Példa 1: a teljes előzmények beszerzése egy webhelyhez</span><span class="sxs-lookup"><span data-stu-id="a7a63-111">Example 1: Get complete history for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="a7a63-112">A MyWebJob teljes előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="a7a63-112">Gets complete history for MyWebJob.</span></span>

### <span data-ttu-id="a7a63-113">2. példa: a legújabb Futtatás beolvasása egy webes feladathoz</span><span class="sxs-lookup"><span data-stu-id="a7a63-113">Example 2: Get latest run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -Latest
```

<span data-ttu-id="a7a63-114">A MyWebJob legújabb futtatási információit kapja.</span><span class="sxs-lookup"><span data-stu-id="a7a63-114">Gets latest run info for MyWebJob.</span></span>

### <span data-ttu-id="a7a63-115">3. példa: speciális Futtatás egy webhelyhez</span><span class="sxs-lookup"><span data-stu-id="a7a63-115">Example 3: Get specific run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -RunId 10
```

<span data-ttu-id="a7a63-116">Az MyWebJob-os azonosítójú 10-es verzióval kapcsolatos minden információ beolvasása.</span><span class="sxs-lookup"><span data-stu-id="a7a63-116">Gets all info about run with id 10 for MyWebJob.</span></span>

## <span data-ttu-id="a7a63-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7a63-117">PARAMETERS</span></span>

### <span data-ttu-id="a7a63-118">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="a7a63-118">-JobName</span></span>
<span data-ttu-id="a7a63-119">A webes feladat neve.</span><span class="sxs-lookup"><span data-stu-id="a7a63-119">The web job name.</span></span>

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

### <span data-ttu-id="a7a63-120">-Legújabb</span><span class="sxs-lookup"><span data-stu-id="a7a63-120">-Latest</span></span>
<span data-ttu-id="a7a63-121">Ha meg van adva, adja vissza a legutóbbi futtatási előzményeket.</span><span class="sxs-lookup"><span data-stu-id="a7a63-121">If specified, return the latest run history.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LatestParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a63-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7a63-122">-Name</span></span>
<span data-ttu-id="a7a63-123">Az Azure-webhely neve.</span><span class="sxs-lookup"><span data-stu-id="a7a63-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="a7a63-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="a7a63-124">-Profile</span></span>
<span data-ttu-id="a7a63-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a7a63-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a7a63-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a7a63-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a7a63-127">-RunId</span><span class="sxs-lookup"><span data-stu-id="a7a63-127">-RunId</span></span>
<span data-ttu-id="a7a63-128">A látni kívánt futási előzmények AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7a63-128">Specifies the ID of the run history you want to see.</span></span>

```yaml
Type: String
Parameter Sets: RunIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a63-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="a7a63-129">-Slot</span></span>
<span data-ttu-id="a7a63-130">Az Azure-webhely tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="a7a63-130">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="a7a63-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a63-131">CommonParameters</span></span>
<span data-ttu-id="a7a63-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7a63-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a63-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a63-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a63-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7a63-134">INPUTS</span></span>

## <span data-ttu-id="a7a63-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7a63-135">OUTPUTS</span></span>

## <span data-ttu-id="a7a63-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7a63-136">NOTES</span></span>

## <span data-ttu-id="a7a63-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7a63-137">RELATED LINKS</span></span>

[<span data-ttu-id="a7a63-138">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a7a63-138">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="a7a63-139">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a7a63-139">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="a7a63-140">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="a7a63-140">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="a7a63-141">Új – AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="a7a63-141">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="a7a63-142">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="a7a63-142">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)


