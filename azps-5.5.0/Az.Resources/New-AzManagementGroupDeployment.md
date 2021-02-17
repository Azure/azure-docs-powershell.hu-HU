---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: 95aa46354fb0ea1f2a1883fe7d319acfda220526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208470"
---
# <span data-ttu-id="405c8-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="405c8-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="405c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="405c8-102">SYNOPSIS</span></span>
<span data-ttu-id="405c8-103">Központi telepítés létrehozása egy felügyeleti csoportban</span><span class="sxs-lookup"><span data-stu-id="405c8-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="405c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="405c8-104">SYNTAX</span></span>

### <span data-ttu-id="405c8-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="405c8-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="405c8-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="405c8-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="405c8-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="405c8-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="405c8-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="405c8-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="405c8-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="405c8-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="405c8-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="405c8-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="405c8-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="405c8-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="405c8-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="405c8-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="405c8-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="405c8-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="405c8-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="405c8-119">ByTemplateSpecResourceId</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="405c8-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="405c8-120">DESCRIPTION</span></span>
<span data-ttu-id="405c8-121">A **New-AzManagementGroupDeployment** parancsmag hozzáad egy telepítést egy felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="405c8-121">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="405c8-122">Ha egy felügyeleti csoportban szeretne központi telepítést hozzáadni, adja meg a felügyeleti csoportot, a helyet és egy sablont.</span><span class="sxs-lookup"><span data-stu-id="405c8-122">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="405c8-123">A hely közli az Azure Resource Managerrel, hogy hol kell tárolni a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="405c8-123">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="405c8-124">A sablon egy JSON-karakterlánc, amely az egyes telepítend kívánt erőforrásokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="405c8-124">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="405c8-125">A sablon paraméterhelyőrzőket tartalmaz a kötelező erőforrásokhoz és a konfigurálható tulajdonságértékekhez, például a nevekhez és a méretekhez.</span><span class="sxs-lookup"><span data-stu-id="405c8-125">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="405c8-126">Ha egyéni sablont használ a telepítéshez, adja meg a *TemplateFile* vagy *a TemplateUri paramétert.*</span><span class="sxs-lookup"><span data-stu-id="405c8-126">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="405c8-127">Minden sablon rendelkezik paraméterekkel a konfigurálható tulajdonságokhoz.</span><span class="sxs-lookup"><span data-stu-id="405c8-127">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="405c8-128">A sablonparaméterek értékeinek megadásához adja meg a *TemplateParameterFile* vagy *a TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="405c8-128">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="405c8-129">Másik lehetőségként használhatja a sablon megadásakor a parancshoz dinamikusan hozzáadott sablonparamétereket is.</span><span class="sxs-lookup"><span data-stu-id="405c8-129">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="405c8-130">Ha dinamikus paramétereket használ, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) egy paraméter jelzésére, és a Tab billentyűvel lépked az elérhető paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="405c8-130">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="405c8-131">A parancssorba beírandó sablon paraméterértékei elsőbbséget élveznek a sablon paraméterobjektumában vagy -fájljában megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="405c8-131">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="405c8-132">Ha erőforrásokat szeretne hozzáadni egy erőforráscsoporthoz, használja a **New-AzResourceGroupDeployment** bővítményt, amely létrehoz egy telepítést egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="405c8-132">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="405c8-133">Ha erőforrásokat szeretne hozzáadni egy előfizetéshez, használja a **New-AzSubscriptionDeployment** bővítményt, amely létrehoz egy telepítést az előfizetési hatókörben, amely az előfizetési szintű erőforrásokat telepíti.</span><span class="sxs-lookup"><span data-stu-id="405c8-133">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="405c8-134">Erőforrások bérlői hatókörben való hozzáadásához használja a **New-AzTenantDeployment** bővítményt, amely létrehoz egy telepítést a bérlői webhelyen.</span><span class="sxs-lookup"><span data-stu-id="405c8-134">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="405c8-135">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="405c8-135">EXAMPLES</span></span>

### <span data-ttu-id="405c8-136">1. példa: Egyéni sablon és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="405c8-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="405c8-137">Ez a parancs létrehoz egy új telepítést a "myMG" felügyeleti csoportban egy egyéni sablon és egy sablonfájl használatával a lemezen, definiált címke paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="405c8-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="405c8-138">A parancs *a TemplateFile paraméterrel* adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="405c8-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="405c8-139">2. példa: Nem nyilvános tárfiókban tárolt sablon üzembe helyezése uri és SAS-jogkivonat használatával</span><span class="sxs-lookup"><span data-stu-id="405c8-139">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="405c8-140">Ez a parancs új telepítést hoz létre a TemplateUri sablonnal, amely nem nyilvános, és a QueryString paraméter használatával biztosítandó token paramétert igényel.</span><span class="sxs-lookup"><span data-stu-id="405c8-140">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="405c8-141">A parancs futtatása hatékonyan hozzáfér a sablonhoz az URL-cím https://example.com/example.json?foo használatával.</span><span class="sxs-lookup"><span data-stu-id="405c8-141">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="405c8-142">Ez akkor használható, ha egy tárolófiókban sablont szeretne használni az SAS-jogkivonat lekérdezési karakterláncként való biztosításával.</span><span class="sxs-lookup"><span data-stu-id="405c8-142">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="405c8-143">3. példa: Egyéni sablonobjektum és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="405c8-143">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="405c8-144">Ez a parancs létrehoz egy új telepítést a "myMG" felügyeleti csoportban egy egyéni sablon és egy, a lemezen található sablonfájl használatával, amelyet a rendszer memórián belülre konvertált hashtable-ként.</span><span class="sxs-lookup"><span data-stu-id="405c8-144">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="405c8-145">Az első két parancs felolvassa a lemezen lévő sablonfájl szövegét, és átalakítja azt egy memóriában lévő hashtable-ként.</span><span class="sxs-lookup"><span data-stu-id="405c8-145">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="405c8-146">Az utolsó parancs *a TemplateObject* paraméter segítségével adja meg ezt a hashtable és *a TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="405c8-146">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="405c8-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="405c8-147">PARAMETERS</span></span>

### <span data-ttu-id="405c8-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="405c8-148">-AsJob</span></span>
<span data-ttu-id="405c8-149">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="405c8-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="405c8-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="405c8-150">-DefaultProfile</span></span>
<span data-ttu-id="405c8-151">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="405c8-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="405c8-152">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="405c8-152">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="405c8-153">A központi telepítés hibakeresési naplószintje.</span><span class="sxs-lookup"><span data-stu-id="405c8-153">The deployment debug log level.</span></span>

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

### <span data-ttu-id="405c8-154">-Location</span><span class="sxs-lookup"><span data-stu-id="405c8-154">-Location</span></span>
<span data-ttu-id="405c8-155">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="405c8-155">The location to store deployment data.</span></span>

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

### <span data-ttu-id="405c8-156">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="405c8-156">-ManagementGroupId</span></span>
<span data-ttu-id="405c8-157">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="405c8-157">The management group ID.</span></span>

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

### <span data-ttu-id="405c8-158">-Name</span><span class="sxs-lookup"><span data-stu-id="405c8-158">-Name</span></span>
<span data-ttu-id="405c8-159">Annak a telepítésnek a neve, amelyből létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="405c8-159">The name of the deployment it's going to create.</span></span> <span data-ttu-id="405c8-160">Ha nincs megadva, alapértelmezés szerint a sablonfájl neve lesz megadva; sablonobjektumok (például "2013123140835") beállítása.</span><span class="sxs-lookup"><span data-stu-id="405c8-160">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="405c8-161">-Pre</span><span class="sxs-lookup"><span data-stu-id="405c8-161">-Pre</span></span>
<span data-ttu-id="405c8-162">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="405c8-162">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="405c8-163">-QueryString</span><span class="sxs-lookup"><span data-stu-id="405c8-163">-QueryString</span></span>
<span data-ttu-id="405c8-164">A TemplateUri paraméterrel használt lekérdezési karakterlánc (például EGY SAS-jogkivonat).</span><span class="sxs-lookup"><span data-stu-id="405c8-164">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="405c8-165">Hivatkozott sablonok esetén használható</span><span class="sxs-lookup"><span data-stu-id="405c8-165">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="405c8-166">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="405c8-166">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="405c8-167">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="405c8-167">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="405c8-168">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="405c8-168">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="405c8-169">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="405c8-169">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="405c8-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="405c8-170">-Tag</span></span>
<span data-ttu-id="405c8-171">Az üzembe helyezéshez szükséges címkék.</span><span class="sxs-lookup"><span data-stu-id="405c8-171">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="405c8-172">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="405c8-172">-TemplateFile</span></span>
<span data-ttu-id="405c8-173">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="405c8-173">Local path to the template file.</span></span>

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

### <span data-ttu-id="405c8-174">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="405c8-174">-TemplateObject</span></span>
<span data-ttu-id="405c8-175">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="405c8-175">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="405c8-176">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="405c8-176">-TemplateParameterFile</span></span>
<span data-ttu-id="405c8-177">Olyan fájl, amely rendelkezik a sablonparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="405c8-177">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="405c8-178">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="405c8-178">-TemplateParameterObject</span></span>
<span data-ttu-id="405c8-179">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="405c8-179">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="405c8-180">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="405c8-180">-TemplateParameterUri</span></span>
<span data-ttu-id="405c8-181">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="405c8-181">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="405c8-182">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="405c8-182">-TemplateSpecId</span></span>
<span data-ttu-id="405c8-183">A telepíteni kívánt sablonSpec erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="405c8-183">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="405c8-184">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="405c8-184">-TemplateUri</span></span>
<span data-ttu-id="405c8-185">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="405c8-185">Uri to the template file.</span></span>

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

### <span data-ttu-id="405c8-186">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="405c8-186">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="405c8-187">A vesszővel elválasztott erőforrás-módosítási típusokat nem lehet kizárni a What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="405c8-187">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="405c8-188">Akkor alkalmazható, ha a -WhatIf vagy a -Confirm kapcsoló be van állítva.</span><span class="sxs-lookup"><span data-stu-id="405c8-188">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="405c8-189">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="405c8-189">-WhatIfResultFormat</span></span>
<span data-ttu-id="405c8-190">A What-If formátuma.</span><span class="sxs-lookup"><span data-stu-id="405c8-190">The What-If result format.</span></span> <span data-ttu-id="405c8-191">Akkor érvényes, ha a -WhatIf vagy a -Confirm kapcsoló be van állítva.</span><span class="sxs-lookup"><span data-stu-id="405c8-191">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="405c8-192">-Confirm</span><span class="sxs-lookup"><span data-stu-id="405c8-192">-Confirm</span></span>
<span data-ttu-id="405c8-193">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="405c8-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="405c8-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="405c8-194">-WhatIf</span></span>
<span data-ttu-id="405c8-195">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="405c8-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="405c8-196">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="405c8-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="405c8-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="405c8-197">CommonParameters</span></span>
<span data-ttu-id="405c8-198">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="405c8-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="405c8-199">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="405c8-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="405c8-200">INPUTS</span><span class="sxs-lookup"><span data-stu-id="405c8-200">INPUTS</span></span>

### <span data-ttu-id="405c8-201">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="405c8-201">System.Collections.Hashtable</span></span>

### <span data-ttu-id="405c8-202">System.String</span><span class="sxs-lookup"><span data-stu-id="405c8-202">System.String</span></span>

## <span data-ttu-id="405c8-203">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="405c8-203">OUTPUTS</span></span>

### <span data-ttu-id="405c8-204">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="405c8-204">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="405c8-205">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="405c8-205">NOTES</span></span>

## <span data-ttu-id="405c8-206">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="405c8-206">RELATED LINKS</span></span>
