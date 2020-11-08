---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024733"
---
# <span data-ttu-id="2c029-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="2c029-101">New-AzMlWebService</span></span>

## <span data-ttu-id="2c029-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c029-102">SYNOPSIS</span></span>
<span data-ttu-id="2c029-103">Új webszolgáltatás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="2c029-103">Creates a new web service.</span></span>

## <span data-ttu-id="2c029-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c029-104">SYNTAX</span></span>

### <span data-ttu-id="2c029-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="2c029-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c029-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="2c029-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c029-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c029-107">DESCRIPTION</span></span>
<span data-ttu-id="2c029-108">Azure Machine learning-webszolgáltatás létrehozása meglévő erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="2c029-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="2c029-109">Ha egy azonos nevű webszolgáltatás megtalálható az erőforrás csoportban, a hívás frissítési műveletként működik, és a meglévő webszolgáltatás felülíródik.</span><span class="sxs-lookup"><span data-stu-id="2c029-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="2c029-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2c029-110">EXAMPLES</span></span>

### <span data-ttu-id="2c029-111">Példa 1: új szolgáltatás létrehozása JSON-fájlon keresztüli definíció alapján</span><span class="sxs-lookup"><span data-stu-id="2c029-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="2c029-112">Létrehoz egy új Azure Machine learning webszolgáltatás "mywebservicename" nevű webszolgáltatását a "myresourcegroup" csoportban és a dél-közép-amerikai régióban, a hivatkozott JSON-fájlban szereplő definíciók alapján.</span><span class="sxs-lookup"><span data-stu-id="2c029-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="2c029-113">2. példa: új szolgáltatás létrehozása objektum-példányból</span><span class="sxs-lookup"><span data-stu-id="2c029-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="2c029-114">A Import-AzMlWebService parancsmag segítségével webszolgáltatási objektum példányát is testre szabhatja a közzététel előtt.</span><span class="sxs-lookup"><span data-stu-id="2c029-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="2c029-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c029-115">PARAMETERS</span></span>

### <span data-ttu-id="2c029-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c029-116">-DefaultProfile</span></span>
<span data-ttu-id="2c029-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2c029-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c029-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="2c029-118">-DefinitionFile</span></span>
<span data-ttu-id="2c029-119">A webszolgáltatás JSON formátum definícióját tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c029-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="2c029-120">A webszolgáltatás definíciójának legújabb specifikációját a hencegés specifikáció csoportban találja https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="2c029-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

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

### <span data-ttu-id="2c029-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2c029-121">-Force</span></span>
<span data-ttu-id="2c029-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c029-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2c029-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="2c029-123">-Location</span></span>
<span data-ttu-id="2c029-124">A webszolgáltatás területe.</span><span class="sxs-lookup"><span data-stu-id="2c029-124">The region of the web service.</span></span>
<span data-ttu-id="2c029-125">Írjon be egy Azure Data Center-régiót (például "Nyugat-amerikai" vagy "Délkelet-ázsiai").</span><span class="sxs-lookup"><span data-stu-id="2c029-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="2c029-126">A webszolgáltatásokat bármely olyan régióban elhelyezheti, amely támogatja az adott típusú erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="2c029-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="2c029-127">A webszolgáltatásnak nem kell ugyanazon a régión belül lennie az Azure-előfizetésben vagy ugyanabban a régióban, mint az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="2c029-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="2c029-128">Az erőforráscsoportok tartalmazhatnak olyan webszolgáltatásokat, amelyek különböző régiókban találhatók.</span><span class="sxs-lookup"><span data-stu-id="2c029-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="2c029-129">Ha meg szeretné állapítani, hogy mely régiók támogatják az egyes erőforrás-típusokat, használja a Get-AzResourceProvidert a ProviderNamespace paraméter parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="2c029-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="2c029-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c029-130">-Name</span></span>
<span data-ttu-id="2c029-131">A webszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="2c029-131">The name for the web service.</span></span>
<span data-ttu-id="2c029-132">A névnek egyedinek kell lennie az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="2c029-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="2c029-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="2c029-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="2c029-134">Az új webszolgáltatás definíciója, amely a szolgáltatást alkotó összes tulajdonságot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2c029-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="2c029-135">Ez a paraméter kötelező, és a Microsoft. Azure. Management. MachineLearning. webszolgáltatás. models. webszolgáltatási osztály példányát jelöli.</span><span class="sxs-lookup"><span data-stu-id="2c029-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="2c029-136">A webszolgáltatás definíciójának legújabb specifikációját a hencegés specifikáció csoportban találja https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="2c029-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

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

### <span data-ttu-id="2c029-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c029-137">-ResourceGroupName</span></span>
<span data-ttu-id="2c029-138">Az az erőforráscsoport, amelybe a webszolgáltatást helyezni szeretné.</span><span class="sxs-lookup"><span data-stu-id="2c029-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="2c029-139">Írjon be egy Azure Data Center-régiót (például "Nyugat-amerikai" vagy "Délkelet-ázsiai").</span><span class="sxs-lookup"><span data-stu-id="2c029-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="2c029-140">A webszolgáltatásokat bármely olyan régióban elhelyezheti, amely támogatja az adott típusú erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="2c029-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="2c029-141">A webszolgáltatásnak nem kell ugyanazon a régión belül lennie az Azure-előfizetésben vagy ugyanabban a régióban, mint az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="2c029-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="2c029-142">Az erőforráscsoportok tartalmazhatnak olyan webszolgáltatásokat, amelyek különböző régiókban találhatók.</span><span class="sxs-lookup"><span data-stu-id="2c029-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="2c029-143">Ha meg szeretné állapítani, hogy mely régiók támogatják az egyes erőforrás-típusokat, használja a Get-AzResourceProvidert a ProviderNamespace paraméter parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="2c029-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="2c029-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c029-144">-Confirm</span></span>
<span data-ttu-id="2c029-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c029-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c029-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c029-146">-WhatIf</span></span>
<span data-ttu-id="2c029-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c029-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c029-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c029-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c029-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c029-149">CommonParameters</span></span>
<span data-ttu-id="2c029-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c029-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c029-151">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c029-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c029-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c029-152">INPUTS</span></span>

### <span data-ttu-id="2c029-153">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="2c029-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="2c029-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c029-154">OUTPUTS</span></span>

### <span data-ttu-id="2c029-155">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="2c029-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="2c029-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c029-156">NOTES</span></span>
<span data-ttu-id="2c029-157">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="2c029-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2c029-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c029-158">RELATED LINKS</span></span>
