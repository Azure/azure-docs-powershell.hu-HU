---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
ms.openlocfilehash: bff748b8c867b272208469d34229cc2724bc8610
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494136"
---
# <span data-ttu-id="d3531-101">Get-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d3531-101">Get-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="d3531-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3531-102">SYNOPSIS</span></span>
<span data-ttu-id="d3531-103">Beolvashatja vagy listázhatja a Képtár képverzióit.</span><span class="sxs-lookup"><span data-stu-id="d3531-103">Get or list gallery image versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3531-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3531-104">SYNTAX</span></span>

### <span data-ttu-id="d3531-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3531-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3531-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d3531-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3531-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3531-107">DESCRIPTION</span></span>
<span data-ttu-id="d3531-108">Beolvashatja vagy listázhatja a Képtár képverzióit.</span><span class="sxs-lookup"><span data-stu-id="d3531-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="d3531-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d3531-109">EXAMPLES</span></span>

### <span data-ttu-id="d3531-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d3531-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="d3531-111">Beolvassa a gyűjtemény képének verzióját.</span><span class="sxs-lookup"><span data-stu-id="d3531-111">Get the gallery image version.</span></span>

## <span data-ttu-id="d3531-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3531-112">PARAMETERS</span></span>

### <span data-ttu-id="d3531-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3531-113">-DefaultProfile</span></span>
<span data-ttu-id="d3531-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3531-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3531-115">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="d3531-115">-ExpandReplicationStatus</span></span>
<span data-ttu-id="d3531-116">Replikációs állapot megjelenítése</span><span class="sxs-lookup"><span data-stu-id="d3531-116">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3531-117">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d3531-117">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="d3531-118">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="d3531-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3531-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="d3531-119">-GalleryName</span></span>
<span data-ttu-id="d3531-120">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="d3531-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="d3531-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3531-121">-Name</span></span>
<span data-ttu-id="d3531-122">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="d3531-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3531-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3531-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3531-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3531-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d3531-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3531-125">-ResourceId</span></span>
<span data-ttu-id="d3531-126">A gyűjtemény képének-verziójához tartozó erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d3531-126">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="d3531-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3531-127">CommonParameters</span></span>
<span data-ttu-id="d3531-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3531-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3531-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3531-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3531-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3531-130">INPUTS</span></span>

### <span data-ttu-id="d3531-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d3531-131">System.String</span></span>

### <span data-ttu-id="d3531-132">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d3531-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="d3531-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3531-133">OUTPUTS</span></span>

### <span data-ttu-id="d3531-134">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d3531-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="d3531-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3531-135">NOTES</span></span>

## <span data-ttu-id="d3531-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3531-136">RELATED LINKS</span></span>
