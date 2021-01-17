---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480985"
---
# <span data-ttu-id="c18b7-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="c18b7-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="c18b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c18b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c18b7-103">A megadott tervrajz-definíció exportálása a megadott kimeneti helyre JSON-fájlként.</span><span class="sxs-lookup"><span data-stu-id="c18b7-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="c18b7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c18b7-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c18b7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c18b7-105">DESCRIPTION</span></span>
<span data-ttu-id="c18b7-106">Exportálja a tervdefiníciót annak tárgyával együtt, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="c18b7-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="c18b7-107">Ez a parancsmag a tervrajz legújabb verzióját (piszkozatát vagy közzétettet) exportálja.</span><span class="sxs-lookup"><span data-stu-id="c18b7-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="c18b7-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c18b7-108">EXAMPLES</span></span>

### <span data-ttu-id="c18b7-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="c18b7-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="c18b7-110">Exportálja a tervdefiníciót annak tárgyával együtt, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="c18b7-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="c18b7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c18b7-111">PARAMETERS</span></span>

### <span data-ttu-id="c18b7-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="c18b7-112">-Blueprint</span></span>
<span data-ttu-id="c18b7-113">Az exportálni használt tervrajzdefiníciós objektum.</span><span class="sxs-lookup"><span data-stu-id="c18b7-113">The blueprint definition object to export.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c18b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c18b7-114">-DefaultProfile</span></span>
<span data-ttu-id="c18b7-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c18b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c18b7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c18b7-116">-Force</span></span>
<span data-ttu-id="c18b7-117">Ha a beállítás igaz, a végrehajtás nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c18b7-117">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c18b7-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c18b7-118">-OutputPath</span></span>
<span data-ttu-id="c18b7-119">Annak a fájlnak az elérési útja a lemezen, ahová exportálni kell a Tervrajz definíciót JSON formátumban.</span><span class="sxs-lookup"><span data-stu-id="c18b7-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="c18b7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c18b7-120">-PassThru</span></span>
<span data-ttu-id="c18b7-121">Ha be van állítva, a parancsmag visszaadja az exportált tervrajz definíciójának megfelelő objektumot.</span><span class="sxs-lookup"><span data-stu-id="c18b7-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="c18b7-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c18b7-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c18b7-123">-Version</span><span class="sxs-lookup"><span data-stu-id="c18b7-123">-Version</span></span>
<span data-ttu-id="c18b7-124">Közzétett tervrajzdefiníciós verzió.</span><span class="sxs-lookup"><span data-stu-id="c18b7-124">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c18b7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c18b7-125">-Confirm</span></span>
<span data-ttu-id="c18b7-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c18b7-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c18b7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c18b7-127">-WhatIf</span></span>
<span data-ttu-id="c18b7-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c18b7-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c18b7-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c18b7-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c18b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c18b7-130">CommonParameters</span></span>
<span data-ttu-id="c18b7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c18b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c18b7-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c18b7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c18b7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c18b7-133">INPUTS</span></span>

### <span data-ttu-id="c18b7-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="c18b7-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="c18b7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c18b7-135">System.String</span></span>

## <span data-ttu-id="c18b7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c18b7-136">OUTPUTS</span></span>

### <span data-ttu-id="c18b7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c18b7-137">System.String</span></span>

## <span data-ttu-id="c18b7-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c18b7-138">NOTES</span></span>

## <span data-ttu-id="c18b7-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c18b7-139">RELATED LINKS</span></span>
