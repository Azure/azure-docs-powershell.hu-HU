---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 38f46b8805b8e259b086e5c5a78e929112dca83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845873"
---
# <span data-ttu-id="6f2db-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f2db-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="6f2db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f2db-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2db-103">Bevezetés létrehozása bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="6f2db-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="6f2db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f2db-104">SYNTAX</span></span>

### <span data-ttu-id="6f2db-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f2db-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f2db-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6f2db-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f2db-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6f2db-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f2db-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6f2db-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f2db-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6f2db-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f2db-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6f2db-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f2db-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6f2db-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f2db-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6f2db-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f2db-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6f2db-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f2db-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6f2db-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f2db-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6f2db-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f2db-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6f2db-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f2db-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f2db-117">DESCRIPTION</span></span>
<span data-ttu-id="6f2db-118">A **New-AzTenantDeployment** parancsmag bevezetést ad a jelenlegi bérlői hatókörhöz.</span><span class="sxs-lookup"><span data-stu-id="6f2db-118">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="6f2db-119">Ha a bérlői hatókörben szeretne bevezetést hozzáadni, adja meg a helyet és a sablont.</span><span class="sxs-lookup"><span data-stu-id="6f2db-119">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="6f2db-120">A hely közli az Azure Resource Manager szolgáltatással, hogy hol tárolja a központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="6f2db-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="6f2db-121">A sablon egy olyan JSON-karakterlánc, amely külön telepítendő erőforrásokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6f2db-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="6f2db-122">A sablon tartalmazza a paraméterek helyőrzőit a szükséges erőforrások és a konfigurálható tulajdonságértékek (például nevek és méretek) esetében.</span><span class="sxs-lookup"><span data-stu-id="6f2db-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="6f2db-123">Ha egyéni sablont szeretne használni a központi telepítéséhez, adja meg a *TemplateFile* paramétert vagy a *TemplateUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="6f2db-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="6f2db-124">Mindegyik sablon rendelkezik a konfigurálható tulajdonságokra vonatkozó paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="6f2db-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="6f2db-125">A sablon paramétereinek értékeinek megadásához adja meg a *TemplateParameterFile* paramétert vagy a *TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="6f2db-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="6f2db-126">Azt is megteheti, hogy egy sablon megadásakor dinamikusan hozzáadja a parancsot a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="6f2db-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="6f2db-127">Ha dinamikus paramétereket szeretne használni, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) a paraméter jelzéséhez, és a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="6f2db-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="6f2db-128">A parancssorba beírt sablon paraméterei felülbírálják a Template paraméteres objektum vagy fájl értékeit.</span><span class="sxs-lookup"><span data-stu-id="6f2db-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="6f2db-129">Ha erőforrásokat szeretne felvenni egy erőforráscsoport számára, használja az **új AzResourceGroupDeployment** , amely egy erőforrás-csoportban hoz létre központi telepítést.</span><span class="sxs-lookup"><span data-stu-id="6f2db-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="6f2db-130">Ha erőforrásokat szeretne hozzáadni az előfizetéshez, használja a **AzSubscriptionDeployment** , amely létrehoz egy telepítést az előfizetéses hatókörben, amely az előfizetési szint erőforrásait telepíti.</span><span class="sxs-lookup"><span data-stu-id="6f2db-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="6f2db-131">Ha erőforrásokat szeretne felvenni egy felügyeleti csoportba, használja az **új AzManagementGroupDeployment** , amely egy felügyeleti csoportban hoz létre központi telepítést.</span><span class="sxs-lookup"><span data-stu-id="6f2db-131">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="6f2db-132">Példák</span><span class="sxs-lookup"><span data-stu-id="6f2db-132">EXAMPLES</span></span>

### <span data-ttu-id="6f2db-133">1. példa: egyéni sablon és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="6f2db-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="6f2db-134">A parancs létrehoz egy új üzembe állítást az aktuális bérlői hatókörben egy egyéni sablon és egy, a lemezen lévő sablonfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="6f2db-134">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="6f2db-135">A parancs a *TemplateFile* paramétert használva adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="6f2db-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="6f2db-136">2. példa: egyéni sablon objektum és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="6f2db-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="6f2db-137">A parancs a jelenlegi bérlői webhelyre egy egyéni sablon és egy, a memória Hashtable-ra átalakított sablonfájl segítségével hoz létre új központi üzembe állítást.</span><span class="sxs-lookup"><span data-stu-id="6f2db-137">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="6f2db-138">Az első két parancs elolvassa a sablonfájl szövegét a lemezen, és a memória-Hashtable alakítja.</span><span class="sxs-lookup"><span data-stu-id="6f2db-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="6f2db-139">Az utolsó parancs a *TemplateObject* paraméterrel adja meg ezt a Hashtable és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="6f2db-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="6f2db-140">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f2db-140">PARAMETERS</span></span>

### <span data-ttu-id="6f2db-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f2db-141">-ApiVersion</span></span>
<span data-ttu-id="6f2db-142">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f2db-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6f2db-143">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6f2db-143">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6f2db-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f2db-144">-AsJob</span></span>
<span data-ttu-id="6f2db-145">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6f2db-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f2db-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f2db-146">-DefaultProfile</span></span>
<span data-ttu-id="6f2db-147">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f2db-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f2db-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="6f2db-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="6f2db-149">A központi telepítő naplózási szintje.</span><span class="sxs-lookup"><span data-stu-id="6f2db-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="6f2db-150">-Hely</span><span class="sxs-lookup"><span data-stu-id="6f2db-150">-Location</span></span>
<span data-ttu-id="6f2db-151">A központi telepítő adatainak tárolására szolgáló hely.</span><span class="sxs-lookup"><span data-stu-id="6f2db-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="6f2db-152">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f2db-152">-Name</span></span>
<span data-ttu-id="6f2db-153">Annak a telepítőnek a neve, amelyet létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="6f2db-153">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="6f2db-154">Csak akkor érvényes, ha sablon van használatban.</span><span class="sxs-lookup"><span data-stu-id="6f2db-154">Only valid when a template is used.</span></span>
<span data-ttu-id="6f2db-155">Ha egy sablont használ, ha a felhasználó nem ad meg központi telepítés nevét, használja az aktuális időpontot, például "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="6f2db-155">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2db-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="6f2db-156">-Pre</span></span>
<span data-ttu-id="6f2db-157">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6f2db-157">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6f2db-158">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="6f2db-158">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="6f2db-159">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="6f2db-159">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="6f2db-160">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="6f2db-160">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="6f2db-161">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="6f2db-161">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="6f2db-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="6f2db-162">-TemplateFile</span></span>
<span data-ttu-id="6f2db-163">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6f2db-163">Local path to the template file.</span></span>

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

### <span data-ttu-id="6f2db-164">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="6f2db-164">-TemplateObject</span></span>
<span data-ttu-id="6f2db-165">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="6f2db-165">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="6f2db-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="6f2db-166">-TemplateParameterFile</span></span>
<span data-ttu-id="6f2db-167">A sablon paramétereit tartalmazó fájl</span><span class="sxs-lookup"><span data-stu-id="6f2db-167">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="6f2db-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="6f2db-168">-TemplateParameterObject</span></span>
<span data-ttu-id="6f2db-169">A paramétereket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="6f2db-169">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="6f2db-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="6f2db-170">-TemplateParameterUri</span></span>
<span data-ttu-id="6f2db-171">URI a sablon paraméter-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="6f2db-171">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="6f2db-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="6f2db-172">-TemplateUri</span></span>
<span data-ttu-id="6f2db-173">A sablonfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="6f2db-173">Uri to the template file.</span></span>

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

### <span data-ttu-id="6f2db-174">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6f2db-174">-Confirm</span></span>
<span data-ttu-id="6f2db-175">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6f2db-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2db-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f2db-176">-WhatIf</span></span>
<span data-ttu-id="6f2db-177">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6f2db-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f2db-178">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6f2db-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2db-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2db-179">CommonParameters</span></span>
<span data-ttu-id="6f2db-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f2db-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2db-181">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6f2db-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2db-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f2db-182">INPUTS</span></span>

### <span data-ttu-id="6f2db-183">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6f2db-183">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6f2db-184">System. String</span><span class="sxs-lookup"><span data-stu-id="6f2db-184">System.String</span></span>

## <span data-ttu-id="6f2db-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f2db-185">OUTPUTS</span></span>

### <span data-ttu-id="6f2db-186">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="6f2db-186">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="6f2db-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f2db-187">NOTES</span></span>

## <span data-ttu-id="6f2db-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f2db-188">RELATED LINKS</span></span>
