---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5144dacb044523c2ad72d0a9c24aa43427f14f99
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329080"
---
# <span data-ttu-id="0f5b9-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0f5b9-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="0f5b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5b9-103">Egy központi telepítést ellenőriz bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="0f5b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f5b9-104">SYNTAX</span></span>

### <span data-ttu-id="0f5b9-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f5b9-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0f5b9-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0f5b9-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0f5b9-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0f5b9-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0f5b9-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0f5b9-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0f5b9-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0f5b9-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0f5b9-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0f5b9-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b9-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0f5b9-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f5b9-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f5b9-117">DESCRIPTION</span></span>
<span data-ttu-id="0f5b9-118">A **Test-AzTenantDeployment parancsmag** határozza meg, hogy egy üzembe helyezési sablon és paraméterértékei érvényesek-e az aktuális bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="0f5b9-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f5b9-119">EXAMPLES</span></span>

### <span data-ttu-id="0f5b9-120">1. példa: A telepítés tesztelése egyéni sablonnal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="0f5b9-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="0f5b9-121">Ez a parancs a megadott sablonfájlt és paraméterfájlt használva teszteli az aktuális bérlői hatókörű telepítést.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="0f5b9-122">2. példa: A telepítés tesztelése egyéni sablonobjektummal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="0f5b9-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="0f5b9-123">Ez a parancs az aktuális bérlői tartományba tartozó telepítést teszteli egy adott sablonfájlból és egy paraméterfájlból létrehozott memória-kivonat segítségével.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="0f5b9-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f5b9-124">PARAMETERS</span></span>

### <span data-ttu-id="0f5b9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f5b9-125">-DefaultProfile</span></span>
<span data-ttu-id="0f5b9-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f5b9-127">-Location</span><span class="sxs-lookup"><span data-stu-id="0f5b9-127">-Location</span></span>
<span data-ttu-id="0f5b9-128">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="0f5b9-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="0f5b9-129">-Pre</span></span>
<span data-ttu-id="0f5b9-130">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0f5b9-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="0f5b9-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="0f5b9-132">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="0f5b9-133">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="0f5b9-134">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="0f5b9-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0f5b9-135">-TemplateFile</span></span>
<span data-ttu-id="0f5b9-136">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="0f5b9-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="0f5b9-137">-TemplateObject</span></span>
<span data-ttu-id="0f5b9-138">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="0f5b9-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0f5b9-139">-TemplateParameterFile</span></span>
<span data-ttu-id="0f5b9-140">Olyan fájl, amely rendelkezik a sablonparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="0f5b9-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0f5b9-141">-TemplateParameterObject</span></span>
<span data-ttu-id="0f5b9-142">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="0f5b9-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0f5b9-143">-TemplateParameterUri</span></span>
<span data-ttu-id="0f5b9-144">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="0f5b9-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0f5b9-145">-TemplateUri</span></span>
<span data-ttu-id="0f5b9-146">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="0f5b9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5b9-147">CommonParameters</span></span>
<span data-ttu-id="0f5b9-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f5b9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5b9-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f5b9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5b9-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f5b9-150">INPUTS</span></span>

### <span data-ttu-id="0f5b9-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0f5b9-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0f5b9-152">System.String</span><span class="sxs-lookup"><span data-stu-id="0f5b9-152">System.String</span></span>

## <span data-ttu-id="0f5b9-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f5b9-153">OUTPUTS</span></span>

### <span data-ttu-id="0f5b9-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="0f5b9-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="0f5b9-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f5b9-155">NOTES</span></span>

## <span data-ttu-id="0f5b9-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f5b9-156">RELATED LINKS</span></span>
