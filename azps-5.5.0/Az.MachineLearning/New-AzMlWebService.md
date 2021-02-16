---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157530"
---
# <span data-ttu-id="19613-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="19613-101">New-AzMlWebService</span></span>

## <span data-ttu-id="19613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19613-102">SYNOPSIS</span></span>
<span data-ttu-id="19613-103">Létrehoz egy új webszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="19613-103">Creates a new web service.</span></span>

## <span data-ttu-id="19613-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19613-104">SYNTAX</span></span>

### <span data-ttu-id="19613-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="19613-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19613-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="19613-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19613-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19613-107">DESCRIPTION</span></span>
<span data-ttu-id="19613-108">Azure Machine Learning webszolgáltatást hoz létre egy meglévő erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="19613-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="19613-109">Ha az erőforráscsoportban létezik azonos nevű webszolgáltatás, a hívás frissítési műveletként működik, és a meglévő webszolgáltatás felülíródik.</span><span class="sxs-lookup"><span data-stu-id="19613-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="19613-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19613-110">EXAMPLES</span></span>

### <span data-ttu-id="19613-111">1. példa: Új szolgáltatás létrehozása Json-fájlalapú definícióból</span><span class="sxs-lookup"><span data-stu-id="19613-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="19613-112">Létrehozza a "myresourcegroup" csoportban és az Egyesült Államok déli részén található "myresourcegroup" nevű új Azure Machine Learning webszolgáltatást a hivatkozott json-fájlban található definíció alapján.</span><span class="sxs-lookup"><span data-stu-id="19613-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="19613-113">2. példa: Új szolgáltatás létrehozása objektumpéldányból</span><span class="sxs-lookup"><span data-stu-id="19613-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="19613-114">A webszolgáltatás-objektumpéldányt az erőforrásként való közzététel előtt testre szabhatja a Import-AzMlWebService parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="19613-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="19613-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19613-115">PARAMETERS</span></span>

### <span data-ttu-id="19613-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19613-116">-DefaultProfile</span></span>
<span data-ttu-id="19613-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="19613-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19613-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="19613-118">-DefinitionFile</span></span>
<span data-ttu-id="19613-119">A webszolgáltatás JSON formátumdefinícióját tartalmazó fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19613-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="19613-120">A webszolgáltatás-definíció legújabb specifikációját a swagger specifikáció alatt https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning találja.</span><span class="sxs-lookup"><span data-stu-id="19613-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19613-121">-Force</span><span class="sxs-lookup"><span data-stu-id="19613-121">-Force</span></span>
<span data-ttu-id="19613-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19613-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="19613-123">-Location</span><span class="sxs-lookup"><span data-stu-id="19613-123">-Location</span></span>
<span data-ttu-id="19613-124">A webszolgáltatás régiója.</span><span class="sxs-lookup"><span data-stu-id="19613-124">The region of the web service.</span></span>
<span data-ttu-id="19613-125">Adjon meg egy Azure-adatközpont régiót, például "Nyugat-Usa" vagy "Délkelet-Ázsia".</span><span class="sxs-lookup"><span data-stu-id="19613-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="19613-126">A webszolgáltatás bármely olyan régióban elhelyelhet, amely támogatja az adott típusú erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="19613-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="19613-127">A webszolgáltatásnak nem kell ugyanabban a régióban lennie, mint az Azure-előfizetésének, vagy ugyanabban a régióban, ahol az erőforráscsoportja található.</span><span class="sxs-lookup"><span data-stu-id="19613-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="19613-128">Az erőforráscsoportok különböző régiókból származó webes szolgáltatásokat tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="19613-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="19613-129">Ha meg szeretné állapítani, hogy mely régiók támogatják az egyes erőforrástípusokat, használja a Get-AzResourceProvider a ProviderNamespace paraméter parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="19613-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="19613-130">-Name</span><span class="sxs-lookup"><span data-stu-id="19613-130">-Name</span></span>
<span data-ttu-id="19613-131">A webszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="19613-131">The name for the web service.</span></span>
<span data-ttu-id="19613-132">A névnek egyedinek kell lennie az erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="19613-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="19613-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="19613-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="19613-134">Az új webszolgáltatás definíciója, amely a szolgáltatást tartalmazó összes tulajdonságot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="19613-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="19613-135">Ez a paraméter kötelező, és a Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService osztály egy példányát képviseli.</span><span class="sxs-lookup"><span data-stu-id="19613-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="19613-136">A webszolgáltatás-definíció legújabb specifikációját a swagger specifikáció alatt https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json találja.</span><span class="sxs-lookup"><span data-stu-id="19613-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19613-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19613-137">-ResourceGroupName</span></span>
<span data-ttu-id="19613-138">Az az erőforráscsoport, amelyben el kell helyezze a webszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="19613-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="19613-139">Adjon meg egy Azure-adatközpont régiót, például "Nyugat-Usa" vagy "Délkelet-Ázsia".</span><span class="sxs-lookup"><span data-stu-id="19613-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="19613-140">A webszolgáltatás bármely olyan régióban elhelyelhet, amely támogatja az adott típusú erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="19613-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="19613-141">A webszolgáltatásnak nem kell ugyanabban a régióban lennie, mint az Azure-előfizetésének, vagy ugyanabban a régióban, ahol az erőforráscsoportja található.</span><span class="sxs-lookup"><span data-stu-id="19613-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="19613-142">Az erőforráscsoportok különböző régiókból származó webes szolgáltatásokat tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="19613-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="19613-143">Ha meg szeretné állapítani, hogy mely régiók támogatják az egyes erőforrástípusokat, használja a Get-AzResourceProvider a ProviderNamespace paraméter parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="19613-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="19613-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19613-144">-Confirm</span></span>
<span data-ttu-id="19613-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="19613-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19613-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19613-146">-WhatIf</span></span>
<span data-ttu-id="19613-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="19613-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19613-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19613-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19613-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19613-149">CommonParameters</span></span>
<span data-ttu-id="19613-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19613-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19613-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19613-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19613-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19613-152">INPUTS</span></span>

### <span data-ttu-id="19613-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="19613-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="19613-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19613-154">OUTPUTS</span></span>

### <span data-ttu-id="19613-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="19613-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="19613-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19613-156">NOTES</span></span>
<span data-ttu-id="19613-157">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="19613-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="19613-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19613-158">RELATED LINKS</span></span>
