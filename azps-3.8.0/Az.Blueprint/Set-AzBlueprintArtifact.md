---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: c71a587dc755ae1834198f14142d5a511fe17ea2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010987"
---
# <span data-ttu-id="6ad5d-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="6ad5d-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="6ad5d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ad5d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad5d-103">A tervrajz definíciójában lévő tárgy frissítése</span><span class="sxs-lookup"><span data-stu-id="6ad5d-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="6ad5d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ad5d-104">SYNTAX</span></span>


### <span data-ttu-id="6ad5d-105">UpdateTemplateArtifact (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ad5d-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad5d-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="6ad5d-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad5d-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="6ad5d-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad5d-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="6ad5d-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ad5d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ad5d-109">DESCRIPTION</span></span>
<span data-ttu-id="6ad5d-110">Frissítsen egy tárgyat.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-110">Update an artifact.</span></span> <span data-ttu-id="6ad5d-111">A tárgyat kétféleképpen frissítheti: vagy a JSON-ot beviteli fájlként vagy a tárgyhoz tartozó szövegközi paramétereket biztosítva.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="6ad5d-112">A JSON-metódusban nem szükséges, hogy a szövegközi paramétert tartalmazó típus típusa legyen a felhasználónak, hogy a tárgy típusa paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="6ad5d-113">Példák</span><span class="sxs-lookup"><span data-stu-id="6ad5d-113">EXAMPLES</span></span>

### <span data-ttu-id="6ad5d-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6ad5d-114">Example 1</span></span>
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

<span data-ttu-id="6ad5d-115">A leletek JSON-fájlon keresztül frissíthetők.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="6ad5d-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="6ad5d-116">Example 2</span></span>
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

<span data-ttu-id="6ad5d-117">Egy tárgy frissítése szövegközi paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-117">Update an artifact through inline parameters.</span></span>


### <span data-ttu-id="6ad5d-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="6ad5d-118">Example 3</span></span>
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

<span data-ttu-id="6ad5d-119">Frissítsen egy tárgyat egy ARM-sablonfájl segítségével.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="6ad5d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ad5d-120">PARAMETERS</span></span>

### <span data-ttu-id="6ad5d-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="6ad5d-121">-ArtifactFile</span></span>
<span data-ttu-id="6ad5d-122">A tárgy fájl helye JSON formátumban a lemezen</span><span class="sxs-lookup"><span data-stu-id="6ad5d-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="6ad5d-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="6ad5d-123">-Blueprint</span></span>
<span data-ttu-id="6ad5d-124">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-124">Blueprint object.</span></span>

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

### <span data-ttu-id="6ad5d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad5d-125">-DefaultProfile</span></span>
<span data-ttu-id="6ad5d-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad5d-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="6ad5d-127">-DependsOn</span></span>
<span data-ttu-id="6ad5d-128">Azoknak az eltéréseknek a listája, amelyeket a jelenlegi tárgy létrehozása előtt létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="6ad5d-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6ad5d-129">-Description</span></span>
<span data-ttu-id="6ad5d-130">A tárgy leírása.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="6ad5d-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ad5d-131">-Name</span></span>
<span data-ttu-id="6ad5d-132">A tárgy neve</span><span class="sxs-lookup"><span data-stu-id="6ad5d-132">Name of the artifact</span></span>

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

### <span data-ttu-id="6ad5d-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6ad5d-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="6ad5d-134">A házirend definíciójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="6ad5d-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="6ad5d-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="6ad5d-136">Hashtable a házirend-definíciós tárgyhoz való továbbításhoz.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="6ad5d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad5d-137">-ResourceGroupName</span></span>
<span data-ttu-id="6ad5d-138">Annak az erőforráscsoportnek a neve, amely a tárgyat fogja használni.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="6ad5d-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6ad5d-139">-RoleDefinitionId</span></span>
<span data-ttu-id="6ad5d-140">A szerepkör-definíciók listája</span><span class="sxs-lookup"><span data-stu-id="6ad5d-140">List of role definition</span></span>

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

### <span data-ttu-id="6ad5d-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="6ad5d-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="6ad5d-142">A szerepkör-definíciós fő azonosítók listája.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="6ad5d-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="6ad5d-143">-TemplateFile</span></span>
<span data-ttu-id="6ad5d-144">A kar sablonfájlt tartalmazó fájl helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="6ad5d-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="6ad5d-145">-TemplateParameterFile</span></span>
<span data-ttu-id="6ad5d-146">A ARM template paraméter fájljának helye a lemezen.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="6ad5d-147">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="6ad5d-147">-Type</span></span>
<span data-ttu-id="6ad5d-148">A tárgy típusa.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-148">Type of the artifact.</span></span>
<span data-ttu-id="6ad5d-149">A következő 3 típus támogatott: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="6ad5d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad5d-150">CommonParameters</span></span>
<span data-ttu-id="6ad5d-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ad5d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6ad5d-152">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad5d-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad5d-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ad5d-153">INPUTS</span></span>

### <span data-ttu-id="6ad5d-154">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad5d-154">System.String</span></span>

### <span data-ttu-id="6ad5d-155">Microsoft. Azure. commands. Blueprint. models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="6ad5d-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="6ad5d-156">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="6ad5d-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="6ad5d-157">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6ad5d-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6ad5d-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ad5d-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6ad5d-159">System. string []</span><span class="sxs-lookup"><span data-stu-id="6ad5d-159">System.String[]</span></span>

## <span data-ttu-id="6ad5d-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ad5d-160">OUTPUTS</span></span>

### <span data-ttu-id="6ad5d-161">Microsoft. Azure. Management. Blueprint. models. ereklyét</span><span class="sxs-lookup"><span data-stu-id="6ad5d-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="6ad5d-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ad5d-162">NOTES</span></span>

## <span data-ttu-id="6ad5d-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ad5d-163">RELATED LINKS</span></span>
