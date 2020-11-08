---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 60db8b7b544b63e29b4834676da946ebbf6c39c3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182168"
---
# <span data-ttu-id="650be-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="650be-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="650be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="650be-102">SYNOPSIS</span></span>
<span data-ttu-id="650be-103">A bevezetést a bérlői hatókörben ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="650be-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="650be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="650be-104">SYNTAX</span></span>

### <span data-ttu-id="650be-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="650be-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="650be-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="650be-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="650be-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="650be-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="650be-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="650be-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="650be-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="650be-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="650be-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="650be-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="650be-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="650be-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="650be-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="650be-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="650be-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="650be-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="650be-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="650be-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="650be-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="650be-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="650be-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="650be-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="650be-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="650be-117">DESCRIPTION</span></span>
<span data-ttu-id="650be-118">A **AzTenantDeployment** parancsmag azt határozza meg, hogy a központi telepítő sablon és a paraméter értéke érvényes-e a jelenlegi bérlői tartományra.</span><span class="sxs-lookup"><span data-stu-id="650be-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="650be-119">Példák</span><span class="sxs-lookup"><span data-stu-id="650be-119">EXAMPLES</span></span>

### <span data-ttu-id="650be-120">1. példa: a bevezetést tesztelheti egyéni sablonnal és paraméteres fájllal</span><span class="sxs-lookup"><span data-stu-id="650be-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="650be-121">Ez a parancs a megadott sablonfájl és a Parameters fájl segítségével teszteli az aktuális bérlői hatókört.</span><span class="sxs-lookup"><span data-stu-id="650be-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="650be-122">2. példa: a bevezetést egyéni sablon objektummal és paraméterrel tartalmazó fájllal tesztelheti.</span><span class="sxs-lookup"><span data-stu-id="650be-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="650be-123">Ez a parancs az aktuális bérlői hatókörben végzett bevezetést teszteli a megadott sablonfájl és egy paraméter-fájl alapján létrehozott beépített Hashtable segítségével.</span><span class="sxs-lookup"><span data-stu-id="650be-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="650be-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="650be-124">PARAMETERS</span></span>

### <span data-ttu-id="650be-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="650be-125">-ApiVersion</span></span>
<span data-ttu-id="650be-126">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="650be-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="650be-127">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="650be-127">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650be-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650be-128">-DefaultProfile</span></span>
<span data-ttu-id="650be-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="650be-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650be-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="650be-130">-Location</span></span>
<span data-ttu-id="650be-131">A központi telepítő adatainak tárolására szolgáló hely.</span><span class="sxs-lookup"><span data-stu-id="650be-131">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650be-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="650be-132">-Pre</span></span>
<span data-ttu-id="650be-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="650be-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650be-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="650be-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="650be-135">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="650be-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="650be-136">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="650be-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="650be-137">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="650be-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650be-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="650be-138">-TemplateFile</span></span>
<span data-ttu-id="650be-139">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="650be-139">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="650be-140">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="650be-140">-TemplateObject</span></span>
<span data-ttu-id="650be-141">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="650be-141">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="650be-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="650be-142">-TemplateParameterFile</span></span>
<span data-ttu-id="650be-143">A sablon paramétereit tartalmazó fájl</span><span class="sxs-lookup"><span data-stu-id="650be-143">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="650be-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="650be-144">-TemplateParameterObject</span></span>
<span data-ttu-id="650be-145">A paramétereket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="650be-145">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="650be-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="650be-146">-TemplateParameterUri</span></span>
<span data-ttu-id="650be-147">URI a sablon paraméter-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="650be-147">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="650be-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="650be-148">-TemplateUri</span></span>
<span data-ttu-id="650be-149">A sablonfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="650be-149">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="650be-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650be-150">CommonParameters</span></span>
<span data-ttu-id="650be-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="650be-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650be-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="650be-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650be-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="650be-153">INPUTS</span></span>

### <span data-ttu-id="650be-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="650be-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="650be-155">System. String</span><span class="sxs-lookup"><span data-stu-id="650be-155">System.String</span></span>

## <span data-ttu-id="650be-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="650be-156">OUTPUTS</span></span>

### <span data-ttu-id="650be-157">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="650be-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="650be-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="650be-158">NOTES</span></span>

## <span data-ttu-id="650be-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="650be-159">RELATED LINKS</span></span>
