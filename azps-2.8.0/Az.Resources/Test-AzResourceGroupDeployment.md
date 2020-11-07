---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 01d7aa0cb0b363dac8e19e5b38796c43523d6296
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838864"
---
# <span data-ttu-id="685a3-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="685a3-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="685a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="685a3-102">SYNOPSIS</span></span>
<span data-ttu-id="685a3-103">Egy erőforráscsoport-telepítő érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="685a3-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="685a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="685a3-104">SYNTAX</span></span>

### <span data-ttu-id="685a3-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="685a3-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="685a3-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="685a3-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685a3-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="685a3-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685a3-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="685a3-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685a3-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="685a3-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685a3-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="685a3-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685a3-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="685a3-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685a3-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="685a3-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685a3-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="685a3-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685a3-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="685a3-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685a3-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="685a3-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="685a3-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="685a3-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="685a3-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="685a3-117">DESCRIPTION</span></span>
<span data-ttu-id="685a3-118">A **AzResourceGroupDeployment** parancsmag azt határozza meg, hogy egy Azure erőforráscsoport-telepítő sablon és a paraméter értéke érvényes-e.</span><span class="sxs-lookup"><span data-stu-id="685a3-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="685a3-119">Példák</span><span class="sxs-lookup"><span data-stu-id="685a3-119">EXAMPLES</span></span>

### <span data-ttu-id="685a3-120">1. példa: a bevezetést egyéni sablon objektummal és paraméterrel tartalmazó fájllal tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="685a3-120">Example 1: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="685a3-121">Ez a parancs a megadott sablonfájl és a paraméter-fájl alapján létrehozott, a memóriában lévő Hashtable segítségével teszteli az adott erőforráscsoport telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="685a3-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="685a3-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="685a3-122">PARAMETERS</span></span>

### <span data-ttu-id="685a3-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="685a3-123">-ApiVersion</span></span>
<span data-ttu-id="685a3-124">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="685a3-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="685a3-125">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="685a3-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="685a3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="685a3-126">-DefaultProfile</span></span>
<span data-ttu-id="685a3-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="685a3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="685a3-128">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="685a3-128">-Mode</span></span>
<span data-ttu-id="685a3-129">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="685a3-129">Specifies the deployment mode.</span></span>
<span data-ttu-id="685a3-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="685a3-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="685a3-131">Növekményes</span><span class="sxs-lookup"><span data-stu-id="685a3-131">Incremental</span></span>
- <span data-ttu-id="685a3-132">Teljes</span><span class="sxs-lookup"><span data-stu-id="685a3-132">Complete</span></span>

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

### <span data-ttu-id="685a3-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="685a3-133">-Pre</span></span>
<span data-ttu-id="685a3-134">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="685a3-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="685a3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="685a3-135">-ResourceGroupName</span></span>
<span data-ttu-id="685a3-136">A tesztelni kívánt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="685a3-136">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="685a3-137">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="685a3-137">-RollBackDeploymentName</span></span>
<span data-ttu-id="685a3-138">Ha az erőforrás csoportban az adott nevű névvel a sikeres telepítésre szeretne visszagörgetni, akkor ne használja a ha-RollbackToLastDeployment használatát.</span><span class="sxs-lookup"><span data-stu-id="685a3-138">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="685a3-139">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="685a3-139">-RollbackToLastDeployment</span></span>
<span data-ttu-id="685a3-140">Az erőforrás csoport utolsó sikeres telepítésére való visszagörgetéskor ne legyen megjelenni, ha-RollBackDeploymentName használja.</span><span class="sxs-lookup"><span data-stu-id="685a3-140">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="685a3-141">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="685a3-141">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="685a3-142">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="685a3-142">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="685a3-143">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="685a3-143">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="685a3-144">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="685a3-144">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="685a3-145">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="685a3-145">-TemplateFile</span></span>
<span data-ttu-id="685a3-146">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="685a3-146">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="685a3-147">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="685a3-147">-TemplateObject</span></span>
<span data-ttu-id="685a3-148">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="685a3-148">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="685a3-149">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="685a3-149">-TemplateParameterFile</span></span>
<span data-ttu-id="685a3-150">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="685a3-150">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="685a3-151">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="685a3-151">-TemplateParameterObject</span></span>
<span data-ttu-id="685a3-152">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="685a3-152">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="685a3-153">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="685a3-153">-TemplateParameterUri</span></span>
<span data-ttu-id="685a3-154">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="685a3-154">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="685a3-155">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="685a3-155">-TemplateUri</span></span>
<span data-ttu-id="685a3-156">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="685a3-156">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="685a3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="685a3-157">CommonParameters</span></span>
<span data-ttu-id="685a3-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="685a3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="685a3-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="685a3-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="685a3-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="685a3-160">INPUTS</span></span>

### <span data-ttu-id="685a3-161">System. String</span><span class="sxs-lookup"><span data-stu-id="685a3-161">System.String</span></span>

### <span data-ttu-id="685a3-162">Microsoft. Azure. Management. ResourceManager. models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="685a3-162">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="685a3-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="685a3-163">System.Collections.Hashtable</span></span>

## <span data-ttu-id="685a3-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="685a3-164">OUTPUTS</span></span>

### <span data-ttu-id="685a3-165">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="685a3-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="685a3-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="685a3-166">NOTES</span></span>

## <span data-ttu-id="685a3-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="685a3-167">RELATED LINKS</span></span>

[<span data-ttu-id="685a3-168">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="685a3-168">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="685a3-169">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="685a3-169">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="685a3-170">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="685a3-170">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="685a3-171">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="685a3-171">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


