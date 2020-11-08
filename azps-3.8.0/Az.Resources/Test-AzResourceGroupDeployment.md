---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 97a16dcebe2730fef1d770fe8cbbf54d5488b49a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011703"
---
# <span data-ttu-id="b59a1-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b59a1-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="b59a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b59a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b59a1-103">Egy erőforráscsoport-telepítő érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="b59a1-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="b59a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b59a1-104">SYNTAX</span></span>

### <span data-ttu-id="b59a1-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b59a1-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b59a1-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b59a1-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b59a1-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b59a1-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b59a1-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b59a1-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b59a1-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b59a1-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b59a1-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b59a1-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b59a1-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b59a1-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b59a1-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b59a1-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b59a1-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b59a1-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b59a1-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b59a1-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b59a1-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b59a1-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b59a1-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b59a1-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b59a1-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="b59a1-117">DESCRIPTION</span></span>
<span data-ttu-id="b59a1-118">A **AzResourceGroupDeployment** parancsmag azt határozza meg, hogy egy Azure erőforráscsoport-telepítő sablon és a paraméter értéke érvényes-e.</span><span class="sxs-lookup"><span data-stu-id="b59a1-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="b59a1-119">Példák</span><span class="sxs-lookup"><span data-stu-id="b59a1-119">EXAMPLES</span></span>

### <span data-ttu-id="b59a1-120">1. példa: a bevezetést egyéni sablon objektummal és paraméterrel tartalmazó fájllal tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="b59a1-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="b59a1-121">Ez a parancs a megadott sablonfájl és a paraméter-fájl alapján létrehozott, a memóriában lévő Hashtable segítségével teszteli az adott erőforráscsoport telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="b59a1-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="b59a1-122">2. példa: a Template-fájl és a paraméter-objektumon keresztüli telepítés tesztelése</span><span class="sxs-lookup"><span data-stu-id="b59a1-122">Example 2: Test deployment via template file and parameter object</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name testDeployment1 -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="b59a1-123">Ez a parancs a megadott sablonfájlt és egy paraméteres fájlt használva teszteli a megadott erőforráscsoport és erőforrás bevezetését.</span><span class="sxs-lookup"><span data-stu-id="b59a1-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="b59a1-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b59a1-124">PARAMETERS</span></span>

### <span data-ttu-id="b59a1-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b59a1-125">-ApiVersion</span></span>
<span data-ttu-id="b59a1-126">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59a1-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b59a1-127">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="b59a1-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b59a1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59a1-128">-DefaultProfile</span></span>
<span data-ttu-id="b59a1-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b59a1-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b59a1-130">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="b59a1-130">-Mode</span></span>
<span data-ttu-id="b59a1-131">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59a1-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="b59a1-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b59a1-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b59a1-133">Növekményes</span><span class="sxs-lookup"><span data-stu-id="b59a1-133">Incremental</span></span>
- <span data-ttu-id="b59a1-134">Teljes</span><span class="sxs-lookup"><span data-stu-id="b59a1-134">Complete</span></span>

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

### <span data-ttu-id="b59a1-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="b59a1-135">-Pre</span></span>
<span data-ttu-id="b59a1-136">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b59a1-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b59a1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b59a1-137">-ResourceGroupName</span></span>
<span data-ttu-id="b59a1-138">A tesztelni kívánt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59a1-138">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="b59a1-139">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="b59a1-139">-RollBackDeploymentName</span></span>
<span data-ttu-id="b59a1-140">Ha az erőforrás csoportban az adott nevű névvel a sikeres telepítésre szeretne visszagörgetni, akkor ne használja a ha-RollbackToLastDeployment használatát.</span><span class="sxs-lookup"><span data-stu-id="b59a1-140">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="b59a1-141">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="b59a1-141">-RollbackToLastDeployment</span></span>
<span data-ttu-id="b59a1-142">Az erőforrás csoport utolsó sikeres telepítésére való visszagörgetéskor ne legyen megjelenni, ha-RollBackDeploymentName használja.</span><span class="sxs-lookup"><span data-stu-id="b59a1-142">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="b59a1-143">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b59a1-143">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b59a1-144">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="b59a1-144">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="b59a1-145">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="b59a1-145">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="b59a1-146">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="b59a1-146">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="b59a1-147">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b59a1-147">-TemplateFile</span></span>
<span data-ttu-id="b59a1-148">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59a1-148">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="b59a1-149">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="b59a1-149">-TemplateObject</span></span>
<span data-ttu-id="b59a1-150">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="b59a1-150">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="b59a1-151">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b59a1-151">-TemplateParameterFile</span></span>
<span data-ttu-id="b59a1-152">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59a1-152">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="b59a1-153">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b59a1-153">-TemplateParameterObject</span></span>
<span data-ttu-id="b59a1-154">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59a1-154">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="b59a1-155">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b59a1-155">-TemplateParameterUri</span></span>
<span data-ttu-id="b59a1-156">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59a1-156">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="b59a1-157">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b59a1-157">-TemplateUri</span></span>
<span data-ttu-id="b59a1-158">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b59a1-158">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="b59a1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59a1-159">CommonParameters</span></span>
<span data-ttu-id="b59a1-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b59a1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59a1-161">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b59a1-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59a1-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b59a1-162">INPUTS</span></span>

### <span data-ttu-id="b59a1-163">System. String</span><span class="sxs-lookup"><span data-stu-id="b59a1-163">System.String</span></span>

### <span data-ttu-id="b59a1-164">Microsoft. Azure. Management. ResourceManager. models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="b59a1-164">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="b59a1-165">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b59a1-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b59a1-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b59a1-166">OUTPUTS</span></span>

### <span data-ttu-id="b59a1-167">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="b59a1-167">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="b59a1-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b59a1-168">NOTES</span></span>

## <span data-ttu-id="b59a1-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b59a1-169">RELATED LINKS</span></span>

[<span data-ttu-id="b59a1-170">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b59a1-170">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="b59a1-171">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b59a1-171">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="b59a1-172">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b59a1-172">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="b59a1-173">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b59a1-173">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


