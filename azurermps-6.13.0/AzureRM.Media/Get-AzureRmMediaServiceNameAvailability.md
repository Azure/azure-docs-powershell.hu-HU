---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: 8de8b9f389f8d57d844c17d92dd492390fbf1884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493663"
---
# <span data-ttu-id="41e5b-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="41e5b-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="41e5b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="41e5b-103">Annak ellenőrzése, hogy elérhető-e egy médiafájl neve.</span><span class="sxs-lookup"><span data-stu-id="41e5b-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="41e5b-104">A médiafájlok nevei globálisan egyediek.</span><span class="sxs-lookup"><span data-stu-id="41e5b-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41e5b-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41e5b-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="41e5b-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="41e5b-106">DESCRIPTION</span></span>
<span data-ttu-id="41e5b-107">A **Get-AzureRmMediaServiceNameAvailability** parancsmag ellenőrzi, hogy elérhető-e egy médiafájl neve.</span><span class="sxs-lookup"><span data-stu-id="41e5b-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="41e5b-108">A médiafájlok nevei globálisan egyediek.</span><span class="sxs-lookup"><span data-stu-id="41e5b-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="41e5b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="41e5b-109">EXAMPLES</span></span>

### <span data-ttu-id="41e5b-110">1. példa: annak ellenőrzése, hogy elérhető-e a médiafájl neve</span><span class="sxs-lookup"><span data-stu-id="41e5b-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="41e5b-111">Ez a parancs ellenőrzi, hogy elérhető-e a MediaService1 név.</span><span class="sxs-lookup"><span data-stu-id="41e5b-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="41e5b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41e5b-112">PARAMETERS</span></span>

### <span data-ttu-id="41e5b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="41e5b-113">-AccountName</span></span>
<span data-ttu-id="41e5b-114">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="41e5b-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e5b-115">-DefaultProfile</span></span>
<span data-ttu-id="41e5b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="41e5b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e5b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e5b-117">CommonParameters</span></span>
<span data-ttu-id="41e5b-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41e5b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e5b-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41e5b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e5b-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41e5b-120">INPUTS</span></span>

### <span data-ttu-id="41e5b-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="41e5b-121">None</span></span>

## <span data-ttu-id="41e5b-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41e5b-122">OUTPUTS</span></span>

### <span data-ttu-id="41e5b-123">Microsoft. Azure. commands. Media. models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="41e5b-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="41e5b-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41e5b-124">NOTES</span></span>

## <span data-ttu-id="41e5b-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41e5b-125">RELATED LINKS</span></span>

[<span data-ttu-id="41e5b-126">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="41e5b-126">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="41e5b-127">Új – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="41e5b-127">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="41e5b-128">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="41e5b-128">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="41e5b-129">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="41e5b-129">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


