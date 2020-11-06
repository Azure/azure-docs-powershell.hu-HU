---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493199"
---
# <span data-ttu-id="b8a92-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b8a92-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="b8a92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8a92-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a92-103">Beolvassa a VMImage összes verzióját.</span><span class="sxs-lookup"><span data-stu-id="b8a92-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8a92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8a92-104">SYNTAX</span></span>

### <span data-ttu-id="b8a92-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="b8a92-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### <span data-ttu-id="b8a92-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="b8a92-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## <span data-ttu-id="b8a92-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8a92-107">DESCRIPTION</span></span>
<span data-ttu-id="b8a92-108">A **Get-AzureRmVMImage** parancsmag a VMImage összes verzióját kapja.</span><span class="sxs-lookup"><span data-stu-id="b8a92-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="b8a92-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b8a92-109">EXAMPLES</span></span>

### <span data-ttu-id="b8a92-110">1. példa: VMImage-objektumok beolvasása</span><span class="sxs-lookup"><span data-stu-id="b8a92-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="b8a92-111">Ez a parancs a megadott értékeknek megfelelő VMImage-verziókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b8a92-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="b8a92-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8a92-112">PARAMETERS</span></span>

### <span data-ttu-id="b8a92-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="b8a92-113">-FilterExpression</span></span>
<span data-ttu-id="b8a92-114">A szűrő kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8a92-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a92-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="b8a92-115">-Location</span></span>
<span data-ttu-id="b8a92-116">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8a92-116">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="b8a92-117">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="b8a92-117">-Offer</span></span>
<span data-ttu-id="b8a92-118">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8a92-118">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="b8a92-119">Képajánlat beolvasásához használja az Get-AzureRmVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b8a92-119">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="b8a92-120">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b8a92-120">-PublisherName</span></span>
<span data-ttu-id="b8a92-121">A VMImage közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8a92-121">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="b8a92-122">Képközzétevő beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b8a92-122">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="b8a92-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="b8a92-123">-Skus</span></span>
<span data-ttu-id="b8a92-124">Egy VMImage SKU-ot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b8a92-124">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="b8a92-125">SKU beolvasásához használja az Get-AzureRmVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b8a92-125">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="b8a92-126">-Verzió</span><span class="sxs-lookup"><span data-stu-id="b8a92-126">-Version</span></span>
<span data-ttu-id="b8a92-127">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8a92-127">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a92-128">CommonParameters</span></span>
<span data-ttu-id="b8a92-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8a92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a92-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a92-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a92-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8a92-131">INPUTS</span></span>

### <span data-ttu-id="b8a92-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="b8a92-132">None</span></span>
<span data-ttu-id="b8a92-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b8a92-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8a92-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8a92-134">OUTPUTS</span></span>

## <span data-ttu-id="b8a92-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8a92-135">NOTES</span></span>

## <span data-ttu-id="b8a92-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8a92-136">RELATED LINKS</span></span>

[<span data-ttu-id="b8a92-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="b8a92-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="b8a92-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b8a92-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="b8a92-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="b8a92-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="b8a92-140">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b8a92-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


