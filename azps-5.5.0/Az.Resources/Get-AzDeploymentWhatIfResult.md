---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 0ad3df8e010beec777bd059bbef708774570792d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206023"
---
# <span data-ttu-id="1d2ca-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="1d2ca-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="1d2ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="1d2ca-103">Egy ARM sablont What-If az előfizetés hatókörében való telepítés eredményéhez.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="1d2ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d2ca-104">SYNTAX</span></span>

### <span data-ttu-id="1d2ca-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d2ca-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1d2ca-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1d2ca-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1d2ca-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1d2ca-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1d2ca-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1d2ca-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1d2ca-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1d2ca-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1d2ca-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1d2ca-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2ca-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1d2ca-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d2ca-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d2ca-117">DESCRIPTION</span></span>
<span data-ttu-id="1d2ca-118">A **Get-AzDeploymentWhatIfResult** parancsmag a ARM sablont What-If az aktuális előfizetési hatókörű sablontelepítés eredményéhez.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="1d2ca-119">Visszaadja a módosítások listáját, jelezve, hogy mely erőforrások lesznek frissítve, ha a telepítést a tényleges erőforrások változtatása nélkül alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="1d2ca-120">Az eredmény formátumának megadásához használja a *ResultFormat paramétert.*</span><span class="sxs-lookup"><span data-stu-id="1d2ca-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="1d2ca-121">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d2ca-121">EXAMPLES</span></span>

### <span data-ttu-id="1d2ca-122">1. példa: Új What-If az előfizetés hatókörében</span><span class="sxs-lookup"><span data-stu-id="1d2ca-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="1d2ca-123">Ez a parancs egy egyéni sablonfájl és egy lemezen található paraméterfájl használatával What-If találatot az aktuális előfizetés hatókörében.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="1d2ca-124">A parancs a *Hely paraméterrel* adja meg, hogy hol tárolja a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="1d2ca-125">A parancs a *TemplateFile paraméterrel* adja meg a sablonfájlt.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="1d2ca-126">A parancs a *TemplateParameterFile paraméterrel* adja meg a sablon paraméterfájlját.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="1d2ca-127">A parancs a *ResultFormat* paraméter segítségével úgy What-If, hogy az tartalmazza a teljes erőforrás-hasznos adatokat.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="1d2ca-128">2. példa: Új What-If az előfizetés hatókörében a ResourceIdOnlyval</span><span class="sxs-lookup"><span data-stu-id="1d2ca-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="1d2ca-129">Ez a parancs What-If az előfizetés aktuális hatókörében egy egyéni sablonfájl és egy paraméterfájl használatával a lemezen.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="1d2ca-130">A parancs a *Hely paraméter* segítségével adja meg, hogy hol tárolja a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="1d2ca-131">A parancs a *TemplateFile paraméterrel* adja meg a sablonfájlt.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="1d2ca-132">A parancs a *TemplateParameterFile paraméterrel* adja meg a sablon paraméterfájlját.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="1d2ca-133">A parancs a *ResultFormat* paraméter segítségével úgy What-If, hogy az csak erőforrás-adatokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="1d2ca-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d2ca-134">PARAMETERS</span></span>

### <span data-ttu-id="1d2ca-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d2ca-135">-DefaultProfile</span></span>
<span data-ttu-id="1d2ca-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d2ca-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="1d2ca-137">-ExcludeChangeType</span></span>
<span data-ttu-id="1d2ca-138">Azon erőforrás-módosítási típusok vesszővel elválasztott listája, amelyek nem tartoznak az What-If eredménybe.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="1d2ca-139">-Location</span><span class="sxs-lookup"><span data-stu-id="1d2ca-139">-Location</span></span>
<span data-ttu-id="1d2ca-140">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="1d2ca-141">-Name</span><span class="sxs-lookup"><span data-stu-id="1d2ca-141">-Name</span></span>
<span data-ttu-id="1d2ca-142">Annak a telepítésnek a neve, amelyből létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="1d2ca-143">Ha nincs megadva, akkor a sablonfájl alapértelmezett neve, ha sablonfájlt ad meg; sablonobjektumok (például "2013123140835") beállítása.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="1d2ca-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="1d2ca-144">-Pre</span></span>
<span data-ttu-id="1d2ca-145">Ha be van állítva, az azt jelenti, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1d2ca-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="1d2ca-146">-ResultFormat</span></span>
<span data-ttu-id="1d2ca-147">A What-If formátuma.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-147">The What-If result format.</span></span>

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

### <span data-ttu-id="1d2ca-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="1d2ca-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="1d2ca-149">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="1d2ca-150">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="1d2ca-151">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="1d2ca-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1d2ca-152">-TemplateFile</span></span>
<span data-ttu-id="1d2ca-153">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="1d2ca-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="1d2ca-154">-TemplateObject</span></span>
<span data-ttu-id="1d2ca-155">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="1d2ca-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1d2ca-156">-TemplateParameterFile</span></span>
<span data-ttu-id="1d2ca-157">Olyan fájl, amely a sablon paramétereit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="1d2ca-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="1d2ca-158">-TemplateParameterObject</span></span>
<span data-ttu-id="1d2ca-159">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="1d2ca-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="1d2ca-160">-TemplateParameterUri</span></span>
<span data-ttu-id="1d2ca-161">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="1d2ca-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="1d2ca-162">-TemplateUri</span></span>
<span data-ttu-id="1d2ca-163">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="1d2ca-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d2ca-164">CommonParameters</span></span>
<span data-ttu-id="1d2ca-165">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d2ca-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d2ca-166">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d2ca-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d2ca-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d2ca-167">INPUTS</span></span>

### <span data-ttu-id="1d2ca-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1d2ca-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1d2ca-169">System.String</span><span class="sxs-lookup"><span data-stu-id="1d2ca-169">System.String</span></span>

## <span data-ttu-id="1d2ca-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d2ca-170">OUTPUTS</span></span>

### <span data-ttu-id="1d2ca-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="1d2ca-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="1d2ca-172">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d2ca-172">NOTES</span></span>

## <span data-ttu-id="1d2ca-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d2ca-173">RELATED LINKS</span></span>
