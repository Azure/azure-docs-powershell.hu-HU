---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: ff47851c998cb88bec7106e8aba6d47d16069321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931194"
---
# <span data-ttu-id="66be2-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="66be2-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="66be2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66be2-102">SYNOPSIS</span></span>
<span data-ttu-id="66be2-103">Információkat kap az adattényezőkről.</span><span class="sxs-lookup"><span data-stu-id="66be2-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="66be2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66be2-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66be2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66be2-105">DESCRIPTION</span></span>
<span data-ttu-id="66be2-106">A **Get-AzDataFactory** parancsmag információt kap egy Azure-erőforráscsoport adattényezőiről.</span><span class="sxs-lookup"><span data-stu-id="66be2-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="66be2-107">Ha megadja egy adatüzem nevét, ez a parancsmag információt kap az adatüzemről.</span><span class="sxs-lookup"><span data-stu-id="66be2-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="66be2-108">Ha nem ad meg nevet, ez a parancsmag információt kap egy Azure-erőforráscsoport összes adattényezőről.</span><span class="sxs-lookup"><span data-stu-id="66be2-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="66be2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66be2-109">EXAMPLES</span></span>

### <span data-ttu-id="66be2-110">1. példa: Az összes adattényező be szerezze</span><span class="sxs-lookup"><span data-stu-id="66be2-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="66be2-111">Ez a parancs az Azure-előfizetés összes adattényezője adatait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="66be2-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="66be2-112">2. példa: Adott adat factory lekérte</span><span class="sxs-lookup"><span data-stu-id="66be2-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="66be2-113">Ez a parancs információkat jelenít meg a WikiADF nevű adatüzemről az ADF nevű erőforráscsoport előfizetésében, majd a $DataFactory tárolja.</span><span class="sxs-lookup"><span data-stu-id="66be2-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="66be2-114">Adja meg *a DataFactory* paramétert a későbbi parancsmagokban a $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="66be2-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="66be2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66be2-115">PARAMETERS</span></span>

### <span data-ttu-id="66be2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66be2-116">-DefaultProfile</span></span>
<span data-ttu-id="66be2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="66be2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66be2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="66be2-118">-Name</span></span>
<span data-ttu-id="66be2-119">Annak az adatüzemnek a nevét adja meg, amelyről információt kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="66be2-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="66be2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66be2-120">-ResourceGroupName</span></span>
<span data-ttu-id="66be2-121">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="66be2-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="66be2-122">Ez a parancsmag információt kap a paraméter által megadott csoporthoz tartozó adattényezőkről.</span><span class="sxs-lookup"><span data-stu-id="66be2-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="66be2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66be2-123">CommonParameters</span></span>
<span data-ttu-id="66be2-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66be2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66be2-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66be2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66be2-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66be2-126">INPUTS</span></span>

### <span data-ttu-id="66be2-127">System.String</span><span class="sxs-lookup"><span data-stu-id="66be2-127">System.String</span></span>

## <span data-ttu-id="66be2-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66be2-128">OUTPUTS</span></span>

### <span data-ttu-id="66be2-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="66be2-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="66be2-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66be2-130">NOTES</span></span>
* <span data-ttu-id="66be2-131">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="66be2-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="66be2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66be2-132">RELATED LINKS</span></span>

[<span data-ttu-id="66be2-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="66be2-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="66be2-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="66be2-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


