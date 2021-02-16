---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 7a6910e18b966c49ee6c766f06fddc88f903914f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168139"
---
# <span data-ttu-id="5d52c-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="5d52c-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="5d52c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d52c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d52c-103">Hozzon létre egy új tárgyat, és mentse a tervrajz definíciójában.</span><span class="sxs-lookup"><span data-stu-id="5d52c-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="5d52c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d52c-104">SYNTAX</span></span>

### <span data-ttu-id="5d52c-105">CreateTemplateArtifact (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d52c-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d52c-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="5d52c-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d52c-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="5d52c-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d52c-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="5d52c-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d52c-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d52c-109">DESCRIPTION</span></span>
<span data-ttu-id="5d52c-110">Új tárgy létrehozása</span><span class="sxs-lookup"><span data-stu-id="5d52c-110">Create a new artifact.</span></span> <span data-ttu-id="5d52c-111">A tárgy kétféleképpen hozható létre: bemeneti fájlként egy JSON-összetevőn keresztül vagy az adott tárgy beágyazott paramétereinek biztosításával.</span><span class="sxs-lookup"><span data-stu-id="5d52c-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="5d52c-112">Bár a JSON metódus nem követeli meg az összetevő típusának beágyazott paraméteres módszerrel való megadva, a felhasználónak meg kell adnia az összetevő típusát a -Type paraméteren keresztül.</span><span class="sxs-lookup"><span data-stu-id="5d52c-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="5d52c-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d52c-113">EXAMPLES</span></span>

### <span data-ttu-id="5d52c-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="5d52c-114">Example 1</span></span>
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

<span data-ttu-id="5d52c-115">Hozzon létre egy új tárgyat egy JSON-fájlon keresztül.</span><span class="sxs-lookup"><span data-stu-id="5d52c-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="5d52c-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="5d52c-116">Example 2</span></span>
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

<span data-ttu-id="5d52c-117">Hozzon létre egy új összetevőt a beágyazott paramétereken keresztül.</span><span class="sxs-lookup"><span data-stu-id="5d52c-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="5d52c-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="5d52c-118">Example 3</span></span>
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

<span data-ttu-id="5d52c-119">Új elem létrehozása egy ARM sablonfájlon keresztül.</span><span class="sxs-lookup"><span data-stu-id="5d52c-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="5d52c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d52c-120">PARAMETERS</span></span>

### <span data-ttu-id="5d52c-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="5d52c-121">-ArtifactFile</span></span>
<span data-ttu-id="5d52c-122">Az összetevőfájl helye JSON formátumban a lemezen.</span><span class="sxs-lookup"><span data-stu-id="5d52c-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="5d52c-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="5d52c-123">-Blueprint</span></span>
<span data-ttu-id="5d52c-124">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="5d52c-124">Blueprint object.</span></span>

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

### <span data-ttu-id="5d52c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d52c-125">-DefaultProfile</span></span>
<span data-ttu-id="5d52c-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d52c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d52c-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="5d52c-127">-DependsOn</span></span>
<span data-ttu-id="5d52c-128">Azoknak az összetevőknek a listája, amelyek az aktuális tárgy létrehozása előtt létrejönnek.</span><span class="sxs-lookup"><span data-stu-id="5d52c-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="5d52c-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5d52c-129">-Description</span></span>
<span data-ttu-id="5d52c-130">Az összetevő leírása.</span><span class="sxs-lookup"><span data-stu-id="5d52c-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="5d52c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="5d52c-131">-Name</span></span>
<span data-ttu-id="5d52c-132">Az összetevő neve</span><span class="sxs-lookup"><span data-stu-id="5d52c-132">Name of the artifact</span></span>

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

### <span data-ttu-id="5d52c-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5d52c-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="5d52c-134">A házirenddefiníció definícióazonosítója.</span><span class="sxs-lookup"><span data-stu-id="5d52c-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="5d52c-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="5d52c-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="5d52c-136">A házirenddefiníciós összetevőnek átadni szükséges paraméterek kivonata.</span><span class="sxs-lookup"><span data-stu-id="5d52c-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="5d52c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d52c-137">-ResourceGroupName</span></span>
<span data-ttu-id="5d52c-138">Annak az erőforráscsoportnak a neve, amely alatt az összetevő fog lennie.</span><span class="sxs-lookup"><span data-stu-id="5d52c-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="5d52c-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5d52c-139">-RoleDefinitionId</span></span>
<span data-ttu-id="5d52c-140">A szerepkör-definíciók listája</span><span class="sxs-lookup"><span data-stu-id="5d52c-140">List of role definition</span></span>

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

### <span data-ttu-id="5d52c-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="5d52c-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="5d52c-142">A szerepkördefiníciós egyszerű azonosítók listája.</span><span class="sxs-lookup"><span data-stu-id="5d52c-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="5d52c-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="5d52c-143">-TemplateFile</span></span>
<span data-ttu-id="5d52c-144">A ARM helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="5d52c-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="5d52c-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="5d52c-145">-TemplateParameterFile</span></span>
<span data-ttu-id="5d52c-146">A ARM sablon paraméterfájljának helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="5d52c-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="5d52c-147">-Type</span><span class="sxs-lookup"><span data-stu-id="5d52c-147">-Type</span></span>
<span data-ttu-id="5d52c-148">Az összetevő típusa.</span><span class="sxs-lookup"><span data-stu-id="5d52c-148">Type of the artifact.</span></span>
<span data-ttu-id="5d52c-149">Három támogatott típus létezik: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="5d52c-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="5d52c-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d52c-150">-Confirm</span></span>
<span data-ttu-id="5d52c-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d52c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d52c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d52c-152">-WhatIf</span></span>
<span data-ttu-id="5d52c-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d52c-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d52c-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d52c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d52c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d52c-155">CommonParameters</span></span>
<span data-ttu-id="5d52c-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d52c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d52c-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d52c-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d52c-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d52c-158">INPUTS</span></span>

### <span data-ttu-id="5d52c-159">System.String</span><span class="sxs-lookup"><span data-stu-id="5d52c-159">System.String</span></span>

### <span data-ttu-id="5d52c-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="5d52c-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="5d52c-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="5d52c-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="5d52c-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5d52c-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="5d52c-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5d52c-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5d52c-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5d52c-164">System.String[]</span></span>

## <span data-ttu-id="5d52c-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d52c-165">OUTPUTS</span></span>

### <span data-ttu-id="5d52c-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="5d52c-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="5d52c-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d52c-167">NOTES</span></span>

## <span data-ttu-id="5d52c-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d52c-168">RELATED LINKS</span></span>
