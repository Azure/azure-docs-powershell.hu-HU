---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 9a1a183ac6a0fb896f6b3d901e8f429fdf225e26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145986"
---
# <span data-ttu-id="647b6-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="647b6-101">Test-AzDeployment</span></span>

## <span data-ttu-id="647b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="647b6-102">SYNOPSIS</span></span>
<span data-ttu-id="647b6-103">Egy központi telepítés ellenőrzése.</span><span class="sxs-lookup"><span data-stu-id="647b6-103">Validates a deployment.</span></span>

## <span data-ttu-id="647b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="647b6-104">SYNTAX</span></span>

### <span data-ttu-id="647b6-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="647b6-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="647b6-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="647b6-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="647b6-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="647b6-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="647b6-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="647b6-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="647b6-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="647b6-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="647b6-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="647b6-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647b6-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="647b6-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="647b6-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="647b6-117">DESCRIPTION</span></span>
<span data-ttu-id="647b6-118">A **Test-AzDeployment** parancsmag határozza meg, hogy egy telepítősablon és paraméterértékei érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="647b6-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="647b6-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="647b6-119">EXAMPLES</span></span>

### <span data-ttu-id="647b6-120">1. példa: Telepítés tesztelése egyéni sablonnal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="647b6-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="647b6-121">Ez a parancs az aktuális előfizetési hatókörű telepítést teszteli a megadott sablonfájl és paraméterfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="647b6-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="647b6-122">2. példa: A telepítés tesztelése egyéni sablonobjektummal és paraméterfájllal</span><span class="sxs-lookup"><span data-stu-id="647b6-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="647b6-123">Ez a parancs az aktuális előfizetési hatókörű telepítést teszteli egy adott sablonfájlból és egy paraméterfájlból létrehozott memória-kivonat segítségével.</span><span class="sxs-lookup"><span data-stu-id="647b6-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="647b6-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="647b6-124">PARAMETERS</span></span>

### <span data-ttu-id="647b6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647b6-125">-DefaultProfile</span></span>
<span data-ttu-id="647b6-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="647b6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="647b6-127">-Location</span><span class="sxs-lookup"><span data-stu-id="647b6-127">-Location</span></span>
<span data-ttu-id="647b6-128">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="647b6-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="647b6-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="647b6-129">-Pre</span></span>
<span data-ttu-id="647b6-130">Ha be van állítva, az azt jelenti, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="647b6-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="647b6-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="647b6-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="647b6-132">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="647b6-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="647b6-133">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="647b6-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="647b6-134">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="647b6-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="647b6-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="647b6-135">-TemplateFile</span></span>
<span data-ttu-id="647b6-136">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="647b6-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="647b6-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="647b6-137">-TemplateObject</span></span>
<span data-ttu-id="647b6-138">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="647b6-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="647b6-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="647b6-139">-TemplateParameterFile</span></span>
<span data-ttu-id="647b6-140">Olyan fájl, amely a sablon paramétereit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="647b6-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="647b6-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="647b6-141">-TemplateParameterObject</span></span>
<span data-ttu-id="647b6-142">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="647b6-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="647b6-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="647b6-143">-TemplateParameterUri</span></span>
<span data-ttu-id="647b6-144">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="647b6-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="647b6-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="647b6-145">-TemplateUri</span></span>
<span data-ttu-id="647b6-146">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="647b6-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="647b6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647b6-147">CommonParameters</span></span>
<span data-ttu-id="647b6-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="647b6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647b6-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="647b6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647b6-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="647b6-150">INPUTS</span></span>

### <span data-ttu-id="647b6-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="647b6-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="647b6-152">System.String</span><span class="sxs-lookup"><span data-stu-id="647b6-152">System.String</span></span>

## <span data-ttu-id="647b6-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="647b6-153">OUTPUTS</span></span>

### <span data-ttu-id="647b6-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="647b6-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="647b6-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="647b6-155">NOTES</span></span>

## <span data-ttu-id="647b6-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="647b6-156">RELATED LINKS</span></span>
