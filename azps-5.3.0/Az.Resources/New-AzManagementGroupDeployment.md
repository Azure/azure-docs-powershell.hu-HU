---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: a04c19df84626fd08968e1950074306dfd7cf1ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466460"
---
# <span data-ttu-id="2e841-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2e841-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="2e841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e841-102">SYNOPSIS</span></span>
<span data-ttu-id="2e841-103">Központi telepítés létrehozása egy felügyeleti csoportban</span><span class="sxs-lookup"><span data-stu-id="2e841-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="2e841-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e841-104">SYNTAX</span></span>

### <span data-ttu-id="2e841-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e841-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e841-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e841-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e841-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e841-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e841-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e841-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e841-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e841-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e841-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e841-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e841-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e841-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e841-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e841-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e841-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e841-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e841-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e841-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e841-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2e841-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e841-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2e841-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e841-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e841-117">DESCRIPTION</span></span>
<span data-ttu-id="2e841-118">A **New-AzManagementGroupDeployment** parancsmag hozzáad egy telepítést egy felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="2e841-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="2e841-119">Ha egy felügyeleti csoportban szeretne központi telepítést hozzáadni, adja meg a felügyeleti csoportot, a helyet és egy sablont.</span><span class="sxs-lookup"><span data-stu-id="2e841-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="2e841-120">A hely közli az Azure Resource Managerrel, hogy hol kell tárolni a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="2e841-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="2e841-121">A sablon egy JSON-karakterlánc, amely az egyes telepítend kívánt erőforrásokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2e841-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="2e841-122">A sablon paraméterhelyőrzőket tartalmaz a kötelező erőforrásokhoz és a konfigurálható tulajdonságértékekhez, például a nevekhez és a méretekhez.</span><span class="sxs-lookup"><span data-stu-id="2e841-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="2e841-123">Ha egyéni sablont használ a telepítéshez, adja meg a *TemplateFile* vagy *a TemplateUri paramétert.*</span><span class="sxs-lookup"><span data-stu-id="2e841-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="2e841-124">Minden sablon rendelkezik paraméterekkel a konfigurálható tulajdonságokhoz.</span><span class="sxs-lookup"><span data-stu-id="2e841-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="2e841-125">A sablonparaméterek értékeinek megadásához adja meg a *TemplateParameterFile* vagy *a TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2e841-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="2e841-126">Másik lehetőségként használhatja a sablon megadásakor a parancshoz dinamikusan hozzáadott sablonparamétereket is.</span><span class="sxs-lookup"><span data-stu-id="2e841-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="2e841-127">Ha dinamikus paramétereket használ, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) egy paraméter jelzésére, és a Tab billentyűvel lépked az elérhető paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="2e841-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="2e841-128">A parancssorba beírandó sablon paraméterértékei elsőbbséget élveznek a sablon paraméterobjektumában vagy -fájljában megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="2e841-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="2e841-129">Ha erőforrásokat szeretne hozzáadni egy erőforráscsoporthoz, használja a **New-AzResourceGroupDeployment** bővítményt, amely létrehoz egy telepítést egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="2e841-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="2e841-130">Ha erőforrásokat szeretne hozzáadni egy előfizetéshez, használja a **New-AzSubscriptionDeployment** bővítményt, amely létrehoz egy telepítést az előfizetési hatókörben, amely az előfizetési szintű erőforrásokat telepíti.</span><span class="sxs-lookup"><span data-stu-id="2e841-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="2e841-131">Erőforrások bérlői hatókörben való hozzáadásához használja a **New-AzTenantDeployment** bővítményt, amely létrehoz egy telepítést a bérlői webhelyen.</span><span class="sxs-lookup"><span data-stu-id="2e841-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="2e841-132">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e841-132">EXAMPLES</span></span>

### <span data-ttu-id="2e841-133">1. példa: Egyéni sablon és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="2e841-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="2e841-134">Ez a parancs létrehoz egy új telepítést a "myMG" felügyeleti csoportban egy egyéni sablon és egy sablonfájl használatával a lemezen, definiált címke paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="2e841-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="2e841-135">A parancs *a TemplateFile paraméterrel* adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="2e841-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="2e841-136">2. példa: Egyéni sablonobjektum és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="2e841-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="2e841-137">Ez a parancs létrehoz egy új telepítést a "myMG" felügyeleti csoportban egy egyéni sablon és egy, a lemezen található sablonfájl használatával, amelyet a rendszer memórián belülre konvertált hashtable-ként.</span><span class="sxs-lookup"><span data-stu-id="2e841-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="2e841-138">Az első két parancs felolvassa a lemezen lévő sablonfájl szövegét, és átalakítja azt egy memóriában lévő hashtable-ként.</span><span class="sxs-lookup"><span data-stu-id="2e841-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="2e841-139">Az utolsó parancs *a TemplateObject* paraméter segítségével adja meg ezt a hashtable és *a TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="2e841-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="2e841-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e841-140">PARAMETERS</span></span>

### <span data-ttu-id="2e841-141">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e841-141">-AsJob</span></span>
<span data-ttu-id="2e841-142">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2e841-142">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e841-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e841-143">-DefaultProfile</span></span>
<span data-ttu-id="2e841-144">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e841-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e841-145">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="2e841-145">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="2e841-146">A központi telepítés hibakeresési naplószintje.</span><span class="sxs-lookup"><span data-stu-id="2e841-146">The deployment debug log level.</span></span>

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

### <span data-ttu-id="2e841-147">-Location</span><span class="sxs-lookup"><span data-stu-id="2e841-147">-Location</span></span>
<span data-ttu-id="2e841-148">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="2e841-148">The location to store deployment data.</span></span>

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

### <span data-ttu-id="2e841-149">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2e841-149">-ManagementGroupId</span></span>
<span data-ttu-id="2e841-150">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e841-150">The management group ID.</span></span>

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

### <span data-ttu-id="2e841-151">-Name</span><span class="sxs-lookup"><span data-stu-id="2e841-151">-Name</span></span>
<span data-ttu-id="2e841-152">Annak a telepítésnek a neve, amelyből létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="2e841-152">The name of the deployment it's going to create.</span></span> <span data-ttu-id="2e841-153">Ha nincs megadva, alapértelmezés szerint a sablonfájl neve lesz megadva; sablonobjektumok (például "2013123140835") beállítása.</span><span class="sxs-lookup"><span data-stu-id="2e841-153">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="2e841-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="2e841-154">-Pre</span></span>
<span data-ttu-id="2e841-155">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2e841-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2e841-156">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2e841-156">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2e841-157">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="2e841-157">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="2e841-158">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="2e841-158">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="2e841-159">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="2e841-159">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2e841-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e841-160">-Tag</span></span>
<span data-ttu-id="2e841-161">Az üzembe helyezéshez szükséges címkék.</span><span class="sxs-lookup"><span data-stu-id="2e841-161">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="2e841-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2e841-162">-TemplateFile</span></span>
<span data-ttu-id="2e841-163">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="2e841-163">Local path to the template file.</span></span>

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

### <span data-ttu-id="2e841-164">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="2e841-164">-TemplateObject</span></span>
<span data-ttu-id="2e841-165">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="2e841-165">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2e841-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e841-166">-TemplateParameterFile</span></span>
<span data-ttu-id="2e841-167">Olyan fájl, amely rendelkezik a sablonparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="2e841-167">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="2e841-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e841-168">-TemplateParameterObject</span></span>
<span data-ttu-id="2e841-169">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="2e841-169">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="2e841-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e841-170">-TemplateParameterUri</span></span>
<span data-ttu-id="2e841-171">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="2e841-171">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="2e841-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2e841-172">-TemplateUri</span></span>
<span data-ttu-id="2e841-173">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="2e841-173">Uri to the template file.</span></span>

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

### <span data-ttu-id="2e841-174">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="2e841-174">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="2e841-175">A vesszővel elválasztott erőforrás-módosítási típusokat nem lehet kizárni a What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="2e841-175">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="2e841-176">Akkor alkalmazható, ha a -WhatIf vagy a -Confirm kapcsoló be van állítva.</span><span class="sxs-lookup"><span data-stu-id="2e841-176">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="2e841-177">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="2e841-177">-WhatIfResultFormat</span></span>
<span data-ttu-id="2e841-178">A What-If formátuma.</span><span class="sxs-lookup"><span data-stu-id="2e841-178">The What-If result format.</span></span> <span data-ttu-id="2e841-179">Akkor alkalmazható, ha a -WhatIf vagy a -Confirm kapcsoló be van állítva.</span><span class="sxs-lookup"><span data-stu-id="2e841-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="2e841-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e841-180">-Confirm</span></span>
<span data-ttu-id="2e841-181">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2e841-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e841-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e841-182">-WhatIf</span></span>
<span data-ttu-id="2e841-183">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2e841-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e841-184">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e841-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e841-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e841-185">CommonParameters</span></span>
<span data-ttu-id="2e841-186">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e841-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e841-187">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e841-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e841-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e841-188">INPUTS</span></span>

### <span data-ttu-id="2e841-189">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e841-189">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2e841-190">System.String</span><span class="sxs-lookup"><span data-stu-id="2e841-190">System.String</span></span>

## <span data-ttu-id="2e841-191">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e841-191">OUTPUTS</span></span>

### <span data-ttu-id="2e841-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="2e841-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2e841-193">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e841-193">NOTES</span></span>

## <span data-ttu-id="2e841-194">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e841-194">RELATED LINKS</span></span>
