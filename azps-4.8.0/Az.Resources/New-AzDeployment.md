---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 56be1071c2a6307bee28f0ce4cf13dde626df72e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017664"
---
# <span data-ttu-id="569ec-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="569ec-101">New-AzDeployment</span></span>

## <span data-ttu-id="569ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="569ec-102">SYNOPSIS</span></span>
<span data-ttu-id="569ec-103">Központi telepítő létrehozása</span><span class="sxs-lookup"><span data-stu-id="569ec-103">Create a deployment</span></span>

## <span data-ttu-id="569ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="569ec-104">SYNTAX</span></span>

### <span data-ttu-id="569ec-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="569ec-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569ec-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="569ec-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="569ec-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="569ec-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="569ec-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="569ec-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="569ec-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="569ec-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="569ec-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="569ec-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569ec-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="569ec-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569ec-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="569ec-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="569ec-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="569ec-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569ec-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="569ec-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569ec-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="569ec-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569ec-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="569ec-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="569ec-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="569ec-117">DESCRIPTION</span></span>
<span data-ttu-id="569ec-118">A **New-AzDeployment** parancsmag bevezetést ad az aktuális előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="569ec-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="569ec-119">Ez a beállítás tartalmazza a telepítéshez szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="569ec-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="569ec-120">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás.</span><span class="sxs-lookup"><span data-stu-id="569ec-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="569ec-121">Az erőforrások egy erőforrás-csoportban, például az adatbázis-kiszolgálón, az adatbázisban, a webhelyen, a virtuális gépen vagy a tárterület-fiókban élhetnek.</span><span class="sxs-lookup"><span data-stu-id="569ec-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="569ec-122">Vagy lehet egy előfizetéses szintű erőforrás, például a szerepkör meghatározása, a házirend meghatározása stb.</span><span class="sxs-lookup"><span data-stu-id="569ec-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="569ec-123">Ha erőforrásokat szeretne felvenni egy erőforráscsoport számára, használja az **új AzResourceGroupDeployment** , amely egy erőforrás-csoportban hoz létre központi telepítést.</span><span class="sxs-lookup"><span data-stu-id="569ec-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="569ec-124">A **New-AzDeployment** parancsmag létrehoz egy központi telepítést a jelenlegi előfizetési tartományhoz, amely az előfizetési szint erőforrásait telepíti.</span><span class="sxs-lookup"><span data-stu-id="569ec-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="569ec-125">Ha fel szeretne venni egy üzembe állítást az előfizetésbe, adja meg a helyét és a sablont.</span><span class="sxs-lookup"><span data-stu-id="569ec-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="569ec-126">A hely közli az Azure Resource Manager szolgáltatással, hogy hol tárolja a központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="569ec-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="569ec-127">A sablon egy olyan JSON-karakterlánc, amely külön telepítendő erőforrásokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="569ec-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="569ec-128">A sablon tartalmazza a paraméterek helyőrzőit a szükséges erőforrások és a konfigurálható tulajdonságértékek (például nevek és méretek) esetében.</span><span class="sxs-lookup"><span data-stu-id="569ec-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="569ec-129">Ha egyéni sablont szeretne használni a központi telepítéséhez, adja meg a *TemplateFile* paramétert vagy a *TemplateUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="569ec-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="569ec-130">Mindegyik sablon rendelkezik a konfigurálható tulajdonságokra vonatkozó paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="569ec-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="569ec-131">A sablon paramétereinek értékeinek megadásához adja meg a *TemplateParameterFile* paramétert vagy a *TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="569ec-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="569ec-132">Azt is megteheti, hogy egy sablon megadásakor dinamikusan hozzáadja a parancsot a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="569ec-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="569ec-133">Ha dinamikus paramétereket szeretne használni, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) a paraméter jelzéséhez, és a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="569ec-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="569ec-134">A parancssorba beírt sablon paraméterei felülbírálják a Template paraméteres objektum vagy fájl értékeit.</span><span class="sxs-lookup"><span data-stu-id="569ec-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="569ec-135">Példák</span><span class="sxs-lookup"><span data-stu-id="569ec-135">EXAMPLES</span></span>

### <span data-ttu-id="569ec-136">1. példa: egyéni sablon és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="569ec-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="569ec-137">Ez a parancs létrehoz egy új üzembe állítást az aktuális előfizetési tartományhoz egy egyéni sablon és egy sablonfájl segítségével a lemezen, a definiált címkék paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="569ec-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="569ec-138">A parancs a *TemplateFile* paramétert használva adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="569ec-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="569ec-139">A *TemplateVersion* paramétert használja a sablon verziójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="569ec-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="569ec-140">2. példa: egyéni sablon objektum és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="569ec-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="569ec-141">A parancs létrehoz egy új üzembe állítást az aktuális előfizetési tartományhoz egy egyéni sablon és egy olyan lemezen lévő sablonfájl segítségével, amelyet a rendszer a memória Hashtable konvertált.</span><span class="sxs-lookup"><span data-stu-id="569ec-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="569ec-142">Az első két parancs elolvassa a sablonfájl szövegét a lemezen, és a memória-Hashtable alakítja.</span><span class="sxs-lookup"><span data-stu-id="569ec-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="569ec-143">Az utolsó parancs a *TemplateObject* paraméterrel adja meg ezt a Hashtable és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="569ec-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="569ec-144">A *TemplateVersion* paramétert használja a sablon verziójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="569ec-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="569ec-145">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="569ec-145">PARAMETERS</span></span>

### <span data-ttu-id="569ec-146">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="569ec-146">-ApiVersion</span></span>
<span data-ttu-id="569ec-147">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="569ec-147">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="569ec-148">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="569ec-148">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="569ec-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="569ec-149">-AsJob</span></span>
<span data-ttu-id="569ec-150">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="569ec-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="569ec-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569ec-151">-DefaultProfile</span></span>
<span data-ttu-id="569ec-152">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="569ec-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="569ec-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="569ec-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="569ec-154">A központi telepítő naplózási szintje.</span><span class="sxs-lookup"><span data-stu-id="569ec-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="569ec-155">-Hely</span><span class="sxs-lookup"><span data-stu-id="569ec-155">-Location</span></span>
<span data-ttu-id="569ec-156">A központi telepítő adatainak tárolására szolgáló hely.</span><span class="sxs-lookup"><span data-stu-id="569ec-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="569ec-157">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="569ec-157">-Name</span></span>
<span data-ttu-id="569ec-158">Annak a telepítőnek a neve, amelyet létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="569ec-158">The name of the deployment it's going to create.</span></span> <span data-ttu-id="569ec-159">Ha nem adja meg, akkor az alapértelmezett érték a sablonfájl nevében, amikor a sablonfájl meg van adva. Alapértelmezés szerint az aktuális időpontot kapja, ha a Template-objektum meg van határozva, például "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="569ec-159">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569ec-160">-Pre</span><span class="sxs-lookup"><span data-stu-id="569ec-160">-Pre</span></span>
<span data-ttu-id="569ec-161">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="569ec-161">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="569ec-162">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="569ec-162">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="569ec-163">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="569ec-163">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="569ec-164">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="569ec-164">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="569ec-165">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="569ec-165">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="569ec-166">-Címke</span><span class="sxs-lookup"><span data-stu-id="569ec-166">-Tag</span></span>
<span data-ttu-id="569ec-167">A üzembe helyezett címkék.</span><span class="sxs-lookup"><span data-stu-id="569ec-167">The tags to put on the deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569ec-168">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="569ec-168">-TemplateFile</span></span>
<span data-ttu-id="569ec-169">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="569ec-169">Local path to the template file.</span></span>

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

### <span data-ttu-id="569ec-170">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="569ec-170">-TemplateObject</span></span>
<span data-ttu-id="569ec-171">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="569ec-171">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="569ec-172">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="569ec-172">-TemplateParameterFile</span></span>
<span data-ttu-id="569ec-173">A sablon paramétereit tartalmazó fájl</span><span class="sxs-lookup"><span data-stu-id="569ec-173">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="569ec-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="569ec-174">-TemplateParameterObject</span></span>
<span data-ttu-id="569ec-175">A paramétereket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="569ec-175">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="569ec-176">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="569ec-176">-TemplateParameterUri</span></span>
<span data-ttu-id="569ec-177">URI a sablon paraméter-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="569ec-177">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="569ec-178">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="569ec-178">-TemplateUri</span></span>
<span data-ttu-id="569ec-179">A sablonfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="569ec-179">Uri to the template file.</span></span>

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

### <span data-ttu-id="569ec-180">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="569ec-180">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="569ec-181">Vesszővel elválasztott erőforrás-módosítási típusokat kell kizárni What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="569ec-181">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="569ec-182">A-WhatIf vagy a-Confirm kapcsoló beállításakor alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="569ec-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569ec-183">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="569ec-183">-WhatIfResultFormat</span></span>
<span data-ttu-id="569ec-184">A What-If eredmény formátuma.</span><span class="sxs-lookup"><span data-stu-id="569ec-184">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569ec-185">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="569ec-185">-Confirm</span></span>
<span data-ttu-id="569ec-186">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="569ec-186">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569ec-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="569ec-187">-WhatIf</span></span>
<span data-ttu-id="569ec-188">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="569ec-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="569ec-189">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="569ec-189">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569ec-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569ec-190">CommonParameters</span></span>
<span data-ttu-id="569ec-191">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="569ec-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569ec-192">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="569ec-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569ec-193">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="569ec-193">INPUTS</span></span>

### <span data-ttu-id="569ec-194">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="569ec-194">System.Collections.Hashtable</span></span>

### <span data-ttu-id="569ec-195">System. String</span><span class="sxs-lookup"><span data-stu-id="569ec-195">System.String</span></span>

## <span data-ttu-id="569ec-196">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="569ec-196">OUTPUTS</span></span>

### <span data-ttu-id="569ec-197">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="569ec-197">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="569ec-198">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="569ec-198">NOTES</span></span>

## <span data-ttu-id="569ec-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="569ec-199">RELATED LINKS</span></span>
