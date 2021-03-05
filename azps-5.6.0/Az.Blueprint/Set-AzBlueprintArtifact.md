---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7e4558d0ff48f2750ed3ac825b2358b5cad437ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009349"
---
# <span data-ttu-id="efc47-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="efc47-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="efc47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efc47-102">SYNOPSIS</span></span>
<span data-ttu-id="efc47-103">Egy tervrajzdefinícióban frissítsen egy tárgyat.</span><span class="sxs-lookup"><span data-stu-id="efc47-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="efc47-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efc47-104">SYNTAX</span></span>

### <span data-ttu-id="efc47-105">UpdateTemplateArtifact (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efc47-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc47-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="efc47-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc47-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="efc47-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc47-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="efc47-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc47-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efc47-109">DESCRIPTION</span></span>
<span data-ttu-id="efc47-110">Tárgy frissítése</span><span class="sxs-lookup"><span data-stu-id="efc47-110">Update an artifact.</span></span> <span data-ttu-id="efc47-111">Kétféleképpen frissíthet egy tárgyat: bemeneti fájlként egy JSON-összetevőn keresztül vagy az adott tárgy beágyazott paramétereinek biztosításával.</span><span class="sxs-lookup"><span data-stu-id="efc47-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="efc47-112">Bár a JSON metódus nem követeli meg az összetevő típusának beágyazott paraméteres módszerrel való megadva, a felhasználónak meg kell adnia az összetevő típusát a -Type paraméteren keresztül.</span><span class="sxs-lookup"><span data-stu-id="efc47-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="efc47-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efc47-113">EXAMPLES</span></span>

### <span data-ttu-id="efc47-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="efc47-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="efc47-115">A JSON-fájlon keresztül frissítheti az egyik tárgyat.</span><span class="sxs-lookup"><span data-stu-id="efc47-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="efc47-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="efc47-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG
```

<span data-ttu-id="efc47-117">Egy összetevő frissítése a beágyazott paramétereken keresztül.</span><span class="sxs-lookup"><span data-stu-id="efc47-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="efc47-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="efc47-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account
```

<span data-ttu-id="efc47-119">Egy elem frissítése egy ARM sablonfájlon keresztül.</span><span class="sxs-lookup"><span data-stu-id="efc47-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="efc47-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efc47-120">PARAMETERS</span></span>

### <span data-ttu-id="efc47-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="efc47-121">-ArtifactFile</span></span>
<span data-ttu-id="efc47-122">Az összetevő-fájl helye JSON formátumban a lemezen.</span><span class="sxs-lookup"><span data-stu-id="efc47-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="efc47-123">-Blueprint</span></span>
<span data-ttu-id="efc47-124">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="efc47-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc47-125">-DefaultProfile</span></span>
<span data-ttu-id="efc47-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efc47-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc47-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="efc47-127">-DependsOn</span></span>
<span data-ttu-id="efc47-128">Azoknak az összetevőknek a listája, amelyek az aktuális tárgy létrehozása előtt létrejönnek.</span><span class="sxs-lookup"><span data-stu-id="efc47-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="efc47-129">-Description</span></span>
<span data-ttu-id="efc47-130">Az összetevő leírása.</span><span class="sxs-lookup"><span data-stu-id="efc47-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-131">-Name</span><span class="sxs-lookup"><span data-stu-id="efc47-131">-Name</span></span>
<span data-ttu-id="efc47-132">Az összetevő neve</span><span class="sxs-lookup"><span data-stu-id="efc47-132">Name of the artifact</span></span>

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

### <span data-ttu-id="efc47-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="efc47-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="efc47-134">A házirenddefiníció definícióazonosítója.</span><span class="sxs-lookup"><span data-stu-id="efc47-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="efc47-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="efc47-136">A házirenddefiníciós összetevőnek átadni szükséges paraméterek kivonata.</span><span class="sxs-lookup"><span data-stu-id="efc47-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc47-137">-ResourceGroupName</span></span>
<span data-ttu-id="efc47-138">Annak az erőforráscsoportnak a neve, amely alatt az összetevő fog lennie.</span><span class="sxs-lookup"><span data-stu-id="efc47-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="efc47-139">-RoleDefinitionId</span></span>
<span data-ttu-id="efc47-140">A szerepkör-definíciók listája</span><span class="sxs-lookup"><span data-stu-id="efc47-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="efc47-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="efc47-142">A szerepkördefiníciós egyszerű azonosítók listája.</span><span class="sxs-lookup"><span data-stu-id="efc47-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="efc47-143">-TemplateFile</span></span>
<span data-ttu-id="efc47-144">A ARM helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="efc47-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="efc47-145">-TemplateParameterFile</span></span>
<span data-ttu-id="efc47-146">A ARM sablon paraméterfájljának helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="efc47-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-147">-Type</span><span class="sxs-lookup"><span data-stu-id="efc47-147">-Type</span></span>
<span data-ttu-id="efc47-148">Az összetevő típusa.</span><span class="sxs-lookup"><span data-stu-id="efc47-148">Type of the artifact.</span></span>
<span data-ttu-id="efc47-149">Három támogatott típus létezik: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="efc47-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc47-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efc47-150">-Confirm</span></span>
<span data-ttu-id="efc47-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="efc47-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc47-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc47-152">-WhatIf</span></span>
<span data-ttu-id="efc47-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="efc47-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efc47-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efc47-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc47-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc47-155">CommonParameters</span></span>
<span data-ttu-id="efc47-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc47-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc47-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efc47-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc47-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efc47-158">INPUTS</span></span>

### <span data-ttu-id="efc47-159">System.String</span><span class="sxs-lookup"><span data-stu-id="efc47-159">System.String</span></span>

### <span data-ttu-id="efc47-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="efc47-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="efc47-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="efc47-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="efc47-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="efc47-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="efc47-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="efc47-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="efc47-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="efc47-164">System.String[]</span></span>

## <span data-ttu-id="efc47-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efc47-165">OUTPUTS</span></span>

### <span data-ttu-id="efc47-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="efc47-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="efc47-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efc47-167">NOTES</span></span>

## <span data-ttu-id="efc47-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efc47-168">RELATED LINKS</span></span>
