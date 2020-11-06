---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 9512a8ae8e6bbd54704212539ad0650797cf4604
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500743"
---
# <span data-ttu-id="8b9a5-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b9a5-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="8b9a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9a5-103">Azure-bevezetést ad hozzá egy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b9a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b9a5-104">SYNTAX</span></span>

### <span data-ttu-id="8b9a5-105">Telepítés sablonon keresztül paraméterek nélkül (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b9a5-105">Deployment via template file without parameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b9a5-106">Telepítés sablonfájl és sablon paraméterei objektum segítségével</span><span class="sxs-lookup"><span data-stu-id="8b9a5-106">Deployment via template file and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b9a5-107">Telepítés sablon URI és sablon paraméterei objektum segítségével</span><span class="sxs-lookup"><span data-stu-id="8b9a5-107">Deployment via template uri and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b9a5-108">Telepítés sablonfájl és sablon paraméterei fájl segítségével</span><span class="sxs-lookup"><span data-stu-id="8b9a5-108">Deployment via template file and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b9a5-109">A telepítés sablon URI és sablon paraméterei fájl segítségével</span><span class="sxs-lookup"><span data-stu-id="8b9a5-109">Deployment via template uri and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b9a5-110">Telepítés sablonon keresztüli sablon paramétereit tartalmazó URI-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="8b9a5-110">Deployment via template file template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b9a5-111">Telepítés sablon URI-és sablon-paraméterek URI-kapcsolaton keresztül</span><span class="sxs-lookup"><span data-stu-id="8b9a5-111">Deployment via template uri and template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b9a5-112">Bevezetés a Template URI-ba paraméterek nélkül</span><span class="sxs-lookup"><span data-stu-id="8b9a5-112">Deployment via template uri without parameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b9a5-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b9a5-113">DESCRIPTION</span></span>
<span data-ttu-id="8b9a5-114">A **New-AzureRmResourceGroupDeployment** parancsmag egy meglévő erőforráscsoport bevezetését adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="8b9a5-115">Ez a beállítás tartalmazza a telepítéshez szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="8b9a5-116">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis, webhely, virtuális gép vagy tárolási fiók.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="8b9a5-117">Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként vannak telepítve, például a webhelyen, az adatbázis-kiszolgálón és a pénzügyi webhelyhez szükséges adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="8b9a5-118">Az erőforráscsoport-telepítés sablon használatával erőforrásokat ad hozzá egy erőforráscsoport számára, és közzéteszi őket, hogy azok elérhetők legyenek az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="8b9a5-119">Ha nem sablon nélkül szeretne erőforrásokat hozzáadni az erőforrás csoporthoz, használja az New-AzureRmResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="8b9a5-120">Erőforráscsoport-telepítő hozzáadásához adja meg egy meglévő erőforráscsoport és egy erőforráscsoport-sablon nevét.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="8b9a5-121">Egy erőforráscsoport-sablon egy olyan JSON karakterlánc, amely egy komplex felhőalapú szolgáltatás erőforráscsoport, például egy webportál.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="8b9a5-122">A sablon tartalmazza a paraméterek helyőrzőit a szükséges erőforrások és a konfigurálható tulajdonságértékek (például nevek és méretek) esetében.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="8b9a5-123">Az Azure template gyűjteményben számos sablon található, vagy saját sablonokat is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="8b9a5-124">Sablon kereséséhez használhatja a **Get-AzureRmResourceGroupGalleryTemplate** parancsmagot a gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="8b9a5-125">Ha egyéni sablont szeretne használni egy erőforráscsoport létrehozásához, adja meg a *TemplateFile* paramétert vagy a *TemplateUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="8b9a5-126">Mindegyik sablon rendelkezik a konfigurálható tulajdonságokra vonatkozó paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="8b9a5-127">A sablon paramétereinek értékeinek megadásához adja meg a *TemplateParameterFile* paramétert vagy a *TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="8b9a5-128">Azt is megteheti, hogy egy sablon megadásakor dinamikusan hozzáadja a parancsot a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="8b9a5-129">Ha dinamikus paramétereket szeretne használni, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) a paraméter jelzéséhez, és a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="8b9a5-130">A parancssorba beírt sablon paraméterei felülbírálják a Template paraméteres objektum vagy fájl értékeit.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="8b9a5-131">Példák</span><span class="sxs-lookup"><span data-stu-id="8b9a5-131">EXAMPLES</span></span>

### <span data-ttu-id="8b9a5-132">1. példa: egyéni sablon és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="8b9a5-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="8b9a5-133">A parancs létrehoz egy új üzembe állítást egy egyéni sablon és egy sablonfájl segítségével a lemezen.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="8b9a5-134">A parancs a *TemplateFile* paramétert használva adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="8b9a5-135">A *TemplateVersion* paramétert használja a sablon verziójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="8b9a5-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b9a5-136">PARAMETERS</span></span>

### <span data-ttu-id="8b9a5-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8b9a5-137">-ApiVersion</span></span>
<span data-ttu-id="8b9a5-138">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8b9a5-139">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8b9a5-140">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="8b9a5-140">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="8b9a5-141">A Debug naplózási szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-141">Specifies a debug log level.</span></span>
<span data-ttu-id="8b9a5-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8b9a5-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8b9a5-143">RequestContent</span><span class="sxs-lookup"><span data-stu-id="8b9a5-143">RequestContent</span></span> 
- <span data-ttu-id="8b9a5-144">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="8b9a5-144">ResponseContent</span></span> 
- <span data-ttu-id="8b9a5-145">Minden</span><span class="sxs-lookup"><span data-stu-id="8b9a5-145">All</span></span> 
- <span data-ttu-id="8b9a5-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="8b9a5-146">None</span></span>

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

### <span data-ttu-id="8b9a5-147">-Force</span><span class="sxs-lookup"><span data-stu-id="8b9a5-147">-Force</span></span>
<span data-ttu-id="8b9a5-148">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-148">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b9a5-149">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="8b9a5-149">-Mode</span></span>
<span data-ttu-id="8b9a5-150">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-150">Specifies the deployment mode.</span></span> <span data-ttu-id="8b9a5-151">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8b9a5-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8b9a5-152">Teljes</span><span class="sxs-lookup"><span data-stu-id="8b9a5-152">Complete</span></span> 
- <span data-ttu-id="8b9a5-153">Növekményes</span><span class="sxs-lookup"><span data-stu-id="8b9a5-153">Incremental</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a5-154">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b9a5-154">-Name</span></span>
<span data-ttu-id="8b9a5-155">A létrehozandó erőforráscsoport-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-155">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="8b9a5-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="8b9a5-156">-Pre</span></span>
<span data-ttu-id="8b9a5-157">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8b9a5-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b9a5-158">-ResourceGroupName</span></span>
<span data-ttu-id="8b9a5-159">A telepítendő erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-159">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="8b9a5-160">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8b9a5-160">-TemplateFile</span></span>
<span data-ttu-id="8b9a5-161">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-161">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="8b9a5-162">Ez lehet egy egyéni sablon vagy egy olyan sablon, amelyet JSON-fájlként mentenek, például a **Save-AzureRmResourceGroupGalleryTemplate** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-162">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a5-163">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8b9a5-163">-TemplateParameterFile</span></span>
<span data-ttu-id="8b9a5-164">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-164">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="8b9a5-165">Ha egy sablon tartalmaz paramétereket, akkor a *TemplateParameterFile* paraméterrel vagy a *TemplateParameterObject* paraméterrel kell megadnia a paraméterek értékét.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-165">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="8b9a5-166">Sablon megadásakor a program dinamikusan hozzáadja a sablon paramétereit a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-166">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="8b9a5-167">A dinamikus paraméterek használatához írjon be egy mínuszjelet (-) a paraméter nevének jelzéséhez, majd a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-167">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a5-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8b9a5-168">-TemplateParameterObject</span></span>
<span data-ttu-id="8b9a5-169">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-169">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="8b9a5-170">Ha segítségre van szüksége a kivonatoló táblázatokhoz a Windows PowerShellben, írja be a következőt `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="8b9a5-170">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="8b9a5-171">Ha egy sablonnak vannak paraméterei, meg kell adnia a paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-171">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="8b9a5-172">Sablon megadásakor a program dinamikusan hozzáadja a sablon paramétereit a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a5-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8b9a5-173">-TemplateParameterUri</span></span>
<span data-ttu-id="8b9a5-174">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-174">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a5-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8b9a5-175">-TemplateUri</span></span>
<span data-ttu-id="8b9a5-176">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-176">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="8b9a5-177">Ez a fájl lehet egy egyéni sablon vagy egy JSON-fájlként mentett gyűjtemény-sablon, például a **Save-AzureRmResourceGroupGalleryTemplate** használatával.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-177">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a5-178">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b9a5-178">-Confirm</span></span>
<span data-ttu-id="8b9a5-179">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b9a5-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b9a5-180">-WhatIf</span></span>
<span data-ttu-id="8b9a5-181">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b9a5-182">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b9a5-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b9a5-183">-DefaultProfile</span></span>
<span data-ttu-id="8b9a5-184">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b9a5-184">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a5-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9a5-185">CommonParameters</span></span>
<span data-ttu-id="8b9a5-186">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b9a5-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9a5-187">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b9a5-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9a5-188">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b9a5-188">INPUTS</span></span>

### <span data-ttu-id="8b9a5-189">Nincs</span><span class="sxs-lookup"><span data-stu-id="8b9a5-189">None</span></span>

## <span data-ttu-id="8b9a5-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b9a5-190">OUTPUTS</span></span>

### <span data-ttu-id="8b9a5-191">Microsoft. Azure. Command. ResourceManager. models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b9a5-191">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="8b9a5-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b9a5-192">NOTES</span></span>

## <span data-ttu-id="8b9a5-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b9a5-193">RELATED LINKS</span></span>

[<span data-ttu-id="8b9a5-194">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b9a5-194">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8b9a5-195">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8b9a5-195">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="8b9a5-196">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b9a5-196">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="8b9a5-197">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b9a5-197">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8b9a5-198">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b9a5-198">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8b9a5-199">Teszt-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b9a5-199">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


