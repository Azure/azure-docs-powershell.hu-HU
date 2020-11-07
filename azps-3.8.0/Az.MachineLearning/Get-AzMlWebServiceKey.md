---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846230"
---
# <span data-ttu-id="ef2b8-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="ef2b8-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="ef2b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef2b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ef2b8-103">Lekéri a webszolgáltatás kulcsait.</span><span class="sxs-lookup"><span data-stu-id="ef2b8-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="ef2b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef2b8-104">SYNTAX</span></span>

### <span data-ttu-id="ef2b8-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef2b8-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef2b8-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="ef2b8-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef2b8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef2b8-107">DESCRIPTION</span></span>
<span data-ttu-id="ef2b8-108">Az Azure Machine learning webszolgáltatás futásidejű API-k elérési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ef2b8-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="ef2b8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ef2b8-109">EXAMPLES</span></span>

### <span data-ttu-id="ef2b8-110">Példa 1 – az erőforráscsoport által megadott webszolgáltatás és a név szerinti billentyűparancsok beszerzése</span><span class="sxs-lookup"><span data-stu-id="ef2b8-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="ef2b8-111">Példa 2 – webszolgáltatási példány kulcsának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ef2b8-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="ef2b8-112">a $mlService a Microsoft. Azure. Management. MachineLearning. webszolgáltatás. models. webszolgáltatás parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef2b8-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="ef2b8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef2b8-113">PARAMETERS</span></span>

### <span data-ttu-id="ef2b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef2b8-114">-DefaultProfile</span></span>
<span data-ttu-id="ef2b8-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ef2b8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef2b8-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="ef2b8-116">-MlWebService</span></span>
<span data-ttu-id="ef2b8-117">Annak a webszolgáltatásnak a neve, amelyhez a hozzáférési kulcsokat lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="ef2b8-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="ef2b8-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef2b8-118">-Name</span></span>
<span data-ttu-id="ef2b8-119">Annak a webszolgáltatásnak a neve, amelyhez a hozzáférési kulcsokat lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="ef2b8-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="ef2b8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef2b8-120">-ResourceGroupName</span></span>
<span data-ttu-id="ef2b8-121">A webszolgáltatás erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="ef2b8-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="ef2b8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef2b8-122">CommonParameters</span></span>
<span data-ttu-id="ef2b8-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef2b8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef2b8-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef2b8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef2b8-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef2b8-125">INPUTS</span></span>

### <span data-ttu-id="ef2b8-126">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="ef2b8-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="ef2b8-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef2b8-127">OUTPUTS</span></span>

### <span data-ttu-id="ef2b8-128">Microsoft. Azure. Management. MachineLearning. webszolgáltatás. models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="ef2b8-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="ef2b8-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef2b8-129">NOTES</span></span>
<span data-ttu-id="ef2b8-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="ef2b8-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ef2b8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef2b8-131">RELATED LINKS</span></span>
