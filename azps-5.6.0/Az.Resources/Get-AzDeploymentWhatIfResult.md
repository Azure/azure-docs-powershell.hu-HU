---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 725984f8893b7373ded513b0d7242d9ec4bd0c6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935538"
---
# <span data-ttu-id="48dff-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="48dff-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="48dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48dff-102">SYNOPSIS</span></span>
<span data-ttu-id="48dff-103">Sablont What-If egy telepítéshez az előfizetés hatókörében.</span><span class="sxs-lookup"><span data-stu-id="48dff-103">Gets a template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="48dff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48dff-104">SYNTAX</span></span>

### <span data-ttu-id="48dff-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48dff-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="48dff-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="48dff-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="48dff-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="48dff-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="48dff-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="48dff-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="48dff-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="48dff-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="48dff-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="48dff-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dff-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="48dff-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48dff-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48dff-117">DESCRIPTION</span></span>
<span data-ttu-id="48dff-118">A **Get-AzDeploymentWhatIfResult** parancsmag megkapja a ARM sablont What-If az aktuális előfizetési hatókörű sablontelepítés eredményéhez.</span><span class="sxs-lookup"><span data-stu-id="48dff-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="48dff-119">Visszaadja a módosítások listáját, jelezve, hogy mely erőforrások lesznek frissítve, ha a telepítést a tényleges erőforrások változtatása nélkül alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="48dff-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="48dff-120">Az eredmény formátumának megadásához használja a *ResultFormat paramétert.*</span><span class="sxs-lookup"><span data-stu-id="48dff-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="48dff-121">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48dff-121">EXAMPLES</span></span>

### <span data-ttu-id="48dff-122">1. példa: Új What-If az előfizetés hatókörében</span><span class="sxs-lookup"><span data-stu-id="48dff-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="48dff-123">Ez a parancs egy egyéni sablonfájl és egy lemezen található paraméterfájl használatával What-If találatot az aktuális előfizetés hatókörében.</span><span class="sxs-lookup"><span data-stu-id="48dff-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="48dff-124">A parancs a *Hely paraméter* segítségével adja meg, hogy hol tárolja a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="48dff-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="48dff-125">A parancs a *TemplateFile paraméterrel* adja meg a sablonfájlt.</span><span class="sxs-lookup"><span data-stu-id="48dff-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="48dff-126">A parancs a *TemplateParameterFile paraméterrel* adja meg a sablon paraméterfájlját.</span><span class="sxs-lookup"><span data-stu-id="48dff-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="48dff-127">A parancs a *ResultFormat* paraméter segítségével úgy What-If, hogy az tartalmazza a teljes erőforrás-terhelést.</span><span class="sxs-lookup"><span data-stu-id="48dff-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="48dff-128">2. példa: Új What-If az előfizetés hatókörében a ResourceIdOnlyval</span><span class="sxs-lookup"><span data-stu-id="48dff-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="48dff-129">Ez a parancs egy egyéni sablonfájl és egy lemezen található paraméterfájl használatával What-If találatot az aktuális előfizetés hatókörében.</span><span class="sxs-lookup"><span data-stu-id="48dff-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="48dff-130">A parancs a *Hely paraméter* segítségével adja meg, hogy hol tárolja a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="48dff-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="48dff-131">A parancs a *TemplateFile paraméterrel* adja meg a sablonfájlt.</span><span class="sxs-lookup"><span data-stu-id="48dff-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="48dff-132">A parancs a *TemplateParameterFile paraméterrel* adja meg a sablon paraméterfájlját.</span><span class="sxs-lookup"><span data-stu-id="48dff-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="48dff-133">A parancs a *ResultFormat* paraméter segítségével úgy What-If, hogy az csak erőforrás-adatokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="48dff-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="48dff-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48dff-134">PARAMETERS</span></span>

### <span data-ttu-id="48dff-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48dff-135">-DefaultProfile</span></span>
<span data-ttu-id="48dff-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48dff-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48dff-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="48dff-137">-ExcludeChangeType</span></span>
<span data-ttu-id="48dff-138">Azon erőforrás-módosítási típusok vesszővel elválasztott listája, amelyek nem lesznek kizárva a What-If eredményekből.</span><span class="sxs-lookup"><span data-stu-id="48dff-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="48dff-139">-Location</span><span class="sxs-lookup"><span data-stu-id="48dff-139">-Location</span></span>
<span data-ttu-id="48dff-140">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="48dff-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="48dff-141">-Name</span><span class="sxs-lookup"><span data-stu-id="48dff-141">-Name</span></span>
<span data-ttu-id="48dff-142">Annak a telepítésnek a neve, amelyből létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="48dff-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="48dff-143">Ha nincs megadva, alapértelmezés szerint a sablonfájl neve lesz megadva; sablonobjektumok (például "2013123140835") beállítása.</span><span class="sxs-lookup"><span data-stu-id="48dff-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="48dff-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="48dff-144">-Pre</span></span>
<span data-ttu-id="48dff-145">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="48dff-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="48dff-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="48dff-146">-ResultFormat</span></span>
<span data-ttu-id="48dff-147">A What-If formátuma.</span><span class="sxs-lookup"><span data-stu-id="48dff-147">The What-If result format.</span></span>

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

### <span data-ttu-id="48dff-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="48dff-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="48dff-149">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="48dff-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="48dff-150">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="48dff-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="48dff-151">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="48dff-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="48dff-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="48dff-152">-TemplateFile</span></span>
<span data-ttu-id="48dff-153">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="48dff-153">Local path to the template file.</span></span> <span data-ttu-id="48dff-154">Támogatott sablonfájltípus: json és bicep.</span><span class="sxs-lookup"><span data-stu-id="48dff-154">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="48dff-155">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="48dff-155">-TemplateObject</span></span>
<span data-ttu-id="48dff-156">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="48dff-156">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="48dff-157">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="48dff-157">-TemplateParameterFile</span></span>
<span data-ttu-id="48dff-158">Olyan fájl, amely rendelkezik a sablonparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="48dff-158">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="48dff-159">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="48dff-159">-TemplateParameterObject</span></span>
<span data-ttu-id="48dff-160">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="48dff-160">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="48dff-161">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="48dff-161">-TemplateParameterUri</span></span>
<span data-ttu-id="48dff-162">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="48dff-162">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="48dff-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="48dff-163">-TemplateUri</span></span>
<span data-ttu-id="48dff-164">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="48dff-164">Uri to the template file.</span></span>

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

### <span data-ttu-id="48dff-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48dff-165">CommonParameters</span></span>
<span data-ttu-id="48dff-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48dff-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48dff-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48dff-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48dff-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48dff-168">INPUTS</span></span>

### <span data-ttu-id="48dff-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="48dff-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="48dff-170">System.String</span><span class="sxs-lookup"><span data-stu-id="48dff-170">System.String</span></span>

## <span data-ttu-id="48dff-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48dff-171">OUTPUTS</span></span>

### <span data-ttu-id="48dff-172">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="48dff-172">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="48dff-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48dff-173">NOTES</span></span>

## <span data-ttu-id="48dff-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48dff-174">RELATED LINKS</span></span>
