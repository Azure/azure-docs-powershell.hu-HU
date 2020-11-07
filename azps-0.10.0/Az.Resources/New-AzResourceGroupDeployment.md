---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 35741c908e57e96fd4d9709ff350ac885f41181d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843326"
---
# <span data-ttu-id="240df-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="240df-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="240df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="240df-102">SYNOPSIS</span></span>
<span data-ttu-id="240df-103">Azure-bevezetést ad hozzá egy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="240df-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="240df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="240df-104">SYNTAX</span></span>

### <span data-ttu-id="240df-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="240df-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240df-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="240df-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240df-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="240df-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240df-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="240df-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240df-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="240df-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240df-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="240df-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240df-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="240df-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240df-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="240df-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="240df-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="240df-113">DESCRIPTION</span></span>
<span data-ttu-id="240df-114">A **New-AzResourceGroupDeployment** parancsmag egy meglévő erőforráscsoport bevezetését adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="240df-114">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="240df-115">Ez a beállítás tartalmazza a telepítéshez szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="240df-115">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="240df-116">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis, webhely, virtuális gép vagy tárolási fiók.</span><span class="sxs-lookup"><span data-stu-id="240df-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="240df-117">Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként vannak telepítve, például a webhelyen, az adatbázis-kiszolgálón és a pénzügyi webhelyhez szükséges adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="240df-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="240df-118">Az erőforráscsoport-telepítés sablon használatával erőforrásokat ad hozzá egy erőforráscsoport számára, és közzéteszi őket, hogy azok elérhetők legyenek az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="240df-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="240df-119">Ha nem sablon nélkül szeretne erőforrásokat hozzáadni az erőforrás csoporthoz, használja az New-AzResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="240df-119">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="240df-120">Erőforráscsoport-telepítő hozzáadásához adja meg egy meglévő erőforráscsoport és egy erőforráscsoport-sablon nevét.</span><span class="sxs-lookup"><span data-stu-id="240df-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="240df-121">Egy erőforráscsoport-sablon egy olyan JSON karakterlánc, amely egy komplex felhőalapú szolgáltatás erőforráscsoport, például egy webportál.</span><span class="sxs-lookup"><span data-stu-id="240df-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="240df-122">A sablon tartalmazza a paraméterek helyőrzőit a szükséges erőforrások és a konfigurálható tulajdonságértékek (például nevek és méretek) esetében.</span><span class="sxs-lookup"><span data-stu-id="240df-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="240df-123">Az Azure template gyűjteményben számos sablon található, vagy saját sablonokat is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="240df-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="240df-124">Sablon kereséséhez használhatja a **Get-AzResourceGroupGalleryTemplate** parancsmagot a gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="240df-124">You can use the **Get-AzResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="240df-125">Ha egyéni sablont szeretne használni egy erőforráscsoport létrehozásához, adja meg a *TemplateFile* paramétert vagy a *TemplateUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="240df-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="240df-126">Mindegyik sablon rendelkezik a konfigurálható tulajdonságokra vonatkozó paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="240df-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="240df-127">A sablon paramétereinek értékeinek megadásához adja meg a *TemplateParameterFile* paramétert vagy a *TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="240df-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="240df-128">Azt is megteheti, hogy egy sablon megadásakor dinamikusan hozzáadja a parancsot a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="240df-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="240df-129">Ha dinamikus paramétereket szeretne használni, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) a paraméter jelzéséhez, és a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="240df-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="240df-130">A parancssorba beírt sablon paraméterei felülbírálják a Template paraméteres objektum vagy fájl értékeit.</span><span class="sxs-lookup"><span data-stu-id="240df-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="240df-131">Példák</span><span class="sxs-lookup"><span data-stu-id="240df-131">EXAMPLES</span></span>

### <span data-ttu-id="240df-132">1. példa: egyéni sablon és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="240df-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="240df-133">A parancs létrehoz egy új üzembe állítást egy egyéni sablon és egy sablonfájl segítségével a lemezen.</span><span class="sxs-lookup"><span data-stu-id="240df-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="240df-134">A parancs a *TemplateFile* paramétert használva adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="240df-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="240df-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="240df-135">PARAMETERS</span></span>

### <span data-ttu-id="240df-136">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="240df-136">-ApiVersion</span></span>
<span data-ttu-id="240df-137">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="240df-137">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="240df-138">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="240df-138">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="240df-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="240df-139">-AsJob</span></span>
<span data-ttu-id="240df-140">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="240df-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="240df-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240df-141">-DefaultProfile</span></span>
<span data-ttu-id="240df-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="240df-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240df-143">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="240df-143">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="240df-144">A Debug naplózási szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="240df-144">Specifies a debug log level.</span></span>
<span data-ttu-id="240df-145">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="240df-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="240df-146">RequestContent</span><span class="sxs-lookup"><span data-stu-id="240df-146">RequestContent</span></span>
- <span data-ttu-id="240df-147">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="240df-147">ResponseContent</span></span>
- <span data-ttu-id="240df-148">Minden</span><span class="sxs-lookup"><span data-stu-id="240df-148">All</span></span>
- <span data-ttu-id="240df-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="240df-149">None</span></span>

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

### <span data-ttu-id="240df-150">-Force</span><span class="sxs-lookup"><span data-stu-id="240df-150">-Force</span></span>
<span data-ttu-id="240df-151">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="240df-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="240df-152">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="240df-152">-Mode</span></span>
<span data-ttu-id="240df-153">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="240df-153">Specifies the deployment mode.</span></span> <span data-ttu-id="240df-154">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="240df-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="240df-155">Teljes</span><span class="sxs-lookup"><span data-stu-id="240df-155">Complete</span></span>
- <span data-ttu-id="240df-156">Növekményes mód: az erőforrás-kezelő törli azokat az erőforrásokat, amelyek szerepelnek az erőforrás csoportban, a sablonban azonban nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="240df-156">Incremental In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="240df-157">A növekményes módban az erőforrás-kezelő nem módosított erőforrásokat hagy az erőforrás csoportban, a sablonban azonban nem.</span><span class="sxs-lookup"><span data-stu-id="240df-157">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="240df-158">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="240df-158">-Name</span></span>
<span data-ttu-id="240df-159">A létrehozandó erőforráscsoport-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="240df-159">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="240df-160">-Pre</span><span class="sxs-lookup"><span data-stu-id="240df-160">-Pre</span></span>
<span data-ttu-id="240df-161">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="240df-161">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="240df-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240df-162">-ResourceGroupName</span></span>
<span data-ttu-id="240df-163">A telepítendő erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="240df-163">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="240df-164">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="240df-164">-RollBackDeploymentName</span></span>
<span data-ttu-id="240df-165">Ha az erőforrás csoportban az adott nevű névvel a sikeres telepítésre szeretne visszagörgetni, akkor ne használja a ha-RollbackToLastDeployment használatát.</span><span class="sxs-lookup"><span data-stu-id="240df-165">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="240df-166">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="240df-166">-RollbackToLastDeployment</span></span>
<span data-ttu-id="240df-167">Az erőforrás csoport utolsó sikeres telepítésére való visszagörgetéskor ne legyen megjelenni, ha-RollBackDeploymentName használja.</span><span class="sxs-lookup"><span data-stu-id="240df-167">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="240df-168">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="240df-168">-TemplateFile</span></span>
<span data-ttu-id="240df-169">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="240df-169">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="240df-170">Ez lehet egy egyéni sablon vagy egy olyan sablon, amelyet JSON-fájlként mentenek, például a **Save-AzResourceGroupGalleryTemplate** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="240df-170">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="240df-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="240df-171">-TemplateParameterFile</span></span>
<span data-ttu-id="240df-172">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="240df-172">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="240df-173">Ha egy sablon tartalmaz paramétereket, akkor a *TemplateParameterFile* paraméterrel vagy a *TemplateParameterObject* paraméterrel kell megadnia a paraméterek értékét.</span><span class="sxs-lookup"><span data-stu-id="240df-173">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="240df-174">Sablon megadásakor a program dinamikusan hozzáadja a sablon paramétereit a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="240df-174">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="240df-175">A dinamikus paraméterek használatához írjon be egy mínuszjelet (-) a paraméter nevének jelzéséhez, majd a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="240df-175">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240df-176">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="240df-176">-TemplateParameterObject</span></span>
<span data-ttu-id="240df-177">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="240df-177">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="240df-178">Ha segítségre van szüksége a kivonatoló táblázatokhoz a Windows PowerShellben, írja be a következőt `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="240df-178">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="240df-179">Ha egy sablonnak vannak paraméterei, meg kell adnia a paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="240df-179">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="240df-180">Sablon megadásakor a program dinamikusan hozzáadja a sablon paramétereit a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="240df-180">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240df-181">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="240df-181">-TemplateParameterUri</span></span>
<span data-ttu-id="240df-182">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="240df-182">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240df-183">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="240df-183">-TemplateUri</span></span>
<span data-ttu-id="240df-184">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="240df-184">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="240df-185">Ez a fájl lehet egy egyéni sablon vagy egy JSON-fájlként mentett gyűjtemény-sablon, például a **Save-AzResourceGroupGalleryTemplate** használatával.</span><span class="sxs-lookup"><span data-stu-id="240df-185">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="240df-186">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="240df-186">-Confirm</span></span>
<span data-ttu-id="240df-187">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="240df-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="240df-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="240df-188">-WhatIf</span></span>
<span data-ttu-id="240df-189">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="240df-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="240df-190">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="240df-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="240df-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240df-191">CommonParameters</span></span>
<span data-ttu-id="240df-192">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="240df-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240df-193">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="240df-193">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240df-194">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="240df-194">INPUTS</span></span>

### <span data-ttu-id="240df-195">Nincs</span><span class="sxs-lookup"><span data-stu-id="240df-195">None</span></span>

## <span data-ttu-id="240df-196">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="240df-196">OUTPUTS</span></span>

### <span data-ttu-id="240df-197">Microsoft. Azure. Command. ResourceManager. models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="240df-197">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="240df-198">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="240df-198">NOTES</span></span>

## <span data-ttu-id="240df-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="240df-199">RELATED LINKS</span></span>

[<span data-ttu-id="240df-200">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="240df-200">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="240df-201">Új – AzResource</span><span class="sxs-lookup"><span data-stu-id="240df-201">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="240df-202">Új – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="240df-202">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="240df-203">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="240df-203">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="240df-204">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="240df-204">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="240df-205">Teszt-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="240df-205">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


