---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 545CAB1C-F08C-4472-A41A-1FE900D2EDA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8ae51b2f239fd9ec7f09fe27e08ccdaa41c4bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015482"
---
# <span data-ttu-id="3c946-101">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="3c946-101">Remove-AzureWebsiteJob</span></span>

## <span data-ttu-id="3c946-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c946-102">SYNOPSIS</span></span>
<span data-ttu-id="3c946-103">Eltávolít egy meglévő webes feladatot egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="3c946-103">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="3c946-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c946-104">SYNTAX</span></span>

```
Remove-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3c946-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c946-105">DESCRIPTION</span></span>
<span data-ttu-id="3c946-106">Eltávolít egy meglévő webes feladatot egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="3c946-106">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="3c946-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3c946-107">EXAMPLES</span></span>

### <span data-ttu-id="3c946-108">1. példa: meglévő webes feladat eltávolítása egy webhelyhez</span><span class="sxs-lookup"><span data-stu-id="3c946-108">Example 1: Remove an existing web job for a website</span></span>
```
PS C:\> Remove-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="3c946-109">Eltávolítja a MyWebJob nevű webes feladatot a MyWebSite.</span><span class="sxs-lookup"><span data-stu-id="3c946-109">Removes a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="3c946-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c946-110">PARAMETERS</span></span>

### <span data-ttu-id="3c946-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3c946-111">-Force</span></span>
<span data-ttu-id="3c946-112">Jelzi, hogy ez a parancsmag eltávolítja a webes feladatot, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c946-112">Indicates that this cmdlet removes the web job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3c946-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="3c946-113">-JobName</span></span>
<span data-ttu-id="3c946-114">A webes feladat neve.</span><span class="sxs-lookup"><span data-stu-id="3c946-114">The web job name.</span></span>

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

### <span data-ttu-id="3c946-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="3c946-115">-JobType</span></span>
<span data-ttu-id="3c946-116">A webes feladat típusa.</span><span class="sxs-lookup"><span data-stu-id="3c946-116">The web job type.</span></span>
<span data-ttu-id="3c946-117">Lehet indító vagy folytonos.</span><span class="sxs-lookup"><span data-stu-id="3c946-117">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="3c946-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c946-118">-Name</span></span>
<span data-ttu-id="3c946-119">Az Azure-webhely neve.</span><span class="sxs-lookup"><span data-stu-id="3c946-119">The name of the Azure website.</span></span>

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

### <span data-ttu-id="3c946-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c946-120">-Profile</span></span>
<span data-ttu-id="3c946-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3c946-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c946-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3c946-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c946-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="3c946-123">-Slot</span></span>
<span data-ttu-id="3c946-124">Az Azure-webhely tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="3c946-124">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="3c946-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c946-125">CommonParameters</span></span>
<span data-ttu-id="3c946-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c946-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c946-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c946-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c946-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c946-128">INPUTS</span></span>

## <span data-ttu-id="3c946-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c946-129">OUTPUTS</span></span>

## <span data-ttu-id="3c946-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c946-130">NOTES</span></span>

## <span data-ttu-id="3c946-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c946-131">RELATED LINKS</span></span>

[<span data-ttu-id="3c946-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3c946-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="3c946-133">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="3c946-133">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="3c946-134">Új – AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="3c946-134">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="3c946-135">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="3c946-135">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="3c946-136">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="3c946-136">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


