---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5131a9ea24ea14114c9a4d5f5600bbe190499f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497504"
---
# <span data-ttu-id="579d5-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="579d5-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="579d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="579d5-102">SYNOPSIS</span></span>
<span data-ttu-id="579d5-103">Megkapja a VMImage SKU-ot.</span><span class="sxs-lookup"><span data-stu-id="579d5-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="579d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="579d5-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="579d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="579d5-105">DESCRIPTION</span></span>
<span data-ttu-id="579d5-106">A **Get-AzureRmVMImageSku** parancsmag VMImage SKU-t kap.</span><span class="sxs-lookup"><span data-stu-id="579d5-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="579d5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="579d5-107">EXAMPLES</span></span>

### <span data-ttu-id="579d5-108">Példa 1: VMImage SKU beszerzése</span><span class="sxs-lookup"><span data-stu-id="579d5-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="579d5-109">Ez a parancs a megadott közzétevőhöz és ajánlathoz kapja a SKU-t.</span><span class="sxs-lookup"><span data-stu-id="579d5-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="579d5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="579d5-110">PARAMETERS</span></span>

### <span data-ttu-id="579d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579d5-111">-DefaultProfile</span></span>
<span data-ttu-id="579d5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="579d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="579d5-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="579d5-113">-Location</span></span>
<span data-ttu-id="579d5-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="579d5-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="579d5-115">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="579d5-115">-Offer</span></span>
<span data-ttu-id="579d5-116">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="579d5-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="579d5-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="579d5-117">-PublisherName</span></span>
<span data-ttu-id="579d5-118">A VMImage közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="579d5-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="579d5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579d5-119">CommonParameters</span></span>
<span data-ttu-id="579d5-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="579d5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579d5-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="579d5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579d5-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="579d5-122">INPUTS</span></span>

### <span data-ttu-id="579d5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="579d5-123">System.String</span></span>

## <span data-ttu-id="579d5-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="579d5-124">OUTPUTS</span></span>

### <span data-ttu-id="579d5-125">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="579d5-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="579d5-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="579d5-126">NOTES</span></span>

## <span data-ttu-id="579d5-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="579d5-127">RELATED LINKS</span></span>

[<span data-ttu-id="579d5-128">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="579d5-128">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="579d5-129">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="579d5-129">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="579d5-130">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="579d5-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="579d5-131">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="579d5-131">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


