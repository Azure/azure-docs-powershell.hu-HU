---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 2f0f4ea68de5071a860b55a464d339d65ff2882c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492326"
---
# <span data-ttu-id="e0d39-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="e0d39-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="e0d39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0d39-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d39-103">Információt kap az adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="e0d39-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0d39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0d39-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0d39-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0d39-105">DESCRIPTION</span></span>
<span data-ttu-id="e0d39-106">A **Get-AzureRmDataFactory** parancsmag információkat kap az adatgyárakról az Azure-erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="e0d39-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="e0d39-107">Ha megadja az adatfeldolgozó nevét, ez a parancsmag információkat kap az adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="e0d39-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="e0d39-108">Ha nem ad meg nevet, ez a parancsmag információt ad az Azure-erőforráscsoport minden adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="e0d39-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="e0d39-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e0d39-109">EXAMPLES</span></span>

### <span data-ttu-id="e0d39-110">Példa 1: az összes adattényező beolvasása</span><span class="sxs-lookup"><span data-stu-id="e0d39-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
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

<span data-ttu-id="e0d39-111">Ez a parancs információt jelenít meg az Azure-előfizetésben szereplő összes adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="e0d39-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="e0d39-112">2. példa: konkrét adatgyár beszerzése</span><span class="sxs-lookup"><span data-stu-id="e0d39-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="e0d39-113">Ez a parancs információt jelenít meg az ADF nevű erőforráscsoport előfizetése WikiADF nevű adatfeldolgozóról, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e0d39-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="e0d39-114">Adja meg a *DataFactory* paramétert a további parancsmagokban az $DataFactory tárolt adatfeldolgozó használatához.</span><span class="sxs-lookup"><span data-stu-id="e0d39-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="e0d39-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0d39-115">PARAMETERS</span></span>

### <span data-ttu-id="e0d39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d39-116">-DefaultProfile</span></span>
<span data-ttu-id="e0d39-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e0d39-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d39-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0d39-118">-Name</span></span>
<span data-ttu-id="e0d39-119">Annak az adatszolgáltatónak a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="e0d39-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d39-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d39-120">-ResourceGroupName</span></span>
<span data-ttu-id="e0d39-121">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0d39-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e0d39-122">Ez a parancsmag információt ad az olyan adatgyárakról, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="e0d39-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e0d39-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d39-123">CommonParameters</span></span>
<span data-ttu-id="e0d39-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0d39-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d39-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d39-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d39-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0d39-126">INPUTS</span></span>

### <span data-ttu-id="e0d39-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="e0d39-127">None</span></span>
<span data-ttu-id="e0d39-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e0d39-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0d39-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0d39-129">OUTPUTS</span></span>

### <span data-ttu-id="e0d39-130">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft. WindowsAzure. commands. Utilities, Version = 0.8.2.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e0d39-130">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="e0d39-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0d39-131">NOTES</span></span>
* <span data-ttu-id="e0d39-132">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="e0d39-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e0d39-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0d39-133">RELATED LINKS</span></span>

[<span data-ttu-id="e0d39-134">Új – AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="e0d39-134">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="e0d39-135">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="e0d39-135">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


