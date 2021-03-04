---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 6ecdf53ecd762c0c3b8ef378b1e8bc78b301a012
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935498"
---
# <span data-ttu-id="eba03-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="eba03-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="eba03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eba03-102">SYNOPSIS</span></span>
<span data-ttu-id="eba03-103">Egy felügyeleti csoport központi telepítésének ellenőrzése.</span><span class="sxs-lookup"><span data-stu-id="eba03-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="eba03-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eba03-104">SYNTAX</span></span>

### <span data-ttu-id="eba03-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eba03-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eba03-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="eba03-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="eba03-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="eba03-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="eba03-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="eba03-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="eba03-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="eba03-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="eba03-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="eba03-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="eba03-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="eba03-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba03-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="eba03-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eba03-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="eba03-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eba03-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="eba03-119">ByTemplateSpecResourceId</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eba03-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eba03-120">DESCRIPTION</span></span>
<span data-ttu-id="eba03-121">A **Test-AzManagementGroupDeployment** parancsmag határozza meg, hogy egy telepítősablon és paraméterértékei érvényesek-e egy felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="eba03-121">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="eba03-122">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eba03-122">EXAMPLES</span></span>

### <span data-ttu-id="eba03-123">1. példa: A telepítés tesztelése egyéni sablonnal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="eba03-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="eba03-124">Ez a parancs teszteli a telepítést a "myMG" felügyeleti csoportban a megadott sablonfájl és paraméterfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="eba03-124">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="eba03-125">2. példa: A telepítés tesztelése egyéni sablonobjektummal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="eba03-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="eba03-126">Ez a parancs egy telepítést tesztel a "myMG" felügyeleti csoportban az adott sablonfájlból és egy paraméterfájlból létrehozott memória-kivonat használatával.</span><span class="sxs-lookup"><span data-stu-id="eba03-126">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="eba03-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eba03-127">PARAMETERS</span></span>

### <span data-ttu-id="eba03-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba03-128">-DefaultProfile</span></span>
<span data-ttu-id="eba03-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eba03-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eba03-130">-Location</span><span class="sxs-lookup"><span data-stu-id="eba03-130">-Location</span></span>
<span data-ttu-id="eba03-131">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="eba03-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="eba03-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="eba03-132">-ManagementGroupId</span></span>
<span data-ttu-id="eba03-133">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eba03-133">The management group id.</span></span>

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

### <span data-ttu-id="eba03-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="eba03-134">-Pre</span></span>
<span data-ttu-id="eba03-135">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="eba03-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="eba03-136">-QueryString</span><span class="sxs-lookup"><span data-stu-id="eba03-136">-QueryString</span></span>
<span data-ttu-id="eba03-137">A TemplateUri paraméterrel használt lekérdezési karakterlánc (például EGY SAS-jogkivonat).</span><span class="sxs-lookup"><span data-stu-id="eba03-137">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="eba03-138">Hivatkozott sablonok esetén használható</span><span class="sxs-lookup"><span data-stu-id="eba03-138">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="eba03-139">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="eba03-139">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="eba03-140">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="eba03-140">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="eba03-141">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="eba03-141">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="eba03-142">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="eba03-142">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="eba03-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="eba03-143">-TemplateFile</span></span>
<span data-ttu-id="eba03-144">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="eba03-144">Local path to the template file.</span></span> <span data-ttu-id="eba03-145">Támogatott sablonfájltípus: json és bicep.</span><span class="sxs-lookup"><span data-stu-id="eba03-145">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="eba03-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="eba03-146">-TemplateObject</span></span>
<span data-ttu-id="eba03-147">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="eba03-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="eba03-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="eba03-148">-TemplateParameterFile</span></span>
<span data-ttu-id="eba03-149">Olyan fájl, amely rendelkezik a sablonparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="eba03-149">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="eba03-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="eba03-150">-TemplateParameterObject</span></span>
<span data-ttu-id="eba03-151">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="eba03-151">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="eba03-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="eba03-152">-TemplateParameterUri</span></span>
<span data-ttu-id="eba03-153">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="eba03-153">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="eba03-154">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="eba03-154">-TemplateSpecId</span></span>
<span data-ttu-id="eba03-155">A telepíteni kívánt sablonSpec erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eba03-155">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="eba03-156">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="eba03-156">-TemplateUri</span></span>
<span data-ttu-id="eba03-157">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="eba03-157">Uri to the template file.</span></span>

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

### <span data-ttu-id="eba03-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba03-158">CommonParameters</span></span>
<span data-ttu-id="eba03-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba03-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba03-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eba03-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba03-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eba03-161">INPUTS</span></span>

### <span data-ttu-id="eba03-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="eba03-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="eba03-163">System.String</span><span class="sxs-lookup"><span data-stu-id="eba03-163">System.String</span></span>

## <span data-ttu-id="eba03-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eba03-164">OUTPUTS</span></span>

### <span data-ttu-id="eba03-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="eba03-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="eba03-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eba03-166">NOTES</span></span>

## <span data-ttu-id="eba03-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eba03-167">RELATED LINKS</span></span>
