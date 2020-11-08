---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1FB590D3-E5D2-45F0-A611-01A1B701938A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 89d0c4dd73e5d921eb447e213876d8906c210b34
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016374"
---
# <span data-ttu-id="84981-101">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="84981-101">Enable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="84981-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84981-102">SYNOPSIS</span></span>
<span data-ttu-id="84981-103">Engedélyezi a webhely hibakeresését.</span><span class="sxs-lookup"><span data-stu-id="84981-103">Enables the website's debug.</span></span>

## <span data-ttu-id="84981-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84981-104">SYNTAX</span></span>

```
Enable-AzureWebsiteDebug [-PassThru] -Version <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="84981-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84981-105">DESCRIPTION</span></span>
<span data-ttu-id="84981-106">Engedélyezi a webhely hibakeresési funkcióját a Visual Studio alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="84981-106">Enables the website's debug feature in Visual Studio.</span></span>

## <span data-ttu-id="84981-107">Példák</span><span class="sxs-lookup"><span data-stu-id="84981-107">EXAMPLES</span></span>

### <span data-ttu-id="84981-108">A Visual Studio 2013 hibakeresésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="84981-108">Enable debugging of Visual Studio 2013</span></span>
```
PS C:\> Enable-AzureWebsiteDebug -Name MyWebsite -Version VS2013
```

<span data-ttu-id="84981-109">Engedélyezi a hibakeresést a VS 2013-on.</span><span class="sxs-lookup"><span data-stu-id="84981-109">Enables debugging on VS 2013.</span></span>

## <span data-ttu-id="84981-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84981-110">PARAMETERS</span></span>

### <span data-ttu-id="84981-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84981-111">-Name</span></span>
<span data-ttu-id="84981-112">Az Azure-webhely neve.</span><span class="sxs-lookup"><span data-stu-id="84981-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="84981-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84981-113">-PassThru</span></span>
<span data-ttu-id="84981-114">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="84981-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="84981-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="84981-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="84981-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="84981-116">-Profile</span></span>
<span data-ttu-id="84981-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="84981-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84981-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="84981-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="84981-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="84981-119">-Slot</span></span>
<span data-ttu-id="84981-120">Az Azure-webhely tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="84981-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="84981-121">-Verzió</span><span class="sxs-lookup"><span data-stu-id="84981-121">-Version</span></span>
<span data-ttu-id="84981-122">A Visual Studio verziója.</span><span class="sxs-lookup"><span data-stu-id="84981-122">The Visual Studio version.</span></span>

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

### <span data-ttu-id="84981-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84981-123">CommonParameters</span></span>
<span data-ttu-id="84981-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84981-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84981-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84981-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84981-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84981-126">INPUTS</span></span>

## <span data-ttu-id="84981-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84981-127">OUTPUTS</span></span>

## <span data-ttu-id="84981-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84981-128">NOTES</span></span>

## <span data-ttu-id="84981-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84981-129">RELATED LINKS</span></span>

[<span data-ttu-id="84981-130">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="84981-130">Disable-AzureWebsiteDebug</span></span>](./Disable-AzureWebsiteDebug.md)

[<span data-ttu-id="84981-131">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="84981-131">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="84981-132">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="84981-132">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="84981-133">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="84981-133">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="84981-134">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="84981-134">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


