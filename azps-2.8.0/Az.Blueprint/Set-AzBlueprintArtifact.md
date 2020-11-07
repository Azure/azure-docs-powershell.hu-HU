---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 6bd05fc372afc6ef04c943906de8b3eb99cc0aa5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667630"
---
# <span data-ttu-id="08580-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="08580-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="08580-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08580-102">SYNOPSIS</span></span>
<span data-ttu-id="08580-103">A tervrajz definíciójában lévő tárgy frissítése</span><span class="sxs-lookup"><span data-stu-id="08580-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="08580-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08580-104">SYNTAX</span></span>


### <span data-ttu-id="08580-105">UpdateTemplateArtifact (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08580-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08580-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="08580-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08580-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="08580-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08580-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="08580-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08580-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="08580-109">DESCRIPTION</span></span>
<span data-ttu-id="08580-110">Frissítsen egy tárgyat.</span><span class="sxs-lookup"><span data-stu-id="08580-110">Update an artifact.</span></span> <span data-ttu-id="08580-111">A tárgyat kétféleképpen frissítheti: vagy a JSON-ot beviteli fájlként vagy a tárgyhoz tartozó szövegközi paramétereket biztosítva.</span><span class="sxs-lookup"><span data-stu-id="08580-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="08580-112">A JSON-metódusban nem szükséges, hogy a szövegközi paramétert tartalmazó típus típusa legyen a felhasználónak, hogy a tárgy típusa paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="08580-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="08580-113">Példák</span><span class="sxs-lookup"><span data-stu-id="08580-113">EXAMPLES</span></span>

### <span data-ttu-id="08580-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08580-114">Example 1</span></span>
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

<span data-ttu-id="08580-115">A leletek JSON-fájlon keresztül frissíthetők.</span><span class="sxs-lookup"><span data-stu-id="08580-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="08580-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="08580-116">Example 2</span></span>
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

<span data-ttu-id="08580-117">Egy tárgy frissítése szövegközi paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="08580-117">Update an artifact through inline parameters.</span></span>


### <span data-ttu-id="08580-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="08580-118">Example 3</span></span>
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

<span data-ttu-id="08580-119">Frissítsen egy tárgyat egy ARM-sablonfájl segítségével.</span><span class="sxs-lookup"><span data-stu-id="08580-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="08580-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08580-120">PARAMETERS</span></span>

### <span data-ttu-id="08580-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="08580-121">-ArtifactFile</span></span>
<span data-ttu-id="08580-122">A tárgy fájl helye JSON formátumban a lemezen</span><span class="sxs-lookup"><span data-stu-id="08580-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="08580-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="08580-123">-Blueprint</span></span>
<span data-ttu-id="08580-124">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="08580-124">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, ArtifactsByBlueprint, CreateRoleAssignmentArtifact, CreatePolicyArtifact
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

### <span data-ttu-id="08580-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08580-125">-DefaultProfile</span></span>
<span data-ttu-id="08580-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08580-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08580-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="08580-127">-DependsOn</span></span>
<span data-ttu-id="08580-128">Azoknak az eltéréseknek a listája, amelyeket a jelenlegi tárgy létrehozása előtt létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="08580-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="08580-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="08580-129">-Description</span></span>
<span data-ttu-id="08580-130">A tárgy leírása.</span><span class="sxs-lookup"><span data-stu-id="08580-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="08580-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08580-131">-Name</span></span>
<span data-ttu-id="08580-132">A tárgy neve</span><span class="sxs-lookup"><span data-stu-id="08580-132">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateArtifactByInputFile, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="08580-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="08580-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="08580-134">A házirend definíciójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="08580-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="08580-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="08580-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="08580-136">Hashtable a házirend-definíciós tárgyhoz való továbbításhoz.</span><span class="sxs-lookup"><span data-stu-id="08580-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="08580-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08580-137">-ResourceGroupName</span></span>
<span data-ttu-id="08580-138">Annak az erőforráscsoportnek a neve, amely a tárgyat fogja használni.</span><span class="sxs-lookup"><span data-stu-id="08580-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="08580-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="08580-139">-RoleDefinitionId</span></span>
<span data-ttu-id="08580-140">A szerepkör-definíciók listája</span><span class="sxs-lookup"><span data-stu-id="08580-140">List of role definition</span></span>

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

### <span data-ttu-id="08580-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="08580-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="08580-142">A szerepkör-definíciós fő azonosítók listája.</span><span class="sxs-lookup"><span data-stu-id="08580-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="08580-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="08580-143">-TemplateFile</span></span>
<span data-ttu-id="08580-144">A kar sablonfájlt tartalmazó fájl helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="08580-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="08580-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="08580-145">-TemplateParameterFile</span></span>
<span data-ttu-id="08580-146">A ARM template paraméter fájljának helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="08580-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="08580-147">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="08580-147">-Type</span></span>
<span data-ttu-id="08580-148">A tárgy típusa.</span><span class="sxs-lookup"><span data-stu-id="08580-148">Type of the artifact.</span></span>
<span data-ttu-id="08580-149">A következő 3 típus támogatott: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="08580-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="08580-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08580-150">CommonParameters</span></span>
<span data-ttu-id="08580-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08580-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="08580-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08580-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08580-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08580-153">INPUTS</span></span>

### <span data-ttu-id="08580-154">System. String</span><span class="sxs-lookup"><span data-stu-id="08580-154">System.String</span></span>

### <span data-ttu-id="08580-155">Microsoft. Azure. commands. Blueprint. models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="08580-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="08580-156">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="08580-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="08580-157">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="08580-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="08580-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="08580-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="08580-159">System. string []</span><span class="sxs-lookup"><span data-stu-id="08580-159">System.String[]</span></span>

## <span data-ttu-id="08580-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08580-160">OUTPUTS</span></span>

### <span data-ttu-id="08580-161">Microsoft. Azure. Management. Blueprint. models. ereklyét</span><span class="sxs-lookup"><span data-stu-id="08580-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="08580-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08580-162">NOTES</span></span>

## <span data-ttu-id="08580-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08580-163">RELATED LINKS</span></span>
