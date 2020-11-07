---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847306"
---
# <span data-ttu-id="22d25-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="22d25-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="22d25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22d25-102">SYNOPSIS</span></span>
<span data-ttu-id="22d25-103">Információkat kaphat az adatáramlással kapcsolatos adatokról.</span><span class="sxs-lookup"><span data-stu-id="22d25-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="22d25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22d25-104">SYNTAX</span></span>

### <span data-ttu-id="22d25-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22d25-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d25-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="22d25-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d25-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="22d25-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22d25-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="22d25-108">DESCRIPTION</span></span>
<span data-ttu-id="22d25-109">Az Get-AzDataFactoryV2DataFlow parancsmag információkat kap az Azure Data Factory adatforgalmáról.</span><span class="sxs-lookup"><span data-stu-id="22d25-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="22d25-110">Ha megadja az adatfolyam nevét, ez a parancsmag információkat kap az adatáramlásról.</span><span class="sxs-lookup"><span data-stu-id="22d25-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="22d25-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatfeldolgozó adatforgalmáról.</span><span class="sxs-lookup"><span data-stu-id="22d25-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="22d25-112">Példák</span><span class="sxs-lookup"><span data-stu-id="22d25-112">EXAMPLES</span></span>
### <span data-ttu-id="22d25-113">1. példa: adatok beolvasása az összes adatforgalomról</span><span class="sxs-lookup"><span data-stu-id="22d25-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="22d25-114">Ez a parancs információt kap a WikiADF nevű adatfeldolgozóban található összes adatforgalomról.</span><span class="sxs-lookup"><span data-stu-id="22d25-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="22d25-115">2. példa: adatok beolvasása egy adott adatfolyamról</span><span class="sxs-lookup"><span data-stu-id="22d25-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="22d25-116">Ez a parancs információt kap a dataflow1 nevű adatforgalomról az WikiADF nevű Data Factory nevű adatforgalomról.</span><span class="sxs-lookup"><span data-stu-id="22d25-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="22d25-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22d25-117">PARAMETERS</span></span>

### <span data-ttu-id="22d25-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="22d25-118">-DataFactory</span></span>
<span data-ttu-id="22d25-119">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="22d25-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22d25-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="22d25-120">-DataFactoryName</span></span>
<span data-ttu-id="22d25-121">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="22d25-121">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d25-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d25-122">-DefaultProfile</span></span>
<span data-ttu-id="22d25-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22d25-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d25-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="22d25-124">-Name</span></span>
<span data-ttu-id="22d25-125">Az adatforgalom neve.</span><span class="sxs-lookup"><span data-stu-id="22d25-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d25-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d25-126">-ResourceGroupName</span></span>
<span data-ttu-id="22d25-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="22d25-127">The resource group name.</span></span>

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

### <span data-ttu-id="22d25-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22d25-128">-ResourceId</span></span>
<span data-ttu-id="22d25-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="22d25-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d25-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d25-130">CommonParameters</span></span>
<span data-ttu-id="22d25-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22d25-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d25-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="22d25-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d25-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22d25-133">INPUTS</span></span>

### <span data-ttu-id="22d25-134">System. String</span><span class="sxs-lookup"><span data-stu-id="22d25-134">System.String</span></span>

### <span data-ttu-id="22d25-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="22d25-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="22d25-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22d25-136">OUTPUTS</span></span>

### <span data-ttu-id="22d25-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="22d25-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="22d25-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22d25-138">NOTES</span></span>
<span data-ttu-id="22d25-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="22d25-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="22d25-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22d25-140">RELATED LINKS</span></span>

[<span data-ttu-id="22d25-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="22d25-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="22d25-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="22d25-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)