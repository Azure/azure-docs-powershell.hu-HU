---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 09b0a1a6691b4c3d491d15d226fb8260fb7ae00e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340494"
---
# <span data-ttu-id="f2353-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f2353-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="f2353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2353-102">SYNOPSIS</span></span>
<span data-ttu-id="f2353-103">Egy ARM sablont What-If az erőforráscsoport hatókörében való telepítés eredményéhez.</span><span class="sxs-lookup"><span data-stu-id="f2353-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="f2353-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2353-104">SYNTAX</span></span>

### <span data-ttu-id="f2353-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2353-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2353-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f2353-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2353-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f2353-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2353-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f2353-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2353-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f2353-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2353-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f2353-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2353-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f2353-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2353-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f2353-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2353-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f2353-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2353-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f2353-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2353-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f2353-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2353-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f2353-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2353-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2353-117">DESCRIPTION</span></span>
<span data-ttu-id="f2353-118">A **Get-AzResourceGroupDeploymentWhatIfResult** parancsmag megkapja a ARM sablon What-If egy sablon telepítésének eredményét a megadott erőforráscsoport-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="f2353-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="f2353-119">Visszaadja a módosítások listáját, jelezve, hogy mely erőforrások lesznek frissítve, ha a telepítést a tényleges erőforrások változtatása nélkül alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="f2353-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="f2353-120">Az eredmény formátumának megadásához használja a *ResultFormat paramétert.*</span><span class="sxs-lookup"><span data-stu-id="f2353-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="f2353-121">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2353-121">EXAMPLES</span></span>

### <span data-ttu-id="f2353-122">1. példa: What-If eredmény az erőforráscsoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="f2353-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="f2353-123">Ez a parancs What-If egy egyéni sablonfájl és egy lemezen található paraméterfájl használatával a megadott erőforráscsoport hatókörében egy új eredményt kap.</span><span class="sxs-lookup"><span data-stu-id="f2353-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="f2353-124">A parancs az *ResourceGroupName* paraméter segítségével megadja azt az erőforráscsoportot, amelyben a sablont telepíteni fogja.</span><span class="sxs-lookup"><span data-stu-id="f2353-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="f2353-125">A parancs a *TemplateFile paraméterrel* adja meg a sablonfájlt.</span><span class="sxs-lookup"><span data-stu-id="f2353-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="f2353-126">A parancs a *TemplateParameterFile paraméterrel* adja meg a sablon paraméterfájlját.</span><span class="sxs-lookup"><span data-stu-id="f2353-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="f2353-127">A parancs a *ResultFormat* paraméter segítségével úgy What-If, hogy az tartalmazza a teljes erőforrás-terhelést.</span><span class="sxs-lookup"><span data-stu-id="f2353-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="f2353-128">2. példa: Eredmény What-If erőforráscsoport hatókörében az ResourceIdOnlyval</span><span class="sxs-lookup"><span data-stu-id="f2353-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="f2353-129">Ez a parancs What-If egy egyéni sablonfájl és egy lemezen található paraméterfájl használatával a megadott erőforráscsoport hatókörében egy új eredményt kap.</span><span class="sxs-lookup"><span data-stu-id="f2353-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="f2353-130">A parancs az *ResourceGroupName* paraméter segítségével megadja azt az erőforráscsoportot, amelyben a sablont telepíteni fogja.</span><span class="sxs-lookup"><span data-stu-id="f2353-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="f2353-131">A parancs a *TemplateFile paraméterrel* adja meg a sablonfájlt.</span><span class="sxs-lookup"><span data-stu-id="f2353-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="f2353-132">A parancs a *TemplateParameterFile paraméterrel* adja meg a sablon paraméterfájlját.</span><span class="sxs-lookup"><span data-stu-id="f2353-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="f2353-133">A parancs a *ResultFormat* paraméter segítségével úgy What-If, hogy az csak erőforrás-adatokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="f2353-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="f2353-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2353-134">PARAMETERS</span></span>

### <span data-ttu-id="f2353-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2353-135">-DefaultProfile</span></span>
<span data-ttu-id="f2353-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2353-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2353-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="f2353-137">-ExcludeChangeType</span></span>
<span data-ttu-id="f2353-138">A vesszővel elválasztott erőforrás-módosítási típusokat nem lehet kizárni a What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="f2353-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="f2353-139">-Mód</span><span class="sxs-lookup"><span data-stu-id="f2353-139">-Mode</span></span>
<span data-ttu-id="f2353-140">A telepítési mód.</span><span class="sxs-lookup"><span data-stu-id="f2353-140">The deployment mode.</span></span>

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

### <span data-ttu-id="f2353-141">-Name</span><span class="sxs-lookup"><span data-stu-id="f2353-141">-Name</span></span>
<span data-ttu-id="f2353-142">Annak a telepítésnek a neve, amelyből létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="f2353-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="f2353-143">Ha nincs megadva, alapértelmezés szerint a sablonfájl neve lesz megadva; sablonobjektumok (például "2013123140835") beállítása.</span><span class="sxs-lookup"><span data-stu-id="f2353-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="f2353-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="f2353-144">-Pre</span></span>
<span data-ttu-id="f2353-145">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f2353-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f2353-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2353-146">-ResourceGroupName</span></span>
<span data-ttu-id="f2353-147">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2353-147">The resource group name.</span></span>

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

### <span data-ttu-id="f2353-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="f2353-148">-ResultFormat</span></span>
<span data-ttu-id="f2353-149">A What-If formátuma.</span><span class="sxs-lookup"><span data-stu-id="f2353-149">The What-If result format.</span></span>

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

### <span data-ttu-id="f2353-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="f2353-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="f2353-151">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="f2353-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="f2353-152">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="f2353-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="f2353-153">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="f2353-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="f2353-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f2353-154">-TemplateFile</span></span>
<span data-ttu-id="f2353-155">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f2353-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="f2353-156">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="f2353-156">-TemplateObject</span></span>
<span data-ttu-id="f2353-157">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="f2353-157">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="f2353-158">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f2353-158">-TemplateParameterFile</span></span>
<span data-ttu-id="f2353-159">Olyan fájl, amely rendelkezik a sablonparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="f2353-159">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="f2353-160">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f2353-160">-TemplateParameterObject</span></span>
<span data-ttu-id="f2353-161">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="f2353-161">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="f2353-162">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f2353-162">-TemplateParameterUri</span></span>
<span data-ttu-id="f2353-163">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="f2353-163">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="f2353-164">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f2353-164">-TemplateUri</span></span>
<span data-ttu-id="f2353-165">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="f2353-165">Uri to the template file.</span></span>

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

### <span data-ttu-id="f2353-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2353-166">CommonParameters</span></span>
<span data-ttu-id="f2353-167">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2353-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2353-168">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2353-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2353-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2353-169">INPUTS</span></span>

### <span data-ttu-id="f2353-170">System.String</span><span class="sxs-lookup"><span data-stu-id="f2353-170">System.String</span></span>

### <span data-ttu-id="f2353-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="f2353-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="f2353-172">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f2353-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f2353-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2353-173">OUTPUTS</span></span>

### <span data-ttu-id="f2353-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="f2353-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="f2353-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2353-175">NOTES</span></span>

## <span data-ttu-id="f2353-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2353-176">RELATED LINKS</span></span>
