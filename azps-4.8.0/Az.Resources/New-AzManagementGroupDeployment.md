---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: c15a7fca43568e63b8e7407b5c2048d03b9b6bc1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184005"
---
# <span data-ttu-id="8b87d-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b87d-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="8b87d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b87d-102">SYNOPSIS</span></span>
<span data-ttu-id="8b87d-103">Bevezetés létrehozása felügyeleti csoportban</span><span class="sxs-lookup"><span data-stu-id="8b87d-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="8b87d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b87d-104">SYNTAX</span></span>

### <span data-ttu-id="8b87d-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b87d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b87d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8b87d-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b87d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8b87d-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b87d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8b87d-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b87d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8b87d-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b87d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8b87d-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b87d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8b87d-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b87d-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8b87d-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b87d-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8b87d-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b87d-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8b87d-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b87d-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8b87d-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b87d-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8b87d-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b87d-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b87d-117">DESCRIPTION</span></span>
<span data-ttu-id="8b87d-118">A **New-AzManagementGroupDeployment** parancsmag egy felügyeleti csoportba helyezi a bevezetést.</span><span class="sxs-lookup"><span data-stu-id="8b87d-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="8b87d-119">Ha egy felügyeleti csoportban szeretne bevezetést hozzáadni, adja meg a kezelési csoportot, a helyet és a sablont.</span><span class="sxs-lookup"><span data-stu-id="8b87d-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="8b87d-120">A hely közli az Azure Resource Manager szolgáltatással, hogy hol tárolja a központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="8b87d-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="8b87d-121">A sablon egy olyan JSON-karakterlánc, amely külön telepítendő erőforrásokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="8b87d-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="8b87d-122">A sablon tartalmazza a paraméterek helyőrzőit a szükséges erőforrások és a konfigurálható tulajdonságértékek (például nevek és méretek) esetében.</span><span class="sxs-lookup"><span data-stu-id="8b87d-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="8b87d-123">Ha egyéni sablont szeretne használni a központi telepítéséhez, adja meg a *TemplateFile* paramétert vagy a *TemplateUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="8b87d-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="8b87d-124">Mindegyik sablon rendelkezik a konfigurálható tulajdonságokra vonatkozó paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="8b87d-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="8b87d-125">A sablon paramétereinek értékeinek megadásához adja meg a *TemplateParameterFile* paramétert vagy a *TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="8b87d-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="8b87d-126">Azt is megteheti, hogy egy sablon megadásakor dinamikusan hozzáadja a parancsot a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="8b87d-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="8b87d-127">Ha dinamikus paramétereket szeretne használni, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) a paraméter jelzéséhez, és a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="8b87d-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="8b87d-128">A parancssorba beírt sablon paraméterei felülbírálják a Template paraméteres objektum vagy fájl értékeit.</span><span class="sxs-lookup"><span data-stu-id="8b87d-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="8b87d-129">Ha erőforrásokat szeretne felvenni egy erőforráscsoport számára, használja az **új AzResourceGroupDeployment** , amely egy erőforrás-csoportban hoz létre központi telepítést.</span><span class="sxs-lookup"><span data-stu-id="8b87d-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="8b87d-130">Ha erőforrásokat szeretne hozzáadni az előfizetéshez, használja a **AzSubscriptionDeployment** , amely létrehoz egy telepítést az előfizetéses hatókörben, amely az előfizetési szint erőforrásait telepíti.</span><span class="sxs-lookup"><span data-stu-id="8b87d-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="8b87d-131">Ha erőforrásokat szeretne felvenni a bérlői hatókörben, használja az **új AzTenantDeployment** , amely a bérlői hatókörben létrehoz egy bevezetést.</span><span class="sxs-lookup"><span data-stu-id="8b87d-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="8b87d-132">Példák</span><span class="sxs-lookup"><span data-stu-id="8b87d-132">EXAMPLES</span></span>

### <span data-ttu-id="8b87d-133">1. példa: egyéni sablon és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="8b87d-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="8b87d-134">A parancs létrehoz egy új üzembe állítást a "myMG" felügyeleti csoportnál egy egyéni sablon és egy sablonfájl segítségével a lemezen, a definiált címkék paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="8b87d-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="8b87d-135">A parancs a *TemplateFile* paramétert használva adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="8b87d-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="8b87d-136">2. példa: egyéni sablon objektum és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="8b87d-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="8b87d-137">Ez a parancs egy új üzembe állítást hoz létre a "myMG" felügyeleti csoportnál egy egyéni sablon és egy olyan lemezen lévő sablonfájl használatával, amely a memória-Hashtable lett átalakítva.</span><span class="sxs-lookup"><span data-stu-id="8b87d-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="8b87d-138">Az első két parancs elolvassa a sablonfájl szövegét a lemezen, és a memória-Hashtable alakítja.</span><span class="sxs-lookup"><span data-stu-id="8b87d-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="8b87d-139">Az utolsó parancs a *TemplateObject* paraméterrel adja meg ezt a Hashtable és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="8b87d-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="8b87d-140">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b87d-140">PARAMETERS</span></span>

### <span data-ttu-id="8b87d-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8b87d-141">-ApiVersion</span></span>
<span data-ttu-id="8b87d-142">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b87d-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8b87d-143">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8b87d-143">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8b87d-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b87d-144">-AsJob</span></span>
<span data-ttu-id="8b87d-145">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8b87d-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b87d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b87d-146">-DefaultProfile</span></span>
<span data-ttu-id="8b87d-147">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b87d-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b87d-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="8b87d-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="8b87d-149">A központi telepítő naplózási szintje.</span><span class="sxs-lookup"><span data-stu-id="8b87d-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="8b87d-150">-Hely</span><span class="sxs-lookup"><span data-stu-id="8b87d-150">-Location</span></span>
<span data-ttu-id="8b87d-151">A központi telepítő adatainak tárolására szolgáló hely.</span><span class="sxs-lookup"><span data-stu-id="8b87d-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="8b87d-152">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="8b87d-152">-ManagementGroupId</span></span>
<span data-ttu-id="8b87d-153">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8b87d-153">The management group ID.</span></span>

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

### <span data-ttu-id="8b87d-154">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b87d-154">-Name</span></span>
<span data-ttu-id="8b87d-155">Annak a telepítőnek a neve, amelyet létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="8b87d-155">The name of the deployment it's going to create.</span></span> <span data-ttu-id="8b87d-156">Ha nem adja meg, akkor az alapértelmezett érték a sablonfájl nevében, amikor a sablonfájl meg van adva. Alapértelmezés szerint az aktuális időpontot kapja, ha a Template-objektum meg van határozva, például "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="8b87d-156">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="8b87d-157">-Pre</span><span class="sxs-lookup"><span data-stu-id="8b87d-157">-Pre</span></span>
<span data-ttu-id="8b87d-158">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8b87d-158">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8b87d-159">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="8b87d-159">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="8b87d-160">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="8b87d-160">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="8b87d-161">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="8b87d-161">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="8b87d-162">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="8b87d-162">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="8b87d-163">-Címke</span><span class="sxs-lookup"><span data-stu-id="8b87d-163">-Tag</span></span>
<span data-ttu-id="8b87d-164">A üzembe helyezett címkék.</span><span class="sxs-lookup"><span data-stu-id="8b87d-164">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="8b87d-165">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8b87d-165">-TemplateFile</span></span>
<span data-ttu-id="8b87d-166">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="8b87d-166">Local path to the template file.</span></span>

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

### <span data-ttu-id="8b87d-167">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="8b87d-167">-TemplateObject</span></span>
<span data-ttu-id="8b87d-168">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="8b87d-168">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="8b87d-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8b87d-169">-TemplateParameterFile</span></span>
<span data-ttu-id="8b87d-170">A sablon paramétereit tartalmazó fájl</span><span class="sxs-lookup"><span data-stu-id="8b87d-170">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="8b87d-171">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8b87d-171">-TemplateParameterObject</span></span>
<span data-ttu-id="8b87d-172">A paramétereket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="8b87d-172">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="8b87d-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8b87d-173">-TemplateParameterUri</span></span>
<span data-ttu-id="8b87d-174">URI a sablon paraméter-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="8b87d-174">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="8b87d-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8b87d-175">-TemplateUri</span></span>
<span data-ttu-id="8b87d-176">A sablonfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="8b87d-176">Uri to the template file.</span></span>

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

### <span data-ttu-id="8b87d-177">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="8b87d-177">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="8b87d-178">Vesszővel elválasztott erőforrás-módosítási típusokat kell kizárni What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="8b87d-178">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="8b87d-179">A-WhatIf vagy a-Confirm kapcsoló beállításakor alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="8b87d-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="8b87d-180">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="8b87d-180">-WhatIfResultFormat</span></span>
<span data-ttu-id="8b87d-181">A What-If eredmény formátuma.</span><span class="sxs-lookup"><span data-stu-id="8b87d-181">The What-If result format.</span></span> <span data-ttu-id="8b87d-182">A-WhatIf vagy a-Confirm kapcsoló beállításakor alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="8b87d-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="8b87d-183">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b87d-183">-Confirm</span></span>
<span data-ttu-id="8b87d-184">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b87d-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b87d-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b87d-185">-WhatIf</span></span>
<span data-ttu-id="8b87d-186">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8b87d-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b87d-187">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b87d-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b87d-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b87d-188">CommonParameters</span></span>
<span data-ttu-id="8b87d-189">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b87d-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b87d-190">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8b87d-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b87d-191">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b87d-191">INPUTS</span></span>

### <span data-ttu-id="8b87d-192">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8b87d-192">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8b87d-193">System. String</span><span class="sxs-lookup"><span data-stu-id="8b87d-193">System.String</span></span>

## <span data-ttu-id="8b87d-194">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b87d-194">OUTPUTS</span></span>

### <span data-ttu-id="8b87d-195">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="8b87d-195">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8b87d-196">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b87d-196">NOTES</span></span>

## <span data-ttu-id="8b87d-197">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b87d-197">RELATED LINKS</span></span>
