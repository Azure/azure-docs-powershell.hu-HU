---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A66ADA39-56D9-421B-BC69-996253352236
online version: ''
schema: 2.0.0
ms.openlocfilehash: b5b2cfaea544b5a8575715ec89735b5b9a1ad28f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015767"
---
# <span data-ttu-id="ec7b1-101">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ec7b1-101">Start-AzureWebsiteJob</span></span>

## <span data-ttu-id="ec7b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7b1-103">Webfeladatot indít egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-103">Starts a web job for a website.</span></span>

## <span data-ttu-id="ec7b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec7b1-104">SYNTAX</span></span>

```
Start-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec7b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec7b1-105">DESCRIPTION</span></span>
<span data-ttu-id="ec7b1-106">A **Start-AzureWebsiteJob** parancsmag webfeladatot indít egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-106">The **Start-AzureWebsiteJob** cmdlet starts a web job for a website.</span></span>

## <span data-ttu-id="ec7b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ec7b1-107">EXAMPLES</span></span>

### <span data-ttu-id="ec7b1-108">1. példa: webes feladat indítása webhelyhez</span><span class="sxs-lookup"><span data-stu-id="ec7b1-108">Example 1: Start a web job for a website</span></span>
```
PS C:\> Start-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="ec7b1-109">Elindítja a MyWebJob nevű webes feladatot a MyWebSite.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-109">Starts a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="ec7b1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec7b1-110">PARAMETERS</span></span>

### <span data-ttu-id="ec7b1-111">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="ec7b1-111">-JobName</span></span>
<span data-ttu-id="ec7b1-112">A webes feladat neve.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-112">The web job name.</span></span>

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

### <span data-ttu-id="ec7b1-113">-JobType</span><span class="sxs-lookup"><span data-stu-id="ec7b1-113">-JobType</span></span>
<span data-ttu-id="ec7b1-114">A webes feladat típusa.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-114">The web job type.</span></span>
<span data-ttu-id="ec7b1-115">Lehet indító vagy folytonos.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-115">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="ec7b1-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec7b1-116">-Name</span></span>
<span data-ttu-id="ec7b1-117">Az Azure-webhely neve.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-117">The name of the Azure website.</span></span>

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

### <span data-ttu-id="ec7b1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec7b1-118">-PassThru</span></span>
<span data-ttu-id="ec7b1-119">Egy logikai értéket ad eredményül, amely azt jelzi, hogy a feladat sikeresen elindult.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-119">Returns a boolean value indicating that the job started successfully.</span></span>
<span data-ttu-id="ec7b1-120">Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-120">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="ec7b1-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="ec7b1-121">-Profile</span></span>
<span data-ttu-id="ec7b1-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec7b1-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec7b1-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="ec7b1-124">-Slot</span></span>
<span data-ttu-id="ec7b1-125">Az Azure-webhely tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="ec7b1-125">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="ec7b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7b1-126">CommonParameters</span></span>
<span data-ttu-id="ec7b1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec7b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7b1-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec7b1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7b1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec7b1-129">INPUTS</span></span>

## <span data-ttu-id="ec7b1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec7b1-130">OUTPUTS</span></span>

## <span data-ttu-id="ec7b1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec7b1-131">NOTES</span></span>

## <span data-ttu-id="ec7b1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec7b1-132">RELATED LINKS</span></span>

[<span data-ttu-id="ec7b1-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ec7b1-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="ec7b1-134">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ec7b1-134">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="ec7b1-135">Új – AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ec7b1-135">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="ec7b1-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ec7b1-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="ec7b1-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ec7b1-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


