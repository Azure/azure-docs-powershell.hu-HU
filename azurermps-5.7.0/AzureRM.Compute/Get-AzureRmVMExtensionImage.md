---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: bae8fb04e71700d1572b8742f8cccbb2ebe8e331
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493204"
---
# <span data-ttu-id="72edc-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="72edc-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="72edc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72edc-102">SYNOPSIS</span></span>
<span data-ttu-id="72edc-103">Az Azure-bővítmény minden verziójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="72edc-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72edc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72edc-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [<CommonParameters>]
```

## <span data-ttu-id="72edc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72edc-105">DESCRIPTION</span></span>
<span data-ttu-id="72edc-106">A **Get-AzureRmVMExtensionImage** parancsmag az Azure-bővítmények minden verzióját bekapja.</span><span class="sxs-lookup"><span data-stu-id="72edc-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="72edc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72edc-107">EXAMPLES</span></span>

### <span data-ttu-id="72edc-108">Példa 1: a kiterjesztési kép verziószámának beszerzése</span><span class="sxs-lookup"><span data-stu-id="72edc-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="72edc-109">Ez a parancs a megadott helyen, a Publisherben és a Type (kiterjesztés) kép összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="72edc-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="72edc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72edc-110">PARAMETERS</span></span>

### <span data-ttu-id="72edc-111">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="72edc-111">-FilterExpression</span></span>
<span data-ttu-id="72edc-112">A szűrő kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="72edc-112">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="72edc-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="72edc-113">-Location</span></span>
<span data-ttu-id="72edc-114">A kiterjesztés helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72edc-114">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="72edc-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="72edc-115">-PublisherName</span></span>
<span data-ttu-id="72edc-116">A bővítmények közzétevői nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72edc-116">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="72edc-117">A bővítmények közzétevőjét az Get-AzureRmVMImagePublisher parancsmag használatával kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="72edc-117">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="72edc-118">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="72edc-118">-Type</span></span>
<span data-ttu-id="72edc-119">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="72edc-119">Specifies the type of the extension.</span></span>
<span data-ttu-id="72edc-120">A bővítmények típusának beolvasásához használja az Get-AzureRmVMExtensionImageType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="72edc-120">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="72edc-121">-Verzió</span><span class="sxs-lookup"><span data-stu-id="72edc-121">-Version</span></span>
<span data-ttu-id="72edc-122">Annak a bővítménynek a verziószámát adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="72edc-122">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="72edc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72edc-123">CommonParameters</span></span>
<span data-ttu-id="72edc-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72edc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72edc-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72edc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72edc-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72edc-126">INPUTS</span></span>

### <span data-ttu-id="72edc-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="72edc-127">None</span></span>
<span data-ttu-id="72edc-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="72edc-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72edc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72edc-129">OUTPUTS</span></span>

## <span data-ttu-id="72edc-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72edc-130">NOTES</span></span>

## <span data-ttu-id="72edc-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72edc-131">RELATED LINKS</span></span>

[<span data-ttu-id="72edc-132">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="72edc-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="72edc-133">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="72edc-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="72edc-134">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="72edc-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


