---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 39b652f1e6096f74da8d23baee10cd5b2ce54b6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184224"
---
# <span data-ttu-id="07125-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="07125-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="07125-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07125-102">SYNOPSIS</span></span>
<span data-ttu-id="07125-103">ARM-sablont kap What-If eredmény a felügyeleti csoport hatókörének kiépítéséhez.</span><span class="sxs-lookup"><span data-stu-id="07125-103">Gets an ARM template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="07125-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07125-104">SYNTAX</span></span>

### <span data-ttu-id="07125-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07125-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07125-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="07125-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07125-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="07125-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07125-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="07125-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07125-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="07125-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07125-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="07125-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07125-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="07125-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07125-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="07125-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07125-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="07125-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07125-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="07125-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07125-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="07125-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07125-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="07125-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07125-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="07125-117">DESCRIPTION</span></span>
<span data-ttu-id="07125-118">A **Get-AzManagementGroupDeploymentWhatIfResult** parancsmag beilleszti a kar sablonját, What-If a megadott felügyeleti csoport hatókörének egy sablonba való bevezetésének eredményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="07125-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="07125-119">A módosítások listáját jeleníti meg, amely azt jelzi, hogy milyen erőforrások fognak frissülni, ha a telepítés a valós erőforrások módosítása nélkül lép érvénybe.</span><span class="sxs-lookup"><span data-stu-id="07125-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="07125-120">Ha meg szeretné adni a visszatérési eredmény formátumát, használja a *ResultFormat* paramétert.</span><span class="sxs-lookup"><span data-stu-id="07125-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="07125-121">Példák</span><span class="sxs-lookup"><span data-stu-id="07125-121">EXAMPLES</span></span>

### <span data-ttu-id="07125-122">Példa 1: What-If eredményének beszerzése a felügyeleti csoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="07125-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="07125-123">Ez a parancs egy egyéni sablonfájl és egy, a lemezen lévő paraméteres fájl segítségével What-If eredményét kapja a felügyeleti csoport hatókörében.</span><span class="sxs-lookup"><span data-stu-id="07125-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="07125-124">A parancs a hely paramétert használva adja meg a központi telepítő adatainak tárolásának *helyét* .</span><span class="sxs-lookup"><span data-stu-id="07125-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="07125-125">A parancs a *ManagementGroupId* paraméterrel adja meg azt a kezelési csoportot, amelyben a sablont telepítik.</span><span class="sxs-lookup"><span data-stu-id="07125-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="07125-126">A parancs a *TemplateFile* paramétert használja a sablonfájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="07125-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="07125-127">A parancs a *TemplateParameterFile* paramétert használva adja meg a sablon paramétereit tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="07125-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="07125-128">A parancs a *ResultFormat* paramétert használja a teljes erőforrás-tartalmakat tartalmazó What-If eredmény beállításához.</span><span class="sxs-lookup"><span data-stu-id="07125-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="07125-129">2. példa: What-If eredményének beszerzése a felügyeleti csoport hatókörében a ResourceIdOnly használatával</span><span class="sxs-lookup"><span data-stu-id="07125-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="07125-130">Ez a parancs egy egyéni sablonfájl és egy, a lemezen lévő paraméteres fájl segítségével What-If eredményét kapja a felügyeleti csoport hatókörében.</span><span class="sxs-lookup"><span data-stu-id="07125-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="07125-131">A parancs a hely paramétert használva adja meg a központi telepítő adatainak tárolásának *helyét* .</span><span class="sxs-lookup"><span data-stu-id="07125-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="07125-132">A parancs a *ManagementGroupId* paraméterrel adja meg azt a kezelési csoportot, amelyben a sablont telepítik.</span><span class="sxs-lookup"><span data-stu-id="07125-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="07125-133">A parancs a *TemplateFile* paramétert használja a sablonfájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="07125-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="07125-134">A parancs a *TemplateParameterFile* paramétert használva adja meg a sablon paramétereit tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="07125-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="07125-135">A parancs a *ResultFormat* paramétert használja a What-If eredményének beállításához, hogy csak az erőforrás-azonosítókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="07125-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="07125-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07125-136">PARAMETERS</span></span>

### <span data-ttu-id="07125-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="07125-137">-ApiVersion</span></span>
<span data-ttu-id="07125-138">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07125-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="07125-139">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="07125-139">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07125-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07125-140">-DefaultProfile</span></span>
<span data-ttu-id="07125-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07125-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07125-142">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="07125-142">-ExcludeChangeType</span></span>
<span data-ttu-id="07125-143">Az erőforrás-módosítási típusok vesszővel elválasztott listája, amelyet ki kell zárni What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="07125-143">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="07125-144">-Hely</span><span class="sxs-lookup"><span data-stu-id="07125-144">-Location</span></span>
<span data-ttu-id="07125-145">A központi telepítő adatainak tárolására szolgáló hely.</span><span class="sxs-lookup"><span data-stu-id="07125-145">The location to store deployment data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07125-146">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="07125-146">-ManagementGroupId</span></span>
<span data-ttu-id="07125-147">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="07125-147">The management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07125-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="07125-148">-Name</span></span>
<span data-ttu-id="07125-149">Annak a telepítőnek a neve, amelyet létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="07125-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="07125-150">Ha nem adja meg, akkor az alapértelmezett érték a sablonfájl nevében, amikor a sablonfájl meg van adva. Alapértelmezés szerint az aktuális időpontot kapja, ha a Template-objektum meg van határozva, például "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="07125-150">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07125-151">-Pre</span><span class="sxs-lookup"><span data-stu-id="07125-151">-Pre</span></span>
<span data-ttu-id="07125-152">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="07125-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="07125-153">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="07125-153">-ResultFormat</span></span>
<span data-ttu-id="07125-154">A What-If eredmény formátuma.</span><span class="sxs-lookup"><span data-stu-id="07125-154">The What-If result format.</span></span>

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

### <span data-ttu-id="07125-155">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="07125-155">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="07125-156">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="07125-156">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="07125-157">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="07125-157">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="07125-158">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="07125-158">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="07125-159">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="07125-159">-TemplateFile</span></span>
<span data-ttu-id="07125-160">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="07125-160">Local path to the template file.</span></span>

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

### <span data-ttu-id="07125-161">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="07125-161">-TemplateObject</span></span>
<span data-ttu-id="07125-162">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="07125-162">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="07125-163">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="07125-163">-TemplateParameterFile</span></span>
<span data-ttu-id="07125-164">A sablon paramétereit tartalmazó fájl</span><span class="sxs-lookup"><span data-stu-id="07125-164">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="07125-165">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="07125-165">-TemplateParameterObject</span></span>
<span data-ttu-id="07125-166">A paramétereket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="07125-166">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="07125-167">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="07125-167">-TemplateParameterUri</span></span>
<span data-ttu-id="07125-168">URI a sablon paraméter-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="07125-168">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="07125-169">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="07125-169">-TemplateUri</span></span>
<span data-ttu-id="07125-170">A sablonfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="07125-170">Uri to the template file.</span></span>

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

### <span data-ttu-id="07125-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07125-171">CommonParameters</span></span>
<span data-ttu-id="07125-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07125-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07125-173">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07125-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07125-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07125-174">INPUTS</span></span>

### <span data-ttu-id="07125-175">System. String</span><span class="sxs-lookup"><span data-stu-id="07125-175">System.String</span></span>

### <span data-ttu-id="07125-176">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="07125-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="07125-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07125-177">OUTPUTS</span></span>

### <span data-ttu-id="07125-178">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. bevezetés. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="07125-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="07125-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07125-179">NOTES</span></span>

## <span data-ttu-id="07125-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07125-180">RELATED LINKS</span></span>
