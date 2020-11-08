---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195794"
---
# <span data-ttu-id="6d479-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="6d479-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="6d479-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d479-102">SYNOPSIS</span></span>
<span data-ttu-id="6d479-103">Annak ellenőrzése, hogy elérhető-e egy médiafájl neve.</span><span class="sxs-lookup"><span data-stu-id="6d479-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="6d479-104">A médiafájlok nevei globálisan egyediek.</span><span class="sxs-lookup"><span data-stu-id="6d479-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="6d479-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d479-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="6d479-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d479-106">DESCRIPTION</span></span>
<span data-ttu-id="6d479-107">A **Get-AzMediaServiceNameAvailability** parancsmag ellenőrzi, hogy elérhető-e egy médiafájl neve.</span><span class="sxs-lookup"><span data-stu-id="6d479-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="6d479-108">A médiafájlok nevei globálisan egyediek.</span><span class="sxs-lookup"><span data-stu-id="6d479-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="6d479-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6d479-109">EXAMPLES</span></span>

### <span data-ttu-id="6d479-110">1. példa: annak ellenőrzése, hogy elérhető-e a médiafájl neve</span><span class="sxs-lookup"><span data-stu-id="6d479-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="6d479-111">Ez a parancs ellenőrzi, hogy elérhető-e a MediaService1 név.</span><span class="sxs-lookup"><span data-stu-id="6d479-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="6d479-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d479-112">PARAMETERS</span></span>

### <span data-ttu-id="6d479-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6d479-113">-AccountName</span></span>
<span data-ttu-id="6d479-114">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="6d479-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6d479-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d479-115">-DefaultProfile</span></span>
<span data-ttu-id="6d479-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6d479-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d479-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d479-117">CommonParameters</span></span>
<span data-ttu-id="6d479-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d479-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d479-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d479-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d479-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d479-120">INPUTS</span></span>

### <span data-ttu-id="6d479-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="6d479-121">None</span></span>

## <span data-ttu-id="6d479-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d479-122">OUTPUTS</span></span>

### <span data-ttu-id="6d479-123">Microsoft. Azure. commands. Media. models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="6d479-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="6d479-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d479-124">NOTES</span></span>

## <span data-ttu-id="6d479-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d479-125">RELATED LINKS</span></span>

[<span data-ttu-id="6d479-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6d479-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="6d479-127">Új – AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6d479-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="6d479-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6d479-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="6d479-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6d479-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


