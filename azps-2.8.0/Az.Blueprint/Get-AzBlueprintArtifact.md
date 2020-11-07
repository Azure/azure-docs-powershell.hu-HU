---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 94a0ff1d4e16748b769f51303fb397da7e029026
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667648"
---
# <span data-ttu-id="ff251-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="ff251-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="ff251-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff251-102">SYNOPSIS</span></span>
<span data-ttu-id="ff251-103">A tervrajz-definícióból származó leletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="ff251-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="ff251-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff251-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff251-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff251-105">DESCRIPTION</span></span>
<span data-ttu-id="ff251-106">A tervrajz-definícióból származó leletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="ff251-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="ff251-107">Ha a Blueprint definition definition verzió nincs megadva, a Piszkozat verzió lekérése.</span><span class="sxs-lookup"><span data-stu-id="ff251-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="ff251-108">Abban az esetben, ha nincs Piszkozat verzió, a legújabb közzétett terv definícióját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ff251-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="ff251-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ff251-109">EXAMPLES</span></span>

### <span data-ttu-id="ff251-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ff251-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192

```

<span data-ttu-id="ff251-111">A Blueprint-definícióból származó leletek lekérése</span><span class="sxs-lookup"><span data-stu-id="ff251-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="ff251-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff251-112">PARAMETERS</span></span>

### <span data-ttu-id="ff251-113">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="ff251-113">-ArtifactFile</span></span>
<span data-ttu-id="ff251-114">A tárgy fájl helye JSON formátumban a lemezen</span><span class="sxs-lookup"><span data-stu-id="ff251-114">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-115">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="ff251-115">-Blueprint</span></span>
<span data-ttu-id="ff251-116">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="ff251-116">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: ArtifactsByBlueprint, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="ff251-117">-BlueprintVersion</span></span>
<span data-ttu-id="ff251-118">A terv változata a leletek beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="ff251-118">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff251-119">-DefaultProfile</span></span>
<span data-ttu-id="ff251-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff251-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff251-121">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="ff251-121">-DependsOn</span></span>
<span data-ttu-id="ff251-122">Azoknak az eltéréseknek a listája, amelyeket a jelenlegi tárgy létrehozása előtt létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="ff251-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ff251-123">-Description</span></span>
<span data-ttu-id="ff251-124">A tárgy leírása.</span><span class="sxs-lookup"><span data-stu-id="ff251-124">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff251-125">-Name</span></span>
<span data-ttu-id="ff251-126">A tárgy neve</span><span class="sxs-lookup"><span data-stu-id="ff251-126">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-127">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ff251-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="ff251-128">A házirend definíciójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ff251-128">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="ff251-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="ff251-130">Hashtable a házirend-definíciós tárgyhoz való továbbításhoz.</span><span class="sxs-lookup"><span data-stu-id="ff251-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff251-131">-ResourceGroupName</span></span>
<span data-ttu-id="ff251-132">Annak az erőforráscsoportnek a neve, amely a tárgyat fogja használni.</span><span class="sxs-lookup"><span data-stu-id="ff251-132">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ff251-133">-RoleDefinitionId</span></span>
<span data-ttu-id="ff251-134">A szerepkör-definíciók listája</span><span class="sxs-lookup"><span data-stu-id="ff251-134">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-135">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="ff251-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="ff251-136">A szerepkör-definíciós fő azonosítók listája.</span><span class="sxs-lookup"><span data-stu-id="ff251-136">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ff251-137">-TemplateFile</span></span>
<span data-ttu-id="ff251-138">A kar sablonfájlt tartalmazó fájl helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="ff251-138">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ff251-139">-TemplateParameterFile</span></span>
<span data-ttu-id="ff251-140">A ARM template paraméter fájljának helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="ff251-140">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-141">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="ff251-141">-Type</span></span>
<span data-ttu-id="ff251-142">A tárgy típusa.</span><span class="sxs-lookup"><span data-stu-id="ff251-142">Type of the artifact.</span></span>
<span data-ttu-id="ff251-143">A következő 3 típus támogatott: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="ff251-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff251-144">-Confirm</span></span>
<span data-ttu-id="ff251-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff251-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff251-146">-WhatIf</span></span>
<span data-ttu-id="ff251-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff251-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff251-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff251-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff251-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff251-149">CommonParameters</span></span>
<span data-ttu-id="ff251-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff251-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ff251-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff251-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff251-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff251-152">INPUTS</span></span>

### <span data-ttu-id="ff251-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ff251-153">System.String</span></span>

### <span data-ttu-id="ff251-154">Microsoft. Azure. commands. Blueprint. models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="ff251-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="ff251-155">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="ff251-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="ff251-156">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ff251-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ff251-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ff251-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ff251-158">System. string []</span><span class="sxs-lookup"><span data-stu-id="ff251-158">System.String[]</span></span>

## <span data-ttu-id="ff251-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff251-159">OUTPUTS</span></span>

### <span data-ttu-id="ff251-160">Microsoft. Azure. commands. Blueprint. models. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="ff251-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="ff251-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff251-161">NOTES</span></span>

## <span data-ttu-id="ff251-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff251-162">RELATED LINKS</span></span>
