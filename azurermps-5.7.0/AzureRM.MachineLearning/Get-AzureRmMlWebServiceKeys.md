---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: a0019b418fbf71a9b8010b4256a062a943244a9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497611"
---
# <span data-ttu-id="92bd3-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="92bd3-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="92bd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="92bd3-103">Lekéri a webszolgáltatás kulcsait.</span><span class="sxs-lookup"><span data-stu-id="92bd3-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92bd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92bd3-104">SYNTAX</span></span>

### <span data-ttu-id="92bd3-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92bd3-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92bd3-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="92bd3-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92bd3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="92bd3-107">DESCRIPTION</span></span>
<span data-ttu-id="92bd3-108">Az Azure Machine learning webszolgáltatás futásidejű API-k elérési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="92bd3-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="92bd3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="92bd3-109">EXAMPLES</span></span>

### <span data-ttu-id="92bd3-110">--------------------------Példa 1 – az erőforráscsoport által megadott webszolgáltatás kulcsai és a név--------------------------</span><span class="sxs-lookup"><span data-stu-id="92bd3-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="92bd3-111">--------------------------Example 2 – webszolgáltatási példány kulcsának beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="92bd3-111">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="92bd3-112">a $mlService a Microsoft. Azure. Management. MachineLearning. webszolgáltatás. models. webszolgáltatás parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="92bd3-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="92bd3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92bd3-113">PARAMETERS</span></span>

### <span data-ttu-id="92bd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92bd3-114">-DefaultProfile</span></span>
<span data-ttu-id="92bd3-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="92bd3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92bd3-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="92bd3-116">-MlWebService</span></span>
<span data-ttu-id="92bd3-117">Annak a webszolgáltatásnak a neve, amelyhez a hozzáférési kulcsokat lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="92bd3-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: WebService
Parameter Sets: GetByInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92bd3-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="92bd3-118">-Name</span></span>
<span data-ttu-id="92bd3-119">Annak a webszolgáltatásnak a neve, amelyhez a hozzáférési kulcsokat lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="92bd3-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bd3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92bd3-120">-ResourceGroupName</span></span>
<span data-ttu-id="92bd3-121">A webszolgáltatás erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="92bd3-121">The resource group for the web service.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bd3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bd3-122">CommonParameters</span></span>
<span data-ttu-id="92bd3-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92bd3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bd3-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92bd3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bd3-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92bd3-125">INPUTS</span></span>

### <span data-ttu-id="92bd3-126">WebService</span><span class="sxs-lookup"><span data-stu-id="92bd3-126">WebService</span></span>
<span data-ttu-id="92bd3-127">A ' MlWebService ' paraméter a "webszolgáltatás" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="92bd3-127">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="92bd3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92bd3-128">OUTPUTS</span></span>

### <span data-ttu-id="92bd3-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="92bd3-129">None</span></span>

## <span data-ttu-id="92bd3-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92bd3-130">NOTES</span></span>
<span data-ttu-id="92bd3-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="92bd3-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="92bd3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92bd3-132">RELATED LINKS</span></span>

