---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: d2a54022768bd3751ed18713fdc123ef2ef9cbf1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208446"
---
# <span data-ttu-id="f84ef-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f84ef-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="f84ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f84ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f84ef-103">Telepítés létrehozása bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="f84ef-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="f84ef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f84ef-104">SYNTAX</span></span>

### <span data-ttu-id="f84ef-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f84ef-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84ef-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f84ef-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f84ef-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f84ef-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f84ef-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f84ef-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f84ef-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f84ef-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f84ef-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f84ef-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84ef-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f84ef-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84ef-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="f84ef-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f84ef-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f84ef-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f84ef-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f84ef-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84ef-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f84ef-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84ef-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="f84ef-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84ef-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f84ef-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84ef-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f84ef-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84ef-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="f84ef-119">ByTemplateSpecResourceId</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f84ef-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f84ef-120">DESCRIPTION</span></span>
<span data-ttu-id="f84ef-121">A **New-AzTenantDeployment** parancsmag hozzáad egy telepítést a bérlő aktuális hatókörében.</span><span class="sxs-lookup"><span data-stu-id="f84ef-121">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="f84ef-122">Ha bérlői hatókörben szeretne központi telepítést hozzáadni, adja meg a helyet és egy sablont.</span><span class="sxs-lookup"><span data-stu-id="f84ef-122">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="f84ef-123">A hely közli az Azure Resource Managerrel, hogy hol kell tárolni a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="f84ef-123">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="f84ef-124">A sablon egy JSON-karakterlánc, amely az egyes telepítend kívánt erőforrásokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f84ef-124">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="f84ef-125">A sablon paraméterhelyőrzőket tartalmaz a kötelező erőforrásokhoz és a konfigurálható tulajdonságértékekhez, például a nevekhez és a méretekhez.</span><span class="sxs-lookup"><span data-stu-id="f84ef-125">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="f84ef-126">Ha egyéni sablont használ a telepítéshez, adja meg a *TemplateFile* vagy *a TemplateUri paramétert.*</span><span class="sxs-lookup"><span data-stu-id="f84ef-126">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="f84ef-127">Minden sablon rendelkezik paraméterekkel a konfigurálható tulajdonságokhoz.</span><span class="sxs-lookup"><span data-stu-id="f84ef-127">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="f84ef-128">A sablonparaméterek értékeinek megadásához adja meg a *TemplateParameterFile* vagy *a TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="f84ef-128">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="f84ef-129">Másik lehetőségként használhatja a sablon megadásakor a parancshoz dinamikusan hozzáadott sablonparamétereket is.</span><span class="sxs-lookup"><span data-stu-id="f84ef-129">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="f84ef-130">Ha dinamikus paramétereket használ, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) egy paraméter jelzésére, és a Tab billentyűvel lépked az elérhető paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="f84ef-130">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="f84ef-131">A parancssorba beírandó sablon paraméterértékei elsőbbséget élveznek a sablon paraméterobjektumában vagy -fájljában megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="f84ef-131">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="f84ef-132">Ha erőforrásokat szeretne hozzáadni egy erőforráscsoporthoz, használja a **New-AzResourceGroupDeployment** bővítményt, amely létrehoz egy telepítést egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f84ef-132">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="f84ef-133">Ha erőforrásokat szeretne hozzáadni egy előfizetéshez, használja a **New-AzSubscriptionDeployment** bővítményt, amely létrehoz egy telepítést az előfizetési hatókörben, amely az előfizetési szintű erőforrásokat telepíti.</span><span class="sxs-lookup"><span data-stu-id="f84ef-133">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="f84ef-134">Ha erőforrásokat szeretne hozzáadni egy felügyeleti csoporthoz, használja a **New-AzManagementGroupDeployment** bővítményt, amely létrehoz egy központi telepítést egy felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="f84ef-134">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="f84ef-135">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f84ef-135">EXAMPLES</span></span>

### <span data-ttu-id="f84ef-136">1. példa: Egyéni sablon és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="f84ef-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="f84ef-137">Ez a parancs új telepítést hoz létre a bérlő aktuális hatókörében egy egyéni sablon és egy lemezen lévő sablonfájl használatával, meghatározott címke paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="f84ef-137">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="f84ef-138">A parancs *a TemplateFile paraméterrel* adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="f84ef-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="f84ef-139">2. példa: Egyéni sablonobjektum és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="f84ef-139">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="f84ef-140">Ez a parancs új telepítést hoz létre az aktuális bérlői webhelyen egy egyéni sablon és egy lemezen lévő sablonfájl használatával, amelyet a rendszer memóriában lévő hashtable-ként konvertált.</span><span class="sxs-lookup"><span data-stu-id="f84ef-140">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="f84ef-141">Az első két parancs felolvassa a lemezen lévő sablonfájl szövegét, és átalakítja azt egy memóriában lévő hashtable-ként.</span><span class="sxs-lookup"><span data-stu-id="f84ef-141">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="f84ef-142">Az utolsó parancs *a TemplateObject* paraméter segítségével adja meg ezt a hashtable és *a TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="f84ef-142">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="f84ef-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f84ef-143">PARAMETERS</span></span>

### <span data-ttu-id="f84ef-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f84ef-144">-AsJob</span></span>
<span data-ttu-id="f84ef-145">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f84ef-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f84ef-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84ef-146">-DefaultProfile</span></span>
<span data-ttu-id="f84ef-147">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f84ef-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f84ef-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="f84ef-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="f84ef-149">A központi telepítés hibakeresési naplószintje.</span><span class="sxs-lookup"><span data-stu-id="f84ef-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="f84ef-150">-Location</span><span class="sxs-lookup"><span data-stu-id="f84ef-150">-Location</span></span>
<span data-ttu-id="f84ef-151">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="f84ef-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="f84ef-152">-Name</span><span class="sxs-lookup"><span data-stu-id="f84ef-152">-Name</span></span>
<span data-ttu-id="f84ef-153">Annak a telepítésnek a neve, amelyből létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="f84ef-153">The name of the deployment it's going to create.</span></span> <span data-ttu-id="f84ef-154">Ha nincs megadva, alapértelmezés szerint a sablonfájl neve lesz megadva; sablonobjektumok (például "2013123140835") beállítása.</span><span class="sxs-lookup"><span data-stu-id="f84ef-154">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="f84ef-155">-Pre</span><span class="sxs-lookup"><span data-stu-id="f84ef-155">-Pre</span></span>
<span data-ttu-id="f84ef-156">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f84ef-156">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f84ef-157">-QueryString</span><span class="sxs-lookup"><span data-stu-id="f84ef-157">-QueryString</span></span>
<span data-ttu-id="f84ef-158">A TemplateUri paraméterrel használt lekérdezési karakterlánc (például EGY SAS-jogkivonat).</span><span class="sxs-lookup"><span data-stu-id="f84ef-158">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="f84ef-159">Hivatkozott sablonok esetén használható</span><span class="sxs-lookup"><span data-stu-id="f84ef-159">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="f84ef-160">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="f84ef-160">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="f84ef-161">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="f84ef-161">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="f84ef-162">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="f84ef-162">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="f84ef-163">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="f84ef-163">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="f84ef-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="f84ef-164">-Tag</span></span>
<span data-ttu-id="f84ef-165">Az üzembe helyezéshez szükséges címkék.</span><span class="sxs-lookup"><span data-stu-id="f84ef-165">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="f84ef-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f84ef-166">-TemplateFile</span></span>
<span data-ttu-id="f84ef-167">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f84ef-167">Local path to the template file.</span></span>

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

### <span data-ttu-id="f84ef-168">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="f84ef-168">-TemplateObject</span></span>
<span data-ttu-id="f84ef-169">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="f84ef-169">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="f84ef-170">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f84ef-170">-TemplateParameterFile</span></span>
<span data-ttu-id="f84ef-171">Olyan fájl, amely a sablon paramétereit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f84ef-171">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="f84ef-172">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f84ef-172">-TemplateParameterObject</span></span>
<span data-ttu-id="f84ef-173">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="f84ef-173">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="f84ef-174">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f84ef-174">-TemplateParameterUri</span></span>
<span data-ttu-id="f84ef-175">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="f84ef-175">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="f84ef-176">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="f84ef-176">-TemplateSpecId</span></span>
<span data-ttu-id="f84ef-177">A telepíteni kívánt sablonSpec erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f84ef-177">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="f84ef-178">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f84ef-178">-TemplateUri</span></span>
<span data-ttu-id="f84ef-179">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="f84ef-179">Uri to the template file.</span></span>

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

### <span data-ttu-id="f84ef-180">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="f84ef-180">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="f84ef-181">A vesszővel elválasztott erőforrás-módosítási típusokat nem lehet kizárni a What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="f84ef-181">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="f84ef-182">Akkor alkalmazható, ha a -WhatIf vagy a -Confirm kapcsoló be van állítva.</span><span class="sxs-lookup"><span data-stu-id="f84ef-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="f84ef-183">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="f84ef-183">-WhatIfResultFormat</span></span>
<span data-ttu-id="f84ef-184">A What-If formátuma.</span><span class="sxs-lookup"><span data-stu-id="f84ef-184">The What-If result format.</span></span> <span data-ttu-id="f84ef-185">Akkor alkalmazható, ha a -WhatIf vagy a -Confirm kapcsoló be van állítva.</span><span class="sxs-lookup"><span data-stu-id="f84ef-185">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="f84ef-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f84ef-186">-Confirm</span></span>
<span data-ttu-id="f84ef-187">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f84ef-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f84ef-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f84ef-188">-WhatIf</span></span>
<span data-ttu-id="f84ef-189">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f84ef-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f84ef-190">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f84ef-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f84ef-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84ef-191">CommonParameters</span></span>
<span data-ttu-id="f84ef-192">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84ef-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84ef-193">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f84ef-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84ef-194">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f84ef-194">INPUTS</span></span>

### <span data-ttu-id="f84ef-195">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f84ef-195">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f84ef-196">System.String</span><span class="sxs-lookup"><span data-stu-id="f84ef-196">System.String</span></span>

## <span data-ttu-id="f84ef-197">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f84ef-197">OUTPUTS</span></span>

### <span data-ttu-id="f84ef-198">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f84ef-198">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f84ef-199">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f84ef-199">NOTES</span></span>

## <span data-ttu-id="f84ef-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f84ef-200">RELATED LINKS</span></span>
