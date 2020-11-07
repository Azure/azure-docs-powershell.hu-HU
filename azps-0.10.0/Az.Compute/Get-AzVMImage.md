---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 7b7a61c6d3043fcb4687d75ac49400b88361b81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844590"
---
# <span data-ttu-id="8e518-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8e518-101">Get-AzVMImage</span></span>

## <span data-ttu-id="8e518-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e518-102">SYNOPSIS</span></span>
<span data-ttu-id="8e518-103">Beolvassa a VMImage összes verzióját.</span><span class="sxs-lookup"><span data-stu-id="8e518-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="8e518-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e518-104">SYNTAX</span></span>

### <span data-ttu-id="8e518-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="8e518-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e518-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="8e518-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e518-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e518-107">DESCRIPTION</span></span>
<span data-ttu-id="8e518-108">A **Get-AzVMImage** parancsmag a VMImage összes verzióját kapja.</span><span class="sxs-lookup"><span data-stu-id="8e518-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="8e518-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8e518-109">EXAMPLES</span></span>

### <span data-ttu-id="8e518-110">1. példa: VMImage-objektumok beolvasása</span><span class="sxs-lookup"><span data-stu-id="8e518-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="8e518-111">Ez a parancs a megadott értékeknek megfelelő VMImage-verziókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8e518-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="8e518-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e518-112">PARAMETERS</span></span>

### <span data-ttu-id="8e518-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e518-113">-DefaultProfile</span></span>
<span data-ttu-id="8e518-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e518-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e518-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="8e518-115">-FilterExpression</span></span>
<span data-ttu-id="8e518-116">A szűrő kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e518-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="8e518-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="8e518-117">-Location</span></span>
<span data-ttu-id="8e518-118">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e518-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="8e518-119">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="8e518-119">-Offer</span></span>
<span data-ttu-id="8e518-120">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e518-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="8e518-121">Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8e518-121">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="8e518-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="8e518-122">-PublisherName</span></span>
<span data-ttu-id="8e518-123">A VMImage közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e518-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="8e518-124">Képközzétevő beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8e518-124">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="8e518-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="8e518-125">-Skus</span></span>
<span data-ttu-id="8e518-126">Egy VMImage SKU-ot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8e518-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="8e518-127">SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8e518-127">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="8e518-128">-Verzió</span><span class="sxs-lookup"><span data-stu-id="8e518-128">-Version</span></span>
<span data-ttu-id="8e518-129">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e518-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="8e518-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e518-130">CommonParameters</span></span>
<span data-ttu-id="8e518-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e518-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e518-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e518-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e518-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e518-133">INPUTS</span></span>

### <span data-ttu-id="8e518-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e518-134">None</span></span>
<span data-ttu-id="8e518-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8e518-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8e518-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e518-136">OUTPUTS</span></span>

### <span data-ttu-id="8e518-137">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="8e518-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="8e518-138">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="8e518-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="8e518-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e518-139">NOTES</span></span>

## <span data-ttu-id="8e518-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e518-140">RELATED LINKS</span></span>

[<span data-ttu-id="8e518-141">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8e518-141">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="8e518-142">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8e518-142">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="8e518-143">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8e518-143">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="8e518-144">Mentés-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8e518-144">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


