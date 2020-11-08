---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016273"
---
# <span data-ttu-id="3a57d-101">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="3a57d-101">Get-AzureWebsiteJob</span></span>

## <span data-ttu-id="3a57d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a57d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a57d-103">A webhelyhez társított webes feladatok beolvasása.</span><span class="sxs-lookup"><span data-stu-id="3a57d-103">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="3a57d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a57d-104">SYNTAX</span></span>

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a57d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a57d-105">DESCRIPTION</span></span>
<span data-ttu-id="3a57d-106">A webhelyhez társított webes feladatok beolvasása.</span><span class="sxs-lookup"><span data-stu-id="3a57d-106">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="3a57d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3a57d-107">EXAMPLES</span></span>

### <span data-ttu-id="3a57d-108">1. példa: konkrét webes munkaköri adatok beolvasása</span><span class="sxs-lookup"><span data-stu-id="3a57d-108">Example 1: Get specific web job info</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="3a57d-109">A MyWebJob nevű internetes feladatot kapja a MyWebsite Production slotból.</span><span class="sxs-lookup"><span data-stu-id="3a57d-109">Gets a web job called MyWebJob from MyWebsite production slot.</span></span>

### <span data-ttu-id="3a57d-110">2. példa: a webhely összes webes feladatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="3a57d-110">Example 2: Get all web jobs for a website</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

<span data-ttu-id="3a57d-111">A MyWebsite-termelési bővítőhelyhez társított összes webes feladat beolvasása.</span><span class="sxs-lookup"><span data-stu-id="3a57d-111">Gets all web jobs associated with MyWebsite production slot.</span></span>

### <span data-ttu-id="3a57d-112">3. példa: az összes aktivált webes feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="3a57d-112">Example 3: Get all triggered web jobs</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

<span data-ttu-id="3a57d-113">Az összes kezdeményezett webes munkahely beolvasása a MyWebsite átmeneti tárolóhelyéről.</span><span class="sxs-lookup"><span data-stu-id="3a57d-113">Gets all triggered web jobs from staging slot of MyWebsite.</span></span>

## <span data-ttu-id="3a57d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a57d-114">PARAMETERS</span></span>

### <span data-ttu-id="3a57d-115">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="3a57d-115">-JobName</span></span>
<span data-ttu-id="3a57d-116">A webes feladat neve</span><span class="sxs-lookup"><span data-stu-id="3a57d-116">The web job name</span></span>

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

### <span data-ttu-id="3a57d-117">-JobType</span><span class="sxs-lookup"><span data-stu-id="3a57d-117">-JobType</span></span>
<span data-ttu-id="3a57d-118">A webes feladat típusa.</span><span class="sxs-lookup"><span data-stu-id="3a57d-118">The web job type.</span></span>
<span data-ttu-id="3a57d-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3a57d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a57d-120">Megjelenő</span><span class="sxs-lookup"><span data-stu-id="3a57d-120">Triggered</span></span>
- <span data-ttu-id="3a57d-121">Folyamatos</span><span class="sxs-lookup"><span data-stu-id="3a57d-121">Continuous</span></span>

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

### <span data-ttu-id="3a57d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a57d-122">-Name</span></span>
<span data-ttu-id="3a57d-123">Az Azure-webhely neve.</span><span class="sxs-lookup"><span data-stu-id="3a57d-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="3a57d-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="3a57d-124">-Profile</span></span>
<span data-ttu-id="3a57d-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3a57d-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a57d-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3a57d-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a57d-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="3a57d-127">-Slot</span></span>
<span data-ttu-id="3a57d-128">Az Azure-webhely tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="3a57d-128">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="3a57d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a57d-129">CommonParameters</span></span>
<span data-ttu-id="3a57d-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a57d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a57d-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a57d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a57d-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a57d-132">INPUTS</span></span>

## <span data-ttu-id="3a57d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a57d-133">OUTPUTS</span></span>

## <span data-ttu-id="3a57d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a57d-134">NOTES</span></span>

## <span data-ttu-id="3a57d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a57d-135">RELATED LINKS</span></span>

[<span data-ttu-id="3a57d-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3a57d-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="3a57d-137">Új – AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="3a57d-137">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="3a57d-138">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="3a57d-138">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="3a57d-139">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="3a57d-139">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="3a57d-140">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="3a57d-140">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


