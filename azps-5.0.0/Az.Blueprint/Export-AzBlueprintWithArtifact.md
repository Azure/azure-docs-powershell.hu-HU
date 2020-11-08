---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186909"
---
# <span data-ttu-id="98945-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="98945-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="98945-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98945-102">SYNOPSIS</span></span>
<span data-ttu-id="98945-103">A megadott terv-definíció exportálása a megadott kimeneti helyre JSON-fájlként.</span><span class="sxs-lookup"><span data-stu-id="98945-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="98945-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98945-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98945-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98945-105">DESCRIPTION</span></span>
<span data-ttu-id="98945-106">Exportálja a terv definícióját a leletekkel, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="98945-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="98945-107">Ez a parancsmag a Blueprint legújabb verzióját (piszkozatát vagy közzétételét) exportálja.</span><span class="sxs-lookup"><span data-stu-id="98945-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="98945-108">Példák</span><span class="sxs-lookup"><span data-stu-id="98945-108">EXAMPLES</span></span>

### <span data-ttu-id="98945-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="98945-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="98945-110">Exportálja a terv definícióját a leletekkel, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="98945-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="98945-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98945-111">PARAMETERS</span></span>

### <span data-ttu-id="98945-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="98945-112">-Blueprint</span></span>
<span data-ttu-id="98945-113">Az exportálni kívánt Blueprint definition objektum.</span><span class="sxs-lookup"><span data-stu-id="98945-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="98945-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98945-114">-DefaultProfile</span></span>
<span data-ttu-id="98945-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98945-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98945-116">-Force</span><span class="sxs-lookup"><span data-stu-id="98945-116">-Force</span></span>
<span data-ttu-id="98945-117">Ha a True értékre van állítva, akkor a végrehajtás nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98945-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="98945-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="98945-118">-OutputPath</span></span>
<span data-ttu-id="98945-119">A fájl elérési útvonala a lemezen, ahol a tervrajz definíciójának exportálása JSON formátumban</span><span class="sxs-lookup"><span data-stu-id="98945-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="98945-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98945-120">-PassThru</span></span>
<span data-ttu-id="98945-121">Ha be van állítva, a parancsmag egy olyan objektumot ad vissza, amely az exportált terv definícióját jelképezi.</span><span class="sxs-lookup"><span data-stu-id="98945-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="98945-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="98945-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="98945-123">-Verzió</span><span class="sxs-lookup"><span data-stu-id="98945-123">-Version</span></span>
<span data-ttu-id="98945-124">Közzétett terv definíciós verziója.</span><span class="sxs-lookup"><span data-stu-id="98945-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="98945-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98945-125">-Confirm</span></span>
<span data-ttu-id="98945-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98945-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98945-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98945-127">-WhatIf</span></span>
<span data-ttu-id="98945-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98945-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98945-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98945-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98945-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98945-130">CommonParameters</span></span>
<span data-ttu-id="98945-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98945-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98945-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="98945-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98945-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98945-133">INPUTS</span></span>

### <span data-ttu-id="98945-134">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="98945-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="98945-135">System. String</span><span class="sxs-lookup"><span data-stu-id="98945-135">System.String</span></span>

## <span data-ttu-id="98945-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98945-136">OUTPUTS</span></span>

### <span data-ttu-id="98945-137">System. String</span><span class="sxs-lookup"><span data-stu-id="98945-137">System.String</span></span>

## <span data-ttu-id="98945-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98945-138">NOTES</span></span>

## <span data-ttu-id="98945-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98945-139">RELATED LINKS</span></span>
