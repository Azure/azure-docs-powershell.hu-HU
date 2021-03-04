---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 0e0d4645901f60f9e290d197a47b133d6bf3db8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930842"
---
# <span data-ttu-id="c43d4-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c43d4-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="c43d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c43d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c43d4-103">Erőforráscsoport-telepítés ellenőrzése.</span><span class="sxs-lookup"><span data-stu-id="c43d4-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="c43d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c43d4-104">SYNTAX</span></span>

### <span data-ttu-id="c43d4-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c43d4-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c43d4-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c43d4-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c43d4-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c43d4-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c43d4-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c43d4-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c43d4-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="c43d4-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c43d4-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c43d4-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c43d4-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="c43d4-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c43d4-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c43d4-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c43d4-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c43d4-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c43d4-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="c43d4-119">ByTemplateSpecResourceId</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c43d4-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c43d4-120">DESCRIPTION</span></span>
<span data-ttu-id="c43d4-121">A **Test-AzResourceGroupDeployment** parancsmag határozza meg, hogy egy Azure-erőforráscsoport-telepítő sablon és paraméterértékei érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="c43d4-121">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="c43d4-122">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c43d4-122">EXAMPLES</span></span>

### <span data-ttu-id="c43d4-123">1. példa: Telepítés tesztelése egyéni sablonobjektummal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="c43d4-123">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="c43d4-124">Ez a parancs teszteli a telepítést a megadott erőforráscsoportban az adott sablonfájlból és egy paraméterfájlból létrehozott memória-kivonat segítségével.</span><span class="sxs-lookup"><span data-stu-id="c43d4-124">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="c43d4-125">2. példa: A telepítés tesztelése sablonfájllal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="c43d4-125">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="c43d4-126">Ez a parancs a megadott erőforráscsoportban és erőforrásban a megadott sablonfájl és egy paraméterfájl használatával teszteli az üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="c43d4-126">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="c43d4-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c43d4-127">PARAMETERS</span></span>

### <span data-ttu-id="c43d4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43d4-128">-DefaultProfile</span></span>
<span data-ttu-id="c43d4-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c43d4-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c43d4-130">-Mód</span><span class="sxs-lookup"><span data-stu-id="c43d4-130">-Mode</span></span>
<span data-ttu-id="c43d4-131">A telepítési módot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c43d4-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="c43d4-132">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="c43d4-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c43d4-133">Növekményes</span><span class="sxs-lookup"><span data-stu-id="c43d4-133">Incremental</span></span>
- <span data-ttu-id="c43d4-134">Kész</span><span class="sxs-lookup"><span data-stu-id="c43d4-134">Complete</span></span>

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

### <span data-ttu-id="c43d4-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="c43d4-135">-Pre</span></span>
<span data-ttu-id="c43d4-136">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="c43d4-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c43d4-137">-QueryString</span><span class="sxs-lookup"><span data-stu-id="c43d4-137">-QueryString</span></span>
<span data-ttu-id="c43d4-138">A TemplateUri paraméterrel használt lekérdezési karakterlánc (például EGY SAS-jogkivonat).</span><span class="sxs-lookup"><span data-stu-id="c43d4-138">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="c43d4-139">Hivatkozott sablonok esetén használható</span><span class="sxs-lookup"><span data-stu-id="c43d4-139">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="c43d4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c43d4-140">-ResourceGroupName</span></span>
<span data-ttu-id="c43d4-141">A tesztelni szükséges erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c43d4-141">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="c43d4-142">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="c43d4-142">-RollBackDeploymentName</span></span>
<span data-ttu-id="c43d4-143">Ha a -RollbackToLastDeployment nevet használja, ne használja az erőforráscsoportban megadott nevű sikeres telepítést.</span><span class="sxs-lookup"><span data-stu-id="c43d4-143">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c43d4-144">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="c43d4-144">-RollbackToLastDeployment</span></span>
<span data-ttu-id="c43d4-145">A -RollBackDeploymentName használata esetén ne legyen jelen az erőforráscsoport utolsó sikeres telepítéséhez való visszatérés.</span><span class="sxs-lookup"><span data-stu-id="c43d4-145">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="c43d4-146">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c43d4-146">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c43d4-147">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="c43d4-147">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="c43d4-148">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="c43d4-148">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="c43d4-149">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="c43d4-149">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c43d4-150">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c43d4-150">-TemplateFile</span></span>
<span data-ttu-id="c43d4-151">A sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c43d4-151">Specifies the full path of a template file.</span></span> <span data-ttu-id="c43d4-152">Támogatott sablonfájltípus: json és bicep.</span><span class="sxs-lookup"><span data-stu-id="c43d4-152">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="c43d4-153">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="c43d4-153">-TemplateObject</span></span>
<span data-ttu-id="c43d4-154">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="c43d4-154">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c43d4-155">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c43d4-155">-TemplateParameterFile</span></span>
<span data-ttu-id="c43d4-156">A sablonparaméterek nevét és értékeit tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c43d4-156">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile, ByTemplateSpecResourceIdAndParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c43d4-157">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c43d4-157">-TemplateParameterObject</span></span>
<span data-ttu-id="c43d4-158">A sablon paraméterneveivel és értékeivel egy kivonattáblát ad meg.</span><span class="sxs-lookup"><span data-stu-id="c43d4-158">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="c43d4-159">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c43d4-159">-TemplateParameterUri</span></span>
<span data-ttu-id="c43d4-160">Egy sablonparaméter-fájl URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c43d4-160">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri, ByTemplateSpecResourceIdAndParamsUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c43d4-161">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="c43d4-161">-TemplateSpecId</span></span>
<span data-ttu-id="c43d4-162">A telepíteni kívánt sablonSpec erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c43d4-162">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c43d4-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c43d4-163">-TemplateUri</span></span>
<span data-ttu-id="c43d4-164">Egy sablonfájl URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c43d4-164">Specifies the URI of a template file.</span></span>

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

### <span data-ttu-id="c43d4-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43d4-165">CommonParameters</span></span>
<span data-ttu-id="c43d4-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c43d4-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43d4-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c43d4-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43d4-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c43d4-168">INPUTS</span></span>

### <span data-ttu-id="c43d4-169">System.String</span><span class="sxs-lookup"><span data-stu-id="c43d4-169">System.String</span></span>

### <span data-ttu-id="c43d4-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="c43d4-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="c43d4-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c43d4-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c43d4-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c43d4-172">OUTPUTS</span></span>

### <span data-ttu-id="c43d4-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="c43d4-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="c43d4-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c43d4-174">NOTES</span></span>

## <span data-ttu-id="c43d4-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c43d4-175">RELATED LINKS</span></span>

[<span data-ttu-id="c43d4-176">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c43d4-176">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="c43d4-177">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c43d4-177">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="c43d4-178">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c43d4-178">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="c43d4-179">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c43d4-179">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


