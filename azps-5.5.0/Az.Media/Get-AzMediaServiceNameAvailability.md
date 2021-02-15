---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207167"
---
# <span data-ttu-id="353e3-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="353e3-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="353e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="353e3-102">SYNOPSIS</span></span>
<span data-ttu-id="353e3-103">Annak ellenőrzése, hogy elérhető-e egy médiaszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="353e3-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="353e3-104">A médiaszolgáltatás nevei globálisan egyediek.</span><span class="sxs-lookup"><span data-stu-id="353e3-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="353e3-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="353e3-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="353e3-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="353e3-106">DESCRIPTION</span></span>
<span data-ttu-id="353e3-107">A **Get-AzMediaServiceNameAvailability** parancsmag ellenőrzi, hogy elérhető-e egy médiaszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="353e3-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="353e3-108">A médiaszolgáltatás nevei globálisan egyediek.</span><span class="sxs-lookup"><span data-stu-id="353e3-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="353e3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="353e3-109">EXAMPLES</span></span>

### <span data-ttu-id="353e3-110">1. példa: Annak ellenőrzése, hogy elérhető-e egy médiaszolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="353e3-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="353e3-111">Ez a parancs ellenőrzi, hogy elérhető-e a MediaService1 név.</span><span class="sxs-lookup"><span data-stu-id="353e3-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="353e3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="353e3-112">PARAMETERS</span></span>

### <span data-ttu-id="353e3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="353e3-113">-AccountName</span></span>
<span data-ttu-id="353e3-114">A parancsmag médiaszolgáltatásának a neve.</span><span class="sxs-lookup"><span data-stu-id="353e3-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="353e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353e3-115">-DefaultProfile</span></span>
<span data-ttu-id="353e3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="353e3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="353e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353e3-117">CommonParameters</span></span>
<span data-ttu-id="353e3-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="353e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353e3-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="353e3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353e3-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="353e3-120">INPUTS</span></span>

### <span data-ttu-id="353e3-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="353e3-121">None</span></span>

## <span data-ttu-id="353e3-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="353e3-122">OUTPUTS</span></span>

### <span data-ttu-id="353e3-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="353e3-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="353e3-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="353e3-124">NOTES</span></span>

## <span data-ttu-id="353e3-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="353e3-125">RELATED LINKS</span></span>

[<span data-ttu-id="353e3-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="353e3-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="353e3-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="353e3-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="353e3-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="353e3-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="353e3-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="353e3-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


