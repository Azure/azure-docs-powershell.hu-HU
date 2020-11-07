---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: eb56542d02498a0d4b8aa4176c77d75ab6ad4da6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844581"
---
# <span data-ttu-id="a4054-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a4054-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="a4054-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4054-102">SYNOPSIS</span></span>
<span data-ttu-id="a4054-103">Beolvassa a VMImage kínálati típust.</span><span class="sxs-lookup"><span data-stu-id="a4054-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="a4054-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4054-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4054-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4054-105">DESCRIPTION</span></span>
<span data-ttu-id="a4054-106">A **Get-AzVMImageOffer** parancsmag a VMImage ajánlatok típusait kapja.</span><span class="sxs-lookup"><span data-stu-id="a4054-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="a4054-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4054-107">EXAMPLES</span></span>

### <span data-ttu-id="a4054-108">1. példa: ajánlati típusok beszerzése Publisherhez</span><span class="sxs-lookup"><span data-stu-id="a4054-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="a4054-109">Ez a parancs a közép-amerikai régióban a megadott közzétevőhöz tartozó ajánlati típusokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4054-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="a4054-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4054-110">PARAMETERS</span></span>

### <span data-ttu-id="a4054-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4054-111">-DefaultProfile</span></span>
<span data-ttu-id="a4054-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4054-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4054-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="a4054-113">-Location</span></span>
<span data-ttu-id="a4054-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4054-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="a4054-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a4054-115">-PublisherName</span></span>
<span data-ttu-id="a4054-116">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4054-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="a4054-117">Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a4054-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="a4054-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4054-118">CommonParameters</span></span>
<span data-ttu-id="a4054-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4054-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4054-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4054-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4054-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4054-121">INPUTS</span></span>

### <span data-ttu-id="a4054-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="a4054-122">None</span></span>
<span data-ttu-id="a4054-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a4054-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4054-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4054-124">OUTPUTS</span></span>

### <span data-ttu-id="a4054-125">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="a4054-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="a4054-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4054-126">NOTES</span></span>

## <span data-ttu-id="a4054-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4054-127">RELATED LINKS</span></span>

[<span data-ttu-id="a4054-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a4054-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="a4054-129">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a4054-129">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a4054-130">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a4054-130">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="a4054-131">Mentés-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a4054-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


