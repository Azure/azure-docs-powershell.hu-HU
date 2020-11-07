---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: eb31437870a77e4af84bdcb94ffa4172d117c78d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680283"
---
# <span data-ttu-id="e371b-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e371b-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="e371b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e371b-102">SYNOPSIS</span></span>
<span data-ttu-id="e371b-103">Beolvassa a VMImage kínálati típust.</span><span class="sxs-lookup"><span data-stu-id="e371b-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e371b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e371b-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e371b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e371b-105">DESCRIPTION</span></span>
<span data-ttu-id="e371b-106">A **Get-AzureRmVMImageOffer** parancsmag a VMImage ajánlatok típusait kapja.</span><span class="sxs-lookup"><span data-stu-id="e371b-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="e371b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e371b-107">EXAMPLES</span></span>

### <span data-ttu-id="e371b-108">1. példa: ajánlati típusok beszerzése Publisherhez</span><span class="sxs-lookup"><span data-stu-id="e371b-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="e371b-109">Ez a parancs a közép-amerikai régióban a megadott közzétevőhöz tartozó ajánlati típusokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e371b-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="e371b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e371b-110">PARAMETERS</span></span>

### <span data-ttu-id="e371b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e371b-111">-DefaultProfile</span></span>
<span data-ttu-id="e371b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e371b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e371b-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="e371b-113">-Location</span></span>
<span data-ttu-id="e371b-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e371b-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="e371b-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="e371b-115">-PublisherName</span></span>
<span data-ttu-id="e371b-116">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e371b-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="e371b-117">Publisher beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e371b-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="e371b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e371b-118">CommonParameters</span></span>
<span data-ttu-id="e371b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e371b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e371b-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e371b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e371b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e371b-121">INPUTS</span></span>

## <span data-ttu-id="e371b-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e371b-122">OUTPUTS</span></span>

## <span data-ttu-id="e371b-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e371b-123">NOTES</span></span>

## <span data-ttu-id="e371b-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e371b-124">RELATED LINKS</span></span>

[<span data-ttu-id="e371b-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e371b-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="e371b-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e371b-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e371b-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e371b-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="e371b-128">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e371b-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


