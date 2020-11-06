---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
ms.openlocfilehash: cdb703144daa6f9abd62aee41eaad94b2cfa50e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494144"
---
# <span data-ttu-id="29597-101">Get-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="29597-101">Get-AzureRmGallery</span></span>

## <span data-ttu-id="29597-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29597-102">SYNOPSIS</span></span>
<span data-ttu-id="29597-103">Beolvashatja vagy listázhatja a gyűjteményeket.</span><span class="sxs-lookup"><span data-stu-id="29597-103">Get or list galleries.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29597-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29597-104">SYNTAX</span></span>

### <span data-ttu-id="29597-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29597-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGallery [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29597-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="29597-106">ResourceIdParameter</span></span>
```
Get-AzureRmGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29597-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="29597-107">DESCRIPTION</span></span>
<span data-ttu-id="29597-108">Beolvashatja vagy listázhatja a gyűjteményeket.</span><span class="sxs-lookup"><span data-stu-id="29597-108">Get or list galleries.</span></span>

## <span data-ttu-id="29597-109">Példák</span><span class="sxs-lookup"><span data-stu-id="29597-109">EXAMPLES</span></span>

### <span data-ttu-id="29597-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29597-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName

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

<span data-ttu-id="29597-111">A gyűjtemény beszerzése.</span><span class="sxs-lookup"><span data-stu-id="29597-111">Get the gallery.</span></span>

## <span data-ttu-id="29597-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29597-112">PARAMETERS</span></span>

### <span data-ttu-id="29597-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29597-113">-DefaultProfile</span></span>
<span data-ttu-id="29597-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29597-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29597-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29597-115">-Name</span></span>
<span data-ttu-id="29597-116">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="29597-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29597-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29597-117">-ResourceGroupName</span></span>
<span data-ttu-id="29597-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="29597-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29597-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29597-119">-ResourceId</span></span>
<span data-ttu-id="29597-120">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="29597-120">The resource id for Gallery</span></span>

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

### <span data-ttu-id="29597-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29597-121">CommonParameters</span></span>
<span data-ttu-id="29597-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29597-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29597-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29597-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29597-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29597-124">INPUTS</span></span>

### <span data-ttu-id="29597-125">System. String</span><span class="sxs-lookup"><span data-stu-id="29597-125">System.String</span></span>

### <span data-ttu-id="29597-126">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="29597-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="29597-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29597-127">OUTPUTS</span></span>

### <span data-ttu-id="29597-128">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="29597-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="29597-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29597-129">NOTES</span></span>

## <span data-ttu-id="29597-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29597-130">RELATED LINKS</span></span>
