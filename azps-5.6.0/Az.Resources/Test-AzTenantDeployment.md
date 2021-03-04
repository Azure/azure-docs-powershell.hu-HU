---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5c440c6f150993b947a0db2162ef0fd664e73220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922666"
---
# <span data-ttu-id="e5ed8-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e5ed8-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="e5ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ed8-103">Egy központi telepítést ellenőriz bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="e5ed8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5ed8-104">SYNTAX</span></span>

### <span data-ttu-id="e5ed8-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5ed8-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5ed8-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5ed8-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5ed8-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e5ed8-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e5ed8-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e5ed8-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="e5ed8-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e5ed8-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e5ed8-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e5ed8-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="e5ed8-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e5ed8-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e5ed8-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5ed8-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="e5ed8-119">ByTemplateSpecResourceId</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5ed8-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5ed8-120">DESCRIPTION</span></span>
<span data-ttu-id="e5ed8-121">A **Test-AzTenantDeployment parancsmag** határozza meg, hogy egy üzembe helyezési sablon és paraméterértékei érvényesek-e az aktuális bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-121">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="e5ed8-122">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5ed8-122">EXAMPLES</span></span>

### <span data-ttu-id="e5ed8-123">1. példa: A telepítés tesztelése egyéni sablonnal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="e5ed8-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="e5ed8-124">Ez a parancs a megadott sablonfájlt és paraméterfájlt használva teszteli az aktuális bérlői hatókörű telepítést.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-124">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="e5ed8-125">2. példa: A telepítés tesztelése egyéni sablonobjektummal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="e5ed8-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="e5ed8-126">Ez a parancs a bérlő aktuális hatókörében lévő telepítést teszteli egy adott sablonfájlból és egy paraméterfájlból létrehozott memória-kivonat segítségével.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-126">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="e5ed8-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5ed8-127">PARAMETERS</span></span>

### <span data-ttu-id="e5ed8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ed8-128">-DefaultProfile</span></span>
<span data-ttu-id="e5ed8-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5ed8-130">-Location</span><span class="sxs-lookup"><span data-stu-id="e5ed8-130">-Location</span></span>
<span data-ttu-id="e5ed8-131">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="e5ed8-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="e5ed8-132">-Pre</span></span>
<span data-ttu-id="e5ed8-133">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e5ed8-134">-QueryString</span><span class="sxs-lookup"><span data-stu-id="e5ed8-134">-QueryString</span></span>
<span data-ttu-id="e5ed8-135">A TemplateUri paraméterrel használt lekérdezési karakterlánc (például EGY SAS-jogkivonat).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-135">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="e5ed8-136">Hivatkozott sablonok esetén használható</span><span class="sxs-lookup"><span data-stu-id="e5ed8-136">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="e5ed8-137">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e5ed8-137">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e5ed8-138">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-138">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="e5ed8-139">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-139">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="e5ed8-140">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-140">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="e5ed8-141">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e5ed8-141">-TemplateFile</span></span>
<span data-ttu-id="e5ed8-142">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-142">Local path to the template file.</span></span> <span data-ttu-id="e5ed8-143">Támogatott sablonfájltípus: json és bicep.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-143">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="e5ed8-144">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="e5ed8-144">-TemplateObject</span></span>
<span data-ttu-id="e5ed8-145">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-145">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="e5ed8-146">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e5ed8-146">-TemplateParameterFile</span></span>
<span data-ttu-id="e5ed8-147">Olyan fájl, amely rendelkezik a sablonparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-147">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="e5ed8-148">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5ed8-148">-TemplateParameterObject</span></span>
<span data-ttu-id="e5ed8-149">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-149">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="e5ed8-150">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e5ed8-150">-TemplateParameterUri</span></span>
<span data-ttu-id="e5ed8-151">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-151">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="e5ed8-152">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="e5ed8-152">-TemplateSpecId</span></span>
<span data-ttu-id="e5ed8-153">A telepíteni kívánt sablonSpec erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-153">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="e5ed8-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e5ed8-154">-TemplateUri</span></span>
<span data-ttu-id="e5ed8-155">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-155">Uri to the template file.</span></span>

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

### <span data-ttu-id="e5ed8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ed8-156">CommonParameters</span></span>
<span data-ttu-id="e5ed8-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ed8-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5ed8-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ed8-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5ed8-159">INPUTS</span></span>

### <span data-ttu-id="e5ed8-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5ed8-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e5ed8-161">System.String</span><span class="sxs-lookup"><span data-stu-id="e5ed8-161">System.String</span></span>

## <span data-ttu-id="e5ed8-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5ed8-162">OUTPUTS</span></span>

### <span data-ttu-id="e5ed8-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="e5ed8-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="e5ed8-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5ed8-164">NOTES</span></span>

## <span data-ttu-id="e5ed8-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5ed8-165">RELATED LINKS</span></span>
