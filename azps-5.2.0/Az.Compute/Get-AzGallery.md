---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332789"
---
# <span data-ttu-id="c1455-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="c1455-101">Get-AzGallery</span></span>

## <span data-ttu-id="c1455-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1455-102">SYNOPSIS</span></span>
<span data-ttu-id="c1455-103">Get or list galleries.</span><span class="sxs-lookup"><span data-stu-id="c1455-103">Get or list galleries.</span></span>

## <span data-ttu-id="c1455-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c1455-104">SYNTAX</span></span>

### <span data-ttu-id="c1455-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1455-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1455-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c1455-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1455-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c1455-107">DESCRIPTION</span></span>
<span data-ttu-id="c1455-108">Get or list galleries.</span><span class="sxs-lookup"><span data-stu-id="c1455-108">Get or list galleries.</span></span>

## <span data-ttu-id="c1455-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c1455-109">EXAMPLES</span></span>

### <span data-ttu-id="c1455-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c1455-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="c1455-111">Gyűjtemény 1</span><span class="sxs-lookup"><span data-stu-id="c1455-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="c1455-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c1455-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="c1455-113">Szerezze be az összes tárat az rg1-ben.</span><span class="sxs-lookup"><span data-stu-id="c1455-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="c1455-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c1455-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="c1455-115">Az előfizetés összes galériájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="c1455-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="c1455-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="c1455-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="c1455-117">Szerezze be az előfizetés összes gyűjteményét, amely a "gyűjtemény" kezdetével kezdődik.</span><span class="sxs-lookup"><span data-stu-id="c1455-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="c1455-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1455-118">PARAMETERS</span></span>

### <span data-ttu-id="c1455-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1455-119">-DefaultProfile</span></span>
<span data-ttu-id="c1455-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1455-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1455-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c1455-121">-Name</span></span>
<span data-ttu-id="c1455-122">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="c1455-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c1455-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1455-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1455-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c1455-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c1455-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1455-125">-ResourceId</span></span>
<span data-ttu-id="c1455-126">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c1455-126">The resource id for Gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1455-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1455-127">CommonParameters</span></span>
<span data-ttu-id="c1455-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1455-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1455-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1455-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1455-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1455-130">INPUTS</span></span>

### <span data-ttu-id="c1455-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c1455-131">System.String</span></span>

## <span data-ttu-id="c1455-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1455-132">OUTPUTS</span></span>

### <span data-ttu-id="c1455-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="c1455-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="c1455-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c1455-134">NOTES</span></span>

## <span data-ttu-id="c1455-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1455-135">RELATED LINKS</span></span>
