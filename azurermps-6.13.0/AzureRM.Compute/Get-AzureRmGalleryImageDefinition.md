---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 75d30165c5dc5d69eabd08e89ad2577df82f7ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494137"
---
# <span data-ttu-id="fbb2c-101">Get-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="fbb2c-101">Get-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="fbb2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbb2c-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb2c-103">Képdefiníciók beolvasása vagy listázása</span><span class="sxs-lookup"><span data-stu-id="fbb2c-103">Get or list gallery image definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbb2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbb2c-104">SYNTAX</span></span>

### <span data-ttu-id="fbb2c-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fbb2c-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbb2c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fbb2c-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbb2c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbb2c-107">DESCRIPTION</span></span>
<span data-ttu-id="fbb2c-108">Képdefiníciók beolvasása vagy listázása</span><span class="sxs-lookup"><span data-stu-id="fbb2c-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="fbb2c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fbb2c-109">EXAMPLES</span></span>

### <span data-ttu-id="fbb2c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fbb2c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image
```

<span data-ttu-id="fbb2c-111">A gyűjtemény képének definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="fbb2c-111">Get the gallery image definition.</span></span>

## <span data-ttu-id="fbb2c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbb2c-112">PARAMETERS</span></span>

### <span data-ttu-id="fbb2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb2c-113">-DefaultProfile</span></span>
<span data-ttu-id="fbb2c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbb2c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb2c-115">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="fbb2c-115">-GalleryName</span></span>
<span data-ttu-id="fbb2c-116">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="fbb2c-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb2c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fbb2c-117">-Name</span></span>
<span data-ttu-id="fbb2c-118">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="fbb2c-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb2c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb2c-119">-ResourceGroupName</span></span>
<span data-ttu-id="fbb2c-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fbb2c-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb2c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbb2c-121">-ResourceId</span></span>
<span data-ttu-id="fbb2c-122">A tár képdefiníciójának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fbb2c-122">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="fbb2c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb2c-123">CommonParameters</span></span>
<span data-ttu-id="fbb2c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbb2c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb2c-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb2c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb2c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbb2c-126">INPUTS</span></span>

### <span data-ttu-id="fbb2c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fbb2c-127">System.String</span></span>

## <span data-ttu-id="fbb2c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbb2c-128">OUTPUTS</span></span>

### <span data-ttu-id="fbb2c-129">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="fbb2c-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="fbb2c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbb2c-130">NOTES</span></span>

## <span data-ttu-id="fbb2c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbb2c-131">RELATED LINKS</span></span>
