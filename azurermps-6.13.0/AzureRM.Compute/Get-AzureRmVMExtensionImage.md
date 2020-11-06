---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 4a348d4e3aa6089ae3e8f3c0bdf871156111ce93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505771"
---
# <span data-ttu-id="c7c5a-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c7c5a-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="c7c5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c5a-103">Az Azure-bővítmény minden verziójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="c7c5a-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7c5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7c5a-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7c5a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7c5a-105">DESCRIPTION</span></span>
<span data-ttu-id="c7c5a-106">A **Get-AzureRmVMExtensionImage** parancsmag az Azure-bővítmények minden verzióját bekapja.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="c7c5a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c7c5a-107">EXAMPLES</span></span>

### <span data-ttu-id="c7c5a-108">Példa 1: a kiterjesztési kép verziószámának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c7c5a-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="c7c5a-109">Ez a parancs a megadott helyen, a Publisherben és a Type (kiterjesztés) kép összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="c7c5a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7c5a-110">PARAMETERS</span></span>

### <span data-ttu-id="c7c5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c5a-111">-DefaultProfile</span></span>
<span data-ttu-id="c7c5a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7c5a-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="c7c5a-113">-FilterExpression</span></span>
<span data-ttu-id="c7c5a-114">A szűrő kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-114">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c5a-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="c7c5a-115">-Location</span></span>
<span data-ttu-id="c7c5a-116">A kiterjesztés helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="c7c5a-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c7c5a-117">-PublisherName</span></span>
<span data-ttu-id="c7c5a-118">A bővítmények közzétevői nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="c7c5a-119">A bővítmények közzétevőjét az Get-AzureRmVMImagePublisher parancsmag használatával kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="c7c5a-120">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="c7c5a-120">-Type</span></span>
<span data-ttu-id="c7c5a-121">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="c7c5a-122">A bővítmények típusának beolvasásához használja az Get-AzureRmVMExtensionImageType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="c7c5a-123">-Verzió</span><span class="sxs-lookup"><span data-stu-id="c7c5a-123">-Version</span></span>
<span data-ttu-id="c7c5a-124">Annak a bővítménynek a verziószámát adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7c5a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c5a-125">CommonParameters</span></span>
<span data-ttu-id="c7c5a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7c5a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c5a-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c5a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c5a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7c5a-128">INPUTS</span></span>

### <span data-ttu-id="c7c5a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c7c5a-129">System.String</span></span>

## <span data-ttu-id="c7c5a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7c5a-130">OUTPUTS</span></span>

### <span data-ttu-id="c7c5a-131">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c7c5a-131">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="c7c5a-132">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="c7c5a-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="c7c5a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7c5a-133">NOTES</span></span>

## <span data-ttu-id="c7c5a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7c5a-134">RELATED LINKS</span></span>

[<span data-ttu-id="c7c5a-135">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="c7c5a-135">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="c7c5a-136">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c7c5a-136">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="c7c5a-137">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c7c5a-137">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


