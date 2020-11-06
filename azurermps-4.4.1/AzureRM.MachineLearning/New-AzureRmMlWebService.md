---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: 1fe6476836622445337ea0b4741b361504a57302
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504891"
---
# <span data-ttu-id="8ab76-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="8ab76-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="8ab76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ab76-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab76-103">Új webszolgáltatás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="8ab76-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ab76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ab76-104">SYNTAX</span></span>

### <span data-ttu-id="8ab76-105">Új Azure ML-webszolgáltatást hozhat létre JSON meghatározás-fájlból.</span><span class="sxs-lookup"><span data-stu-id="8ab76-105">Create a new Azure ML webservice from a JSON definiton file.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab76-106">Hozzon létre egy új Azure ML-webszolgáltatást egy webszolgáltatási példány-definícióból.</span><span class="sxs-lookup"><span data-stu-id="8ab76-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ab76-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ab76-107">DESCRIPTION</span></span>
<span data-ttu-id="8ab76-108">Azure Machine learning-webszolgáltatás létrehozása meglévő erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="8ab76-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="8ab76-109">Ha egy azonos nevű webszolgáltatás megtalálható az erőforrás csoportban, a hívás frissítési műveletként működik, és a meglévő webszolgáltatás felülíródik.</span><span class="sxs-lookup"><span data-stu-id="8ab76-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="8ab76-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8ab76-110">EXAMPLES</span></span>

### <span data-ttu-id="8ab76-111">--------------------------Példa 1: új szolgáltatás létrehozása JSON-fájlból épülő definícióból--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ab76-111">--------------------------  Example 1: Create a new service from a Json file based definition  --------------------------</span></span>
<span data-ttu-id="8ab76-112">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="8ab76-112">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="8ab76-113">Létrehoz egy új Azure Machine learning webszolgáltatás "mywebservicename" nevű webszolgáltatását a "myresourcegroup" csoportban és a dél-közép-amerikai régióban, a hivatkozott JSON-fájlban szereplő definíciók alapján.</span><span class="sxs-lookup"><span data-stu-id="8ab76-113">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="8ab76-114">--------------------------Példa: új szolgáltatás létrehozása objektum-példányból--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ab76-114">--------------------------  Example 2: Create a new service from an object instance  --------------------------</span></span>
<span data-ttu-id="8ab76-115">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="8ab76-115">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="8ab76-116">A Import-AzureRmMlWebService parancsmag segítségével webszolgáltatási objektum példányát is testre szabhatja a közzététel előtt.</span><span class="sxs-lookup"><span data-stu-id="8ab76-116">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="8ab76-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ab76-117">PARAMETERS</span></span>

### <span data-ttu-id="8ab76-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="8ab76-118">-DefinitionFile</span></span>
<span data-ttu-id="8ab76-119">Specifes a webszolgáltatás JSON formátumú definícióját tartalmazó fájl elérési útját.</span><span class="sxs-lookup"><span data-stu-id="8ab76-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="8ab76-120">A webszolgáltatás definíciójának legújabb specifikációját a hencegés specifikáció csoportban találja https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="8ab76-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: Create a new Azure ML webservice from a JSON definiton file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab76-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8ab76-121">-Force</span></span>
<span data-ttu-id="8ab76-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ab76-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8ab76-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="8ab76-123">-Location</span></span>
<span data-ttu-id="8ab76-124">A webszolgáltatás területe.</span><span class="sxs-lookup"><span data-stu-id="8ab76-124">The region of the web service.</span></span>
<span data-ttu-id="8ab76-125">Írjon be egy Azure Data Center-régiót (például "Nyugat-amerikai" vagy "Délkelet-ázsiai").</span><span class="sxs-lookup"><span data-stu-id="8ab76-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="8ab76-126">A webszolgáltatásokat bármely olyan régióban elhelyezheti, amely támogatja az adott típusú erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="8ab76-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="8ab76-127">A webszolgáltatásnak nem kell ugyanazon a régión belül lennie az Azure-előfizetésben vagy ugyanabban a régióban, mint az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="8ab76-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="8ab76-128">Az erőforráscsoportok tartalmazhatnak olyan webszolgáltatásokat, amelyek különböző régiókban találhatók.</span><span class="sxs-lookup"><span data-stu-id="8ab76-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="8ab76-129">Ha meg szeretné állapítani, hogy mely régiók támogatják az egyes erőforrás-típusokat, használja a Get-AzureRmResourceProvidert a ProviderNamespace paraméter parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="8ab76-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="8ab76-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ab76-130">-Name</span></span>
<span data-ttu-id="8ab76-131">A webszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="8ab76-131">The name for the web service.</span></span>
<span data-ttu-id="8ab76-132">A névnek egyedinek kell lennie az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="8ab76-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="8ab76-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="8ab76-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="8ab76-134">Az új webszolgáltatás definíciója, amely a szolgáltatást alkotó összes tulajdonságot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8ab76-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="8ab76-135">Ez a paraméter kötelező, és a Microsoft. Azure. Management. MachineLearning. webszolgáltatás. models. webszolgáltatási osztály példányát jelöli.</span><span class="sxs-lookup"><span data-stu-id="8ab76-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="8ab76-136">A webszolgáltatás definíciójának legújabb specifikációját a hencegés specifikáció csoportban találja https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="8ab76-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab76-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ab76-137">-ResourceGroupName</span></span>
<span data-ttu-id="8ab76-138">Az az erőforráscsoport, amelybe a webszolgáltatást helyezni szeretné.</span><span class="sxs-lookup"><span data-stu-id="8ab76-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="8ab76-139">Írjon be egy Azure Data Center-régiót (például "Nyugat-amerikai" vagy "Délkelet-ázsiai").</span><span class="sxs-lookup"><span data-stu-id="8ab76-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="8ab76-140">A webszolgáltatásokat bármely olyan régióban elhelyezheti, amely támogatja az adott típusú erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="8ab76-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="8ab76-141">A webszolgáltatásnak nem kell ugyanazon a régión belül lennie az Azure-előfizetésben vagy ugyanabban a régióban, mint az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="8ab76-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="8ab76-142">Az erőforráscsoportok tartalmazhatnak olyan webszolgáltatásokat, amelyek különböző régiókban találhatók.</span><span class="sxs-lookup"><span data-stu-id="8ab76-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="8ab76-143">Ha meg szeretné állapítani, hogy mely régiók támogatják az egyes erőforrás-típusokat, használja a Get-AzureRmResourceProvidert a ProviderNamespace paraméter parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="8ab76-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="8ab76-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8ab76-144">-Confirm</span></span>
<span data-ttu-id="8ab76-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ab76-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ab76-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab76-146">-WhatIf</span></span>
<span data-ttu-id="8ab76-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8ab76-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ab76-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ab76-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ab76-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab76-149">-DefaultProfile</span></span>
<span data-ttu-id="8ab76-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ab76-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ab76-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab76-151">CommonParameters</span></span>
<span data-ttu-id="8ab76-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ab76-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab76-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ab76-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab76-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ab76-154">INPUTS</span></span>

### <span data-ttu-id="8ab76-155">WebService</span><span class="sxs-lookup"><span data-stu-id="8ab76-155">WebService</span></span>
<span data-ttu-id="8ab76-156">A ' NewWebServiceDefinition ' paraméter a "webszolgáltatás" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8ab76-156">Parameter 'NewWebServiceDefinition' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="8ab76-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ab76-157">OUTPUTS</span></span>

### <span data-ttu-id="8ab76-158">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="8ab76-158">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="8ab76-159">Az Azure Machine learning webszolgáltatás összefoglaló leírása.</span><span class="sxs-lookup"><span data-stu-id="8ab76-159">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="8ab76-160">Hasonló a visszaadott leíráshoz, ha az Get-AzureRmMlWebService parancsmagot egy meglévő webszolgáltatásban hívja fel.</span><span class="sxs-lookup"><span data-stu-id="8ab76-160">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="8ab76-161">Ez a leírás nem tartalmaz bizalmas tulajdonságokat, például a tárolási fiók hitelesítő adatait és a szolgáltatás elérési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="8ab76-161">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="8ab76-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ab76-162">NOTES</span></span>
<span data-ttu-id="8ab76-163">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="8ab76-163">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="8ab76-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ab76-164">RELATED LINKS</span></span>

