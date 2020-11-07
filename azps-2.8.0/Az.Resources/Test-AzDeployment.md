---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 182cf4d60cf2b81f5a465f9ffad5d862b09e3787
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838865"
---
# <span data-ttu-id="98fb7-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="98fb7-101">Test-AzDeployment</span></span>

## <span data-ttu-id="98fb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="98fb7-103">Ellenőrzi a központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="98fb7-103">Validates a deployment.</span></span>

## <span data-ttu-id="98fb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98fb7-104">SYNTAX</span></span>

### <span data-ttu-id="98fb7-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98fb7-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fb7-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="98fb7-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98fb7-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="98fb7-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98fb7-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="98fb7-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98fb7-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="98fb7-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98fb7-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="98fb7-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98fb7-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="98fb7-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98fb7-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="98fb7-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98fb7-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="98fb7-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98fb7-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="98fb7-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98fb7-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="98fb7-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fb7-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="98fb7-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98fb7-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="98fb7-117">DESCRIPTION</span></span>
<span data-ttu-id="98fb7-118">A **AzDeployment** parancsmag azt határozza meg, hogy a központi telepítő sablon és a paraméter értéke érvényes-e.</span><span class="sxs-lookup"><span data-stu-id="98fb7-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="98fb7-119">Példák</span><span class="sxs-lookup"><span data-stu-id="98fb7-119">EXAMPLES</span></span>

### <span data-ttu-id="98fb7-120">1. példa: a bevezetést tesztelheti egyéni sablonnal és paraméteres fájllal</span><span class="sxs-lookup"><span data-stu-id="98fb7-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="98fb7-121">Ez a parancs az aktuális előfizetési tartományon alapuló központi telepítés tesztelésére szolgál a megadott sablonfájl és a parameters (sablonfájl) fájllal.</span><span class="sxs-lookup"><span data-stu-id="98fb7-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="98fb7-122">2. példa: a bevezetést egyéni sablon objektummal és paraméterrel tartalmazó fájllal tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="98fb7-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="98fb7-123">Ez a parancs az aktuális előfizetési tartományon belüli, a megadott sablonfájl és a paraméteres fájlból létrehozott Hashtable segítségével teszteli a bevezetést.</span><span class="sxs-lookup"><span data-stu-id="98fb7-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="98fb7-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98fb7-124">PARAMETERS</span></span>

### <span data-ttu-id="98fb7-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="98fb7-125">-ApiVersion</span></span>
<span data-ttu-id="98fb7-126">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="98fb7-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="98fb7-127">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="98fb7-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="98fb7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fb7-128">-DefaultProfile</span></span>
<span data-ttu-id="98fb7-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98fb7-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98fb7-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="98fb7-130">-Location</span></span>
<span data-ttu-id="98fb7-131">A központi telepítő adatainak tárolására szolgáló hely.</span><span class="sxs-lookup"><span data-stu-id="98fb7-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="98fb7-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="98fb7-132">-Pre</span></span>
<span data-ttu-id="98fb7-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="98fb7-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="98fb7-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="98fb7-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="98fb7-135">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="98fb7-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="98fb7-136">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="98fb7-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="98fb7-137">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="98fb7-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="98fb7-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="98fb7-138">-TemplateFile</span></span>
<span data-ttu-id="98fb7-139">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="98fb7-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="98fb7-140">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="98fb7-140">-TemplateObject</span></span>
<span data-ttu-id="98fb7-141">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="98fb7-141">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="98fb7-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="98fb7-142">-TemplateParameterFile</span></span>
<span data-ttu-id="98fb7-143">A sablon paramétereit tartalmazó fájl</span><span class="sxs-lookup"><span data-stu-id="98fb7-143">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="98fb7-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="98fb7-144">-TemplateParameterObject</span></span>
<span data-ttu-id="98fb7-145">A paramétereket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="98fb7-145">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="98fb7-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="98fb7-146">-TemplateParameterUri</span></span>
<span data-ttu-id="98fb7-147">URI a sablon paraméter-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="98fb7-147">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="98fb7-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="98fb7-148">-TemplateUri</span></span>
<span data-ttu-id="98fb7-149">A sablonfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="98fb7-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="98fb7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fb7-150">CommonParameters</span></span>
<span data-ttu-id="98fb7-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98fb7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fb7-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98fb7-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fb7-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98fb7-153">INPUTS</span></span>

### <span data-ttu-id="98fb7-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="98fb7-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="98fb7-155">System. String</span><span class="sxs-lookup"><span data-stu-id="98fb7-155">System.String</span></span>

## <span data-ttu-id="98fb7-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98fb7-156">OUTPUTS</span></span>

### <span data-ttu-id="98fb7-157">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="98fb7-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="98fb7-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98fb7-158">NOTES</span></span>

## <span data-ttu-id="98fb7-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98fb7-159">RELATED LINKS</span></span>
