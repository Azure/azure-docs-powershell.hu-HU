---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 87b911f480e5bd3186b956f5d9529afbef1e4582
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849889"
---
# <span data-ttu-id="65028-101">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="65028-101">New-AzureRmDeployment</span></span>

## <span data-ttu-id="65028-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65028-102">SYNOPSIS</span></span>
<span data-ttu-id="65028-103">A központi telepítő létrehozása</span><span class="sxs-lookup"><span data-stu-id="65028-103">Creat a deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65028-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65028-104">SYNTAX</span></span>

### <span data-ttu-id="65028-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65028-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65028-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="65028-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65028-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="65028-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65028-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="65028-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65028-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="65028-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65028-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="65028-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65028-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="65028-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65028-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="65028-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65028-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="65028-113">DESCRIPTION</span></span>
<span data-ttu-id="65028-114">A **New-AzureRmDeployment** parancsmag bevezetést ad az aktuális előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="65028-114">The **New-AzureRmDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="65028-115">Ez a beállítás tartalmazza a telepítéshez szükséges erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="65028-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="65028-116">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás.</span><span class="sxs-lookup"><span data-stu-id="65028-116">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="65028-117">Az erőforrások egy erőforrás-csoportban, például az adatbázis-kiszolgálón, az adatbázisban, a webhelyen, a virtuális gépen vagy a tárterület-fiókban élhetnek.</span><span class="sxs-lookup"><span data-stu-id="65028-117">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span> <span data-ttu-id="65028-118">Vagy lehet egy előfizetéses szintű erőforrás, például a szerepkör meghatározása, a házirend meghatározása stb.</span><span class="sxs-lookup"><span data-stu-id="65028-118">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="65028-119">Ha erőforrásokat szeretne felvenni egy erőforráscsoport számára, használja az **új AzureRmDeployment** , amely egy erőforrás-csoportban hoz létre központi telepítést.</span><span class="sxs-lookup"><span data-stu-id="65028-119">To add resources to a resource group, use the **New-AzureRmDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="65028-120">A **New-AzureRmDeployment** parancsmag létrehoz egy központi telepítést a jelenlegi előfizetési tartományhoz, amely az előfizetési szint erőforrásait telepíti.</span><span class="sxs-lookup"><span data-stu-id="65028-120">The **New-AzureRmDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span> 

<span data-ttu-id="65028-121">Ha fel szeretne venni egy üzembe állítást az előfizetésbe, adja meg a helyét és a sablont.</span><span class="sxs-lookup"><span data-stu-id="65028-121">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="65028-122">A hely közli az Azure Resource Manager szolgáltatással, hogy hol tárolja a központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="65028-122">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="65028-123">A sablon egy olyan JSON-karakterlánc, amely külön telepítendő erőforrásokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="65028-123">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="65028-124">A sablon tartalmazza a paraméterek helyőrzőit a szükséges erőforrások és a konfigurálható tulajdonságértékek (például nevek és méretek) esetében.</span><span class="sxs-lookup"><span data-stu-id="65028-124">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="65028-125">Ha egyéni sablont szeretne használni a központi telepítéséhez, adja meg a *TemplateFile* paramétert vagy a *TemplateUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="65028-125">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="65028-126">Mindegyik sablon rendelkezik a konfigurálható tulajdonságokra vonatkozó paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="65028-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="65028-127">A sablon paramétereinek értékeinek megadásához adja meg a *TemplateParameterFile* paramétert vagy a *TemplateParameterObject* paramétert.</span><span class="sxs-lookup"><span data-stu-id="65028-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="65028-128">Azt is megteheti, hogy egy sablon megadásakor dinamikusan hozzáadja a parancsot a parancshoz.</span><span class="sxs-lookup"><span data-stu-id="65028-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="65028-129">Ha dinamikus paramétereket szeretne használni, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) a paraméter jelzéséhez, és a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="65028-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="65028-130">A parancssorba beírt sablon paraméterei felülbírálják a Template paraméteres objektum vagy fájl értékeit.</span><span class="sxs-lookup"><span data-stu-id="65028-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="65028-131">Példák</span><span class="sxs-lookup"><span data-stu-id="65028-131">EXAMPLES</span></span>

### <span data-ttu-id="65028-132">1. példa: egyéni sablon és paraméteres fájl használata a központi telepítő létrehozásához</span><span class="sxs-lookup"><span data-stu-id="65028-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="65028-133">A parancs létrehoz egy új üzembe állítást az aktuális előfizetési tartományhoz egy egyéni sablon és egy, a lemezen lévő sablonfájl használatával.</span><span class="sxs-lookup"><span data-stu-id="65028-133">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="65028-134">A parancs a *TemplateFile* paramétert használva adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.</span><span class="sxs-lookup"><span data-stu-id="65028-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="65028-135">A *TemplateVersion* paramétert használja a sablon verziójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="65028-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="65028-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65028-136">PARAMETERS</span></span>

### <span data-ttu-id="65028-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="65028-137">-ApiVersion</span></span>
<span data-ttu-id="65028-138">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="65028-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="65028-139">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="65028-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="65028-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65028-140">-AsJob</span></span>
<span data-ttu-id="65028-141">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65028-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65028-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65028-142">-DefaultProfile</span></span>
<span data-ttu-id="65028-143">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65028-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65028-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="65028-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="65028-145">A központi telepítő naplózási szintje.</span><span class="sxs-lookup"><span data-stu-id="65028-145">The deployment debug log level.</span></span>

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

### <span data-ttu-id="65028-146">-Hely</span><span class="sxs-lookup"><span data-stu-id="65028-146">-Location</span></span>
<span data-ttu-id="65028-147">A központi telepítő adatainak tárolására szolgáló hely.</span><span class="sxs-lookup"><span data-stu-id="65028-147">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65028-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65028-148">-Name</span></span>
<span data-ttu-id="65028-149">Annak a telepítőnek a neve, amelyet létre fog hozni.</span><span class="sxs-lookup"><span data-stu-id="65028-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="65028-150">Csak akkor érvényes, ha sablon van használatban.</span><span class="sxs-lookup"><span data-stu-id="65028-150">Only valid when a template is used.</span></span>
<span data-ttu-id="65028-151">Ha egy sablont használ, ha a felhasználó nem ad meg központi telepítés nevét, használja az aktuális időpontot, például "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="65028-151">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65028-152">-Pre</span><span class="sxs-lookup"><span data-stu-id="65028-152">-Pre</span></span>
<span data-ttu-id="65028-153">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="65028-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="65028-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="65028-154">-TemplateFile</span></span>
<span data-ttu-id="65028-155">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="65028-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="65028-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="65028-156">-TemplateParameterFile</span></span>
<span data-ttu-id="65028-157">A sablon paramétereit tartalmazó fájl</span><span class="sxs-lookup"><span data-stu-id="65028-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="65028-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="65028-158">-TemplateParameterObject</span></span>
<span data-ttu-id="65028-159">A paramétereket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="65028-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="65028-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="65028-160">-TemplateParameterUri</span></span>
<span data-ttu-id="65028-161">URI a sablon paraméter-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="65028-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="65028-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="65028-162">-TemplateUri</span></span>
<span data-ttu-id="65028-163">A sablonfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="65028-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="65028-164">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65028-164">-Confirm</span></span>
<span data-ttu-id="65028-165">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65028-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65028-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65028-166">-WhatIf</span></span>
<span data-ttu-id="65028-167">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65028-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65028-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65028-168">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65028-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65028-169">CommonParameters</span></span>
<span data-ttu-id="65028-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65028-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65028-171">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65028-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65028-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65028-172">INPUTS</span></span>

### <span data-ttu-id="65028-173">System. String</span><span class="sxs-lookup"><span data-stu-id="65028-173">System.String</span></span>
<span data-ttu-id="65028-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="65028-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="65028-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65028-175">OUTPUTS</span></span>

### <span data-ttu-id="65028-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="65028-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="65028-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65028-177">NOTES</span></span>

## <span data-ttu-id="65028-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65028-178">RELATED LINKS</span></span>
