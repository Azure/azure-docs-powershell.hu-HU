---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 12028dfd15ca27f7d57f2ffa55e473c835e0391f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836562"
---
# <span data-ttu-id="a113d-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a113d-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="a113d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a113d-102">SYNOPSIS</span></span>
<span data-ttu-id="a113d-103">Információt kap az adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="a113d-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="a113d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a113d-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a113d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a113d-105">DESCRIPTION</span></span>
<span data-ttu-id="a113d-106">A **Get-AzDataFactory** parancsmag információkat kap az adatgyárakról az Azure-erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="a113d-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="a113d-107">Ha megadja az adatfeldolgozó nevét, ez a parancsmag információkat kap az adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="a113d-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="a113d-108">Ha nem ad meg nevet, ez a parancsmag információt ad az Azure-erőforráscsoport minden adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="a113d-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="a113d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a113d-109">EXAMPLES</span></span>

### <span data-ttu-id="a113d-110">Példa 1: az összes adattényező beolvasása</span><span class="sxs-lookup"><span data-stu-id="a113d-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="a113d-111">Ez a parancs információt jelenít meg az Azure-előfizetésben szereplő összes adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="a113d-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="a113d-112">2. példa: konkrét adatgyár beszerzése</span><span class="sxs-lookup"><span data-stu-id="a113d-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="a113d-113">Ez a parancs információt jelenít meg az ADF nevű erőforráscsoport előfizetése WikiADF nevű adatfeldolgozóról, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a113d-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="a113d-114">Adja meg a *DataFactory* paramétert a további parancsmagokban az $DataFactory tárolt adatfeldolgozó használatához.</span><span class="sxs-lookup"><span data-stu-id="a113d-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="a113d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a113d-115">PARAMETERS</span></span>

### <span data-ttu-id="a113d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a113d-116">-DefaultProfile</span></span>
<span data-ttu-id="a113d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a113d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a113d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a113d-118">-Name</span></span>
<span data-ttu-id="a113d-119">Annak az adatszolgáltatónak a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="a113d-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a113d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a113d-120">-ResourceGroupName</span></span>
<span data-ttu-id="a113d-121">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a113d-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a113d-122">Ez a parancsmag információt ad az olyan adatgyárakról, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="a113d-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a113d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a113d-123">CommonParameters</span></span>
<span data-ttu-id="a113d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a113d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a113d-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a113d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a113d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a113d-126">INPUTS</span></span>

### <span data-ttu-id="a113d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a113d-127">System.String</span></span>

## <span data-ttu-id="a113d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a113d-128">OUTPUTS</span></span>

### <span data-ttu-id="a113d-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a113d-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a113d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a113d-130">NOTES</span></span>
* <span data-ttu-id="a113d-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="a113d-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a113d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a113d-132">RELATED LINKS</span></span>

[<span data-ttu-id="a113d-133">Új – AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a113d-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="a113d-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a113d-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


