---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 7bd25d444a4277e2aa423026be551fab1c5f360e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397866"
---
# <span data-ttu-id="88510-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="88510-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="88510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88510-102">SYNOPSIS</span></span>
<span data-ttu-id="88510-103">Információkat kap a Data Factoryban folyó adatfolyamok adatairól.</span><span class="sxs-lookup"><span data-stu-id="88510-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="88510-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="88510-104">SYNTAX</span></span>

### <span data-ttu-id="88510-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88510-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88510-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="88510-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88510-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="88510-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88510-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="88510-108">DESCRIPTION</span></span>
<span data-ttu-id="88510-109">A Get-AzDataFactoryV2DataFlow parancsmag információkat kap az Azure Data Factorybeli adatfolyamokkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="88510-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="88510-110">Ha megadja egy adatfolyam nevét, ez a parancsmag információt kap az adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="88510-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="88510-111">Ha nem ad meg nevet, ez a parancsmag információt kap az adat factoryban található összes adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="88510-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="88510-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="88510-112">EXAMPLES</span></span>
### <span data-ttu-id="88510-113">1. példa: Információ az összes adatfolyamról</span><span class="sxs-lookup"><span data-stu-id="88510-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="88510-114">Ez a parancs információkat kap a WikiADF nevű adat factoryban folyó összes adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="88510-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="88510-115">2. példa: Információ lekérte egy adott adatfolyamról</span><span class="sxs-lookup"><span data-stu-id="88510-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="88510-116">Ez a parancs információkat kap a WikiADF nevű adat factory dataflow1 nevű adatfolyamról.</span><span class="sxs-lookup"><span data-stu-id="88510-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="88510-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88510-117">PARAMETERS</span></span>

### <span data-ttu-id="88510-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="88510-118">-DataFactory</span></span>
<span data-ttu-id="88510-119">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="88510-119">The data factory object.</span></span>

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

### <span data-ttu-id="88510-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="88510-120">-DataFactoryName</span></span>
<span data-ttu-id="88510-121">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="88510-121">The data factory name.</span></span>

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

### <span data-ttu-id="88510-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88510-122">-DefaultProfile</span></span>
<span data-ttu-id="88510-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88510-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88510-124">-Name</span><span class="sxs-lookup"><span data-stu-id="88510-124">-Name</span></span>
<span data-ttu-id="88510-125">Az adatfolyam neve.</span><span class="sxs-lookup"><span data-stu-id="88510-125">The data flow name.</span></span>

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

### <span data-ttu-id="88510-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88510-126">-ResourceGroupName</span></span>
<span data-ttu-id="88510-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="88510-127">The resource group name.</span></span>

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

### <span data-ttu-id="88510-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88510-128">-ResourceId</span></span>
<span data-ttu-id="88510-129">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="88510-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="88510-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88510-130">CommonParameters</span></span>
<span data-ttu-id="88510-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88510-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88510-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88510-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88510-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88510-133">INPUTS</span></span>

### <span data-ttu-id="88510-134">System.String</span><span class="sxs-lookup"><span data-stu-id="88510-134">System.String</span></span>

### <span data-ttu-id="88510-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="88510-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="88510-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88510-136">OUTPUTS</span></span>

### <span data-ttu-id="88510-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="88510-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="88510-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="88510-138">NOTES</span></span>
<span data-ttu-id="88510-139">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="88510-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="88510-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88510-140">RELATED LINKS</span></span>


