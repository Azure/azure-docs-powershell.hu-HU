---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468545"
---
# <span data-ttu-id="04682-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="04682-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="04682-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04682-102">SYNOPSIS</span></span>
<span data-ttu-id="04682-103">Egy felügyeleti csoport központi telepítésének ellenőrzése.</span><span class="sxs-lookup"><span data-stu-id="04682-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="04682-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04682-104">SYNTAX</span></span>

### <span data-ttu-id="04682-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04682-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04682-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="04682-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04682-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="04682-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04682-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="04682-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04682-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="04682-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04682-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="04682-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04682-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="04682-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04682-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="04682-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04682-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="04682-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04682-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="04682-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04682-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="04682-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04682-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="04682-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04682-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04682-117">DESCRIPTION</span></span>
<span data-ttu-id="04682-118">A **Test-AzManagementGroupDeployment** parancsmag határozza meg, hogy egy telepítősablon és paraméterértékei érvényesek-e egy felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="04682-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="04682-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04682-119">EXAMPLES</span></span>

### <span data-ttu-id="04682-120">1. példa: A telepítés tesztelése egyéni sablonnal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="04682-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="04682-121">Ez a parancs teszteli a telepítést a "myMG" felügyeleti csoportban a megadott sablonfájl és paraméterfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="04682-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="04682-122">2. példa: A telepítés tesztelése egyéni sablonobjektummal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="04682-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="04682-123">Ez a parancs egy telepítést tesztel a "myMG" felügyeleti csoportban az adott sablonfájlból és egy paraméterfájlból létrehozott memória-kivonat használatával.</span><span class="sxs-lookup"><span data-stu-id="04682-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="04682-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04682-124">PARAMETERS</span></span>

### <span data-ttu-id="04682-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04682-125">-DefaultProfile</span></span>
<span data-ttu-id="04682-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04682-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04682-127">-Location</span><span class="sxs-lookup"><span data-stu-id="04682-127">-Location</span></span>
<span data-ttu-id="04682-128">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="04682-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="04682-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="04682-129">-ManagementGroupId</span></span>
<span data-ttu-id="04682-130">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="04682-130">The management group id.</span></span>

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

### <span data-ttu-id="04682-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="04682-131">-Pre</span></span>
<span data-ttu-id="04682-132">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="04682-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="04682-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="04682-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="04682-134">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="04682-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="04682-135">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="04682-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="04682-136">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="04682-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="04682-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="04682-137">-TemplateFile</span></span>
<span data-ttu-id="04682-138">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="04682-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="04682-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="04682-139">-TemplateObject</span></span>
<span data-ttu-id="04682-140">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="04682-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="04682-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="04682-141">-TemplateParameterFile</span></span>
<span data-ttu-id="04682-142">Olyan fájl, amely rendelkezik a sablonparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="04682-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="04682-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="04682-143">-TemplateParameterObject</span></span>
<span data-ttu-id="04682-144">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="04682-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="04682-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="04682-145">-TemplateParameterUri</span></span>
<span data-ttu-id="04682-146">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="04682-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="04682-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="04682-147">-TemplateUri</span></span>
<span data-ttu-id="04682-148">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="04682-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="04682-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04682-149">CommonParameters</span></span>
<span data-ttu-id="04682-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04682-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04682-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04682-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04682-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04682-152">INPUTS</span></span>

### <span data-ttu-id="04682-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="04682-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="04682-154">System.String</span><span class="sxs-lookup"><span data-stu-id="04682-154">System.String</span></span>

## <span data-ttu-id="04682-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04682-155">OUTPUTS</span></span>

### <span data-ttu-id="04682-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="04682-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="04682-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04682-157">NOTES</span></span>

## <span data-ttu-id="04682-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04682-158">RELATED LINKS</span></span>
