---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186092"
---
# <span data-ttu-id="f1d4e-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="f1d4e-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="f1d4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d4e-103">A tervrajz definíciójában lévő tárgy frissítése</span><span class="sxs-lookup"><span data-stu-id="f1d4e-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="f1d4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1d4e-104">SYNTAX</span></span>

### <span data-ttu-id="f1d4e-105">UpdateTemplateArtifact (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1d4e-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d4e-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="f1d4e-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d4e-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="f1d4e-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d4e-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="f1d4e-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1d4e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1d4e-109">DESCRIPTION</span></span>
<span data-ttu-id="f1d4e-110">Frissítsen egy tárgyat.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-110">Update an artifact.</span></span> <span data-ttu-id="f1d4e-111">A tárgyat kétféleképpen frissítheti: vagy a JSON-ot beviteli fájlként vagy a tárgyhoz tartozó szövegközi paramétereket biztosítva.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="f1d4e-112">A JSON-metódusban nem szükséges, hogy a szövegközi paramétert tartalmazó típus típusa legyen a felhasználónak, hogy a tárgy típusa paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="f1d4e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f1d4e-113">EXAMPLES</span></span>

### <span data-ttu-id="f1d4e-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f1d4e-114">Example 1</span></span>
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

<span data-ttu-id="f1d4e-115">A leletek JSON-fájlon keresztül frissíthetők.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="f1d4e-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="f1d4e-116">Example 2</span></span>
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

<span data-ttu-id="f1d4e-117">Egy tárgy frissítése szövegközi paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="f1d4e-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="f1d4e-118">Example 3</span></span>
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

<span data-ttu-id="f1d4e-119">Frissítsen egy tárgyat egy ARM-sablonfájl segítségével.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="f1d4e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1d4e-120">PARAMETERS</span></span>

### <span data-ttu-id="f1d4e-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="f1d4e-121">-ArtifactFile</span></span>
<span data-ttu-id="f1d4e-122">A tárgy fájl helye JSON formátumban a lemezen</span><span class="sxs-lookup"><span data-stu-id="f1d4e-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="f1d4e-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="f1d4e-123">-Blueprint</span></span>
<span data-ttu-id="f1d4e-124">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-124">Blueprint object.</span></span>

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

### <span data-ttu-id="f1d4e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d4e-125">-DefaultProfile</span></span>
<span data-ttu-id="f1d4e-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1d4e-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="f1d4e-127">-DependsOn</span></span>
<span data-ttu-id="f1d4e-128">Azoknak az eltéréseknek a listája, amelyeket a jelenlegi tárgy létrehozása előtt létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="f1d4e-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f1d4e-129">-Description</span></span>
<span data-ttu-id="f1d4e-130">A tárgy leírása.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="f1d4e-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1d4e-131">-Name</span></span>
<span data-ttu-id="f1d4e-132">A tárgy neve</span><span class="sxs-lookup"><span data-stu-id="f1d4e-132">Name of the artifact</span></span>

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

### <span data-ttu-id="f1d4e-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f1d4e-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="f1d4e-134">A házirend definíciójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="f1d4e-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="f1d4e-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="f1d4e-136">Hashtable a házirend-definíciós tárgyhoz való továbbításhoz.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="f1d4e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1d4e-137">-ResourceGroupName</span></span>
<span data-ttu-id="f1d4e-138">Annak az erőforráscsoportnek a neve, amely a tárgyat fogja használni.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="f1d4e-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f1d4e-139">-RoleDefinitionId</span></span>
<span data-ttu-id="f1d4e-140">A szerepkör-definíciók listája</span><span class="sxs-lookup"><span data-stu-id="f1d4e-140">List of role definition</span></span>

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

### <span data-ttu-id="f1d4e-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="f1d4e-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="f1d4e-142">A szerepkör-definíciós fő azonosítók listája.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="f1d4e-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f1d4e-143">-TemplateFile</span></span>
<span data-ttu-id="f1d4e-144">A kar sablonfájlt tartalmazó fájl helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="f1d4e-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f1d4e-145">-TemplateParameterFile</span></span>
<span data-ttu-id="f1d4e-146">A ARM template paraméter fájljának helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="f1d4e-147">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="f1d4e-147">-Type</span></span>
<span data-ttu-id="f1d4e-148">A tárgy típusa.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-148">Type of the artifact.</span></span>
<span data-ttu-id="f1d4e-149">A következő 3 típus támogatott: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="f1d4e-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1d4e-150">-Confirm</span></span>
<span data-ttu-id="f1d4e-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1d4e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1d4e-152">-WhatIf</span></span>
<span data-ttu-id="f1d4e-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1d4e-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1d4e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d4e-155">CommonParameters</span></span>
<span data-ttu-id="f1d4e-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1d4e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d4e-157">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f1d4e-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d4e-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1d4e-158">INPUTS</span></span>

### <span data-ttu-id="f1d4e-159">System. String</span><span class="sxs-lookup"><span data-stu-id="f1d4e-159">System.String</span></span>

### <span data-ttu-id="f1d4e-160">Microsoft. Azure. commands. Blueprint. models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="f1d4e-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="f1d4e-161">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="f1d4e-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="f1d4e-162">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f1d4e-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f1d4e-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1d4e-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f1d4e-164">System. string []</span><span class="sxs-lookup"><span data-stu-id="f1d4e-164">System.String[]</span></span>

## <span data-ttu-id="f1d4e-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1d4e-165">OUTPUTS</span></span>

### <span data-ttu-id="f1d4e-166">Microsoft. Azure. Management. Blueprint. models. ereklyét</span><span class="sxs-lookup"><span data-stu-id="f1d4e-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="f1d4e-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1d4e-167">NOTES</span></span>

## <span data-ttu-id="f1d4e-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1d4e-168">RELATED LINKS</span></span>
