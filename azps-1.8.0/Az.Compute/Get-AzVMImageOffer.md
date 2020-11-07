---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: 5ec6b8c01badec3677e77254128db215c0e41554
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836778"
---
# <span data-ttu-id="cd237-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="cd237-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="cd237-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd237-102">SYNOPSIS</span></span>
<span data-ttu-id="cd237-103">Beolvassa a VMImage kínálati típust.</span><span class="sxs-lookup"><span data-stu-id="cd237-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="cd237-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd237-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd237-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd237-105">DESCRIPTION</span></span>
<span data-ttu-id="cd237-106">A **Get-AzVMImageOffer** parancsmag a VMImage ajánlatok típusait kapja.</span><span class="sxs-lookup"><span data-stu-id="cd237-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="cd237-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd237-107">EXAMPLES</span></span>

### <span data-ttu-id="cd237-108">1. példa: ajánlati típusok beszerzése Publisherhez</span><span class="sxs-lookup"><span data-stu-id="cd237-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="cd237-109">Ez a parancs a közép-amerikai régióban a megadott közzétevőhöz tartozó ajánlati típusokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cd237-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="cd237-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd237-110">PARAMETERS</span></span>

### <span data-ttu-id="cd237-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd237-111">-DefaultProfile</span></span>
<span data-ttu-id="cd237-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd237-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd237-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="cd237-113">-Location</span></span>
<span data-ttu-id="cd237-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd237-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="cd237-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="cd237-115">-PublisherName</span></span>
<span data-ttu-id="cd237-116">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd237-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="cd237-117">Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cd237-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="cd237-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd237-118">CommonParameters</span></span>
<span data-ttu-id="cd237-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd237-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd237-120">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cd237-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd237-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd237-121">INPUTS</span></span>

### <span data-ttu-id="cd237-122">System. String</span><span class="sxs-lookup"><span data-stu-id="cd237-122">System.String</span></span>

## <span data-ttu-id="cd237-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd237-123">OUTPUTS</span></span>

### <span data-ttu-id="cd237-124">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="cd237-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="cd237-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd237-125">NOTES</span></span>

## <span data-ttu-id="cd237-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd237-126">RELATED LINKS</span></span>

[<span data-ttu-id="cd237-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="cd237-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="cd237-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="cd237-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="cd237-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="cd237-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="cd237-130">Mentés-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="cd237-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


