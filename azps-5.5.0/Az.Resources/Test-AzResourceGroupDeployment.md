---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145971"
---
# <span data-ttu-id="a8fda-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8fda-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="a8fda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8fda-102">SYNOPSIS</span></span>
<span data-ttu-id="a8fda-103">Erőforráscsoport-telepítés ellenőrzése.</span><span class="sxs-lookup"><span data-stu-id="a8fda-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="a8fda-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8fda-104">SYNTAX</span></span>

### <span data-ttu-id="a8fda-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8fda-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a8fda-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a8fda-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a8fda-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a8fda-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a8fda-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a8fda-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a8fda-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a8fda-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a8fda-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a8fda-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fda-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a8fda-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8fda-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8fda-117">DESCRIPTION</span></span>
<span data-ttu-id="a8fda-118">A **Test-AzResourceGroupDeployment** parancsmag határozza meg, hogy egy Azure-erőforráscsoport-telepítő sablon és paraméterértékei érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="a8fda-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="a8fda-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8fda-119">EXAMPLES</span></span>

### <span data-ttu-id="a8fda-120">1. példa: Telepítés tesztelése egyéni sablonobjektummal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="a8fda-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="a8fda-121">Ez a parancs teszteli a telepítést a megadott erőforráscsoportban az adott sablonfájlból és egy paraméterfájlból létrehozott memória-kivonat segítségével.</span><span class="sxs-lookup"><span data-stu-id="a8fda-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="a8fda-122">2. példa: A telepítés tesztelése sablonfájllal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="a8fda-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="a8fda-123">Ez a parancs a megadott erőforráscsoportban és erőforrásban a megadott sablonfájl és egy paraméterfájl használatával teszteli az üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="a8fda-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="a8fda-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8fda-124">PARAMETERS</span></span>

### <span data-ttu-id="a8fda-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8fda-125">-DefaultProfile</span></span>
<span data-ttu-id="a8fda-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a8fda-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8fda-127">-Mód</span><span class="sxs-lookup"><span data-stu-id="a8fda-127">-Mode</span></span>
<span data-ttu-id="a8fda-128">A telepítési módot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a8fda-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="a8fda-129">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="a8fda-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8fda-130">Növekményes</span><span class="sxs-lookup"><span data-stu-id="a8fda-130">Incremental</span></span>
- <span data-ttu-id="a8fda-131">Kész</span><span class="sxs-lookup"><span data-stu-id="a8fda-131">Complete</span></span>

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

### <span data-ttu-id="a8fda-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="a8fda-132">-Pre</span></span>
<span data-ttu-id="a8fda-133">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="a8fda-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a8fda-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8fda-134">-ResourceGroupName</span></span>
<span data-ttu-id="a8fda-135">A tesztelni szükséges erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fda-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="a8fda-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="a8fda-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="a8fda-137">Ha a -RollbackToLastDeployment nevet használja, ne használja az erőforráscsoportban megadott nevű sikeres telepítést.</span><span class="sxs-lookup"><span data-stu-id="a8fda-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="a8fda-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="a8fda-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="a8fda-139">Ha a -RollBackDeploymentName paramétert használja, ne legyen jelen az erőforráscsoport utolsó sikeres telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="a8fda-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="a8fda-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="a8fda-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="a8fda-141">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="a8fda-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="a8fda-142">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="a8fda-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="a8fda-143">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="a8fda-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="a8fda-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a8fda-144">-TemplateFile</span></span>
<span data-ttu-id="a8fda-145">Egy JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fda-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="a8fda-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="a8fda-146">-TemplateObject</span></span>
<span data-ttu-id="a8fda-147">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="a8fda-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="a8fda-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a8fda-148">-TemplateParameterFile</span></span>
<span data-ttu-id="a8fda-149">A sablonparaméterek nevét és értékeit tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fda-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="a8fda-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a8fda-150">-TemplateParameterObject</span></span>
<span data-ttu-id="a8fda-151">A sablon paraméterneveivel és értékeivel egy kivonattáblát ad meg.</span><span class="sxs-lookup"><span data-stu-id="a8fda-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="a8fda-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a8fda-152">-TemplateParameterUri</span></span>
<span data-ttu-id="a8fda-153">Egy sablonparaméter-fájl URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fda-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="a8fda-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a8fda-154">-TemplateUri</span></span>
<span data-ttu-id="a8fda-155">Egy JSON-sablonfájl URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fda-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="a8fda-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8fda-156">CommonParameters</span></span>
<span data-ttu-id="a8fda-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8fda-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8fda-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8fda-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8fda-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8fda-159">INPUTS</span></span>

### <span data-ttu-id="a8fda-160">System.String</span><span class="sxs-lookup"><span data-stu-id="a8fda-160">System.String</span></span>

### <span data-ttu-id="a8fda-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="a8fda-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="a8fda-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a8fda-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a8fda-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8fda-163">OUTPUTS</span></span>

### <span data-ttu-id="a8fda-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="a8fda-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="a8fda-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8fda-165">NOTES</span></span>

## <span data-ttu-id="a8fda-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8fda-166">RELATED LINKS</span></span>

[<span data-ttu-id="a8fda-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8fda-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="a8fda-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8fda-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="a8fda-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8fda-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="a8fda-170">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8fda-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


