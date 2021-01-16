---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363858"
---
# <span data-ttu-id="fe697-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="fe697-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="fe697-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe697-102">SYNOPSIS</span></span>
<span data-ttu-id="fe697-103">A megadott tervrajz-definíció exportálása a megadott kimeneti helyre JSON-fájlként.</span><span class="sxs-lookup"><span data-stu-id="fe697-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="fe697-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fe697-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe697-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fe697-105">DESCRIPTION</span></span>
<span data-ttu-id="fe697-106">Exportálja a tervdefiníciót annak tárgyával együtt, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="fe697-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="fe697-107">Ez a parancsmag a tervrajz legújabb verzióját (piszkozatát vagy közzétettet) exportálja.</span><span class="sxs-lookup"><span data-stu-id="fe697-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="fe697-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fe697-108">EXAMPLES</span></span>

### <span data-ttu-id="fe697-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="fe697-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="fe697-110">Exportálja a tervdefiníciót annak tárgyával együtt, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="fe697-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="fe697-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe697-111">PARAMETERS</span></span>

### <span data-ttu-id="fe697-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="fe697-112">-Blueprint</span></span>
<span data-ttu-id="fe697-113">Az exportálni használt tervrajzdefiníciós objektum.</span><span class="sxs-lookup"><span data-stu-id="fe697-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="fe697-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe697-114">-DefaultProfile</span></span>
<span data-ttu-id="fe697-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe697-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe697-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fe697-116">-Force</span></span>
<span data-ttu-id="fe697-117">Ha a beállítás igaz, a végrehajtás nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe697-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="fe697-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="fe697-118">-OutputPath</span></span>
<span data-ttu-id="fe697-119">Annak a fájlnak az elérési útja a lemezen, ahová exportálni kell a Tervrajz definíciót JSON formátumban.</span><span class="sxs-lookup"><span data-stu-id="fe697-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="fe697-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe697-120">-PassThru</span></span>
<span data-ttu-id="fe697-121">Ha be van állítva, a parancsmag visszaadja az exportált tervrajz definíciójának megfelelő objektumot.</span><span class="sxs-lookup"><span data-stu-id="fe697-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="fe697-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fe697-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe697-123">-Version</span><span class="sxs-lookup"><span data-stu-id="fe697-123">-Version</span></span>
<span data-ttu-id="fe697-124">Közzétett tervdefiníciós verzió.</span><span class="sxs-lookup"><span data-stu-id="fe697-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="fe697-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe697-125">-Confirm</span></span>
<span data-ttu-id="fe697-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fe697-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe697-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe697-127">-WhatIf</span></span>
<span data-ttu-id="fe697-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fe697-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe697-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe697-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe697-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe697-130">CommonParameters</span></span>
<span data-ttu-id="fe697-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe697-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe697-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe697-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe697-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe697-133">INPUTS</span></span>

### <span data-ttu-id="fe697-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="fe697-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="fe697-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fe697-135">System.String</span></span>

## <span data-ttu-id="fe697-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe697-136">OUTPUTS</span></span>

### <span data-ttu-id="fe697-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fe697-137">System.String</span></span>

## <span data-ttu-id="fe697-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fe697-138">NOTES</span></span>

## <span data-ttu-id="fe697-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe697-139">RELATED LINKS</span></span>
