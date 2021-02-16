---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204463"
---
# <span data-ttu-id="5951d-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5951d-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="5951d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5951d-102">SYNOPSIS</span></span>
<span data-ttu-id="5951d-103">Információkat kap a Data Factoryról.</span><span class="sxs-lookup"><span data-stu-id="5951d-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="5951d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5951d-104">SYNTAX</span></span>

### <span data-ttu-id="5951d-105">BySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5951d-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5951d-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="5951d-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5951d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5951d-107">DESCRIPTION</span></span>
<span data-ttu-id="5951d-108">A Get-AzDataFactoryV2 parancsmag információkat kap egy Azure-erőforráscsoport adattényezőiről.</span><span class="sxs-lookup"><span data-stu-id="5951d-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="5951d-109">Ha megadja egy adatüzem nevét, ez a parancsmag információt kap az adatüzemről.</span><span class="sxs-lookup"><span data-stu-id="5951d-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="5951d-110">Ha nem ad meg nevet, ez a parancsmag információt kap egy Azure-erőforráscsoport összes adattényezőjeről.</span><span class="sxs-lookup"><span data-stu-id="5951d-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="5951d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5951d-111">EXAMPLES</span></span>

### <span data-ttu-id="5951d-112">1. példa: Az összes adattényező be szerezze</span><span class="sxs-lookup"><span data-stu-id="5951d-112">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="5951d-113">Információkat jelenít meg az Azure-előfizetésben található összes adattényezőről.</span><span class="sxs-lookup"><span data-stu-id="5951d-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="5951d-114">2. példa: Adott adat factory lekérte</span><span class="sxs-lookup"><span data-stu-id="5951d-114">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="5951d-115">Ez a parancs információkat jelenít meg a WikiADF nevű adatüzemről az ADF nevű erőforráscsoport előfizetésében, majd a $DataFactory tárolja.</span><span class="sxs-lookup"><span data-stu-id="5951d-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="5951d-116">Adja meg a DataFactory paramétert a későbbi parancsmagokban a $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="5951d-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="5951d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5951d-117">PARAMETERS</span></span>

### <span data-ttu-id="5951d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5951d-118">-DefaultProfile</span></span>
<span data-ttu-id="5951d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5951d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5951d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5951d-120">-Name</span></span>
<span data-ttu-id="5951d-121">Annak az adatüzemnek a nevét adja meg, amelyről információt kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="5951d-121">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="5951d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5951d-122">-ResourceGroupName</span></span>
<span data-ttu-id="5951d-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5951d-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5951d-124">Ez a parancsmag információt kap a paraméter által megadott csoporthoz tartozó adattényezőkről.</span><span class="sxs-lookup"><span data-stu-id="5951d-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="5951d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5951d-125">CommonParameters</span></span>
<span data-ttu-id="5951d-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5951d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5951d-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5951d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5951d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5951d-128">INPUTS</span></span>

### <span data-ttu-id="5951d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5951d-129">System.String</span></span>

## <span data-ttu-id="5951d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5951d-130">OUTPUTS</span></span>

### <span data-ttu-id="5951d-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5951d-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5951d-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5951d-132">NOTES</span></span>
<span data-ttu-id="5951d-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="5951d-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5951d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5951d-134">RELATED LINKS</span></span>

[<span data-ttu-id="5951d-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5951d-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="5951d-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5951d-136">Remove-AzDataFactoryV2</span></span>]()

