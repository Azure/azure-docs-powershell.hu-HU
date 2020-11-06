---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499132"
---
# <span data-ttu-id="4bd5b-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4bd5b-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="4bd5b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd5b-103">Információt kap az adatgyárról.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd5b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bd5b-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## <span data-ttu-id="4bd5b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bd5b-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd5b-106">Az Get-AzureRmDataFactoryV2 parancsmag az Azure-erőforráscsoport adatgyárakról kap információkat.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="4bd5b-107">Ha megadja az adatfeldolgozó nevét, ez a parancsmag információkat kap az adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="4bd5b-108">Ha nem ad meg nevet, ez a parancsmag információt ad az Azure-erőforráscsoport minden adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>


## <span data-ttu-id="4bd5b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4bd5b-109">EXAMPLES</span></span>

### <span data-ttu-id="4bd5b-110">Példa 1: az összes adattényező beolvasása</span><span class="sxs-lookup"><span data-stu-id="4bd5b-110">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded

```

<span data-ttu-id="4bd5b-111">Információt jelenít meg az Azure-előfizetésben szereplő összes adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="4bd5b-112">2. példa: konkrét adatgyár beszerzése</span><span class="sxs-lookup"><span data-stu-id="4bd5b-112">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="4bd5b-113">Ez a parancs információt jelenít meg az ADF nevű erőforráscsoport előfizetése WikiADF nevű adatfeldolgozóról, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="4bd5b-114">Adja meg a DataFactory paramétert a további parancsmagokban az $DataFactory tárolt adatfeldolgozó használatához.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="4bd5b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bd5b-115">PARAMETERS</span></span>

### <span data-ttu-id="4bd5b-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4bd5b-116">-Name</span></span>
<span data-ttu-id="4bd5b-117">Annak az adatszolgáltatónak a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd5b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd5b-118">-ResourceGroupName</span></span>
<span data-ttu-id="4bd5b-119">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4bd5b-120">Ez a parancsmag információt ad a csoporthoz tartozó adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="4bd5b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bd5b-121">INPUTS</span></span>

### <span data-ttu-id="4bd5b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd5b-122">System.String</span></span>


## <span data-ttu-id="4bd5b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bd5b-123">OUTPUTS</span></span>

### <span data-ttu-id="4bd5b-124">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. Command. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4bd5b-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="4bd5b-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd5b-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="4bd5b-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bd5b-126">NOTES</span></span>
<span data-ttu-id="4bd5b-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="4bd5b-127">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4bd5b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bd5b-128">RELATED LINKS</span></span>
[<span data-ttu-id="4bd5b-129">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4bd5b-129">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="4bd5b-130">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4bd5b-130">Remove-AzureRmDataFactoryV2</span></span>]()

