---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154770"
---
# <span data-ttu-id="fd855-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="fd855-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="fd855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd855-102">SYNOPSIS</span></span>
<span data-ttu-id="fd855-103">Egy vagy több webes szolgáltatás összegző adatait olvassa be.</span><span class="sxs-lookup"><span data-stu-id="fd855-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="fd855-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd855-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd855-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd855-105">DESCRIPTION</span></span>
<span data-ttu-id="fd855-106">Webszolgáltatás-definíciós adatok beolvasása.</span><span class="sxs-lookup"><span data-stu-id="fd855-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="fd855-107">A átadott paraméterektől függően a parancsmag visszaadja egy adott webszolgáltatás definícióját, a webszolgáltatások definíciógyűjteményét az aktuális előfizetés egy adott erőforráscsoportjában, illetve a webszolgáltatások definíciógyűjteményét az aktuális előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="fd855-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="fd855-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd855-108">EXAMPLES</span></span>

### <span data-ttu-id="fd855-109">1. példa: Adott webszolgáltatás részleteinek megtekintése</span><span class="sxs-lookup"><span data-stu-id="fd855-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="fd855-110">2. példa: Az aktuális előfizetés összes webszolgáltatás-erőforrásának lekérte</span><span class="sxs-lookup"><span data-stu-id="fd855-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="fd855-111">3. példa: Az aktuális előfizetés és adott erőforráscsoport összes webes szolgáltatásának lekérte</span><span class="sxs-lookup"><span data-stu-id="fd855-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="fd855-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd855-112">PARAMETERS</span></span>

### <span data-ttu-id="fd855-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd855-113">-DefaultProfile</span></span>
<span data-ttu-id="fd855-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fd855-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd855-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fd855-115">-Name</span></span>
<span data-ttu-id="fd855-116">Annak a webszolgáltatásnak a neve, amely adatait lekéri.</span><span class="sxs-lookup"><span data-stu-id="fd855-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="fd855-117">-Régió</span><span class="sxs-lookup"><span data-stu-id="fd855-117">-Region</span></span>
<span data-ttu-id="fd855-118">A régió neve</span><span class="sxs-lookup"><span data-stu-id="fd855-118">The name of region</span></span>

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

### <span data-ttu-id="fd855-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd855-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd855-120">Az az erőforráscsoport, amelyből a webszolgáltatás adatait lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="fd855-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="fd855-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd855-121">CommonParameters</span></span>
<span data-ttu-id="fd855-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd855-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd855-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd855-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd855-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd855-124">INPUTS</span></span>

### <span data-ttu-id="fd855-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="fd855-125">None</span></span>

## <span data-ttu-id="fd855-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd855-126">OUTPUTS</span></span>

### <span data-ttu-id="fd855-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="fd855-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="fd855-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd855-128">NOTES</span></span>
<span data-ttu-id="fd855-129">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="fd855-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="fd855-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd855-130">RELATED LINKS</span></span>
