---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 44439d49fc89f00abaef904e80112d076121890f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407437"
---
# <span data-ttu-id="9e433-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="9e433-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="9e433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e433-102">SYNOPSIS</span></span>
<span data-ttu-id="9e433-103">Adatfolyamot hoz létre a Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="9e433-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="9e433-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e433-104">SYNTAX</span></span>

### <span data-ttu-id="9e433-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e433-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e433-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e433-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e433-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e433-107">DESCRIPTION</span></span>
<span data-ttu-id="9e433-108">A Set-AzDataFactoryV2DataFlow parancsmag adatfolyamot hoz létre, vagy frissíti a meglévő adatfolyamot az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="9e433-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="9e433-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e433-109">EXAMPLES</span></span>

### <span data-ttu-id="9e433-110">1. példa: Adatfolyam létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e433-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="9e433-111">Ezzel a paranccsal a WikiADF nevű adatüzemben létrehozza a TaxiDemo1 nevű adatfolyamot.</span><span class="sxs-lookup"><span data-stu-id="9e433-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="9e433-112">A parancs az adatfolyamot a fájlon TaxiDemo1.jsadatok alapján.</span><span class="sxs-lookup"><span data-stu-id="9e433-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="9e433-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e433-113">PARAMETERS</span></span>

### <span data-ttu-id="9e433-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9e433-114">-DataFactoryName</span></span>
<span data-ttu-id="9e433-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="9e433-115">The data factory name.</span></span>

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

### <span data-ttu-id="9e433-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e433-116">-DefaultProfile</span></span>
<span data-ttu-id="9e433-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e433-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e433-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9e433-118">-DefinitionFile</span></span>
<span data-ttu-id="9e433-119">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9e433-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e433-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9e433-120">-Force</span></span>
<span data-ttu-id="9e433-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e433-121">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e433-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9e433-122">-Name</span></span>
<span data-ttu-id="9e433-123">Az adatfolyam neve.</span><span class="sxs-lookup"><span data-stu-id="9e433-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e433-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e433-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e433-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9e433-125">The resource group name.</span></span>

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

### <span data-ttu-id="9e433-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e433-126">-ResourceId</span></span>
<span data-ttu-id="9e433-127">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="9e433-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9e433-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e433-128">-Confirm</span></span>
<span data-ttu-id="9e433-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9e433-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e433-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e433-130">-WhatIf</span></span>
<span data-ttu-id="9e433-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9e433-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e433-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e433-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e433-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e433-133">CommonParameters</span></span>
<span data-ttu-id="9e433-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e433-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e433-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e433-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e433-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e433-136">INPUTS</span></span>

### <span data-ttu-id="9e433-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9e433-137">System.String</span></span>

## <span data-ttu-id="9e433-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e433-138">OUTPUTS</span></span>

### <span data-ttu-id="9e433-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="9e433-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="9e433-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e433-140">NOTES</span></span>
<span data-ttu-id="9e433-141">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="9e433-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9e433-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e433-142">RELATED LINKS</span></span>


