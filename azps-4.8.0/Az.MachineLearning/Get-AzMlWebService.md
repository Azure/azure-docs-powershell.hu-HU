---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018194"
---
# <span data-ttu-id="ce9f1-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="ce9f1-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="ce9f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce9f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9f1-103">Lekérdezi egy vagy több webes szolgáltatás összefoglaló adatait.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="ce9f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce9f1-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce9f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce9f1-105">DESCRIPTION</span></span>
<span data-ttu-id="ce9f1-106">A webszolgáltatás-definíciós adatok beolvasása</span><span class="sxs-lookup"><span data-stu-id="ce9f1-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="ce9f1-107">Az átadott paraméterektől függően a parancsmag egy adott webszolgáltatás definícióját adja eredményül, amely az aktuális előfizetésben szereplő adott erőforráscsoport webszolgáltatásainak definícióját, illetve az aktuális előfizetésben szereplő webes szolgáltatások definíciójának gyűjteményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="ce9f1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ce9f1-108">EXAMPLES</span></span>

### <span data-ttu-id="ce9f1-109">Példa 1: adott webszolgáltatás részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="ce9f1-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="ce9f1-110">2. példa: az összes webszolgáltatás-erőforrás beolvasása a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="ce9f1-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="ce9f1-111">3. példa: az aktuális előfizetés és a megadott erőforráscsoport összes webes szolgáltatásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ce9f1-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="ce9f1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce9f1-112">PARAMETERS</span></span>

### <span data-ttu-id="ce9f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce9f1-113">-DefaultProfile</span></span>
<span data-ttu-id="ce9f1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ce9f1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce9f1-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce9f1-115">-Name</span></span>
<span data-ttu-id="ce9f1-116">Annak a webszolgáltatásnak a neve, amelybe a részleteket lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="ce9f1-117">-Region (régió)</span><span class="sxs-lookup"><span data-stu-id="ce9f1-117">-Region</span></span>
<span data-ttu-id="ce9f1-118">A régió neve</span><span class="sxs-lookup"><span data-stu-id="ce9f1-118">The name of region</span></span>

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

### <span data-ttu-id="ce9f1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce9f1-119">-ResourceGroupName</span></span>
<span data-ttu-id="ce9f1-120">Az az erőforráscsoport, amelyből a webszolgáltatás adatait beolvassák.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="ce9f1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9f1-121">CommonParameters</span></span>
<span data-ttu-id="ce9f1-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce9f1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9f1-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce9f1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9f1-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce9f1-124">INPUTS</span></span>

### <span data-ttu-id="ce9f1-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="ce9f1-125">None</span></span>

## <span data-ttu-id="ce9f1-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce9f1-126">OUTPUTS</span></span>

### <span data-ttu-id="ce9f1-127">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="ce9f1-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="ce9f1-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce9f1-128">NOTES</span></span>
<span data-ttu-id="ce9f1-129">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="ce9f1-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ce9f1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce9f1-130">RELATED LINKS</span></span>
