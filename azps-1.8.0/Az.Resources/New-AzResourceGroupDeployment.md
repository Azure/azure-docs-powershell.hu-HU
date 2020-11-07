---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 067faa4688f079d24f2fc79a4771c84f6c02d0c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669376"
---
# <span data-ttu-id="038ed-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="038ed-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="038ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="038ed-102">SYNOPSIS</span></span>
<span data-ttu-id="038ed-103">Azure-bevezetést ad hozzá egy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="038ed-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="038ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="038ed-104">SYNTAX</span></span>

### <span data-ttu-id="038ed-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="038ed-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="038ed-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="038ed-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="038ed-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="038ed-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="038ed-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="038ed-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="038ed-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="038ed-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="038ed-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="038ed-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="038ed-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="038ed-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="038ed-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="038ed-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="038ed-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="038ed-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="038ed-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="038ed-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="038ed-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="038ed-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="038ed-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="038ed-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="038ed-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="038ed-117">DESCRIPTION</span></span>
<span data-ttu-id="038ed-118">A **New-AzResourceGroupDeployment** parancsmag egy meglévő erőforráscsoport bevezetését adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="038ed-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="038ed-119">Ez a beállítás tartalmazza a telepítéshez szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="038ed-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="038ed-120">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis, webhely, virtuális gép vagy tárolási fiók.</span><span class="sxs-lookup"><span data-stu-id="038ed-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="038ed-121">Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként vannak telepítve, például a webhelyen, az adatbázis-kiszolgálón és a pénzügyi webhelyhez szükséges adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="038ed-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="038ed-122">Az erőforráscsoport-telepítés sablon használatával erőforrásokat ad hozzá egy erőforráscsoport számára, és közzéteszi őket, hogy azok elérhetők legyenek az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="038ed-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="038ed-123">Ha nem sablon nélkül szeretne erőforrásokat hozzáadni az erőforrás csoporthoz, használja az New-AzResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="038ed-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="038ed-124">Erőforráscsoport-telepítő hozzáadásához adja meg egy meglévő erőforráscsoport és egy erőforráscsoport-sablon nevét.</span><span class="sxs-lookup"><span data-stu-id="038ed-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="038ed-125">Egy erőforráscsoport-sablon egy olyan JSON karakterlánc, amely egy komplex felhőalapú szolgáltatás erőforráscsoport, például egy webportál.</span><span class="sxs-lookup"><span data-stu-id="038ed-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="038ed-126">A sablon tartalmazza a paraméterek helyőrzőit a szükséges erőforrások és a konfigurálható tulajdonságértékek (például nevek és méretek) esetében.</span><span class="sxs-lookup"><span data-stu-id="038ed-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="038ed-127">Az Azure template gyűjteményben számos sablon található, vagy saját sablonokat is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="038ed-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="038ed-128">Sablon kereséséhez használhatja a **Get-AzResourceGroupGalleryTemplate** parancsmagot a gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="038ed-128">You can use the **Get-AzResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="038ed-129">Ha egyéni sablont szeretne használni egy erőforráscsoport létrehozásához, adja meg a *TemplateFile* paramétert vagy a *TemplateUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="038ed-129">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="038ed-130">Mindegyik sablon rendelkezik a konfigurálható tulajdonságokra vonatkozó paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="038ed-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="038ed-131">A sablon paramétereinek értékeinek megadásához adja meg a *TemplateParameterFile* paramétert vagy a *TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="038ed-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="038ed-132">Azt is megteheti, hogy egy sablon megadásakor dinamikusan hozzáadja a parancsot a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="038ed-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="038ed-133">Ha dinamikus paramétereket szeretne használni, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) a paraméter jelzéséhez, és a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="038ed-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="038ed-134">A parancssorba beírt sablon paraméterei felülbírálják a Template paraméteres objektum vagy fájl értékeit.</span><span class="sxs-lookup"><span data-stu-id="038ed-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="038ed-135">Példák</span><span class="sxs-lookup"><span data-stu-id="038ed-135">EXAMPLES</span></span>

### <span data-ttu-id="038ed-136">1. példa: egyéni sablon és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="038ed-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="038ed-137">A parancs létrehoz egy új üzembe állítást egy egyéni sablon és egy sablonfájl segítségével a lemezen.</span><span class="sxs-lookup"><span data-stu-id="038ed-137">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="038ed-138">A parancs a *TemplateFile* paramétert használva adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="038ed-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="038ed-139">2. példa: egyéni sablon objektum és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="038ed-139">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="038ed-140">Ez a parancs egy új üzembe állítást hoz létre egy olyan egyéni és egy sablonfájl segítségével, amelyet a memóriában lévő Hashtable alakítottak.</span><span class="sxs-lookup"><span data-stu-id="038ed-140">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="038ed-141">Az első két parancs elolvassa a sablonfájl szövegét a lemezen, és a memória-Hashtable alakítja.</span><span class="sxs-lookup"><span data-stu-id="038ed-141">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="038ed-142">Az utolsó parancs a *TemplateObject* paramétert használva adja meg a Hashtable és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="038ed-142">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="038ed-143">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="038ed-143">PARAMETERS</span></span>

### <span data-ttu-id="038ed-144">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="038ed-144">-ApiVersion</span></span>
<span data-ttu-id="038ed-145">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="038ed-145">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="038ed-146">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="038ed-146">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="038ed-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="038ed-147">-AsJob</span></span>
<span data-ttu-id="038ed-148">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="038ed-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="038ed-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="038ed-149">-DefaultProfile</span></span>
<span data-ttu-id="038ed-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="038ed-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="038ed-151">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="038ed-151">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="038ed-152">A Debug naplózási szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="038ed-152">Specifies a debug log level.</span></span>
<span data-ttu-id="038ed-153">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="038ed-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="038ed-154">RequestContent</span><span class="sxs-lookup"><span data-stu-id="038ed-154">RequestContent</span></span>
- <span data-ttu-id="038ed-155">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="038ed-155">ResponseContent</span></span>
- <span data-ttu-id="038ed-156">Minden</span><span class="sxs-lookup"><span data-stu-id="038ed-156">All</span></span>
- <span data-ttu-id="038ed-157">Nincs</span><span class="sxs-lookup"><span data-stu-id="038ed-157">None</span></span>

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

### <span data-ttu-id="038ed-158">-Force</span><span class="sxs-lookup"><span data-stu-id="038ed-158">-Force</span></span>
<span data-ttu-id="038ed-159">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="038ed-159">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="038ed-160">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="038ed-160">-Mode</span></span>
<span data-ttu-id="038ed-161">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="038ed-161">Specifies the deployment mode.</span></span> <span data-ttu-id="038ed-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="038ed-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="038ed-163">Kész: az erőforrás-kezelő az erőforrás csoportban található erőforrásokat törli, a sablonban azonban nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="038ed-163">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="038ed-164">Növekményes: az erőforrás-kezelő nem módosított erőforrásokat hagy elő az erőforrás csoportban, a sablonban azonban nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="038ed-164">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="038ed-165">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="038ed-165">-Name</span></span>
<span data-ttu-id="038ed-166">A létrehozandó erőforráscsoport-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="038ed-166">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="038ed-167">-Pre</span><span class="sxs-lookup"><span data-stu-id="038ed-167">-Pre</span></span>
<span data-ttu-id="038ed-168">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="038ed-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="038ed-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="038ed-169">-ResourceGroupName</span></span>
<span data-ttu-id="038ed-170">A telepítendő erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="038ed-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="038ed-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="038ed-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="038ed-172">Ha az erőforrás csoportban az adott nevű névvel a sikeres telepítésre szeretne visszagörgetni, akkor ne használja a ha-RollbackToLastDeployment használatát.</span><span class="sxs-lookup"><span data-stu-id="038ed-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="038ed-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="038ed-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="038ed-174">Az erőforrás csoport utolsó sikeres telepítésére való visszagörgetéskor ne legyen megjelenni, ha-RollBackDeploymentName használja.</span><span class="sxs-lookup"><span data-stu-id="038ed-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="038ed-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="038ed-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="038ed-176">A PowerShell dinamikus paraméter-feldolgozási folyamatának átugrása, amely ellenőrzi, hogy a megadott sablon paraméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="038ed-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="038ed-177">Ez az ellenőrzés arra kéri a felhasználót, hogy adjon meg egy értéket a hiányzó paramétereknek, de a-SkipTemplateParameterPrompt kihagyása után a rendszer azonnal kihagyja ezt a figyelmeztetést, ha egy paraméter nem kötődik a sablonhoz.</span><span class="sxs-lookup"><span data-stu-id="038ed-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="038ed-178">A nem interaktív parancsfájlok esetében a-SkipTemplateParameterPrompt megadható, hogy jobb hibaüzenetet kapjanak abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="038ed-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="038ed-179">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="038ed-179">-TemplateFile</span></span>
<span data-ttu-id="038ed-180">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="038ed-180">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="038ed-181">Ez lehet egy egyéni sablon vagy egy olyan sablon, amelyet JSON-fájlként mentenek, például a **Save-AzResourceGroupGalleryTemplate** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="038ed-181">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="038ed-182">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="038ed-182">-TemplateObject</span></span>
<span data-ttu-id="038ed-183">A sablont jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="038ed-183">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="038ed-184">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="038ed-184">-TemplateParameterFile</span></span>
<span data-ttu-id="038ed-185">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="038ed-185">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="038ed-186">Ha egy sablon tartalmaz paramétereket, akkor a *TemplateParameterFile* paraméterrel vagy a *TemplateParameterObject* paraméterrel kell megadnia a paraméterek értékét.</span><span class="sxs-lookup"><span data-stu-id="038ed-186">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="038ed-187">Sablon megadásakor a program dinamikusan hozzáadja a sablon paramétereit a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="038ed-187">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="038ed-188">A dinamikus paraméterek használatához írjon be egy mínuszjelet (-) a paraméter nevének jelzéséhez, majd a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="038ed-188">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="038ed-189">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="038ed-189">-TemplateParameterObject</span></span>
<span data-ttu-id="038ed-190">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="038ed-190">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="038ed-191">Ha segítségre van szüksége a kivonatoló táblázatokhoz a Windows PowerShellben, írja be a következőt `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="038ed-191">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="038ed-192">Ha egy sablonnak vannak paraméterei, meg kell adnia a paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="038ed-192">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="038ed-193">Sablon megadásakor a program dinamikusan hozzáadja a sablon paramétereit a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="038ed-193">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="038ed-194">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="038ed-194">-TemplateParameterUri</span></span>
<span data-ttu-id="038ed-195">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="038ed-195">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="038ed-196">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="038ed-196">-TemplateUri</span></span>
<span data-ttu-id="038ed-197">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="038ed-197">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="038ed-198">Ez a fájl lehet egy egyéni sablon vagy egy JSON-fájlként mentett gyűjtemény-sablon, például a **Save-AzResourceGroupGalleryTemplate** használatával.</span><span class="sxs-lookup"><span data-stu-id="038ed-198">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="038ed-199">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="038ed-199">-Confirm</span></span>
<span data-ttu-id="038ed-200">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="038ed-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="038ed-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="038ed-201">-WhatIf</span></span>
<span data-ttu-id="038ed-202">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="038ed-202">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="038ed-203">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="038ed-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="038ed-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038ed-204">CommonParameters</span></span>
<span data-ttu-id="038ed-205">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="038ed-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038ed-206">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="038ed-206">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038ed-207">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="038ed-207">INPUTS</span></span>

### <span data-ttu-id="038ed-208">System. String</span><span class="sxs-lookup"><span data-stu-id="038ed-208">System.String</span></span>

### <span data-ttu-id="038ed-209">Microsoft. Azure. Management. ResourceManager. models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="038ed-209">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="038ed-210">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="038ed-210">System.Collections.Hashtable</span></span>

## <span data-ttu-id="038ed-211">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="038ed-211">OUTPUTS</span></span>

### <span data-ttu-id="038ed-212">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="038ed-212">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="038ed-213">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="038ed-213">NOTES</span></span>

## <span data-ttu-id="038ed-214">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="038ed-214">RELATED LINKS</span></span>

[<span data-ttu-id="038ed-215">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="038ed-215">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="038ed-216">Új – AzResource</span><span class="sxs-lookup"><span data-stu-id="038ed-216">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="038ed-217">Új – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="038ed-217">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="038ed-218">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="038ed-218">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="038ed-219">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="038ed-219">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="038ed-220">Teszt-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="038ed-220">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


