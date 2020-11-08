---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2136a224a5d187951b77c6f48e0b610b48b021b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012378"
---
# <span data-ttu-id="1bd9f-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="1bd9f-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="1bd9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1bd9f-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd9f-103">A megadott terv-definíció exportálása a megadott kimeneti helyre JSON-fájlként.</span><span class="sxs-lookup"><span data-stu-id="1bd9f-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="1bd9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1bd9f-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bd9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1bd9f-105">DESCRIPTION</span></span>
<span data-ttu-id="1bd9f-106">Exportálja a terv definícióját a leletekkel, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="1bd9f-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="1bd9f-107">Ez a parancsmag a Blueprint legújabb verzióját (piszkozatát vagy közzétételét) exportálja.</span><span class="sxs-lookup"><span data-stu-id="1bd9f-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="1bd9f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1bd9f-108">EXAMPLES</span></span>

### <span data-ttu-id="1bd9f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1bd9f-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="1bd9f-110">Exportálja a terv definícióját a leletekkel, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="1bd9f-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="1bd9f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1bd9f-111">PARAMETERS</span></span>

### <span data-ttu-id="1bd9f-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="1bd9f-112">-Blueprint</span></span>
<span data-ttu-id="1bd9f-113">Az exportálni kívánt Blueprint definition objektum.</span><span class="sxs-lookup"><span data-stu-id="1bd9f-113">The blueprint definition object to export.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd9f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bd9f-114">-DefaultProfile</span></span>
<span data-ttu-id="1bd9f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1bd9f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd9f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1bd9f-116">-Force</span></span>
<span data-ttu-id="1bd9f-117">Ha a True értékre van állítva, akkor a végrehajtás nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1bd9f-117">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd9f-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="1bd9f-118">-OutputPath</span></span>
<span data-ttu-id="1bd9f-119">A fájl elérési útvonala a lemezen, ahol a tervrajz definíciójának exportálása JSON formátumban</span><span class="sxs-lookup"><span data-stu-id="1bd9f-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="1bd9f-120">-Verzió</span><span class="sxs-lookup"><span data-stu-id="1bd9f-120">-Version</span></span>
<span data-ttu-id="1bd9f-121">Közzétett terv definíciós verziója.</span><span class="sxs-lookup"><span data-stu-id="1bd9f-121">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="1bd9f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd9f-122">CommonParameters</span></span>
<span data-ttu-id="1bd9f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1bd9f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1bd9f-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bd9f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd9f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bd9f-125">INPUTS</span></span>

### <span data-ttu-id="1bd9f-126">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="1bd9f-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="1bd9f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1bd9f-127">System.String</span></span>

## <span data-ttu-id="1bd9f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bd9f-128">OUTPUTS</span></span>

### <span data-ttu-id="1bd9f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1bd9f-129">System.String</span></span>

## <span data-ttu-id="1bd9f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1bd9f-130">NOTES</span></span>

## <span data-ttu-id="1bd9f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bd9f-131">RELATED LINKS</span></span>
