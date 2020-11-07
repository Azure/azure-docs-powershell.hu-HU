---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimage
schema: 2.0.0
ms.openlocfilehash: ccb48064bb2d6b91801a58ecfa9d229a748889a8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849401"
---
# <span data-ttu-id="1f784-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1f784-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="1f784-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f784-102">SYNOPSIS</span></span>
<span data-ttu-id="1f784-103">Az Azure-bővítmény minden verziójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="1f784-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f784-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f784-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f784-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f784-105">DESCRIPTION</span></span>
<span data-ttu-id="1f784-106">A **Get-AzureRmVMExtensionImage** parancsmag az Azure-bővítmények minden verzióját bekapja.</span><span class="sxs-lookup"><span data-stu-id="1f784-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="1f784-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1f784-107">EXAMPLES</span></span>

### <span data-ttu-id="1f784-108">Példa 1: a kiterjesztési kép verziószámának beszerzése</span><span class="sxs-lookup"><span data-stu-id="1f784-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="1f784-109">Ez a parancs a megadott helyen, a Publisherben és a Type (kiterjesztés) kép összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="1f784-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="1f784-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f784-110">PARAMETERS</span></span>

### <span data-ttu-id="1f784-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f784-111">-DefaultProfile</span></span>
<span data-ttu-id="1f784-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f784-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f784-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="1f784-113">-FilterExpression</span></span>
<span data-ttu-id="1f784-114">A szűrő kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f784-114">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="1f784-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="1f784-115">-Location</span></span>
<span data-ttu-id="1f784-116">A kiterjesztés helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f784-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="1f784-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="1f784-117">-PublisherName</span></span>
<span data-ttu-id="1f784-118">A bővítmények közzétevői nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f784-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="1f784-119">A bővítmények közzétevőjét az Get-AzureRmVMImagePublisher parancsmag használatával kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="1f784-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="1f784-120">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="1f784-120">-Type</span></span>
<span data-ttu-id="1f784-121">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f784-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="1f784-122">A bővítmények típusának beolvasásához használja az Get-AzureRmVMExtensionImageType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1f784-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="1f784-123">-Verzió</span><span class="sxs-lookup"><span data-stu-id="1f784-123">-Version</span></span>
<span data-ttu-id="1f784-124">Annak a bővítménynek a verziószámát adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="1f784-124">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1f784-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f784-125">CommonParameters</span></span>
<span data-ttu-id="1f784-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f784-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f784-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f784-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f784-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f784-128">INPUTS</span></span>

### <span data-ttu-id="1f784-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="1f784-129">None</span></span>
<span data-ttu-id="1f784-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1f784-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f784-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f784-131">OUTPUTS</span></span>

### <span data-ttu-id="1f784-132">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1f784-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="1f784-133">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="1f784-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="1f784-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f784-134">NOTES</span></span>

## <span data-ttu-id="1f784-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f784-135">RELATED LINKS</span></span>

[<span data-ttu-id="1f784-136">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="1f784-136">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="1f784-137">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1f784-137">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="1f784-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1f784-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


