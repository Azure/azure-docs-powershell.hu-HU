---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 83d54f9c0b47db5dc718d273b1a1760ab319a666
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480858"
---
# <span data-ttu-id="d5159-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d5159-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="d5159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5159-102">SYNOPSIS</span></span>
<span data-ttu-id="d5159-103">Egy Azure-bővítmény összes verzióját beveszi.</span><span class="sxs-lookup"><span data-stu-id="d5159-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="d5159-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d5159-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5159-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d5159-105">DESCRIPTION</span></span>
<span data-ttu-id="d5159-106">A **Get-AzVMExtensionImage parancsmag az Azure-bővítmény** összes verzióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="d5159-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="d5159-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d5159-107">EXAMPLES</span></span>

### <span data-ttu-id="d5159-108">1. példa: Bővítménykép verzióinak lekérte</span><span class="sxs-lookup"><span data-stu-id="d5159-108">Example 1: Get the versions of an extension image</span></span>
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

<span data-ttu-id="d5159-109">Ez a parancs a bővítménykép összes verzióját lekérte a megadott helyre, közzétevőre és típusra.</span><span class="sxs-lookup"><span data-stu-id="d5159-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="d5159-110">2. példa: Bővítménykép verzióinak lekérte a verzión keresztüli szűrést</span><span class="sxs-lookup"><span data-stu-id="d5159-110">Example 2: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="d5159-111">Ez a parancs a bővítménykép összes verzióját beveszi a megadott helyre, közzétevőre, típusra és verzióra a 12-estől kezdve.</span><span class="sxs-lookup"><span data-stu-id="d5159-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="d5159-112">3. példa: Bővítménykép verzióinak lekérte a verzión keresztüli szűrőt</span><span class="sxs-lookup"><span data-stu-id="d5159-112">Example 3: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="d5159-113">Ez a parancs a bővítménykép összes verzióját lekérte a megadott helyre, közzétevőre, típusra és verzióra.</span><span class="sxs-lookup"><span data-stu-id="d5159-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="d5159-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5159-114">PARAMETERS</span></span>

### <span data-ttu-id="d5159-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5159-115">-DefaultProfile</span></span>
<span data-ttu-id="d5159-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5159-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5159-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="d5159-117">-FilterExpression</span></span>
<span data-ttu-id="d5159-118">Egy szűrőkifejezést ad meg.</span><span class="sxs-lookup"><span data-stu-id="d5159-118">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="d5159-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d5159-119">-Location</span></span>
<span data-ttu-id="d5159-120">A bővítmény helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d5159-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="d5159-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="d5159-121">-PublisherName</span></span>
<span data-ttu-id="d5159-122">A bővítmény közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5159-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="d5159-123">Bővítménykiadó beszerzéséhez használja a Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d5159-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="d5159-124">-Type</span><span class="sxs-lookup"><span data-stu-id="d5159-124">-Type</span></span>
<span data-ttu-id="d5159-125">A bővítmény típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d5159-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="d5159-126">Bővítménytípus beszerzéséhez használja a Get-AzVMExtensionImageType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d5159-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="d5159-127">-Version</span><span class="sxs-lookup"><span data-stu-id="d5159-127">-Version</span></span>
<span data-ttu-id="d5159-128">A parancsmag bővítményverzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5159-128">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d5159-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5159-129">CommonParameters</span></span>
<span data-ttu-id="d5159-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5159-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5159-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5159-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5159-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5159-132">INPUTS</span></span>

### <span data-ttu-id="d5159-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d5159-133">System.String</span></span>

## <span data-ttu-id="d5159-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5159-134">OUTPUTS</span></span>

### <span data-ttu-id="d5159-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d5159-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="d5159-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="d5159-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="d5159-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d5159-137">NOTES</span></span>

## <span data-ttu-id="d5159-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5159-138">RELATED LINKS</span></span>

[<span data-ttu-id="d5159-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="d5159-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="d5159-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d5159-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="d5159-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d5159-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


