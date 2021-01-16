---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: ad5979d65565107ac071bcaac94bc178b8c36d1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358034"
---
# <span data-ttu-id="c14be-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="c14be-101">New-AzDeployment</span></span>

## <span data-ttu-id="c14be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c14be-102">SYNOPSIS</span></span>
<span data-ttu-id="c14be-103">Telepítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="c14be-103">Create a deployment</span></span>

## <span data-ttu-id="c14be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c14be-104">SYNTAX</span></span>

### <span data-ttu-id="c14be-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c14be-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c14be-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c14be-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c14be-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c14be-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c14be-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c14be-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c14be-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c14be-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c14be-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c14be-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14be-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c14be-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c14be-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c14be-117">DESCRIPTION</span></span>
<span data-ttu-id="c14be-118">A **New-AzDeployment** parancsmag hozzáad egy telepítést az aktuális előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="c14be-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="c14be-119">Ide tartoznak a telepítéshez szükséges erőforrások is.</span><span class="sxs-lookup"><span data-stu-id="c14be-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="c14be-120">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás.</span><span class="sxs-lookup"><span data-stu-id="c14be-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="c14be-121">Az erőforrások egy erőforráscsoportban, például adatbázis-kiszolgálón, adatbázisban, webhelyen, virtuális gépen vagy tárfiókban is megélnek.</span><span class="sxs-lookup"><span data-stu-id="c14be-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="c14be-122">Az is lehet előfizetési szintű erőforrás, például szerepkör-definíció, házirend-definíció stb.</span><span class="sxs-lookup"><span data-stu-id="c14be-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="c14be-123">Ha erőforrásokat szeretne hozzáadni egy erőforráscsoporthoz, használja a **New-AzResourceGroupDeployment** bővítményt, amely létrehoz egy telepítést egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c14be-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="c14be-124">A **New-AzDeployment** parancsmag létrehoz egy telepítést az aktuális előfizetési hatókörben, amely az előfizetési szintű erőforrásokat telepíti.</span><span class="sxs-lookup"><span data-stu-id="c14be-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="c14be-125">Ha egy központi telepítést szeretne hozzáadni az előfizetéshez, adja meg a helyet és egy sablont.</span><span class="sxs-lookup"><span data-stu-id="c14be-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="c14be-126">A hely közli az Azure Resource Managerrel, hogy hol kell tárolni a telepítési adatokat.</span><span class="sxs-lookup"><span data-stu-id="c14be-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="c14be-127">A sablon egy JSON-karakterlánc, amely az egyes telepítend kívánt erőforrásokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c14be-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="c14be-128">A sablon paraméterhelyőrzőket tartalmaz a kötelező erőforrásokhoz és a konfigurálható tulajdonságértékekhez, például a nevekhez és a méretekhez.</span><span class="sxs-lookup"><span data-stu-id="c14be-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="c14be-129">Ha egyéni sablont használ a telepítéshez, adja meg a *TemplateFile* vagy *a TemplateUri paramétert.*</span><span class="sxs-lookup"><span data-stu-id="c14be-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="c14be-130">Minden sablon rendelkezik paraméterekkel a konfigurálható tulajdonságokhoz.</span><span class="sxs-lookup"><span data-stu-id="c14be-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="c14be-131">A sablonparaméterek értékeinek megadásához adja meg a *TemplateParameterFile* vagy *a TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="c14be-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="c14be-132">Másik lehetőségként használhatja a sablon megadásakor a parancshoz dinamikusan hozzáadott sablonparamétereket is.</span><span class="sxs-lookup"><span data-stu-id="c14be-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="c14be-133">Ha dinamikus paramétereket használ, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) egy paraméter jelzésére, és a Tab billentyűvel lépked az elérhető paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="c14be-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="c14be-134">A parancssorba beírandó sablon paraméterértékei elsőbbséget élveznek a sablon paraméterobjektumában vagy -fájljában megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="c14be-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="c14be-135">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c14be-135">EXAMPLES</span></span>

### <span data-ttu-id="c14be-136">1. példa: Egyéni sablon és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="c14be-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="c14be-137">Ez a parancs új telepítést hoz létre az aktuális előfizetési hatókörben egy egyéni sablon és egy lemezen lévő sablonfájl használatával, meghatározott címke paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="c14be-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="c14be-138">A parancs *a TemplateFile paraméterrel* adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="c14be-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="c14be-139">A *sablon verzióját a TemplateVersion* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="c14be-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="c14be-140">2. példa: Egyéni sablonobjektum és paraméterfájl használata telepítés létrehozására</span><span class="sxs-lookup"><span data-stu-id="c14be-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="c14be-141">Ez a parancs új telepítést hoz létre az aktuális előfizetési hatókörben egy egyéni sablon és egy, a lemezen lévő sablonfájl használatával, amelyet a rendszer memórián belülre konvertált hashtable-ként.</span><span class="sxs-lookup"><span data-stu-id="c14be-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="c14be-142">Az első két parancs felolvassa a lemezen lévő sablonfájl szövegét, és átalakítja azt egy memóriában lévő hashtable-ként.</span><span class="sxs-lookup"><span data-stu-id="c14be-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="c14be-143">Az utolsó parancs *a TemplateObject* paraméter segítségével adja meg ezt a hashtable és *a TemplateParameterFile* paramétert egy paramétereket és paraméterértékeket tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="c14be-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="c14be-144">A *sablon verzióját a TemplateVersion* paraméterrel adja meg.</span><span class="sxs-lookup"><span data-stu-id="c14be-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="c14be-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c14be-145">PARAMETERS</span></span>

### <span data-ttu-id="c14be-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c14be-146">-AsJob</span></span>
<span data-ttu-id="c14be-147">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c14be-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c14be-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14be-148">-DefaultProfile</span></span>
<span data-ttu-id="c14be-149">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c14be-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14be-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="c14be-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="c14be-151">A központi telepítés hibakeresési naplószintje.</span><span class="sxs-lookup"><span data-stu-id="c14be-151">The deployment debug log level.</span></span>

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

### <span data-ttu-id="c14be-152">-Location</span><span class="sxs-lookup"><span data-stu-id="c14be-152">-Location</span></span>
<span data-ttu-id="c14be-153">A telepítési adatok tárolására vonatkozó hely.</span><span class="sxs-lookup"><span data-stu-id="c14be-153">The location to store deployment data.</span></span>

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

### <span data-ttu-id="c14be-154">-Name</span><span class="sxs-lookup"><span data-stu-id="c14be-154">-Name</span></span>
<span data-ttu-id="c14be-155">Annak a telepítésnek a neve, amelyből létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="c14be-155">The name of the deployment it's going to create.</span></span> <span data-ttu-id="c14be-156">Ha nincs megadva, alapértelmezés szerint a sablonfájl neve lesz megadva; sablonobjektumok (például "2013123140835") beállítása.</span><span class="sxs-lookup"><span data-stu-id="c14be-156">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="c14be-157">-Pre</span><span class="sxs-lookup"><span data-stu-id="c14be-157">-Pre</span></span>
<span data-ttu-id="c14be-158">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c14be-158">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c14be-159">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c14be-159">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c14be-160">Kihagyja a PowerShell dinamikus paraméter-feldolgozását, amely ellenőrzi, hogy a megadott sablonparaméter tartalmazza-e a sablon által használt összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="c14be-160">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="c14be-161">Ez az ellenőrzés azt kéri a felhasználótól, hogy adjon meg egy értéket a hiányzó paraméterekhez, de a -SkipTemplateParameterPrompt paraméter megadása esetén a rendszer azonnal figyelmen kívül hagyja ezt a figyelmeztetést és hibát, ha egy paramétert nem kötöttnek talált a sablonban.</span><span class="sxs-lookup"><span data-stu-id="c14be-161">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="c14be-162">Nem interaktív parancsfájlok esetén -SkipTemplateParameterPrompt is meg lehet adni, hogy jobb hibaüzenetet biztosítson abban az esetben, ha nem minden szükséges paraméter teljesül.</span><span class="sxs-lookup"><span data-stu-id="c14be-162">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c14be-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="c14be-163">-Tag</span></span>
<span data-ttu-id="c14be-164">Az üzembe helyezéshez szükséges címkék.</span><span class="sxs-lookup"><span data-stu-id="c14be-164">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="c14be-165">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c14be-165">-TemplateFile</span></span>
<span data-ttu-id="c14be-166">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c14be-166">Local path to the template file.</span></span>

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

### <span data-ttu-id="c14be-167">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="c14be-167">-TemplateObject</span></span>
<span data-ttu-id="c14be-168">A sablont képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="c14be-168">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c14be-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c14be-169">-TemplateParameterFile</span></span>
<span data-ttu-id="c14be-170">Olyan fájl, amely rendelkezik a sablonparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="c14be-170">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="c14be-171">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c14be-171">-TemplateParameterObject</span></span>
<span data-ttu-id="c14be-172">A paramétereket képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="c14be-172">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="c14be-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c14be-173">-TemplateParameterUri</span></span>
<span data-ttu-id="c14be-174">Uri– a sablon paraméterfájlja.</span><span class="sxs-lookup"><span data-stu-id="c14be-174">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="c14be-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c14be-175">-TemplateUri</span></span>
<span data-ttu-id="c14be-176">Uri a sablonfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="c14be-176">Uri to the template file.</span></span>

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

### <span data-ttu-id="c14be-177">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="c14be-177">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="c14be-178">A vesszővel elválasztott erőforrás-módosítási típusokat nem lehet kizárni a What-If eredményből.</span><span class="sxs-lookup"><span data-stu-id="c14be-178">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="c14be-179">Akkor alkalmazható, ha a -WhatIf vagy a -Confirm kapcsoló be van állítva.</span><span class="sxs-lookup"><span data-stu-id="c14be-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="c14be-180">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="c14be-180">-WhatIfResultFormat</span></span>
<span data-ttu-id="c14be-181">A What-If formátuma.</span><span class="sxs-lookup"><span data-stu-id="c14be-181">The What-If result format.</span></span>

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

### <span data-ttu-id="c14be-182">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c14be-182">-Confirm</span></span>
<span data-ttu-id="c14be-183">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c14be-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c14be-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c14be-184">-WhatIf</span></span>
<span data-ttu-id="c14be-185">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c14be-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c14be-186">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c14be-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c14be-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14be-187">CommonParameters</span></span>
<span data-ttu-id="c14be-188">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14be-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14be-189">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c14be-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14be-190">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c14be-190">INPUTS</span></span>

### <span data-ttu-id="c14be-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c14be-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c14be-192">System.String</span><span class="sxs-lookup"><span data-stu-id="c14be-192">System.String</span></span>

## <span data-ttu-id="c14be-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c14be-193">OUTPUTS</span></span>

### <span data-ttu-id="c14be-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c14be-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c14be-195">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c14be-195">NOTES</span></span>

## <span data-ttu-id="c14be-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c14be-196">RELATED LINKS</span></span>
