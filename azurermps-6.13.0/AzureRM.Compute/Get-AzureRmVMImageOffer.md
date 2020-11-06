---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: 66c0355af202c5900fddc60c81e92f2851ddc1ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497515"
---
# <span data-ttu-id="7355a-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7355a-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="7355a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7355a-102">SYNOPSIS</span></span>
<span data-ttu-id="7355a-103">Beolvassa a VMImage kínálati típust.</span><span class="sxs-lookup"><span data-stu-id="7355a-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7355a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7355a-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7355a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7355a-105">DESCRIPTION</span></span>
<span data-ttu-id="7355a-106">A **Get-AzureRmVMImageOffer** parancsmag a VMImage ajánlatok típusait kapja.</span><span class="sxs-lookup"><span data-stu-id="7355a-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="7355a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7355a-107">EXAMPLES</span></span>

### <span data-ttu-id="7355a-108">1. példa: ajánlati típusok beszerzése Publisherhez</span><span class="sxs-lookup"><span data-stu-id="7355a-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="7355a-109">Ez a parancs a közép-amerikai régióban a megadott közzétevőhöz tartozó ajánlati típusokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7355a-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="7355a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7355a-110">PARAMETERS</span></span>

### <span data-ttu-id="7355a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7355a-111">-DefaultProfile</span></span>
<span data-ttu-id="7355a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7355a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7355a-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="7355a-113">-Location</span></span>
<span data-ttu-id="7355a-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7355a-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="7355a-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7355a-115">-PublisherName</span></span>
<span data-ttu-id="7355a-116">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7355a-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="7355a-117">Publisher beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7355a-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="7355a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7355a-118">CommonParameters</span></span>
<span data-ttu-id="7355a-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7355a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7355a-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7355a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7355a-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7355a-121">INPUTS</span></span>

### <span data-ttu-id="7355a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="7355a-122">System.String</span></span>

## <span data-ttu-id="7355a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7355a-123">OUTPUTS</span></span>

### <span data-ttu-id="7355a-124">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="7355a-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="7355a-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7355a-125">NOTES</span></span>

## <span data-ttu-id="7355a-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7355a-126">RELATED LINKS</span></span>

[<span data-ttu-id="7355a-127">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7355a-127">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="7355a-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7355a-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="7355a-129">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7355a-129">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="7355a-130">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7355a-130">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


