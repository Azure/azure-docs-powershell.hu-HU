---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: 33c833004269e26204d97b9993db93aac7389642
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667478"
---
# <span data-ttu-id="5dede-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="5dede-101">Get-AzGallery</span></span>

## <span data-ttu-id="5dede-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5dede-102">SYNOPSIS</span></span>
<span data-ttu-id="5dede-103">Beolvashatja vagy listázhatja a gyűjteményeket.</span><span class="sxs-lookup"><span data-stu-id="5dede-103">Get or list galleries.</span></span>

## <span data-ttu-id="5dede-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5dede-104">SYNTAX</span></span>

### <span data-ttu-id="5dede-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5dede-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5dede-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5dede-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dede-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5dede-107">DESCRIPTION</span></span>
<span data-ttu-id="5dede-108">Beolvashatja vagy listázhatja a gyűjteményeket.</span><span class="sxs-lookup"><span data-stu-id="5dede-108">Get or list galleries.</span></span>

## <span data-ttu-id="5dede-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5dede-109">EXAMPLES</span></span>

### <span data-ttu-id="5dede-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5dede-110">Example 1</span></span>
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

<span data-ttu-id="5dede-111">A "gallery1" gyűjtemény beszerzése</span><span class="sxs-lookup"><span data-stu-id="5dede-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="5dede-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="5dede-112">Example 2</span></span>
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

<span data-ttu-id="5dede-113">Az összes gyűjtemény beszerzése a rg1.</span><span class="sxs-lookup"><span data-stu-id="5dede-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="5dede-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="5dede-114">Example 3</span></span>
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

<span data-ttu-id="5dede-115">Az összes gyűjtemény beszerzése előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="5dede-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="5dede-116">4. példa</span><span class="sxs-lookup"><span data-stu-id="5dede-116">Example 4</span></span>
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

<span data-ttu-id="5dede-117">A "gyűjtemény" kezdetű előfizetésben az összes gyűjtemény beolvasása</span><span class="sxs-lookup"><span data-stu-id="5dede-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="5dede-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5dede-118">PARAMETERS</span></span>

### <span data-ttu-id="5dede-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dede-119">-DefaultProfile</span></span>
<span data-ttu-id="5dede-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5dede-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dede-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5dede-121">-Name</span></span>
<span data-ttu-id="5dede-122">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="5dede-122">The name of the gallery.</span></span>

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

### <span data-ttu-id="5dede-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dede-123">-ResourceGroupName</span></span>
<span data-ttu-id="5dede-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5dede-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5dede-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5dede-125">-ResourceId</span></span>
<span data-ttu-id="5dede-126">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5dede-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="5dede-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dede-127">CommonParameters</span></span>
<span data-ttu-id="5dede-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5dede-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dede-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5dede-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dede-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5dede-130">INPUTS</span></span>

### <span data-ttu-id="5dede-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5dede-131">System.String</span></span>

## <span data-ttu-id="5dede-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5dede-132">OUTPUTS</span></span>

### <span data-ttu-id="5dede-133">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="5dede-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="5dede-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5dede-134">NOTES</span></span>

## <span data-ttu-id="5dede-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5dede-135">RELATED LINKS</span></span>
