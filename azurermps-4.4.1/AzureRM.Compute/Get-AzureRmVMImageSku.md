---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5bdce17c963cc2529fab3f328b9ab64cc549e1d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680907"
---
# <span data-ttu-id="3006e-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="3006e-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="3006e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3006e-102">SYNOPSIS</span></span>
<span data-ttu-id="3006e-103">Megkapja a VMImage SKU-ot.</span><span class="sxs-lookup"><span data-stu-id="3006e-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3006e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3006e-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3006e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3006e-105">DESCRIPTION</span></span>
<span data-ttu-id="3006e-106">A **Get-AzureRmVMImageSku** parancsmag VMImage SKU-t kap.</span><span class="sxs-lookup"><span data-stu-id="3006e-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="3006e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3006e-107">EXAMPLES</span></span>

### <span data-ttu-id="3006e-108">Példa 1: VMImage SKU beszerzése</span><span class="sxs-lookup"><span data-stu-id="3006e-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="3006e-109">Ez a parancs a megadott közzétevőhöz és ajánlathoz kapja a SKU-t.</span><span class="sxs-lookup"><span data-stu-id="3006e-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="3006e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3006e-110">PARAMETERS</span></span>

### <span data-ttu-id="3006e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3006e-111">-DefaultProfile</span></span>
<span data-ttu-id="3006e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3006e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3006e-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="3006e-113">-Location</span></span>
<span data-ttu-id="3006e-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3006e-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="3006e-115">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="3006e-115">-Offer</span></span>
<span data-ttu-id="3006e-116">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3006e-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="3006e-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3006e-117">-PublisherName</span></span>
<span data-ttu-id="3006e-118">A VMImage közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3006e-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="3006e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3006e-119">CommonParameters</span></span>
<span data-ttu-id="3006e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3006e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3006e-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3006e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3006e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3006e-122">INPUTS</span></span>

## <span data-ttu-id="3006e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3006e-123">OUTPUTS</span></span>

## <span data-ttu-id="3006e-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3006e-124">NOTES</span></span>

## <span data-ttu-id="3006e-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3006e-125">RELATED LINKS</span></span>

[<span data-ttu-id="3006e-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3006e-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="3006e-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="3006e-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="3006e-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3006e-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="3006e-129">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3006e-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


