---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 09b0a1a6691b4c3d491d15d226fb8260fb7ae00e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301109"
---
# <span data-ttu-id="cb22d-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="cb22d-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="cb22d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb22d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb22d-103">Egy ARM-sablon beolvasása What-If eredmény a bevezetéshez az erőforráscsoport hatókörében.</span><span class="sxs-lookup"><span data-stu-id="cb22d-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="cb22d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb22d-104">SYNTAX</span></span>

### <span data-ttu-id="cb22d-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb22d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb22d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb22d-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb22d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb22d-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb22d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb22d-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb22d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb22d-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb22d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb22d-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb22d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb22d-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb22d-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb22d-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb22d-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb22d-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb22d-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb22d-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb22d-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="cb22d-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb22d-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="cb22d-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb22d-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb22d-117">DESCRIPTION</span></span>
<span data-ttu-id="cb22d-118">A **Get-AzResourceGroupDeploymentWhatIfResult** parancsmag beilleszti a kar sablonját, What-If a megadott erőforráscsoport-tartományba tartozó sablonok bevezetésének eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="cb22d-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="cb22d-119">A módosítások listáját jeleníti meg, amely azt jelzi, hogy milyen erőforrások fognak frissülni, ha a telepítés a valós erőforrások módosítása nélkül lép érvénybe.</span><span class="sxs-lookup"><span data-stu-id="cb22d-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="cb22d-120">Ha meg szeretné adni a visszatérési eredmény formátumát, használja a *ResultFormat* paramétert.</span><span class="sxs-lookup"><span data-stu-id="cb22d-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="cb22d-121">Példák</span><span class="sxs-lookup"><span data-stu-id="cb22d-121">EXAMPLES</span></span>

### <span data-ttu-id="cb22d-122">Példa 1: What-If eredmény beszerzése erőforráscsoport-hatókörben</span><span class="sxs-lookup"><span data-stu-id="cb22d-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="cb22d-123">Ez a parancs a megadott erőforráscsoport-hatókörben a What-If eredményét adja meg egy egyéni sablonfájl és egy, a lemezen lévő paramétert tartalmazó fájl használatával.</span><span class="sxs-lookup"><span data-stu-id="cb22d-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="cb22d-124">A parancs a *ResourceGroupName* paraméterrel megadhatja azt az erőforráscsoport-csoportot, amelyben a sablont telepítik.</span><span class="sxs-lookup"><span data-stu-id="cb22d-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="cb22d-125">A parancs a *TemplateFile* paramétert használja a sablonfájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="cb22d-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="cb22d-126">A parancs a *TemplateParameterFile* paramétert használva adja meg a sablon paramétereit tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="cb22d-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="cb22d-127">A parancs a *ResultFormat* paramétert használja a teljes erőforrás-tartalmakat tartalmazó What-If eredmény beállításához.</span><span class="sxs-lookup"><span data-stu-id="cb22d-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="cb22d-128">2. példa: What-If eredményének beszerzése erőforráscsoport-hatókörben a ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="cb22d-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="cb22d-129">Ez a parancs a megadott erőforráscsoport-hatókörben a What-If eredményét adja meg egy egyéni sablonfájl és egy, a lemezen lévő paramétert tartalmazó fájl használatával.</span><span class="sxs-lookup"><span data-stu-id="cb22d-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="cb22d-130">A parancs a *ResourceGroupName* paraméterrel megadhatja azt az erőforráscsoport-csoportot, amelyben a sablont telepítik.</span><span class="sxs-lookup"><span data-stu-id="cb22d-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="cb22d-131">A parancs a *TemplateFile* paramétert használja a sablonfájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="cb22d-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="cb22d-132">A parancs a *TemplateParameterFile* paramétert használva adja meg a sablon paramétereit tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="cb22d-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="cb22d-133">A parancs a *ResultFormat* paramétert használja a What-If eredményének beállításához, hogy csak az erőforrás-azonosítókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cb22d-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="cb22d-134">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb22d-134">PARAMETERS</span></span>

### <span data-ttu-id="cb22d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb22d-135">-DefaultProfile</span></span>
<span data-ttu-id="cb22d-136">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb22d-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb22d-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="cb22d-137">-ExcludeChangeType</span></span>
<span data-ttu-id="cb22d-138">Vesszővel elválasztott erőforrás-módosítási típusokat kell kizárni What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="cb22d-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb22d-139">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="cb22d-139">-Mode</span></span>
<span data-ttu-id="cb22d-140">A központi telepítő üzemmód.</span><span class="sxs-lookup"><span data-stu-id="cb22d-140">The deployment mode.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb22d-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb22d-141">-Name</span></span>
<span data-ttu-id="cb22d-142">Annak a telepítőnek a neve, amelyet létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="cb22d-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="cb22d-143">Ha nem adja meg, akkor az alapértelmezett érték a sablonfájl nevében, amikor a sablonfájl meg van adva. Alapértelmezés szerint az aktuális időpontot kapja, ha a Template-objektum meg van határozva, például "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="cb22d-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb22d-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="cb22d-144">-Pre</span></span>
<span data-ttu-id="cb22d-145">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="cb22d-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="cb22d-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb22d-146">-ResourceGroupName</span></span>
<span data-ttu-id="cb22d-147">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cb22d-147">The resource group name.</span></span>

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

### <span data-ttu-id="cb22d-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="cb22d-148">-ResultFormat</span></span>
<span data-ttu-id="cb22d-149">A What-If eredmény formátuma.</span><span class="sxs-lookup"><span data-stu-id="cb22d-149">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb22d-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="cb22d-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="cb22d-151">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="cb22d-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="cb22d-152">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="cb22d-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="cb22d-153">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="cb22d-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="cb22d-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="cb22d-154">-TemplateFile</span></span>
<span data-ttu-id="cb22d-155">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="cb22d-155">Local path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb22d-156">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="cb22d-156">-TemplateObject</span></span>
<span data-ttu-id="cb22d-157">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="cb22d-157">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb22d-158">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="cb22d-158">-TemplateParameterFile</span></span>
<span data-ttu-id="cb22d-159">A sablon paramétereit tartalmazó fájl</span><span class="sxs-lookup"><span data-stu-id="cb22d-159">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb22d-160">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="cb22d-160">-TemplateParameterObject</span></span>
<span data-ttu-id="cb22d-161">A paramétereket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="cb22d-161">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb22d-162">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="cb22d-162">-TemplateParameterUri</span></span>
<span data-ttu-id="cb22d-163">URI a sablon paraméter-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="cb22d-163">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb22d-164">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="cb22d-164">-TemplateUri</span></span>
<span data-ttu-id="cb22d-165">A sablonfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="cb22d-165">Uri to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb22d-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb22d-166">CommonParameters</span></span>
<span data-ttu-id="cb22d-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb22d-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb22d-168">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cb22d-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb22d-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb22d-169">INPUTS</span></span>

### <span data-ttu-id="cb22d-170">System. String</span><span class="sxs-lookup"><span data-stu-id="cb22d-170">System.String</span></span>

### <span data-ttu-id="cb22d-171">Microsoft. Azure. Management. ResourceManager. models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="cb22d-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="cb22d-172">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cb22d-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cb22d-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb22d-173">OUTPUTS</span></span>

### <span data-ttu-id="cb22d-174">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. bevezetés. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="cb22d-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="cb22d-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb22d-175">NOTES</span></span>

## <span data-ttu-id="cb22d-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb22d-176">RELATED LINKS</span></span>
