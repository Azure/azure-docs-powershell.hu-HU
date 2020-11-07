---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: ebe1720154c45b08eb84cfe6c1ee4e339859e5fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667436"
---
# <span data-ttu-id="5fba8-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5fba8-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="5fba8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fba8-102">SYNOPSIS</span></span>
<span data-ttu-id="5fba8-103">Az Azure-bővítmény minden verziójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="5fba8-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="5fba8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fba8-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fba8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fba8-105">DESCRIPTION</span></span>
<span data-ttu-id="5fba8-106">A **Get-AzVMExtensionImage** parancsmag az Azure-bővítmények minden verzióját bekapja.</span><span class="sxs-lookup"><span data-stu-id="5fba8-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="5fba8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5fba8-107">EXAMPLES</span></span>

### <span data-ttu-id="5fba8-108">Példa 1: a kiterjesztési kép verziószámának beszerzése</span><span class="sxs-lookup"><span data-stu-id="5fba8-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="5fba8-109">Ez a parancs a megadott helyen, a Publisherben és a Type (kiterjesztés) kép összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="5fba8-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="5fba8-110">2. példa: a kiterjesztési kép verziószámának beszerzése a verzióval való szűréssel</span><span class="sxs-lookup"><span data-stu-id="5fba8-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="5fba8-111">Ez a parancs a 12-es verzióval kezdődően megadott helyen, a Publisherben, a típusban és a verzióban lévő kiterjesztési kép összes verzióját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="5fba8-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="5fba8-112">3. példa: a kiterjesztési kép verziószámának beszerzése a verzióval való szűréssel</span><span class="sxs-lookup"><span data-stu-id="5fba8-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="5fba8-113">Ez a parancs a megadott helyen, Publisherben, típusban és verzióban lévő kiterjesztési kép összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="5fba8-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="5fba8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fba8-114">PARAMETERS</span></span>

### <span data-ttu-id="5fba8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fba8-115">-DefaultProfile</span></span>
<span data-ttu-id="5fba8-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fba8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fba8-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="5fba8-117">-FilterExpression</span></span>
<span data-ttu-id="5fba8-118">A szűrő kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fba8-118">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="5fba8-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="5fba8-119">-Location</span></span>
<span data-ttu-id="5fba8-120">A kiterjesztés helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fba8-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="5fba8-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="5fba8-121">-PublisherName</span></span>
<span data-ttu-id="5fba8-122">A bővítmények közzétevői nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fba8-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="5fba8-123">A bővítmények közzétevőjét az Get-AzVMImagePublisher parancsmag használatával kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="5fba8-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="5fba8-124">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="5fba8-124">-Type</span></span>
<span data-ttu-id="5fba8-125">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fba8-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="5fba8-126">A bővítmények típusának beolvasásához használja az Get-AzVMExtensionImageType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5fba8-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="5fba8-127">-Verzió</span><span class="sxs-lookup"><span data-stu-id="5fba8-127">-Version</span></span>
<span data-ttu-id="5fba8-128">Annak a bővítménynek a verziószámát adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="5fba8-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5fba8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fba8-129">CommonParameters</span></span>
<span data-ttu-id="5fba8-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fba8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fba8-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5fba8-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fba8-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fba8-132">INPUTS</span></span>

### <span data-ttu-id="5fba8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5fba8-133">System.String</span></span>

## <span data-ttu-id="5fba8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fba8-134">OUTPUTS</span></span>

### <span data-ttu-id="5fba8-135">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5fba8-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="5fba8-136">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="5fba8-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="5fba8-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fba8-137">NOTES</span></span>

## <span data-ttu-id="5fba8-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fba8-138">RELATED LINKS</span></span>

[<span data-ttu-id="5fba8-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="5fba8-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="5fba8-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5fba8-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="5fba8-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="5fba8-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


