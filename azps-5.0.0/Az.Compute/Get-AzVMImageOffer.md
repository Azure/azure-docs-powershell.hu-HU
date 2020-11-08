---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187630"
---
# <span data-ttu-id="32fec-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="32fec-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="32fec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32fec-102">SYNOPSIS</span></span>
<span data-ttu-id="32fec-103">Beolvassa a VMImage kínálati típust.</span><span class="sxs-lookup"><span data-stu-id="32fec-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="32fec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32fec-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32fec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32fec-105">DESCRIPTION</span></span>
<span data-ttu-id="32fec-106">A **Get-AzVMImageOffer** parancsmag a VMImage ajánlatok típusait kapja.</span><span class="sxs-lookup"><span data-stu-id="32fec-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="32fec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="32fec-107">EXAMPLES</span></span>

### <span data-ttu-id="32fec-108">1. példa: ajánlati típusok beszerzése Publisherhez</span><span class="sxs-lookup"><span data-stu-id="32fec-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="32fec-109">Ez a parancs a közép-amerikai régióban a megadott közzétevőhöz tartozó ajánlati típusokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="32fec-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="32fec-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32fec-110">PARAMETERS</span></span>

### <span data-ttu-id="32fec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32fec-111">-DefaultProfile</span></span>
<span data-ttu-id="32fec-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32fec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32fec-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="32fec-113">-Location</span></span>
<span data-ttu-id="32fec-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32fec-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="32fec-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="32fec-115">-PublisherName</span></span>
<span data-ttu-id="32fec-116">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32fec-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="32fec-117">Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="32fec-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="32fec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fec-118">CommonParameters</span></span>
<span data-ttu-id="32fec-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32fec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fec-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="32fec-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fec-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32fec-121">INPUTS</span></span>

### <span data-ttu-id="32fec-122">System. String</span><span class="sxs-lookup"><span data-stu-id="32fec-122">System.String</span></span>

## <span data-ttu-id="32fec-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32fec-123">OUTPUTS</span></span>

### <span data-ttu-id="32fec-124">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="32fec-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="32fec-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32fec-125">NOTES</span></span>

## <span data-ttu-id="32fec-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32fec-126">RELATED LINKS</span></span>

[<span data-ttu-id="32fec-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="32fec-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="32fec-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="32fec-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="32fec-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="32fec-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="32fec-130">Mentés-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="32fec-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)

