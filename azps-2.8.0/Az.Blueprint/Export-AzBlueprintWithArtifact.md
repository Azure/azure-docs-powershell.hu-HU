---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2c349d99e8a3529d4f1423a43bd31ab2500664c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667652"
---
# <span data-ttu-id="cd123-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="cd123-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="cd123-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd123-102">SYNOPSIS</span></span>
<span data-ttu-id="cd123-103">A megadott terv-definíció exportálása a megadott kimeneti helyre JSON-fájlként.</span><span class="sxs-lookup"><span data-stu-id="cd123-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="cd123-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd123-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd123-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd123-105">DESCRIPTION</span></span>
<span data-ttu-id="cd123-106">Exportálja a terv definícióját a leletekkel, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="cd123-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="cd123-107">Ez a parancsmag a Blueprint legújabb verzióját (piszkozatát vagy közzétételét) exportálja.</span><span class="sxs-lookup"><span data-stu-id="cd123-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="cd123-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cd123-108">EXAMPLES</span></span>

### <span data-ttu-id="cd123-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cd123-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="cd123-110">Exportálja a terv definícióját a leletekkel, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="cd123-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="cd123-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd123-111">PARAMETERS</span></span>

### <span data-ttu-id="cd123-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="cd123-112">-Blueprint</span></span>
<span data-ttu-id="cd123-113">Az exportálni kívánt Blueprint definition objektum.</span><span class="sxs-lookup"><span data-stu-id="cd123-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="cd123-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd123-114">-DefaultProfile</span></span>
<span data-ttu-id="cd123-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd123-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd123-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cd123-116">-Force</span></span>
<span data-ttu-id="cd123-117">Ha a True értékre van állítva, akkor a végrehajtás nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd123-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="cd123-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="cd123-118">-OutputPath</span></span>
<span data-ttu-id="cd123-119">A fájl elérési útvonala a lemezen, ahol a tervrajz definíciójának exportálása JSON formátumban</span><span class="sxs-lookup"><span data-stu-id="cd123-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="cd123-120">-Verzió</span><span class="sxs-lookup"><span data-stu-id="cd123-120">-Version</span></span>
<span data-ttu-id="cd123-121">Közzétett terv definíciós verziója.</span><span class="sxs-lookup"><span data-stu-id="cd123-121">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="cd123-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd123-122">CommonParameters</span></span>
<span data-ttu-id="cd123-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd123-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cd123-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd123-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd123-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd123-125">INPUTS</span></span>

### <span data-ttu-id="cd123-126">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="cd123-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="cd123-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cd123-127">System.String</span></span>

## <span data-ttu-id="cd123-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd123-128">OUTPUTS</span></span>

### <span data-ttu-id="cd123-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cd123-129">System.String</span></span>

## <span data-ttu-id="cd123-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd123-130">NOTES</span></span>

## <span data-ttu-id="cd123-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd123-131">RELATED LINKS</span></span>
