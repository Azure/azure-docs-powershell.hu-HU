---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 5588d320d63a298fab632ea55d7c3b6c2220db85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492565"
---
# <span data-ttu-id="c00ce-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c00ce-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="c00ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c00ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c00ce-103">Beolvassa a VMImage összes verzióját.</span><span class="sxs-lookup"><span data-stu-id="c00ce-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c00ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c00ce-104">SYNTAX</span></span>

### <span data-ttu-id="c00ce-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="c00ce-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c00ce-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="c00ce-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c00ce-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c00ce-107">DESCRIPTION</span></span>
<span data-ttu-id="c00ce-108">A **Get-AzureRmVMImage** parancsmag a VMImage összes verzióját kapja.</span><span class="sxs-lookup"><span data-stu-id="c00ce-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="c00ce-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c00ce-109">EXAMPLES</span></span>

### <span data-ttu-id="c00ce-110">1. példa: VMImage-objektumok beolvasása</span><span class="sxs-lookup"><span data-stu-id="c00ce-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="c00ce-111">Ez a parancs a megadott értékeknek megfelelő VMImage-verziókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c00ce-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="c00ce-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c00ce-112">PARAMETERS</span></span>

### <span data-ttu-id="c00ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c00ce-113">-DefaultProfile</span></span>
<span data-ttu-id="c00ce-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c00ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c00ce-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="c00ce-115">-FilterExpression</span></span>
<span data-ttu-id="c00ce-116">A szűrő kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="c00ce-116">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00ce-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="c00ce-117">-Location</span></span>
<span data-ttu-id="c00ce-118">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c00ce-118">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c00ce-119">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="c00ce-119">-Offer</span></span>
<span data-ttu-id="c00ce-120">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c00ce-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="c00ce-121">Képajánlat beolvasásához használja az Get-AzureRmVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c00ce-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c00ce-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c00ce-122">-PublisherName</span></span>
<span data-ttu-id="c00ce-123">A VMImage közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c00ce-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="c00ce-124">Képközzétevő beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c00ce-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c00ce-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="c00ce-125">-Skus</span></span>
<span data-ttu-id="c00ce-126">Egy VMImage SKU-ot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c00ce-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="c00ce-127">SKU beolvasásához használja az Get-AzureRmVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c00ce-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c00ce-128">-Verzió</span><span class="sxs-lookup"><span data-stu-id="c00ce-128">-Version</span></span>
<span data-ttu-id="c00ce-129">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c00ce-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c00ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c00ce-130">CommonParameters</span></span>
<span data-ttu-id="c00ce-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c00ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c00ce-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c00ce-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c00ce-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c00ce-133">INPUTS</span></span>

## <span data-ttu-id="c00ce-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c00ce-134">OUTPUTS</span></span>

## <span data-ttu-id="c00ce-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c00ce-135">NOTES</span></span>

## <span data-ttu-id="c00ce-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c00ce-136">RELATED LINKS</span></span>

[<span data-ttu-id="c00ce-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c00ce-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="c00ce-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c00ce-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="c00ce-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c00ce-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="c00ce-140">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c00ce-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


