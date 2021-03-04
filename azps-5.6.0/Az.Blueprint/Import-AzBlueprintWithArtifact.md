---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: eb0fddc34a83d5a23aeb990c920f36d7a3e03ff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932050"
---
# <span data-ttu-id="d347b-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="d347b-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="d347b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d347b-102">SYNOPSIS</span></span>
<span data-ttu-id="d347b-103">Egy tervrajzfájlT JSON formátumban importálhat egy tervrajzobjektumba, és a megadott előfizetés vagy felügyeleti csoporton belül mentheti.</span><span class="sxs-lookup"><span data-stu-id="d347b-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="d347b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d347b-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d347b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d347b-105">DESCRIPTION</span></span>
<span data-ttu-id="d347b-106">Importálja a tervdefiníciót annak tárgyával együtt.</span><span class="sxs-lookup"><span data-stu-id="d347b-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="d347b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d347b-107">EXAMPLES</span></span>

### <span data-ttu-id="d347b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d347b-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="d347b-109">Importálhat egy tervrajz-definíciót annak tárgyával együtt, és mentheti az előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="d347b-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="d347b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d347b-110">PARAMETERS</span></span>

### <span data-ttu-id="d347b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d347b-111">-DefaultProfile</span></span>
<span data-ttu-id="d347b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d347b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d347b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d347b-113">-Force</span></span>
<span data-ttu-id="d347b-114">Ha a beállítás igaz, a végrehajtás nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d347b-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="d347b-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="d347b-115">-IncludeSubFolders</span></span>
<span data-ttu-id="d347b-116">Ha igaz értékűre van állítva, az almappákban található összetevők is bekerülnek.</span><span class="sxs-lookup"><span data-stu-id="d347b-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="d347b-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="d347b-117">-InputPath</span></span>
<span data-ttu-id="d347b-118">Path to a Blueprint JSON file on disk.</span><span class="sxs-lookup"><span data-stu-id="d347b-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="d347b-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d347b-119">-ManagementGroupId</span></span>
<span data-ttu-id="d347b-120">Management Group Id where the blueprint definition is or will be saved.</span><span class="sxs-lookup"><span data-stu-id="d347b-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="d347b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d347b-121">-Name</span></span>
<span data-ttu-id="d347b-122">A tervrajz definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="d347b-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="d347b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d347b-123">-PassThru</span></span>
<span data-ttu-id="d347b-124">Ha be van állítva, a parancsmag az importált tervrajz definíciójának megfelelő objektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d347b-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="d347b-125">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d347b-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d347b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d347b-126">-SubscriptionId</span></span>
<span data-ttu-id="d347b-127">Előfizetés azonosítója, ahol a tervrajz definíciója mentve van vagy mentve lesz.</span><span class="sxs-lookup"><span data-stu-id="d347b-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="d347b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d347b-128">-Confirm</span></span>
<span data-ttu-id="d347b-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d347b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d347b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d347b-130">-WhatIf</span></span>
<span data-ttu-id="d347b-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d347b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d347b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d347b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d347b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d347b-133">CommonParameters</span></span>
<span data-ttu-id="d347b-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d347b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d347b-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d347b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d347b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d347b-136">INPUTS</span></span>

### <span data-ttu-id="d347b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d347b-137">System.String</span></span>

## <span data-ttu-id="d347b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d347b-138">OUTPUTS</span></span>

### <span data-ttu-id="d347b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d347b-139">System.String</span></span>

## <span data-ttu-id="d347b-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d347b-140">NOTES</span></span>

## <span data-ttu-id="d347b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d347b-141">RELATED LINKS</span></span>
