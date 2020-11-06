---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 7d0df70118f50274ccecfd730e752efabcf52519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496003"
---
# <span data-ttu-id="5aea1-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="5aea1-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="5aea1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5aea1-102">SYNOPSIS</span></span>
<span data-ttu-id="5aea1-103">Lekéri a webszolgáltatás kulcsait.</span><span class="sxs-lookup"><span data-stu-id="5aea1-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5aea1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5aea1-104">SYNTAX</span></span>

### <span data-ttu-id="5aea1-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5aea1-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5aea1-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="5aea1-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5aea1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5aea1-107">DESCRIPTION</span></span>
<span data-ttu-id="5aea1-108">Az Azure Machine learning webszolgáltatás futásidejű API-k elérési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5aea1-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="5aea1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5aea1-109">EXAMPLES</span></span>

### <span data-ttu-id="5aea1-110">Példa 1 – az erőforráscsoport által megadott webszolgáltatás és a név szerinti billentyűparancsok beszerzése</span><span class="sxs-lookup"><span data-stu-id="5aea1-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="5aea1-111">Példa 2 – webszolgáltatási példány kulcsának beszerzése</span><span class="sxs-lookup"><span data-stu-id="5aea1-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="5aea1-112">a $mlService a Microsoft. Azure. Management. MachineLearning. webszolgáltatás. models. webszolgáltatás parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5aea1-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="5aea1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5aea1-113">PARAMETERS</span></span>

### <span data-ttu-id="5aea1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aea1-114">-DefaultProfile</span></span>
<span data-ttu-id="5aea1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5aea1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5aea1-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="5aea1-116">-MlWebService</span></span>
<span data-ttu-id="5aea1-117">Annak a webszolgáltatásnak a neve, amelyhez a hozzáférési kulcsokat lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="5aea1-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5aea1-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5aea1-118">-Name</span></span>
<span data-ttu-id="5aea1-119">Annak a webszolgáltatásnak a neve, amelyhez a hozzáférési kulcsokat lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="5aea1-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aea1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aea1-120">-ResourceGroupName</span></span>
<span data-ttu-id="5aea1-121">A webszolgáltatás erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="5aea1-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aea1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aea1-122">CommonParameters</span></span>
<span data-ttu-id="5aea1-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5aea1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aea1-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aea1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aea1-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5aea1-125">INPUTS</span></span>

### <span data-ttu-id="5aea1-126">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="5aea1-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="5aea1-127">Paraméterek: MlWebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5aea1-127">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="5aea1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5aea1-128">OUTPUTS</span></span>

### <span data-ttu-id="5aea1-129">Microsoft. Azure. Management. MachineLearning. webszolgáltatás. models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="5aea1-129">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="5aea1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5aea1-130">NOTES</span></span>
<span data-ttu-id="5aea1-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="5aea1-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5aea1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5aea1-132">RELATED LINKS</span></span>
