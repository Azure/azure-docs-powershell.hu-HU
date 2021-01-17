---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 7a6910e18b966c49ee6c766f06fddc88f903914f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480979"
---
# <span data-ttu-id="8d510-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="8d510-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="8d510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d510-102">SYNOPSIS</span></span>
<span data-ttu-id="8d510-103">Hozzon létre egy új tárgyat, és mentse a tervrajz definíciójában.</span><span class="sxs-lookup"><span data-stu-id="8d510-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="8d510-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d510-104">SYNTAX</span></span>

### <span data-ttu-id="8d510-105">CreateTemplateArtifact (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d510-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d510-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="8d510-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d510-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="8d510-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d510-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="8d510-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d510-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d510-109">DESCRIPTION</span></span>
<span data-ttu-id="8d510-110">Új tárgy létrehozása</span><span class="sxs-lookup"><span data-stu-id="8d510-110">Create a new artifact.</span></span> <span data-ttu-id="8d510-111">A tárgy kétféleképpen hozható létre: bemeneti fájlként egy JSON-összetevőn keresztül vagy az adott tárgy beágyazott paramétereinek biztosításával.</span><span class="sxs-lookup"><span data-stu-id="8d510-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="8d510-112">Bár a JSON metódus nem követeli meg az összetevő típusának beágyazott paraméteres módszerrel való megadva, a felhasználónak meg kell adnia az összetevő típusát a -Type paraméteren keresztül.</span><span class="sxs-lookup"><span data-stu-id="8d510-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="8d510-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d510-113">EXAMPLES</span></span>

### <span data-ttu-id="8d510-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="8d510-114">Example 1</span></span>
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

<span data-ttu-id="8d510-115">Hozzon létre egy új tárgyat egy JSON-fájlon keresztül.</span><span class="sxs-lookup"><span data-stu-id="8d510-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="8d510-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="8d510-116">Example 2</span></span>
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

<span data-ttu-id="8d510-117">Hozzon létre egy új összetevőt a beágyazott paramétereken keresztül.</span><span class="sxs-lookup"><span data-stu-id="8d510-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="8d510-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="8d510-118">Example 3</span></span>
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

<span data-ttu-id="8d510-119">Új elem létrehozása egy ARM sablonfájlon keresztül.</span><span class="sxs-lookup"><span data-stu-id="8d510-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="8d510-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d510-120">PARAMETERS</span></span>

### <span data-ttu-id="8d510-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="8d510-121">-ArtifactFile</span></span>
<span data-ttu-id="8d510-122">Az összetevő-fájl helye JSON formátumban a lemezen.</span><span class="sxs-lookup"><span data-stu-id="8d510-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="8d510-123">-Blueprint</span></span>
<span data-ttu-id="8d510-124">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="8d510-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d510-125">-DefaultProfile</span></span>
<span data-ttu-id="8d510-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d510-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d510-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="8d510-127">-DependsOn</span></span>
<span data-ttu-id="8d510-128">Azoknak az összetevőknek a listája, amelyek az aktuális tárgy létrehozása előtt létrejönnek.</span><span class="sxs-lookup"><span data-stu-id="8d510-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8d510-129">-Description</span></span>
<span data-ttu-id="8d510-130">Az összetevő leírása.</span><span class="sxs-lookup"><span data-stu-id="8d510-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-131">-Name</span><span class="sxs-lookup"><span data-stu-id="8d510-131">-Name</span></span>
<span data-ttu-id="8d510-132">Az összetevő neve</span><span class="sxs-lookup"><span data-stu-id="8d510-132">Name of the artifact</span></span>

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

### <span data-ttu-id="8d510-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="8d510-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="8d510-134">A házirenddefiníció definícióazonosítója.</span><span class="sxs-lookup"><span data-stu-id="8d510-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="8d510-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="8d510-136">A házirenddefiníciós összetevőnek átadni szükséges paraméterek kivonata.</span><span class="sxs-lookup"><span data-stu-id="8d510-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d510-137">-ResourceGroupName</span></span>
<span data-ttu-id="8d510-138">Annak az erőforráscsoportnak a neve, amely alatt az összetevő fog lennie.</span><span class="sxs-lookup"><span data-stu-id="8d510-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="8d510-139">-RoleDefinitionId</span></span>
<span data-ttu-id="8d510-140">Szerepkördefiníciók listája</span><span class="sxs-lookup"><span data-stu-id="8d510-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="8d510-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="8d510-142">A szerepkördefiníciós egyszerű azonosítók listája.</span><span class="sxs-lookup"><span data-stu-id="8d510-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8d510-143">-TemplateFile</span></span>
<span data-ttu-id="8d510-144">A ARM helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="8d510-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8d510-145">-TemplateParameterFile</span></span>
<span data-ttu-id="8d510-146">A ARM sablon paraméterfájljának helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="8d510-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-147">-Type</span><span class="sxs-lookup"><span data-stu-id="8d510-147">-Type</span></span>
<span data-ttu-id="8d510-148">Az összetevő típusa.</span><span class="sxs-lookup"><span data-stu-id="8d510-148">Type of the artifact.</span></span>
<span data-ttu-id="8d510-149">Három támogatott típus létezik: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="8d510-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d510-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d510-150">-Confirm</span></span>
<span data-ttu-id="8d510-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8d510-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d510-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d510-152">-WhatIf</span></span>
<span data-ttu-id="8d510-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8d510-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d510-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d510-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d510-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d510-155">CommonParameters</span></span>
<span data-ttu-id="8d510-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d510-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d510-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d510-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d510-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d510-158">INPUTS</span></span>

### <span data-ttu-id="8d510-159">System.String</span><span class="sxs-lookup"><span data-stu-id="8d510-159">System.String</span></span>

### <span data-ttu-id="8d510-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="8d510-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="8d510-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="8d510-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="8d510-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8d510-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="8d510-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8d510-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8d510-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8d510-164">System.String[]</span></span>

## <span data-ttu-id="8d510-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d510-165">OUTPUTS</span></span>

### <span data-ttu-id="8d510-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="8d510-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="8d510-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d510-167">NOTES</span></span>

## <span data-ttu-id="8d510-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d510-168">RELATED LINKS</span></span>
