---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: d3b9fce538512fdb55328d6c2e846c955bcfbb5d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153658"
---
# <span data-ttu-id="58f60-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="58f60-101">New-AzDeployment</span></span>

## <span data-ttu-id="58f60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58f60-102">SYNOPSIS</span></span>
<span data-ttu-id="58f60-103">Telepítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="58f60-103">Create a deployment</span></span>

## <span data-ttu-id="58f60-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58f60-104">SYNTAX</span></span>

### <span data-ttu-id="58f60-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="58f60-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="58f60-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="58f60-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="58f60-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="58f60-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="58f60-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="58f60-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="58f60-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="58f60-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="58f60-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="58f60-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="58f60-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="58f60-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="58f60-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f60-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="58f60-119">ByTemplateSpecResourceId</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58f60-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58f60-120">DESCRIPTION</span></span>
<span data-ttu-id="58f60-121">A **New-AzDeployment** parancsmag hozzáad egy telepítést az aktuális előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="58f60-121">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="58f60-122">Ide tartoznak a telepítéshez szükséges erőforrások is.</span><span class="sxs-lookup"><span data-stu-id="58f60-122">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="58f60-123">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás.</span><span class="sxs-lookup"><span data-stu-id="58f60-123">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="58f60-124">Az erőforrások egy erőforráscsoportban, például adatbázis-kiszolgálón, adatbázisban, webhelyen, virtuális gépen vagy tárfiókban is megélnek.</span><span class="sxs-lookup"><span data-stu-id="58f60-124">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="58f60-125">Az is lehet előfizetési szintű erőforrás, például szerepkör-definíció, házirend-definíció stb.</span><span class="sxs-lookup"><span data-stu-id="58f60-125">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="58f60-126">Ha erőforrásokat szeretne hozzáadni egy erőforráscsoporthoz, használja a **New-AzResourceGroupDeployment** bővítményt, amely létrehoz egy telepítést egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="58f60-126">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="58f60-127">A **New-AzDeployment** parancsmag létrehoz egy telepítést az aktuális előfizetési hatókörben, amely az előfizetési szintű erőforrásokat telepíti.</span><span class="sxs-lookup"><span data-stu-id="58f60-127">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="58f60-128">Ha egy központi telepítést szeretne hozzáadni az előfizetéshez, adja meg a helyet és egy sablont.</span><span class="sxs-lookup"><span data-stu-id="58f60-128">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="58f60-129">A hely közli az Azure Resource Managerrel, hogy hol kell tárolni a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="58f60-129">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="58f60-130">A sablon egy JSON-karakterlánc, amely az egyes telepítend kívánt erőforrásokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="58f60-130">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="58f60-131">A sablon paraméterhelyőrzőket tartalmaz a kötelező erőforrásokhoz és a konfigurálható tulajdonságértékekhez, például a nevekhez és a méretekhez.</span><span class="sxs-lookup"><span data-stu-id="58f60-131">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="58f60-132">Ha egyéni sablont használ a telepítéshez, adja meg a *TemplateFile* vagy *a TemplateUri paramétert.*</span><span class="sxs-lookup"><span data-stu-id="58f60-132">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="58f60-133">Minden sablon rendelkezik paraméterekkel a konfigurálható tulajdonságokhoz.</span><span class="sxs-lookup"><span data-stu-id="58f60-133">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="58f60-134">A sablonparaméterek értékeinek megadásához adja meg a *TemplateParameterFile* vagy *a TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="58f60-134">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="58f60-135">Másik lehetőségként használhatja a sablon megadásakor a parancshoz dinamikusan hozzáadott sablonparamétereket is.</span><span class="sxs-lookup"><span data-stu-id="58f60-135">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="58f60-136">Ha dinamikus paramétereket használ, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) egy paraméter jelzésére, és a Tab billentyűvel lépked az elérhető paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="58f60-136">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="58f60-137">A parancssorba beírandó sablon paraméterértékei elsőbbséget élveznek a sablon paraméterobjektumában vagy -fájljában megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="58f60-137">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="58f60-138">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58f60-138">EXAMPLES</span></span>

### <span data-ttu-id="58f60-139">1. példa: Egyéni sablon és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="58f60-139">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="58f60-140">Ez a parancs új telepítést hoz létre az aktuális előfizetési hatókörben egy egyéni sablon és egy lemezen lévő sablonfájl használatával, meghatározott címke paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="58f60-140">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="58f60-141">A parancs *a TemplateFile paraméter* segítségével adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="58f60-141">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="58f60-142">A *sablon verzióját a TemplateVersion* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="58f60-142">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="58f60-143">2. példa: Nem nyilvános tárfiókban tárolt sablon üzembe helyezése uri és SAS-jogkivonat használatával</span><span class="sxs-lookup"><span data-stu-id="58f60-143">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="58f60-144">Ez a parancs új telepítést hoz létre a TemplateUri sablonnal, amely nem nyilvános, és a QueryString paraméter használatával biztosítandó token paramétert igényel.</span><span class="sxs-lookup"><span data-stu-id="58f60-144">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="58f60-145">A parancs futtatása hatékonyan hozzáfér a sablonhoz az URL-cím https://example.com/example.json?foo használatával.</span><span class="sxs-lookup"><span data-stu-id="58f60-145">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="58f60-146">Ez akkor használható, ha egy tárolófiókban sablont szeretne használni az SAS-jogkivonat lekérdezési karakterláncként való biztosításával.</span><span class="sxs-lookup"><span data-stu-id="58f60-146">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="58f60-147">3. példa: Egyéni sablonobjektum és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="58f60-147">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="58f60-148">Ez a parancs új telepítést hoz létre az aktuális előfizetési hatókörben egy egyéni sablon és egy, a lemezen lévő sablonfájl használatával, amelyet a rendszer memórián belülre konvertált hashtable-ként.</span><span class="sxs-lookup"><span data-stu-id="58f60-148">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="58f60-149">Az első két parancs felolvassa a lemezen lévő sablonfájl szövegét, és átalakítja azt egy memóriában lévő hashtable-ként.</span><span class="sxs-lookup"><span data-stu-id="58f60-149">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="58f60-150">Az utolsó parancs *a TemplateObject* paraméter segítségével adja meg ezt a hashtable és *a TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="58f60-150">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="58f60-151">A *sablon verzióját a TemplateVersion* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="58f60-151">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="58f60-152">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58f60-152">PARAMETERS</span></span>

### <span data-ttu-id="58f60-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58f60-153">-AsJob</span></span>
<span data-ttu-id="58f60-154">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="58f60-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58f60-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f60-155">-DefaultProfile</span></span>
<span data-ttu-id="58f60-156">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58f60-156">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58f60-157">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="58f60-157">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="58f60-158">A központi telepítés hibakeresési naplószintje.</span><span class="sxs-lookup"><span data-stu-id="58f60-158">The deployment debug log level.</span></span>

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

### <span data-ttu-id="58f60-159">-Location</span><span class="sxs-lookup"><span data-stu-id="58f60-159">-Location</span></span>
<span data-ttu-id="58f60-160">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="58f60-160">The location to store deployment data.</span></span>

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

### <span data-ttu-id="58f60-161">-Name</span><span class="sxs-lookup"><span data-stu-id="58f60-161">-Name</span></span>
<span data-ttu-id="58f60-162">Annak a telepítésnek a neve, amelyből létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="58f60-162">The name of the deployment it's going to create.</span></span> <span data-ttu-id="58f60-163">Ha nincs megadva, alapértelmezés szerint a sablonfájl neve lesz megadva; sablonobjektumok (például "2013123140835") beállítása.</span><span class="sxs-lookup"><span data-stu-id="58f60-163">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="58f60-164">-Pre</span><span class="sxs-lookup"><span data-stu-id="58f60-164">-Pre</span></span>
<span data-ttu-id="58f60-165">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="58f60-165">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="58f60-166">-QueryString</span><span class="sxs-lookup"><span data-stu-id="58f60-166">-QueryString</span></span>
<span data-ttu-id="58f60-167">A TemplateUri paraméterrel használt lekérdezési karakterlánc (például EGY SAS-jogkivonat).</span><span class="sxs-lookup"><span data-stu-id="58f60-167">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="58f60-168">Hivatkozott sablonok esetén használható</span><span class="sxs-lookup"><span data-stu-id="58f60-168">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="58f60-169">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="58f60-169">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="58f60-170">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="58f60-170">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="58f60-171">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="58f60-171">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="58f60-172">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="58f60-172">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="58f60-173">-Tag</span><span class="sxs-lookup"><span data-stu-id="58f60-173">-Tag</span></span>
<span data-ttu-id="58f60-174">Az üzembe helyezéshez szükséges címkék.</span><span class="sxs-lookup"><span data-stu-id="58f60-174">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="58f60-175">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="58f60-175">-TemplateFile</span></span>
<span data-ttu-id="58f60-176">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="58f60-176">Local path to the template file.</span></span>

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

### <span data-ttu-id="58f60-177">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="58f60-177">-TemplateObject</span></span>
<span data-ttu-id="58f60-178">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="58f60-178">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="58f60-179">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="58f60-179">-TemplateParameterFile</span></span>
<span data-ttu-id="58f60-180">Olyan fájl, amely a sablon paramétereit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="58f60-180">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="58f60-181">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="58f60-181">-TemplateParameterObject</span></span>
<span data-ttu-id="58f60-182">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="58f60-182">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="58f60-183">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="58f60-183">-TemplateParameterUri</span></span>
<span data-ttu-id="58f60-184">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="58f60-184">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="58f60-185">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="58f60-185">-TemplateSpecId</span></span>
<span data-ttu-id="58f60-186">A telepíteni kívánt sablonSpec erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="58f60-186">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="58f60-187">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="58f60-187">-TemplateUri</span></span>
<span data-ttu-id="58f60-188">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="58f60-188">Uri to the template file.</span></span>

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

### <span data-ttu-id="58f60-189">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="58f60-189">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="58f60-190">Vesszővel elválasztott erőforrás-módosítási típusok, amelyek nem lesznek kizárva a What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="58f60-190">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="58f60-191">Akkor érvényes, ha a -WhatIf vagy a -Confirm kapcsoló be van állítva.</span><span class="sxs-lookup"><span data-stu-id="58f60-191">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="58f60-192">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="58f60-192">-WhatIfResultFormat</span></span>
<span data-ttu-id="58f60-193">A What-If formátuma.</span><span class="sxs-lookup"><span data-stu-id="58f60-193">The What-If result format.</span></span>

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

### <span data-ttu-id="58f60-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58f60-194">-Confirm</span></span>
<span data-ttu-id="58f60-195">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="58f60-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58f60-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58f60-196">-WhatIf</span></span>
<span data-ttu-id="58f60-197">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="58f60-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58f60-198">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58f60-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58f60-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f60-199">CommonParameters</span></span>
<span data-ttu-id="58f60-200">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f60-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f60-201">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58f60-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f60-202">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58f60-202">INPUTS</span></span>

### <span data-ttu-id="58f60-203">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="58f60-203">System.Collections.Hashtable</span></span>

### <span data-ttu-id="58f60-204">System.String</span><span class="sxs-lookup"><span data-stu-id="58f60-204">System.String</span></span>

## <span data-ttu-id="58f60-205">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58f60-205">OUTPUTS</span></span>

### <span data-ttu-id="58f60-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="58f60-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="58f60-207">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58f60-207">NOTES</span></span>

## <span data-ttu-id="58f60-208">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58f60-208">RELATED LINKS</span></span>
