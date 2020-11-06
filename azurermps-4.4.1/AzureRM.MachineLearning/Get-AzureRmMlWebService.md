---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504911"
---
# <span data-ttu-id="9685d-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="9685d-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="9685d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9685d-102">SYNOPSIS</span></span>
<span data-ttu-id="9685d-103">Lekérdezi egy vagy több webes szolgáltatás összefoglaló adatait.</span><span class="sxs-lookup"><span data-stu-id="9685d-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9685d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9685d-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9685d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9685d-105">DESCRIPTION</span></span>
<span data-ttu-id="9685d-106">A webszolgáltatás Defintion kapcsolatos adatok beolvasása</span><span class="sxs-lookup"><span data-stu-id="9685d-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="9685d-107">Az átadott paramenters függően a parancsmag egy adott webszolgáltatás Defintion ad eredményül, amely az aktuális előfizetésben lévő adott erőforráscsoport webszolgáltatásainak defintions, illetve az aktuális előfizetésben szereplő webes szolgáltatások defintions gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="9685d-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="9685d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9685d-108">EXAMPLES</span></span>

### <span data-ttu-id="9685d-109">--------------------------Példa 1: adott webszolgáltatás részleteinek beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="9685d-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
<span data-ttu-id="9685d-110">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="9685d-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="9685d-111">--------------------------Példa 2: az összes webszolgáltatás-erőforrás beolvasása a jelenlegi előfizetésben--------------------------</span><span class="sxs-lookup"><span data-stu-id="9685d-111">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
<span data-ttu-id="9685d-112">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="9685d-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService
```

### <span data-ttu-id="9685d-113">--------------------------Example 3: az összes webes szolgáltatás beszerzése az aktuális előfizetésben és az adott erőforráscsoport--------------------------</span><span class="sxs-lookup"><span data-stu-id="9685d-113">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="9685d-114">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="9685d-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="9685d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9685d-115">PARAMETERS</span></span>

### <span data-ttu-id="9685d-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9685d-116">-Name</span></span>
<span data-ttu-id="9685d-117">Annak a webszolgáltatásnak a neve, amelybe a részleteket lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="9685d-117">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="9685d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9685d-118">-ResourceGroupName</span></span>
<span data-ttu-id="9685d-119">Az az erőforráscsoport, amelyből a webszolgáltatás adatait beolvassák.</span><span class="sxs-lookup"><span data-stu-id="9685d-119">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="9685d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9685d-120">-DefaultProfile</span></span>
<span data-ttu-id="9685d-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9685d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9685d-122">-Region (régió)</span><span class="sxs-lookup"><span data-stu-id="9685d-122">-Region</span></span>
<span data-ttu-id="9685d-123">A régió neve</span><span class="sxs-lookup"><span data-stu-id="9685d-123">The name of region</span></span>

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

### <span data-ttu-id="9685d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9685d-124">CommonParameters</span></span>
<span data-ttu-id="9685d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9685d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9685d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9685d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9685d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9685d-127">INPUTS</span></span>

## <span data-ttu-id="9685d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9685d-128">OUTPUTS</span></span>

### <span data-ttu-id="9685d-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="9685d-129">None</span></span>

## <span data-ttu-id="9685d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9685d-130">NOTES</span></span>
<span data-ttu-id="9685d-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="9685d-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="9685d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9685d-132">RELATED LINKS</span></span>

