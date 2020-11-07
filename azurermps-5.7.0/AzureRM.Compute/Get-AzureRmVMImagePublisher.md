---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: f299d0f299eaef61ba3655e8ec221cc55f5ab578
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680189"
---
# <span data-ttu-id="178ea-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="178ea-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="178ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="178ea-102">SYNOPSIS</span></span>
<span data-ttu-id="178ea-103">Megkapja a VMImage-közzétevőket.</span><span class="sxs-lookup"><span data-stu-id="178ea-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="178ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="178ea-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [<CommonParameters>]
```

## <span data-ttu-id="178ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="178ea-105">DESCRIPTION</span></span>
<span data-ttu-id="178ea-106">A **Get-AzureRmVMImagePublisher** parancsmag a VMImage-közzétevőket kapja.</span><span class="sxs-lookup"><span data-stu-id="178ea-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="178ea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="178ea-107">EXAMPLES</span></span>

### <span data-ttu-id="178ea-108">Példa 1: VMImage-közzétevők beszerzése régióhoz</span><span class="sxs-lookup"><span data-stu-id="178ea-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="178ea-109">Ez a parancs a VMImage-példányok közzétevőit a közép-amerikai régióban az Azure-profilon belül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="178ea-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="178ea-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="178ea-110">PARAMETERS</span></span>

### <span data-ttu-id="178ea-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="178ea-111">-Location</span></span>
<span data-ttu-id="178ea-112">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="178ea-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="178ea-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178ea-113">CommonParameters</span></span>
<span data-ttu-id="178ea-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="178ea-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178ea-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178ea-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178ea-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="178ea-116">INPUTS</span></span>

### <span data-ttu-id="178ea-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="178ea-117">None</span></span>
<span data-ttu-id="178ea-118">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="178ea-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="178ea-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="178ea-119">OUTPUTS</span></span>

## <span data-ttu-id="178ea-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="178ea-120">NOTES</span></span>

## <span data-ttu-id="178ea-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="178ea-121">RELATED LINKS</span></span>

[<span data-ttu-id="178ea-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="178ea-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="178ea-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="178ea-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="178ea-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="178ea-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="178ea-125">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="178ea-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


