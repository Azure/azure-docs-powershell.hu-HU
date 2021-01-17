---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477786"
---
# <span data-ttu-id="b0ebf-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="b0ebf-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="b0ebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="b0ebf-103">VMImage-SKUs-t kap.</span><span class="sxs-lookup"><span data-stu-id="b0ebf-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="b0ebf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0ebf-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0ebf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0ebf-105">DESCRIPTION</span></span>
<span data-ttu-id="b0ebf-106">A **Get-AzVMImageSku** parancsmag VMImage termékváltozatokat kap.</span><span class="sxs-lookup"><span data-stu-id="b0ebf-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="b0ebf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0ebf-107">EXAMPLES</span></span>

### <span data-ttu-id="b0ebf-108">1. példa: VMImage-SKUs-k lekérte</span><span class="sxs-lookup"><span data-stu-id="b0ebf-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="b0ebf-109">Ez a parancs a megadott közzétevő és ajánlat SKUs-ját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b0ebf-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="b0ebf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0ebf-110">PARAMETERS</span></span>

### <span data-ttu-id="b0ebf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0ebf-111">-DefaultProfile</span></span>
<span data-ttu-id="b0ebf-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0ebf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0ebf-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b0ebf-113">-Location</span></span>
<span data-ttu-id="b0ebf-114">A VMImage helyének megadása.</span><span class="sxs-lookup"><span data-stu-id="b0ebf-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="b0ebf-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="b0ebf-115">-Offer</span></span>
<span data-ttu-id="b0ebf-116">A VMImage-ajánlat típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b0ebf-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="b0ebf-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b0ebf-117">-PublisherName</span></span>
<span data-ttu-id="b0ebf-118">A VMImage-fájl közzétevője.</span><span class="sxs-lookup"><span data-stu-id="b0ebf-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="b0ebf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ebf-119">CommonParameters</span></span>
<span data-ttu-id="b0ebf-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0ebf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ebf-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0ebf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ebf-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0ebf-122">INPUTS</span></span>

### <span data-ttu-id="b0ebf-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b0ebf-123">System.String</span></span>

## <span data-ttu-id="b0ebf-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0ebf-124">OUTPUTS</span></span>

### <span data-ttu-id="b0ebf-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="b0ebf-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="b0ebf-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0ebf-126">NOTES</span></span>

## <span data-ttu-id="b0ebf-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0ebf-127">RELATED LINKS</span></span>

[<span data-ttu-id="b0ebf-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b0ebf-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="b0ebf-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="b0ebf-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="b0ebf-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b0ebf-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="b0ebf-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b0ebf-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


