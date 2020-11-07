---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 1864b4c2dcbd4b3d9934ffb15c54fae18082c920
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844593"
---
# <span data-ttu-id="ac360-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ac360-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="ac360-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac360-102">SYNOPSIS</span></span>
<span data-ttu-id="ac360-103">Az Azure-bővítmény minden verziójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="ac360-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="ac360-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac360-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac360-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac360-105">DESCRIPTION</span></span>
<span data-ttu-id="ac360-106">A **Get-AzVMExtensionImage** parancsmag az Azure-bővítmények minden verzióját bekapja.</span><span class="sxs-lookup"><span data-stu-id="ac360-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="ac360-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ac360-107">EXAMPLES</span></span>

### <span data-ttu-id="ac360-108">Példa 1: a kiterjesztési kép verziószámának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ac360-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="ac360-109">Ez a parancs a megadott helyen, a Publisherben és a Type (kiterjesztés) kép összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="ac360-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="ac360-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac360-110">PARAMETERS</span></span>

### <span data-ttu-id="ac360-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac360-111">-DefaultProfile</span></span>
<span data-ttu-id="ac360-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac360-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac360-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="ac360-113">-FilterExpression</span></span>
<span data-ttu-id="ac360-114">A szűrő kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac360-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac360-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="ac360-115">-Location</span></span>
<span data-ttu-id="ac360-116">A kiterjesztés helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac360-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="ac360-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="ac360-117">-PublisherName</span></span>
<span data-ttu-id="ac360-118">A bővítmények közzétevői nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac360-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="ac360-119">A bővítmények közzétevőjét az Get-AzVMImagePublisher parancsmag használatával kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="ac360-119">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="ac360-120">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="ac360-120">-Type</span></span>
<span data-ttu-id="ac360-121">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac360-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="ac360-122">A bővítmények típusának beolvasásához használja az Get-AzVMExtensionImageType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ac360-122">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="ac360-123">-Verzió</span><span class="sxs-lookup"><span data-stu-id="ac360-123">-Version</span></span>
<span data-ttu-id="ac360-124">Annak a bővítménynek a verziószámát adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="ac360-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac360-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac360-125">CommonParameters</span></span>
<span data-ttu-id="ac360-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac360-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac360-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac360-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac360-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac360-128">INPUTS</span></span>

### <span data-ttu-id="ac360-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="ac360-129">None</span></span>
<span data-ttu-id="ac360-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ac360-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac360-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac360-131">OUTPUTS</span></span>

### <span data-ttu-id="ac360-132">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ac360-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="ac360-133">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="ac360-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="ac360-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac360-134">NOTES</span></span>

## <span data-ttu-id="ac360-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac360-135">RELATED LINKS</span></span>

[<span data-ttu-id="ac360-136">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="ac360-136">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="ac360-137">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ac360-137">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="ac360-138">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ac360-138">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


