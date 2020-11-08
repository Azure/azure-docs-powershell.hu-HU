---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024193"
---
# <span data-ttu-id="b93ce-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="b93ce-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="b93ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b93ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b93ce-103">A megadott terv-definíció exportálása a megadott kimeneti helyre JSON-fájlként.</span><span class="sxs-lookup"><span data-stu-id="b93ce-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="b93ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b93ce-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b93ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b93ce-105">DESCRIPTION</span></span>
<span data-ttu-id="b93ce-106">Exportálja a terv definícióját a leletekkel, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="b93ce-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="b93ce-107">Ez a parancsmag a Blueprint legújabb verzióját (piszkozatát vagy közzétételét) exportálja.</span><span class="sxs-lookup"><span data-stu-id="b93ce-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="b93ce-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b93ce-108">EXAMPLES</span></span>

### <span data-ttu-id="b93ce-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b93ce-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="b93ce-110">Exportálja a terv definícióját a leletekkel, és mentse a lemezre.</span><span class="sxs-lookup"><span data-stu-id="b93ce-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="b93ce-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b93ce-111">PARAMETERS</span></span>

### <span data-ttu-id="b93ce-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="b93ce-112">-Blueprint</span></span>
<span data-ttu-id="b93ce-113">Az exportálni kívánt Blueprint definition objektum.</span><span class="sxs-lookup"><span data-stu-id="b93ce-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="b93ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93ce-114">-DefaultProfile</span></span>
<span data-ttu-id="b93ce-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b93ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b93ce-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b93ce-116">-Force</span></span>
<span data-ttu-id="b93ce-117">Ha a True értékre van állítva, akkor a végrehajtás nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b93ce-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="b93ce-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b93ce-118">-OutputPath</span></span>
<span data-ttu-id="b93ce-119">A fájl elérési útvonala a lemezen, ahol a tervrajz definíciójának exportálása JSON formátumban</span><span class="sxs-lookup"><span data-stu-id="b93ce-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="b93ce-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b93ce-120">-PassThru</span></span>
<span data-ttu-id="b93ce-121">Ha be van állítva, a parancsmag egy olyan objektumot ad vissza, amely az exportált terv definícióját jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b93ce-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="b93ce-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b93ce-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b93ce-123">-Verzió</span><span class="sxs-lookup"><span data-stu-id="b93ce-123">-Version</span></span>
<span data-ttu-id="b93ce-124">Közzétett terv definíciós verziója.</span><span class="sxs-lookup"><span data-stu-id="b93ce-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="b93ce-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b93ce-125">-Confirm</span></span>
<span data-ttu-id="b93ce-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b93ce-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b93ce-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b93ce-127">-WhatIf</span></span>
<span data-ttu-id="b93ce-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b93ce-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b93ce-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b93ce-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b93ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93ce-130">CommonParameters</span></span>
<span data-ttu-id="b93ce-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b93ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93ce-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b93ce-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93ce-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b93ce-133">INPUTS</span></span>

### <span data-ttu-id="b93ce-134">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="b93ce-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="b93ce-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b93ce-135">System.String</span></span>

## <span data-ttu-id="b93ce-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b93ce-136">OUTPUTS</span></span>

### <span data-ttu-id="b93ce-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b93ce-137">System.String</span></span>

## <span data-ttu-id="b93ce-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b93ce-138">NOTES</span></span>

## <span data-ttu-id="b93ce-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b93ce-139">RELATED LINKS</span></span>
