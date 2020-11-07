---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 6355ce5cea881f66473ca8d541585187a79fe23e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836776"
---
# <span data-ttu-id="6cba4-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="6cba4-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="6cba4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cba4-102">SYNOPSIS</span></span>
<span data-ttu-id="6cba4-103">Megkapja a VMImage SKU-ot.</span><span class="sxs-lookup"><span data-stu-id="6cba4-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="6cba4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cba4-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cba4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cba4-105">DESCRIPTION</span></span>
<span data-ttu-id="6cba4-106">A **Get-AzVMImageSku** parancsmag VMImage SKU-t kap.</span><span class="sxs-lookup"><span data-stu-id="6cba4-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="6cba4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6cba4-107">EXAMPLES</span></span>

### <span data-ttu-id="6cba4-108">Példa 1: VMImage SKU beszerzése</span><span class="sxs-lookup"><span data-stu-id="6cba4-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="6cba4-109">Ez a parancs a megadott közzétevőhöz és ajánlathoz kapja a SKU-t.</span><span class="sxs-lookup"><span data-stu-id="6cba4-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="6cba4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cba4-110">PARAMETERS</span></span>

### <span data-ttu-id="6cba4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cba4-111">-DefaultProfile</span></span>
<span data-ttu-id="6cba4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cba4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cba4-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="6cba4-113">-Location</span></span>
<span data-ttu-id="6cba4-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cba4-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="6cba4-115">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="6cba4-115">-Offer</span></span>
<span data-ttu-id="6cba4-116">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cba4-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="6cba4-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6cba4-117">-PublisherName</span></span>
<span data-ttu-id="6cba4-118">A VMImage közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cba4-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="6cba4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cba4-119">CommonParameters</span></span>
<span data-ttu-id="6cba4-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cba4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cba4-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6cba4-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cba4-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cba4-122">INPUTS</span></span>

### <span data-ttu-id="6cba4-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6cba4-123">System.String</span></span>

## <span data-ttu-id="6cba4-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cba4-124">OUTPUTS</span></span>

### <span data-ttu-id="6cba4-125">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="6cba4-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="6cba4-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cba4-126">NOTES</span></span>

## <span data-ttu-id="6cba4-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cba4-127">RELATED LINKS</span></span>

[<span data-ttu-id="6cba4-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="6cba4-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="6cba4-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="6cba4-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="6cba4-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6cba4-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="6cba4-131">Mentés-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="6cba4-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


