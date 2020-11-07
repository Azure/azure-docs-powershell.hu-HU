---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: c69474929fa91b2e4ae1c7f4e50d5961a9322f66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849378"
---
# <span data-ttu-id="fcb47-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fcb47-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="fcb47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcb47-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb47-103">Beolvassa a VMImage összes verzióját.</span><span class="sxs-lookup"><span data-stu-id="fcb47-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcb47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcb47-104">SYNTAX</span></span>

### <span data-ttu-id="fcb47-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="fcb47-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcb47-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="fcb47-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcb47-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcb47-107">DESCRIPTION</span></span>
<span data-ttu-id="fcb47-108">A **Get-AzureRmVMImage** parancsmag a VMImage összes verzióját kapja.</span><span class="sxs-lookup"><span data-stu-id="fcb47-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="fcb47-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fcb47-109">EXAMPLES</span></span>

### <span data-ttu-id="fcb47-110">1. példa: VMImage-objektumok beolvasása</span><span class="sxs-lookup"><span data-stu-id="fcb47-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="fcb47-111">Ez a parancs a megadott értékeknek megfelelő VMImage-verziókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb47-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="fcb47-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcb47-112">PARAMETERS</span></span>

### <span data-ttu-id="fcb47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb47-113">-DefaultProfile</span></span>
<span data-ttu-id="fcb47-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcb47-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb47-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="fcb47-115">-FilterExpression</span></span>
<span data-ttu-id="fcb47-116">A szűrő kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb47-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="fcb47-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="fcb47-117">-Location</span></span>
<span data-ttu-id="fcb47-118">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb47-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="fcb47-119">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="fcb47-119">-Offer</span></span>
<span data-ttu-id="fcb47-120">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb47-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="fcb47-121">Képajánlat beolvasásához használja az Get-AzureRmVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fcb47-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="fcb47-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="fcb47-122">-PublisherName</span></span>
<span data-ttu-id="fcb47-123">A VMImage közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb47-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="fcb47-124">Képközzétevő beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fcb47-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="fcb47-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="fcb47-125">-Skus</span></span>
<span data-ttu-id="fcb47-126">Egy VMImage SKU-ot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fcb47-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="fcb47-127">SKU beolvasásához használja az Get-AzureRmVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fcb47-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="fcb47-128">-Verzió</span><span class="sxs-lookup"><span data-stu-id="fcb47-128">-Version</span></span>
<span data-ttu-id="fcb47-129">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb47-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="fcb47-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb47-130">CommonParameters</span></span>
<span data-ttu-id="fcb47-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcb47-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb47-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb47-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb47-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcb47-133">INPUTS</span></span>

### <span data-ttu-id="fcb47-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="fcb47-134">None</span></span>
<span data-ttu-id="fcb47-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fcb47-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fcb47-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcb47-136">OUTPUTS</span></span>

### <span data-ttu-id="fcb47-137">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="fcb47-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="fcb47-138">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="fcb47-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="fcb47-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcb47-139">NOTES</span></span>

## <span data-ttu-id="fcb47-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcb47-140">RELATED LINKS</span></span>

[<span data-ttu-id="fcb47-141">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="fcb47-141">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="fcb47-142">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fcb47-142">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="fcb47-143">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fcb47-143">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="fcb47-144">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fcb47-144">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


