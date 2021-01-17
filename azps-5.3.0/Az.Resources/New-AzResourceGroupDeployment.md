---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 916e2fea0e88a1409bc2586ab8b2e80b11ec1a70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466447"
---
# <span data-ttu-id="4c836-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c836-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4c836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c836-102">SYNOPSIS</span></span>
<span data-ttu-id="4c836-103">Hozzáad egy Azure-telepítést egy erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4c836-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="4c836-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4c836-104">SYNTAX</span></span>

### <span data-ttu-id="4c836-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c836-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4c836-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4c836-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4c836-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4c836-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4c836-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4c836-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4c836-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4c836-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4c836-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4c836-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c836-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4c836-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c836-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4c836-117">DESCRIPTION</span></span>
<span data-ttu-id="4c836-118">A **New-AzResourceGroupDeployment** parancsmag hozzáad egy telepítést egy meglévő erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4c836-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="4c836-119">Ide tartoznak a telepítéshez szükséges erőforrások is.</span><span class="sxs-lookup"><span data-stu-id="4c836-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="4c836-120">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis, webhely, virtuális gép vagy tárfiók.</span><span class="sxs-lookup"><span data-stu-id="4c836-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="4c836-121">Az Azure-erőforráscsoportok egy egységként üzembe helyezett Azure-erőforrások gyűjteményei, például a webhely, az adatbázis-kiszolgáló és a pénzügyi webhelyhez szükséges adatbázisok.</span><span class="sxs-lookup"><span data-stu-id="4c836-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="4c836-122">Az erőforráscsoportok telepítése sablon alapján adja hozzá az erőforrásokat egy erőforráscsoporthoz, és közzéteszi őket, hogy elérhetővé tegye őket az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="4c836-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="4c836-123">Ha sablon használata nélkül szeretne erőforrásokat hozzáadni egy erőforráscsoporthoz, használja a New-AzResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4c836-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="4c836-124">Erőforráscsoport-telepítés hozzáadásához adja meg egy meglévő erőforráscsoport nevét és egy erőforráscsoportsablont.</span><span class="sxs-lookup"><span data-stu-id="4c836-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="4c836-125">Az erőforráscsoport-sablon egy olyan JSON-karakterlánc, amely egy összetett felhőalapú szolgáltatás, például egy webportál erőforráscsoportját képviseli.</span><span class="sxs-lookup"><span data-stu-id="4c836-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="4c836-126">A sablon paraméterhelyőrzőket tartalmaz a kötelező erőforrásokhoz és a konfigurálható tulajdonságértékekhez, például a nevekhez és a méretekhez.</span><span class="sxs-lookup"><span data-stu-id="4c836-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="4c836-127">Az Azure sablongyűjteményében számos sablont talál, de saját sablonokat is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="4c836-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="4c836-128">Ha egyéni sablont használva hoz létre erőforráscsoportot, adja meg a *TemplateFile* vagy a *TemplateUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="4c836-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="4c836-129">Minden sablon rendelkezik paraméterekkel a konfigurálható tulajdonságokhoz.</span><span class="sxs-lookup"><span data-stu-id="4c836-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="4c836-130">A sablonparaméterek értékeinek megadásához adja meg a *TemplateParameterFile* vagy *a TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="4c836-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="4c836-131">Másik lehetőségként használhatja a sablon megadásakor a parancshoz dinamikusan hozzáadott sablonparamétereket is.</span><span class="sxs-lookup"><span data-stu-id="4c836-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="4c836-132">Ha dinamikus paramétereket használ, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) egy paraméter jelzésére, és a Tab billentyűvel lépked az elérhető paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="4c836-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="4c836-133">A parancssorba beírandó sablon paraméterértékei elsőbbséget élveznek a sablon paraméterobjektumában vagy -fájljában megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="4c836-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="4c836-134">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4c836-134">EXAMPLES</span></span>

### <span data-ttu-id="4c836-135">1. példa: Egyéni sablon és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="4c836-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="4c836-136">Ez a parancs létrehoz egy új telepítést egy egyéni sablon és egy sablonfájl használatával a lemezen, definiált címke paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="4c836-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="4c836-137">A parancs *a TemplateFile paraméterrel* adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="4c836-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="4c836-138">2. példa: Egyéni sablonobjektum és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="4c836-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="4c836-139">Ez a parancs új telepítést hoz létre egy egyéni és egy, a lemezen található sablonfájl használatával, amelyet a rendszer memórián lévő hashtable-ként konvertált.</span><span class="sxs-lookup"><span data-stu-id="4c836-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="4c836-140">Az első két parancs felolvassa a lemezen lévő sablonfájl szövegét, és átalakítja azt egy memóriában lévő hashtable-ként.</span><span class="sxs-lookup"><span data-stu-id="4c836-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="4c836-141">Az utolsó parancs *a TemplateObject* paraméter segítségével adja meg a hashtable és a *TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="4c836-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="4c836-142">3. példa</span><span class="sxs-lookup"><span data-stu-id="4c836-142">Example 3</span></span>

<span data-ttu-id="4c836-143">Hozzáad egy Azure-telepítést egy erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4c836-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="4c836-144">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="4c836-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="4c836-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c836-145">PARAMETERS</span></span>

### <span data-ttu-id="4c836-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c836-146">-AsJob</span></span>
<span data-ttu-id="4c836-147">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4c836-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c836-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c836-148">-DefaultProfile</span></span>
<span data-ttu-id="4c836-149">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4c836-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c836-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="4c836-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="4c836-151">Hibakeresési naplószintet ad meg.</span><span class="sxs-lookup"><span data-stu-id="4c836-151">Specifies a debug log level.</span></span>
<span data-ttu-id="4c836-152">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="4c836-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c836-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="4c836-153">RequestContent</span></span>
- <span data-ttu-id="4c836-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="4c836-154">ResponseContent</span></span>
- <span data-ttu-id="4c836-155">Mind</span><span class="sxs-lookup"><span data-stu-id="4c836-155">All</span></span>
- <span data-ttu-id="4c836-156">Nincs</span><span class="sxs-lookup"><span data-stu-id="4c836-156">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestContent, ResponseContent, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c836-157">-Force</span><span class="sxs-lookup"><span data-stu-id="4c836-157">-Force</span></span>
<span data-ttu-id="4c836-158">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4c836-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c836-159">-Mód</span><span class="sxs-lookup"><span data-stu-id="4c836-159">-Mode</span></span>
<span data-ttu-id="4c836-160">A telepítési módot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4c836-160">Specifies the deployment mode.</span></span> <span data-ttu-id="4c836-161">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="4c836-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c836-162">Kész: Teljes módban az Erőforrás-kezelő törli az erőforráscsoportban található, de a sablonban nem megadott erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="4c836-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="4c836-163">Növekményes: Növekményes módban az Erőforrás-kezelő változatlanul hagyja az erőforráscsoportban meglévő, de a sablonban nem megadott erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="4c836-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c836-164">-Name</span><span class="sxs-lookup"><span data-stu-id="4c836-164">-Name</span></span>
<span data-ttu-id="4c836-165">Annak a telepítésnek a neve, amelyből létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="4c836-165">The name of the deployment it's going to create.</span></span> <span data-ttu-id="4c836-166">Ha nincs megadva, alapértelmezés szerint a sablonfájl neve lesz megadva; sablonobjektumok (például "2013123140835") beállítása.</span><span class="sxs-lookup"><span data-stu-id="4c836-166">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c836-167">-Pre</span><span class="sxs-lookup"><span data-stu-id="4c836-167">-Pre</span></span>
<span data-ttu-id="4c836-168">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="4c836-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4c836-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c836-169">-ResourceGroupName</span></span>
<span data-ttu-id="4c836-170">A központi telepítéshez szükséges erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c836-170">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c836-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="4c836-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="4c836-172">Ha a -RollbackToLastDeployment nevet használja, ne használja az erőforráscsoportban megadott nevű sikeres telepítést.</span><span class="sxs-lookup"><span data-stu-id="4c836-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c836-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="4c836-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="4c836-174">A -RollBackDeploymentName használata esetén ne legyen jelen az erőforráscsoport utolsó sikeres telepítéséhez való visszatérés.</span><span class="sxs-lookup"><span data-stu-id="4c836-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="4c836-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4c836-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4c836-176">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="4c836-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="4c836-177">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="4c836-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="4c836-178">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="4c836-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4c836-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="4c836-179">-Tag</span></span>
<span data-ttu-id="4c836-180">Az üzembe helyezéshez szükséges címkék.</span><span class="sxs-lookup"><span data-stu-id="4c836-180">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="4c836-181">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4c836-181">-TemplateFile</span></span>
<span data-ttu-id="4c836-182">Egy JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c836-182">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="4c836-183">Ez lehet egyéni sablon vagy JSON-fájlként mentett gyűjteménysablon, például a **Save-AzResourceGroupGalleryTemplate** parancsmaggal létrehozott sablon.</span><span class="sxs-lookup"><span data-stu-id="4c836-183">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="4c836-184">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4c836-184">-TemplateObject</span></span>
<span data-ttu-id="4c836-185">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="4c836-185">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4c836-186">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4c836-186">-TemplateParameterFile</span></span>
<span data-ttu-id="4c836-187">A sablonparaméterek nevét és értékeit tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c836-187">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="4c836-188">Ha egy sablon paraméterekkel rendelkezik, a paraméterértékeket *a TemplateParameterFile* vagy a *TemplateParameterObject* paraméterrel kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="4c836-188">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="4c836-189">Sablon megadásakor a sablonparaméterek dinamikusan bekerülnek a parancsba.</span><span class="sxs-lookup"><span data-stu-id="4c836-189">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="4c836-190">A dinamikus paramétereket mínuszjellel (-) jelezheti a paraméter neveként, majd a Tab billentyűvel lépkedheti végig a rendelkezésre álló paramétereket.</span><span class="sxs-lookup"><span data-stu-id="4c836-190">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="4c836-191">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4c836-191">-TemplateParameterObject</span></span>
<span data-ttu-id="4c836-192">A sablon paraméterneveivel és értékeivel egy kivonattáblát ad meg.</span><span class="sxs-lookup"><span data-stu-id="4c836-192">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="4c836-193">Ha segítségre van szüksége a kivonattáblákhoz a Windows PowerShellben, írja be a `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="4c836-193">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="4c836-194">Ha egy sablon paraméterekkel rendelkezik, meg kell adnia a paraméterértékeket.</span><span class="sxs-lookup"><span data-stu-id="4c836-194">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="4c836-195">Sablon megadásakor a sablonparaméterek dinamikusan bekerülnek a parancsba.</span><span class="sxs-lookup"><span data-stu-id="4c836-195">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="4c836-196">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4c836-196">-TemplateParameterUri</span></span>
<span data-ttu-id="4c836-197">Egy sablonparaméter-fájl URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c836-197">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="4c836-198">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4c836-198">-TemplateUri</span></span>
<span data-ttu-id="4c836-199">Egy JSON-sablonfájl URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c836-199">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="4c836-200">Ez a fájl lehet egy egyéni sablon vagy egy gyűjteménysablon, amely JSON-fájlként van mentve, például a **Save-AzResourceGroupGalleryTemplate használatával.**</span><span class="sxs-lookup"><span data-stu-id="4c836-200">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="4c836-201">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="4c836-201">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="4c836-202">A vesszővel elválasztott erőforrás-módosítási típusokat nem lehet kizárni a What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="4c836-202">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="4c836-203">Akkor alkalmazható, ha a -WhatIf vagy a -Confirm kapcsoló be van állítva.</span><span class="sxs-lookup"><span data-stu-id="4c836-203">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="4c836-204">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="4c836-204">-WhatIfResultFormat</span></span>
<span data-ttu-id="4c836-205">A What-If formátuma.</span><span class="sxs-lookup"><span data-stu-id="4c836-205">The What-If result format.</span></span>

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

### <span data-ttu-id="4c836-206">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c836-206">-Confirm</span></span>
<span data-ttu-id="4c836-207">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4c836-207">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c836-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c836-208">-WhatIf</span></span>
<span data-ttu-id="4c836-209">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4c836-209">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c836-210">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c836-210">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c836-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c836-211">CommonParameters</span></span>
<span data-ttu-id="4c836-212">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c836-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c836-213">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c836-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c836-214">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c836-214">INPUTS</span></span>

### <span data-ttu-id="4c836-215">System.String</span><span class="sxs-lookup"><span data-stu-id="4c836-215">System.String</span></span>

### <span data-ttu-id="4c836-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="4c836-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="4c836-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4c836-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4c836-218">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c836-218">OUTPUTS</span></span>

### <span data-ttu-id="4c836-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c836-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="4c836-220">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4c836-220">NOTES</span></span>

## <span data-ttu-id="4c836-221">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c836-221">RELATED LINKS</span></span>

[<span data-ttu-id="4c836-222">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c836-222">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4c836-223">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="4c836-223">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="4c836-224">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4c836-224">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="4c836-225">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c836-225">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="4c836-226">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c836-226">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="4c836-227">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c836-227">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)