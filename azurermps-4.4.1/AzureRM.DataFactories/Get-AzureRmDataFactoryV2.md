---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
ms.openlocfilehash: cba3540f47d2ce53b11a11f237adb28aa0bec6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493561"
---
# <span data-ttu-id="5e83a-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5e83a-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="5e83a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e83a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e83a-103">Információt kap az adatgyárról.</span><span class="sxs-lookup"><span data-stu-id="5e83a-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e83a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e83a-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e83a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e83a-105">DESCRIPTION</span></span>
<span data-ttu-id="5e83a-106">Az Get-AzureRmDataFactoryV2 parancsmag az Azure-erőforráscsoport adatgyárakról kap információkat.</span><span class="sxs-lookup"><span data-stu-id="5e83a-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="5e83a-107">Ha megadja az adatfeldolgozó nevét, ez a parancsmag információkat kap az adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="5e83a-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="5e83a-108">Ha nem ad meg nevet, ez a parancsmag információt ad az Azure-erőforráscsoport minden adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="5e83a-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="5e83a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5e83a-109">EXAMPLES</span></span>

### <span data-ttu-id="5e83a-110">Példa 1: az összes adattényező beolvasása</span><span class="sxs-lookup"><span data-stu-id="5e83a-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="5e83a-111">Információt jelenít meg az Azure-előfizetésben szereplő összes adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="5e83a-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="5e83a-112">2. példa: konkrét adatgyár beszerzése</span><span class="sxs-lookup"><span data-stu-id="5e83a-112">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="5e83a-113">Ez a parancs információt jelenít meg az ADF nevű erőforráscsoport előfizetése WikiADF nevű adatfeldolgozóról, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5e83a-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="5e83a-114">Adja meg a DataFactory paramétert a további parancsmagokban az $DataFactory tárolt adatfeldolgozó használatához.</span><span class="sxs-lookup"><span data-stu-id="5e83a-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="5e83a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e83a-115">PARAMETERS</span></span>

### <span data-ttu-id="5e83a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5e83a-116">-Name</span></span>
<span data-ttu-id="5e83a-117">Annak az adatszolgáltatónak a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="5e83a-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e83a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e83a-118">-ResourceGroupName</span></span>
<span data-ttu-id="5e83a-119">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e83a-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5e83a-120">Ez a parancsmag információt ad a csoporthoz tartozó adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="5e83a-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e83a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e83a-121">-DefaultProfile</span></span>
<span data-ttu-id="5e83a-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e83a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e83a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e83a-123">CommonParameters</span></span>
<span data-ttu-id="5e83a-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e83a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e83a-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e83a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e83a-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e83a-126">INPUTS</span></span>

### <span data-ttu-id="5e83a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5e83a-127">System.String</span></span>

## <span data-ttu-id="5e83a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e83a-128">OUTPUTS</span></span>

### <span data-ttu-id="5e83a-129">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. Command. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5e83a-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5e83a-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5e83a-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5e83a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e83a-131">NOTES</span></span>
<span data-ttu-id="5e83a-132">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="5e83a-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5e83a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e83a-133">RELATED LINKS</span></span>

[<span data-ttu-id="5e83a-134">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5e83a-134">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="5e83a-135">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5e83a-135">Remove-AzureRmDataFactoryV2</span></span>]()

