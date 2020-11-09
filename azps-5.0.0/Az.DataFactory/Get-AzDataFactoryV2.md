---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298559"
---
# <span data-ttu-id="91c17-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="91c17-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="91c17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91c17-102">SYNOPSIS</span></span>
<span data-ttu-id="91c17-103">Információt kap az adatgyárról.</span><span class="sxs-lookup"><span data-stu-id="91c17-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="91c17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91c17-104">SYNTAX</span></span>

### <span data-ttu-id="91c17-105">BySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91c17-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91c17-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="91c17-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91c17-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="91c17-107">DESCRIPTION</span></span>
<span data-ttu-id="91c17-108">Az Get-AzDataFactoryV2 parancsmag az Azure-erőforráscsoport adatgyárakról kap információkat.</span><span class="sxs-lookup"><span data-stu-id="91c17-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="91c17-109">Ha megadja az adatfeldolgozó nevét, ez a parancsmag információkat kap az adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="91c17-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="91c17-110">Ha nem ad meg nevet, ez a parancsmag információt ad az Azure-erőforráscsoport minden adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="91c17-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="91c17-111">Példák</span><span class="sxs-lookup"><span data-stu-id="91c17-111">EXAMPLES</span></span>

### <span data-ttu-id="91c17-112">Példa 1: az összes adattényező beolvasása</span><span class="sxs-lookup"><span data-stu-id="91c17-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

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

<span data-ttu-id="91c17-113">Információt jelenít meg az Azure-előfizetésben szereplő összes adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="91c17-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="91c17-114">2. példa: konkrét adatgyár beszerzése</span><span class="sxs-lookup"><span data-stu-id="91c17-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="91c17-115">Ez a parancs információt jelenít meg az ADF nevű erőforráscsoport előfizetése WikiADF nevű adatfeldolgozóról, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="91c17-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="91c17-116">Adja meg a DataFactory paramétert a további parancsmagokban az $DataFactory tárolt adatfeldolgozó használatához.</span><span class="sxs-lookup"><span data-stu-id="91c17-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="91c17-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91c17-117">PARAMETERS</span></span>

### <span data-ttu-id="91c17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c17-118">-DefaultProfile</span></span>
<span data-ttu-id="91c17-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91c17-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91c17-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91c17-120">-Name</span></span>
<span data-ttu-id="91c17-121">Annak az adatszolgáltatónak a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="91c17-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c17-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c17-122">-ResourceGroupName</span></span>
<span data-ttu-id="91c17-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91c17-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="91c17-124">Ez a parancsmag információt ad a csoporthoz tartozó adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="91c17-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c17-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c17-125">CommonParameters</span></span>
<span data-ttu-id="91c17-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91c17-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c17-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91c17-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c17-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91c17-128">INPUTS</span></span>

### <span data-ttu-id="91c17-129">System. String</span><span class="sxs-lookup"><span data-stu-id="91c17-129">System.String</span></span>

## <span data-ttu-id="91c17-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91c17-130">OUTPUTS</span></span>

### <span data-ttu-id="91c17-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="91c17-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="91c17-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91c17-132">NOTES</span></span>
<span data-ttu-id="91c17-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="91c17-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="91c17-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91c17-134">RELATED LINKS</span></span>

[<span data-ttu-id="91c17-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="91c17-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="91c17-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="91c17-136">Remove-AzDataFactoryV2</span></span>]()

