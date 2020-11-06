---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504903"
---
# <span data-ttu-id="2cec9-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="2cec9-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="2cec9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2cec9-102">SYNOPSIS</span></span>
<span data-ttu-id="2cec9-103">Lekéri a webszolgáltatás kulcsait.</span><span class="sxs-lookup"><span data-stu-id="2cec9-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cec9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2cec9-104">SYNTAX</span></span>

### <span data-ttu-id="2cec9-105">Az Azure ML webszolgáltatás elérési kulcsait a neve és az erőforráscsoport adja meg.</span><span class="sxs-lookup"><span data-stu-id="2cec9-105">Get an Azure ML web service's access keys given its name and resource group.</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cec9-106">A megadott webszolgáltatás-példány elérési kesy beszerzése</span><span class="sxs-lookup"><span data-stu-id="2cec9-106">Get the access kesy for the given web service instance.</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cec9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2cec9-107">DESCRIPTION</span></span>
<span data-ttu-id="2cec9-108">Az Azure Machine learning webszolgáltatás futásidejű API-k elérési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2cec9-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="2cec9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2cec9-109">EXAMPLES</span></span>

### <span data-ttu-id="2cec9-110">--------------------------Példa 1 – az erőforráscsoport által megadott webszolgáltatás kulcsai és a név--------------------------</span><span class="sxs-lookup"><span data-stu-id="2cec9-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
<span data-ttu-id="2cec9-111">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="2cec9-111">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="2cec9-112">--------------------------Example 2 – webszolgáltatási példány kulcsának beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="2cec9-112">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
<span data-ttu-id="2cec9-113">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="2cec9-113">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="2cec9-114">a $mlService a Microsoft. Azure. Management. MachineLearning. webszolgáltatás. models. webszolgáltatás parancsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2cec9-114">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="2cec9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2cec9-115">PARAMETERS</span></span>

### <span data-ttu-id="2cec9-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="2cec9-116">-MlWebService</span></span>
<span data-ttu-id="2cec9-117">Annak a webszolgáltatásnak a neve, amelyhez a hozzáférési kulcsokat lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="2cec9-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cec9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2cec9-118">-Name</span></span>
<span data-ttu-id="2cec9-119">Annak a webszolgáltatásnak a neve, amelyhez a hozzáférési kulcsokat lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="2cec9-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cec9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cec9-120">-ResourceGroupName</span></span>
<span data-ttu-id="2cec9-121">A webszolgáltatás erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="2cec9-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cec9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cec9-122">-DefaultProfile</span></span>
<span data-ttu-id="2cec9-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cec9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cec9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cec9-124">CommonParameters</span></span>
<span data-ttu-id="2cec9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2cec9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cec9-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cec9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cec9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cec9-127">INPUTS</span></span>

### <span data-ttu-id="2cec9-128">WebService</span><span class="sxs-lookup"><span data-stu-id="2cec9-128">WebService</span></span>
<span data-ttu-id="2cec9-129">A ' MlWebService ' paraméter a "webszolgáltatás" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2cec9-129">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="2cec9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cec9-130">OUTPUTS</span></span>

### <span data-ttu-id="2cec9-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="2cec9-131">None</span></span>

## <span data-ttu-id="2cec9-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2cec9-132">NOTES</span></span>
<span data-ttu-id="2cec9-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="2cec9-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2cec9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cec9-134">RELATED LINKS</span></span>

