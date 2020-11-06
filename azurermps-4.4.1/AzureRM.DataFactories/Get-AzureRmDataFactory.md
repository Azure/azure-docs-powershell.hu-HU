---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 5a7faf2e3eebcb00650bce367747e1945f7524da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493577"
---
# <span data-ttu-id="26f40-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="26f40-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="26f40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26f40-102">SYNOPSIS</span></span>
<span data-ttu-id="26f40-103">Információt kap az adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="26f40-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26f40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26f40-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26f40-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26f40-105">DESCRIPTION</span></span>
<span data-ttu-id="26f40-106">A **Get-AzureRmDataFactory** parancsmag információkat kap az adatgyárakról az Azure-erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="26f40-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="26f40-107">Ha megadja az adatfeldolgozó nevét, ez a parancsmag információkat kap az adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="26f40-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="26f40-108">Ha nem ad meg nevet, ez a parancsmag információt ad az Azure-erőforráscsoport minden adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="26f40-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="26f40-109">Példák</span><span class="sxs-lookup"><span data-stu-id="26f40-109">EXAMPLES</span></span>

### <span data-ttu-id="26f40-110">Példa 1: az összes adattényező beolvasása</span><span class="sxs-lookup"><span data-stu-id="26f40-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="26f40-111">Ez a parancs információt jelenít meg az Azure-előfizetésben szereplő összes adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="26f40-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="26f40-112">2. példa: konkrét adatgyár beszerzése</span><span class="sxs-lookup"><span data-stu-id="26f40-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="26f40-113">Ez a parancs információt jelenít meg az ADF nevű erőforráscsoport előfizetése WikiADF nevű adatfeldolgozóról, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="26f40-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="26f40-114">Adja meg a *DataFactory* paramétert a további parancsmagokban az $DataFactory tárolt adatfeldolgozó használatához.</span><span class="sxs-lookup"><span data-stu-id="26f40-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="26f40-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26f40-115">PARAMETERS</span></span>

### <span data-ttu-id="26f40-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26f40-116">-Name</span></span>
<span data-ttu-id="26f40-117">Annak az adatszolgáltatónak a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="26f40-117">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="26f40-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f40-118">-ResourceGroupName</span></span>
<span data-ttu-id="26f40-119">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26f40-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="26f40-120">Ez a parancsmag információt ad az olyan adatgyárakról, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="26f40-120">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="26f40-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f40-121">-DefaultProfile</span></span>
<span data-ttu-id="26f40-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26f40-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26f40-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f40-123">CommonParameters</span></span>
<span data-ttu-id="26f40-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26f40-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f40-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f40-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f40-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26f40-126">INPUTS</span></span>

## <span data-ttu-id="26f40-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26f40-127">OUTPUTS</span></span>

### <span data-ttu-id="26f40-128">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft. WindowsAzure. commands. Utilities, Version = 0.8.2.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="26f40-128">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="26f40-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26f40-129">NOTES</span></span>
* <span data-ttu-id="26f40-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="26f40-130">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="26f40-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26f40-131">RELATED LINKS</span></span>

[<span data-ttu-id="26f40-132">Új – AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="26f40-132">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="26f40-133">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="26f40-133">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


