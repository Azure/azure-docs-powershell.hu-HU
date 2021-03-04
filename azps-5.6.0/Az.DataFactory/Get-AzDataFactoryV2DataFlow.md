---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 4838ba48d12fa3a4b1fd7d129e63e0a643357a78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930258"
---
# <span data-ttu-id="f253f-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="f253f-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="f253f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f253f-102">SYNOPSIS</span></span>
<span data-ttu-id="f253f-103">Információkat kap a Data Factoryban folyó adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="f253f-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="f253f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f253f-104">SYNTAX</span></span>

### <span data-ttu-id="f253f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f253f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f253f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f253f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f253f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f253f-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f253f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f253f-108">DESCRIPTION</span></span>
<span data-ttu-id="f253f-109">A Get-AzDataFactoryV2DataFlow parancsmag információkat kap az Azure Data Factorybeli adatfolyamokkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="f253f-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="f253f-110">Ha megadja egy adatfolyam nevét, ez a parancsmag információt kap az adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="f253f-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="f253f-111">Ha nem ad meg nevet, ez a parancsmag információt kap az adatüzemben folyó összes adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="f253f-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="f253f-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f253f-112">EXAMPLES</span></span>
### <span data-ttu-id="f253f-113">1. példa: Információ az összes adatfolyamról</span><span class="sxs-lookup"><span data-stu-id="f253f-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="f253f-114">Ez a parancs információkat kap a WikiADF nevű adat factoryban folyó összes adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="f253f-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="f253f-115">2. példa: Információ lekérte egy adott adatfolyamról</span><span class="sxs-lookup"><span data-stu-id="f253f-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="f253f-116">Ez a parancs információkat kap a WikiADF nevű dataflow1 nevű adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="f253f-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="f253f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f253f-117">PARAMETERS</span></span>

### <span data-ttu-id="f253f-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f253f-118">-DataFactory</span></span>
<span data-ttu-id="f253f-119">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="f253f-119">The data factory object.</span></span>

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

### <span data-ttu-id="f253f-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f253f-120">-DataFactoryName</span></span>
<span data-ttu-id="f253f-121">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="f253f-121">The data factory name.</span></span>

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

### <span data-ttu-id="f253f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f253f-122">-DefaultProfile</span></span>
<span data-ttu-id="f253f-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f253f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f253f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f253f-124">-Name</span></span>
<span data-ttu-id="f253f-125">Az adatfolyam neve.</span><span class="sxs-lookup"><span data-stu-id="f253f-125">The data flow name.</span></span>

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

### <span data-ttu-id="f253f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f253f-126">-ResourceGroupName</span></span>
<span data-ttu-id="f253f-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f253f-127">The resource group name.</span></span>

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

### <span data-ttu-id="f253f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f253f-128">-ResourceId</span></span>
<span data-ttu-id="f253f-129">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="f253f-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f253f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f253f-130">CommonParameters</span></span>
<span data-ttu-id="f253f-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f253f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f253f-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f253f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f253f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f253f-133">INPUTS</span></span>

### <span data-ttu-id="f253f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f253f-134">System.String</span></span>

### <span data-ttu-id="f253f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f253f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f253f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f253f-136">OUTPUTS</span></span>

### <span data-ttu-id="f253f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="f253f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="f253f-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f253f-138">NOTES</span></span>
<span data-ttu-id="f253f-139">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="f253f-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f253f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f253f-140">RELATED LINKS</span></span>

[<span data-ttu-id="f253f-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="f253f-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="f253f-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="f253f-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)