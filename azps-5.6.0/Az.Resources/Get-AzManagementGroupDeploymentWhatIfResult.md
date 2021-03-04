---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 981d9e771a988a4166f542854959b38e140d2061
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928538"
---
# <span data-ttu-id="ad6ab-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="ad6ab-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="ad6ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6ab-103">Sablont What-If egy központi telepítéshez a felügyeleti csoport hatókörében.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-103">Gets a template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="ad6ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad6ab-104">SYNTAX</span></span>

### <span data-ttu-id="ad6ab-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad6ab-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ad6ab-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ad6ab-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ad6ab-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ad6ab-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ad6ab-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ad6ab-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ad6ab-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ad6ab-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ad6ab-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ad6ab-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6ab-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ad6ab-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad6ab-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad6ab-117">DESCRIPTION</span></span>
<span data-ttu-id="ad6ab-118">A **Get-AzManagementGroupDeploymentWhatIfResult** parancsmag egy ARM sablont kap What-If egy sablon telepítéséhez a megadott felügyeleti csoport hatókörében.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="ad6ab-119">Visszaadja a módosítások listáját, jelezve, hogy mely erőforrások lesznek frissítve, ha a telepítést a tényleges erőforrások változtatása nélkül alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="ad6ab-120">Az eredmény formátumának megadásához használja a *ResultFormat paramétert.*</span><span class="sxs-lookup"><span data-stu-id="ad6ab-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="ad6ab-121">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad6ab-121">EXAMPLES</span></span>

### <span data-ttu-id="ad6ab-122">1. példa: What-If eredmény a felügyeleti csoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="ad6ab-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="ad6ab-123">Ez a parancs egy What-If egy egyéni sablonfájl és egy lemezen található paraméterfájl használatával kap egy találatot a felügyeleti csoport hatókörében.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="ad6ab-124">A parancs a *Hely paraméter* segítségével adja meg, hogy hol tárolja a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="ad6ab-125">A parancs a *ManagementGroupId paramétert használva* adja meg azt a felügyeleti csoportot, amelyben a sablont telepíteni fogja.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="ad6ab-126">A parancs a *TemplateFile paraméterrel* adja meg a sablonfájlt.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="ad6ab-127">A parancs a *TemplateParameterFile paraméterrel* adja meg a sablon paraméterfájlját.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="ad6ab-128">A parancs a *ResultFormat* paraméter segítségével úgy What-If, hogy az tartalmazza a teljes erőforrás-terhelést.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="ad6ab-129">2. példa: What-If eredmény a felügyeleti csoport hatókörében az ResourceIdOnlyval</span><span class="sxs-lookup"><span data-stu-id="ad6ab-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="ad6ab-130">Ez a parancs egy What-If egy egyéni sablonfájl és egy lemezen található paraméterfájl használatával kap egy találatot a felügyeleti csoport hatókörében.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="ad6ab-131">A parancs a *Hely paraméter* segítségével adja meg, hogy hol tárolja a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="ad6ab-132">A parancs a *ManagementGroupId paramétert használva* adja meg azt a felügyeleti csoportot, amelyben a sablont telepíteni fogja.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="ad6ab-133">A parancs a *TemplateFile paraméterrel* adja meg a sablonfájlt.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="ad6ab-134">A parancs a *TemplateParameterFile paraméterrel* adja meg a sablon paraméterfájlját.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="ad6ab-135">A parancs a *ResultFormat* paraméter segítségével úgy What-If, hogy az csak erőforrás-adatokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="ad6ab-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad6ab-136">PARAMETERS</span></span>

### <span data-ttu-id="ad6ab-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6ab-137">-DefaultProfile</span></span>
<span data-ttu-id="ad6ab-138">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad6ab-139">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="ad6ab-139">-ExcludeChangeType</span></span>
<span data-ttu-id="ad6ab-140">Azon erőforrás-módosítási típusok vesszővel elválasztott listája, amelyek nem lesznek kizárva a What-If eredményekből.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-140">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="ad6ab-141">-Location</span><span class="sxs-lookup"><span data-stu-id="ad6ab-141">-Location</span></span>
<span data-ttu-id="ad6ab-142">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-142">The location to store deployment data.</span></span>

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

### <span data-ttu-id="ad6ab-143">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ad6ab-143">-ManagementGroupId</span></span>
<span data-ttu-id="ad6ab-144">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-144">The management group ID.</span></span>

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

### <span data-ttu-id="ad6ab-145">-Name</span><span class="sxs-lookup"><span data-stu-id="ad6ab-145">-Name</span></span>
<span data-ttu-id="ad6ab-146">Annak a telepítésnek a neve, amelyből létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-146">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="ad6ab-147">Ha nincs megadva, alapértelmezés szerint a sablonfájl neve lesz megadva; sablonobjektumok (például "2013123140835") beállítása.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-147">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="ad6ab-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="ad6ab-148">-Pre</span></span>
<span data-ttu-id="ad6ab-149">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-149">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ad6ab-150">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="ad6ab-150">-ResultFormat</span></span>
<span data-ttu-id="ad6ab-151">A What-If formátuma.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-151">The What-If result format.</span></span>

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

### <span data-ttu-id="ad6ab-152">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="ad6ab-152">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="ad6ab-153">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-153">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="ad6ab-154">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-154">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="ad6ab-155">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-155">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="ad6ab-156">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ad6ab-156">-TemplateFile</span></span>
<span data-ttu-id="ad6ab-157">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-157">Local path to the template file.</span></span> <span data-ttu-id="ad6ab-158">Támogatott sablonfájltípus: json és bicep.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-158">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="ad6ab-159">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="ad6ab-159">-TemplateObject</span></span>
<span data-ttu-id="ad6ab-160">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-160">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="ad6ab-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ad6ab-161">-TemplateParameterFile</span></span>
<span data-ttu-id="ad6ab-162">Olyan fájl, amely rendelkezik a sablonparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-162">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="ad6ab-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="ad6ab-163">-TemplateParameterObject</span></span>
<span data-ttu-id="ad6ab-164">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-164">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="ad6ab-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="ad6ab-165">-TemplateParameterUri</span></span>
<span data-ttu-id="ad6ab-166">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-166">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="ad6ab-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ad6ab-167">-TemplateUri</span></span>
<span data-ttu-id="ad6ab-168">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-168">Uri to the template file.</span></span>

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

### <span data-ttu-id="ad6ab-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6ab-169">CommonParameters</span></span>
<span data-ttu-id="ad6ab-170">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6ab-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6ab-171">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad6ab-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6ab-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad6ab-172">INPUTS</span></span>

### <span data-ttu-id="ad6ab-173">System.String</span><span class="sxs-lookup"><span data-stu-id="ad6ab-173">System.String</span></span>

### <span data-ttu-id="ad6ab-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad6ab-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad6ab-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad6ab-175">OUTPUTS</span></span>

### <span data-ttu-id="ad6ab-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="ad6ab-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="ad6ab-177">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad6ab-177">NOTES</span></span>

## <span data-ttu-id="ad6ab-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad6ab-178">RELATED LINKS</span></span>
