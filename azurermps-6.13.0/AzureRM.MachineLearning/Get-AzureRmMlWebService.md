---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 5632de726797dd36af377f76b5919590c5826606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496011"
---
# <span data-ttu-id="37e85-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="37e85-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="37e85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37e85-102">SYNOPSIS</span></span>
<span data-ttu-id="37e85-103">Lekérdezi egy vagy több webes szolgáltatás összefoglaló adatait.</span><span class="sxs-lookup"><span data-stu-id="37e85-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37e85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37e85-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37e85-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="37e85-105">DESCRIPTION</span></span>
<span data-ttu-id="37e85-106">A webszolgáltatás Defintion kapcsolatos adatok beolvasása</span><span class="sxs-lookup"><span data-stu-id="37e85-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="37e85-107">Az átadott paramenters függően a parancsmag egy adott webszolgáltatás Defintion ad eredményül, amely az aktuális előfizetésben lévő adott erőforráscsoport webszolgáltatásainak defintions, illetve az aktuális előfizetésben szereplő webes szolgáltatások defintions gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="37e85-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="37e85-108">Példák</span><span class="sxs-lookup"><span data-stu-id="37e85-108">EXAMPLES</span></span>

### <span data-ttu-id="37e85-109">Példa 1: adott webszolgáltatás részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="37e85-109">Example 1: Get details of specific web service</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="37e85-110">2. példa: az összes webszolgáltatás-erőforrás beolvasása a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="37e85-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzureRmMlWebService
```

### <span data-ttu-id="37e85-111">3. példa: az aktuális előfizetés és a megadott erőforráscsoport összes webes szolgáltatásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="37e85-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="37e85-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37e85-112">PARAMETERS</span></span>

### <span data-ttu-id="37e85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e85-113">-DefaultProfile</span></span>
<span data-ttu-id="37e85-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="37e85-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37e85-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="37e85-115">-Name</span></span>
<span data-ttu-id="37e85-116">Annak a webszolgáltatásnak a neve, amelybe a részleteket lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="37e85-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="37e85-117">-Region (régió)</span><span class="sxs-lookup"><span data-stu-id="37e85-117">-Region</span></span>
<span data-ttu-id="37e85-118">A Regio neve</span><span class="sxs-lookup"><span data-stu-id="37e85-118">The name of regio</span></span>

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

### <span data-ttu-id="37e85-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e85-119">-ResourceGroupName</span></span>
<span data-ttu-id="37e85-120">Az az erőforráscsoport, amelyből a webszolgáltatás adatait beolvassák.</span><span class="sxs-lookup"><span data-stu-id="37e85-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="37e85-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e85-121">CommonParameters</span></span>
<span data-ttu-id="37e85-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37e85-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e85-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37e85-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e85-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37e85-124">INPUTS</span></span>

### <span data-ttu-id="37e85-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="37e85-125">None</span></span>

## <span data-ttu-id="37e85-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37e85-126">OUTPUTS</span></span>

### <span data-ttu-id="37e85-127">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="37e85-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="37e85-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37e85-128">NOTES</span></span>
<span data-ttu-id="37e85-129">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="37e85-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="37e85-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37e85-130">RELATED LINKS</span></span>
