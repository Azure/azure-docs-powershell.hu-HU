---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1254A28B-F670-44B2-BB0E-BD41B9483E3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1910a0da546bdc4d5b167d82685608669b7565c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016183"
---
# <span data-ttu-id="bf5de-101">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="bf5de-101">New-AzureWebsiteJob</span></span>

## <span data-ttu-id="bf5de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf5de-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5de-103">Webes feladatot hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="bf5de-103">Creates a web job for a website.</span></span>

## <span data-ttu-id="bf5de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf5de-104">SYNTAX</span></span>

```
New-AzureWebsiteJob -JobName <String> -JobType <WebJobType> -JobFile <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bf5de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf5de-105">DESCRIPTION</span></span>
<span data-ttu-id="bf5de-106">A **New-AzureWebsiteJob** parancsmag webes feladatot hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="bf5de-106">The **New-AzureWebsiteJob** cmdlet creates a web job for a website.</span></span>

## <span data-ttu-id="bf5de-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf5de-107">EXAMPLES</span></span>

### <span data-ttu-id="bf5de-108">1. példa: új webes feladat létrehozása egy webhelyhez</span><span class="sxs-lookup"><span data-stu-id="bf5de-108">Example 1: Create new web job for a website</span></span>
```
PS C:\> New-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous -JobFile job.bat
```

<span data-ttu-id="bf5de-109">Folytonos feladatot hoz létre job.bat a webhely MyWebsite.</span><span class="sxs-lookup"><span data-stu-id="bf5de-109">Creates a continuous job to call job.bat on website MyWebsite.</span></span>

## <span data-ttu-id="bf5de-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf5de-110">PARAMETERS</span></span>

### <span data-ttu-id="bf5de-111">-JobFile</span><span class="sxs-lookup"><span data-stu-id="bf5de-111">-JobFile</span></span>
<span data-ttu-id="bf5de-112">A webes Job fájl.</span><span class="sxs-lookup"><span data-stu-id="bf5de-112">The web job file.</span></span>

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

### <span data-ttu-id="bf5de-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="bf5de-113">-JobName</span></span>
<span data-ttu-id="bf5de-114">A webes feladat neve.</span><span class="sxs-lookup"><span data-stu-id="bf5de-114">The web job name.</span></span>

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

### <span data-ttu-id="bf5de-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="bf5de-115">-JobType</span></span>
<span data-ttu-id="bf5de-116">A webes feladat típusa.</span><span class="sxs-lookup"><span data-stu-id="bf5de-116">The web job type.</span></span>
<span data-ttu-id="bf5de-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bf5de-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf5de-118">Megjelenő</span><span class="sxs-lookup"><span data-stu-id="bf5de-118">Triggered</span></span> 
- <span data-ttu-id="bf5de-119">Folyamatos</span><span class="sxs-lookup"><span data-stu-id="bf5de-119">Continuous</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf5de-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf5de-120">-Name</span></span>
<span data-ttu-id="bf5de-121">Az Azure-webhely neve.</span><span class="sxs-lookup"><span data-stu-id="bf5de-121">The name of the Azure website.</span></span>

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

### <span data-ttu-id="bf5de-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="bf5de-122">-Profile</span></span>
<span data-ttu-id="bf5de-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="bf5de-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf5de-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="bf5de-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf5de-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="bf5de-125">-Slot</span></span>
<span data-ttu-id="bf5de-126">Az Azure-webhely tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="bf5de-126">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="bf5de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5de-127">CommonParameters</span></span>
<span data-ttu-id="bf5de-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf5de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5de-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf5de-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5de-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf5de-130">INPUTS</span></span>

## <span data-ttu-id="bf5de-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf5de-131">OUTPUTS</span></span>

## <span data-ttu-id="bf5de-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf5de-132">NOTES</span></span>

## <span data-ttu-id="bf5de-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf5de-133">RELATED LINKS</span></span>

[<span data-ttu-id="bf5de-134">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bf5de-134">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="bf5de-135">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="bf5de-135">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="bf5de-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="bf5de-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="bf5de-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="bf5de-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="bf5de-138">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="bf5de-138">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


