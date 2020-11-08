---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185879"
---
# <span data-ttu-id="ae9dc-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ae9dc-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="ae9dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9dc-103">Egy erőforráscsoport-telepítő érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="ae9dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae9dc-104">SYNTAX</span></span>

### <span data-ttu-id="ae9dc-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae9dc-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ae9dc-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ae9dc-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ae9dc-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ae9dc-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ae9dc-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ae9dc-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ae9dc-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ae9dc-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ae9dc-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ae9dc-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9dc-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ae9dc-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae9dc-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae9dc-117">DESCRIPTION</span></span>
<span data-ttu-id="ae9dc-118">A **AzResourceGroupDeployment** parancsmag azt határozza meg, hogy egy Azure erőforráscsoport-telepítő sablon és a paraméter értéke érvényes-e.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="ae9dc-119">Példák</span><span class="sxs-lookup"><span data-stu-id="ae9dc-119">EXAMPLES</span></span>

### <span data-ttu-id="ae9dc-120">1. példa: a bevezetést egyéni sablon objektummal és paraméterrel tartalmazó fájllal tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="ae9dc-121">Ez a parancs a megadott sablonfájl és a paraméter-fájl alapján létrehozott, a memóriában lévő Hashtable segítségével teszteli az adott erőforráscsoport telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="ae9dc-122">2. példa: a telepítés a sablonfájl és a paraméter fájlja segítségével</span><span class="sxs-lookup"><span data-stu-id="ae9dc-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="ae9dc-123">Ez a parancs a megadott sablonfájlt és egy paraméteres fájlt használva teszteli a megadott erőforráscsoport és erőforrás bevezetését.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="ae9dc-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae9dc-124">PARAMETERS</span></span>

### <span data-ttu-id="ae9dc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9dc-125">-DefaultProfile</span></span>
<span data-ttu-id="ae9dc-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ae9dc-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae9dc-127">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="ae9dc-127">-Mode</span></span>
<span data-ttu-id="ae9dc-128">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="ae9dc-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ae9dc-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ae9dc-130">Növekményes</span><span class="sxs-lookup"><span data-stu-id="ae9dc-130">Incremental</span></span>
- <span data-ttu-id="ae9dc-131">Teljes</span><span class="sxs-lookup"><span data-stu-id="ae9dc-131">Complete</span></span>

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

### <span data-ttu-id="ae9dc-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="ae9dc-132">-Pre</span></span>
<span data-ttu-id="ae9dc-133">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ae9dc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae9dc-134">-ResourceGroupName</span></span>
<span data-ttu-id="ae9dc-135">A tesztelni kívánt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="ae9dc-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="ae9dc-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="ae9dc-137">Ha az erőforrás csoportban az adott nevű névvel a sikeres telepítésre szeretne visszagörgetni, akkor ne használja a ha-RollbackToLastDeployment használatát.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="ae9dc-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="ae9dc-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="ae9dc-139">Az erőforrás csoport utolsó sikeres telepítésére való visszagörgetéskor ne legyen megjelenni, ha-RollBackDeploymentName használja.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="ae9dc-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="ae9dc-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="ae9dc-141">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="ae9dc-142">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="ae9dc-143">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="ae9dc-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ae9dc-144">-TemplateFile</span></span>
<span data-ttu-id="ae9dc-145">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="ae9dc-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="ae9dc-146">-TemplateObject</span></span>
<span data-ttu-id="ae9dc-147">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="ae9dc-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ae9dc-148">-TemplateParameterFile</span></span>
<span data-ttu-id="ae9dc-149">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="ae9dc-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="ae9dc-150">-TemplateParameterObject</span></span>
<span data-ttu-id="ae9dc-151">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="ae9dc-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="ae9dc-152">-TemplateParameterUri</span></span>
<span data-ttu-id="ae9dc-153">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="ae9dc-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ae9dc-154">-TemplateUri</span></span>
<span data-ttu-id="ae9dc-155">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="ae9dc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9dc-156">CommonParameters</span></span>
<span data-ttu-id="ae9dc-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae9dc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9dc-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ae9dc-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9dc-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae9dc-159">INPUTS</span></span>

### <span data-ttu-id="ae9dc-160">System. String</span><span class="sxs-lookup"><span data-stu-id="ae9dc-160">System.String</span></span>

### <span data-ttu-id="ae9dc-161">Microsoft. Azure. Management. ResourceManager. models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="ae9dc-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="ae9dc-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae9dc-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ae9dc-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae9dc-163">OUTPUTS</span></span>

### <span data-ttu-id="ae9dc-164">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="ae9dc-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="ae9dc-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae9dc-165">NOTES</span></span>

## <span data-ttu-id="ae9dc-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae9dc-166">RELATED LINKS</span></span>

[<span data-ttu-id="ae9dc-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ae9dc-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="ae9dc-168">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ae9dc-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="ae9dc-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ae9dc-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="ae9dc-170">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ae9dc-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


