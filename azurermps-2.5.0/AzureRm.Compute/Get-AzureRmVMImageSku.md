---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
ms.openlocfilehash: 8d2253e20e87a0e6a5d97f2dd0e405412f5a9282
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850157"
---
# <span data-ttu-id="e788b-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e788b-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="e788b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e788b-102">SYNOPSIS</span></span>
<span data-ttu-id="e788b-103">Megkapja a VMImage SKU-ot.</span><span class="sxs-lookup"><span data-stu-id="e788b-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e788b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e788b-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e788b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e788b-105">DESCRIPTION</span></span>
<span data-ttu-id="e788b-106">A **Get-AzureRmVMImageSku** parancsmag VMImage SKU-t kap.</span><span class="sxs-lookup"><span data-stu-id="e788b-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="e788b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e788b-107">EXAMPLES</span></span>

### <span data-ttu-id="e788b-108">Példa 1: VMImage SKU beszerzése</span><span class="sxs-lookup"><span data-stu-id="e788b-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="e788b-109">Ez a parancs a megadott közzétevőhöz és ajánlathoz kapja a SKU-t.</span><span class="sxs-lookup"><span data-stu-id="e788b-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="e788b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e788b-110">PARAMETERS</span></span>

### <span data-ttu-id="e788b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e788b-111">-DefaultProfile</span></span>
<span data-ttu-id="e788b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e788b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e788b-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="e788b-113">-Location</span></span>
<span data-ttu-id="e788b-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e788b-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="e788b-115">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="e788b-115">-Offer</span></span>
<span data-ttu-id="e788b-116">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e788b-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="e788b-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="e788b-117">-PublisherName</span></span>
<span data-ttu-id="e788b-118">A VMImage közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e788b-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="e788b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e788b-119">CommonParameters</span></span>
<span data-ttu-id="e788b-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e788b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e788b-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e788b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e788b-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e788b-122">INPUTS</span></span>

### <span data-ttu-id="e788b-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="e788b-123">None</span></span>
<span data-ttu-id="e788b-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e788b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e788b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e788b-125">OUTPUTS</span></span>

### <span data-ttu-id="e788b-126">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="e788b-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="e788b-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e788b-127">NOTES</span></span>

## <span data-ttu-id="e788b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e788b-128">RELATED LINKS</span></span>

[<span data-ttu-id="e788b-129">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e788b-129">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="e788b-130">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e788b-130">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="e788b-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e788b-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e788b-132">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e788b-132">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


