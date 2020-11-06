---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: ccdc7ee8a63c0a633caf162f8549fd1ba737ce8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503855"
---
# <span data-ttu-id="30788-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="30788-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="30788-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30788-102">SYNOPSIS</span></span>
<span data-ttu-id="30788-103">Beolvassa a VMImage kínálati típust.</span><span class="sxs-lookup"><span data-stu-id="30788-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30788-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30788-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="30788-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30788-105">DESCRIPTION</span></span>
<span data-ttu-id="30788-106">A **Get-AzureRmVMImageOffer** parancsmag a VMImage ajánlatok típusait kapja.</span><span class="sxs-lookup"><span data-stu-id="30788-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="30788-107">Példák</span><span class="sxs-lookup"><span data-stu-id="30788-107">EXAMPLES</span></span>

### <span data-ttu-id="30788-108">1. példa: ajánlati típusok beszerzése Publisherhez</span><span class="sxs-lookup"><span data-stu-id="30788-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="30788-109">Ez a parancs a közép-amerikai régióban a megadott közzétevőhöz tartozó ajánlati típusokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="30788-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="30788-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30788-110">PARAMETERS</span></span>

### <span data-ttu-id="30788-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="30788-111">-Location</span></span>
<span data-ttu-id="30788-112">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30788-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="30788-113">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="30788-113">-PublisherName</span></span>
<span data-ttu-id="30788-114">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30788-114">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="30788-115">Publisher beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="30788-115">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="30788-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30788-116">CommonParameters</span></span>
<span data-ttu-id="30788-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30788-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30788-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30788-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30788-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30788-119">INPUTS</span></span>

### <span data-ttu-id="30788-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="30788-120">None</span></span>
<span data-ttu-id="30788-121">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="30788-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30788-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30788-122">OUTPUTS</span></span>

## <span data-ttu-id="30788-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30788-123">NOTES</span></span>

## <span data-ttu-id="30788-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30788-124">RELATED LINKS</span></span>

[<span data-ttu-id="30788-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="30788-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="30788-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="30788-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="30788-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="30788-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="30788-128">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="30788-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


