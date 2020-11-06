---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 514d1257d917dc1bbf20f93d05236af9f36bd832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494370"
---
# <span data-ttu-id="2fce3-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fce3-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="2fce3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2fce3-102">SYNOPSIS</span></span>
<span data-ttu-id="2fce3-103">Azure-bevezetést ad hozzá egy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="2fce3-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fce3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2fce3-104">SYNTAX</span></span>

### <span data-ttu-id="2fce3-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2fce3-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fce3-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2fce3-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fce3-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2fce3-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fce3-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2fce3-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fce3-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2fce3-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fce3-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2fce3-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fce3-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2fce3-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fce3-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2fce3-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fce3-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="2fce3-113">DESCRIPTION</span></span>
<span data-ttu-id="2fce3-114">A **New-AzureRmResourceGroupDeployment** parancsmag egy meglévő erőforráscsoport bevezetését adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2fce3-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="2fce3-115">Ez a beállítás tartalmazza a telepítéshez szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="2fce3-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="2fce3-116">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis, webhely, virtuális gép vagy tárolási fiók.</span><span class="sxs-lookup"><span data-stu-id="2fce3-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="2fce3-117">Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként vannak telepítve, például a webhelyen, az adatbázis-kiszolgálón és a pénzügyi webhelyhez szükséges adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="2fce3-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="2fce3-118">Az erőforráscsoport-telepítés sablon használatával erőforrásokat ad hozzá egy erőforráscsoport számára, és közzéteszi őket, hogy azok elérhetők legyenek az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="2fce3-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="2fce3-119">Ha nem sablon nélkül szeretne erőforrásokat hozzáadni az erőforrás csoporthoz, használja az New-AzureRmResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2fce3-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="2fce3-120">Erőforráscsoport-telepítő hozzáadásához adja meg egy meglévő erőforráscsoport és egy erőforráscsoport-sablon nevét.</span><span class="sxs-lookup"><span data-stu-id="2fce3-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="2fce3-121">Egy erőforráscsoport-sablon egy olyan JSON karakterlánc, amely egy komplex felhőalapú szolgáltatás erőforráscsoport, például egy webportál.</span><span class="sxs-lookup"><span data-stu-id="2fce3-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="2fce3-122">A sablon tartalmazza a paraméterek helyőrzőit a szükséges erőforrások és a konfigurálható tulajdonságértékek (például nevek és méretek) esetében.</span><span class="sxs-lookup"><span data-stu-id="2fce3-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="2fce3-123">Az Azure template gyűjteményben számos sablon található, vagy saját sablonokat is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="2fce3-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="2fce3-124">Sablon kereséséhez használhatja a **Get-AzureRmResourceGroupGalleryTemplate** parancsmagot a gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="2fce3-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="2fce3-125">Ha egyéni sablont szeretne használni egy erőforráscsoport létrehozásához, adja meg a *TemplateFile* paramétert vagy a *TemplateUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2fce3-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="2fce3-126">Mindegyik sablon rendelkezik a konfigurálható tulajdonságokra vonatkozó paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="2fce3-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="2fce3-127">A sablon paramétereinek értékeinek megadásához adja meg a *TemplateParameterFile* paramétert vagy a *TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2fce3-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="2fce3-128">Azt is megteheti, hogy egy sablon megadásakor dinamikusan hozzáadja a parancsot a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="2fce3-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="2fce3-129">Ha dinamikus paramétereket szeretne használni, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) a paraméter jelzéséhez, és a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="2fce3-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="2fce3-130">A parancssorba beírt sablon paraméterei felülbírálják a Template paraméteres objektum vagy fájl értékeit.</span><span class="sxs-lookup"><span data-stu-id="2fce3-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="2fce3-131">Példák</span><span class="sxs-lookup"><span data-stu-id="2fce3-131">EXAMPLES</span></span>

### <span data-ttu-id="2fce3-132">1. példa: egyéni sablon és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="2fce3-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="2fce3-133">A parancs létrehoz egy új üzembe állítást egy egyéni sablon és egy sablonfájl segítségével a lemezen.</span><span class="sxs-lookup"><span data-stu-id="2fce3-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="2fce3-134">A parancs a *TemplateFile* paramétert használva adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="2fce3-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="2fce3-135">A *TemplateVersion* paramétert használja a sablon verziójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="2fce3-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="2fce3-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2fce3-136">PARAMETERS</span></span>

### <span data-ttu-id="2fce3-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2fce3-137">-ApiVersion</span></span>
<span data-ttu-id="2fce3-138">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fce3-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2fce3-139">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="2fce3-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2fce3-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fce3-140">-AsJob</span></span>
<span data-ttu-id="2fce3-141">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2fce3-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fce3-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fce3-142">-DefaultProfile</span></span>
<span data-ttu-id="2fce3-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2fce3-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fce3-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="2fce3-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="2fce3-145">A Debug naplózási szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fce3-145">Specifies a debug log level.</span></span>
<span data-ttu-id="2fce3-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2fce3-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fce3-147">RequestContent</span><span class="sxs-lookup"><span data-stu-id="2fce3-147">RequestContent</span></span>
- <span data-ttu-id="2fce3-148">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="2fce3-148">ResponseContent</span></span>
- <span data-ttu-id="2fce3-149">Minden</span><span class="sxs-lookup"><span data-stu-id="2fce3-149">All</span></span>
- <span data-ttu-id="2fce3-150">Nincs</span><span class="sxs-lookup"><span data-stu-id="2fce3-150">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fce3-151">-Force</span><span class="sxs-lookup"><span data-stu-id="2fce3-151">-Force</span></span>
<span data-ttu-id="2fce3-152">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2fce3-152">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fce3-153">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="2fce3-153">-Mode</span></span>
<span data-ttu-id="2fce3-154">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fce3-154">Specifies the deployment mode.</span></span> <span data-ttu-id="2fce3-155">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2fce3-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fce3-156">Teljes</span><span class="sxs-lookup"><span data-stu-id="2fce3-156">Complete</span></span>
- <span data-ttu-id="2fce3-157">Növekményes</span><span class="sxs-lookup"><span data-stu-id="2fce3-157">Incremental</span></span>

<span data-ttu-id="2fce3-158">A teljes módban az erőforrás-kezelő törli azokat az erőforrásokat, amelyek szerepelnek az erőforrás csoportban, a sablonban azonban nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="2fce3-158">In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="2fce3-159">A növekményes módban az erőforrás-kezelő nem módosított erőforrásokat hagy az erőforrás csoportban, a sablonban azonban nem.</span><span class="sxs-lookup"><span data-stu-id="2fce3-159">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fce3-160">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2fce3-160">-Name</span></span>
<span data-ttu-id="2fce3-161">A létrehozandó erőforráscsoport-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fce3-161">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fce3-162">-Pre</span><span class="sxs-lookup"><span data-stu-id="2fce3-162">-Pre</span></span>
<span data-ttu-id="2fce3-163">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2fce3-163">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2fce3-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fce3-164">-ResourceGroupName</span></span>
<span data-ttu-id="2fce3-165">A telepítendő erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fce3-165">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fce3-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2fce3-166">-TemplateFile</span></span>
<span data-ttu-id="2fce3-167">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fce3-167">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="2fce3-168">Ez lehet egy egyéni sablon vagy egy olyan sablon, amelyet JSON-fájlként mentenek, például a **Save-AzureRmResourceGroupGalleryTemplate** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="2fce3-168">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="2fce3-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2fce3-169">-TemplateParameterFile</span></span>
<span data-ttu-id="2fce3-170">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fce3-170">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="2fce3-171">Ha egy sablon tartalmaz paramétereket, akkor a *TemplateParameterFile* paraméterrel vagy a *TemplateParameterObject* paraméterrel kell megadnia a paraméterek értékét.</span><span class="sxs-lookup"><span data-stu-id="2fce3-171">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="2fce3-172">Sablon megadásakor a program dinamikusan hozzáadja a sablon paramétereit a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="2fce3-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="2fce3-173">A dinamikus paraméterek használatához írjon be egy mínuszjelet (-) a paraméter nevének jelzéséhez, majd a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="2fce3-173">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fce3-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2fce3-174">-TemplateParameterObject</span></span>
<span data-ttu-id="2fce3-175">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fce3-175">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="2fce3-176">Ha segítségre van szüksége a kivonatoló táblázatokhoz a Windows PowerShellben, írja be a következőt `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="2fce3-176">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="2fce3-177">Ha egy sablonnak vannak paraméterei, meg kell adnia a paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="2fce3-177">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="2fce3-178">Sablon megadásakor a program dinamikusan hozzáadja a sablon paramétereit a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="2fce3-178">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fce3-179">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2fce3-179">-TemplateParameterUri</span></span>
<span data-ttu-id="2fce3-180">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fce3-180">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fce3-181">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2fce3-181">-TemplateUri</span></span>
<span data-ttu-id="2fce3-182">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fce3-182">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="2fce3-183">Ez a fájl lehet egy egyéni sablon vagy egy JSON-fájlként mentett gyűjtemény-sablon, például a **Save-AzureRmResourceGroupGalleryTemplate** használatával.</span><span class="sxs-lookup"><span data-stu-id="2fce3-183">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="2fce3-184">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2fce3-184">-Confirm</span></span>
<span data-ttu-id="2fce3-185">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2fce3-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fce3-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fce3-186">-WhatIf</span></span>
<span data-ttu-id="2fce3-187">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2fce3-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fce3-188">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2fce3-188">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fce3-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fce3-189">CommonParameters</span></span>
<span data-ttu-id="2fce3-190">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2fce3-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fce3-191">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fce3-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fce3-192">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fce3-192">INPUTS</span></span>

### <span data-ttu-id="2fce3-193">Nincs</span><span class="sxs-lookup"><span data-stu-id="2fce3-193">None</span></span>

## <span data-ttu-id="2fce3-194">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fce3-194">OUTPUTS</span></span>

### <span data-ttu-id="2fce3-195">Microsoft. Azure. Command. ResourceManager. models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fce3-195">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="2fce3-196">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2fce3-196">NOTES</span></span>

## <span data-ttu-id="2fce3-197">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fce3-197">RELATED LINKS</span></span>

[<span data-ttu-id="2fce3-198">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fce3-198">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2fce3-199">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2fce3-199">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="2fce3-200">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2fce3-200">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="2fce3-201">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fce3-201">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2fce3-202">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fce3-202">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2fce3-203">Teszt-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fce3-203">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


