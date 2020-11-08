---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194867"
---
# <span data-ttu-id="1e9a6-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1e9a6-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="1e9a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9a6-103">Egy felügyeleti csoportban ellenőrzi a bevezetést.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="1e9a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e9a6-104">SYNTAX</span></span>

### <span data-ttu-id="1e9a6-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e9a6-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e9a6-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e9a6-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e9a6-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e9a6-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e9a6-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e9a6-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e9a6-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e9a6-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e9a6-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1e9a6-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e9a6-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1e9a6-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e9a6-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e9a6-117">DESCRIPTION</span></span>
<span data-ttu-id="1e9a6-118">A **AzManagementGroupDeployment** parancsmag azt határozza meg, hogy egy központi üzembe állítási sablon és a paraméter értéke egy felügyeleti csoportban érvényes-e.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="1e9a6-119">Példák</span><span class="sxs-lookup"><span data-stu-id="1e9a6-119">EXAMPLES</span></span>

### <span data-ttu-id="1e9a6-120">1. példa: a bevezetést tesztelheti egyéni sablonnal és paraméteres fájllal</span><span class="sxs-lookup"><span data-stu-id="1e9a6-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="1e9a6-121">Ez a parancs a "myMG" felügyeleti csoport telepítésével teszteli a megadott sablonfájl és a Parameters fájlt.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="1e9a6-122">2. példa: a bevezetést egyéni sablon objektummal és paraméterrel tartalmazó fájllal tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="1e9a6-123">Ez a parancs a "myMG" felügyeleti csoport telepítésével teszteli a megadott sablonfájl és egy paraméter fájlból létrehozott, a memóriában Hashtable.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="1e9a6-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e9a6-124">PARAMETERS</span></span>

### <span data-ttu-id="1e9a6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9a6-125">-DefaultProfile</span></span>
<span data-ttu-id="1e9a6-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e9a6-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="1e9a6-127">-Location</span></span>
<span data-ttu-id="1e9a6-128">A központi telepítő adatainak tárolására szolgáló hely.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="1e9a6-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1e9a6-129">-ManagementGroupId</span></span>
<span data-ttu-id="1e9a6-130">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-130">The management group id.</span></span>

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

### <span data-ttu-id="1e9a6-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="1e9a6-131">-Pre</span></span>
<span data-ttu-id="1e9a6-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1e9a6-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="1e9a6-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="1e9a6-134">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="1e9a6-135">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="1e9a6-136">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="1e9a6-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1e9a6-137">-TemplateFile</span></span>
<span data-ttu-id="1e9a6-138">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="1e9a6-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="1e9a6-139">-TemplateObject</span></span>
<span data-ttu-id="1e9a6-140">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="1e9a6-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e9a6-141">-TemplateParameterFile</span></span>
<span data-ttu-id="1e9a6-142">A sablon paramétereit tartalmazó fájl</span><span class="sxs-lookup"><span data-stu-id="1e9a6-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="1e9a6-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e9a6-143">-TemplateParameterObject</span></span>
<span data-ttu-id="1e9a6-144">A paramétereket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="1e9a6-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e9a6-145">-TemplateParameterUri</span></span>
<span data-ttu-id="1e9a6-146">URI a sablon paraméter-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="1e9a6-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="1e9a6-147">-TemplateUri</span></span>
<span data-ttu-id="1e9a6-148">A sablonfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="1e9a6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9a6-149">CommonParameters</span></span>
<span data-ttu-id="1e9a6-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e9a6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9a6-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1e9a6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9a6-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e9a6-152">INPUTS</span></span>

### <span data-ttu-id="1e9a6-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e9a6-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1e9a6-154">System. String</span><span class="sxs-lookup"><span data-stu-id="1e9a6-154">System.String</span></span>

## <span data-ttu-id="1e9a6-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e9a6-155">OUTPUTS</span></span>

### <span data-ttu-id="1e9a6-156">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="1e9a6-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="1e9a6-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e9a6-157">NOTES</span></span>

## <span data-ttu-id="1e9a6-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e9a6-158">RELATED LINKS</span></span>
