---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 6827fb627a3d393c8971886cee869c330f7d4099
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942873"
---
# <span data-ttu-id="aaa10-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="aaa10-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="aaa10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaa10-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa10-103">Adatfolyamot hoz létre a Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="aaa10-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="aaa10-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aaa10-104">SYNTAX</span></span>

### <span data-ttu-id="aaa10-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aaa10-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aaa10-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aaa10-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaa10-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aaa10-107">DESCRIPTION</span></span>
<span data-ttu-id="aaa10-108">A Set-AzDataFactoryV2DataFlow parancsmag adatfolyamot hoz létre, vagy frissíti a meglévő adatfolyamot az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="aaa10-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="aaa10-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aaa10-109">EXAMPLES</span></span>

### <span data-ttu-id="aaa10-110">1. példa: Adatfolyam létrehozása</span><span class="sxs-lookup"><span data-stu-id="aaa10-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="aaa10-111">Ezzel a paranccsal a WikiADF nevű adatüzemben létrehozza a TaxiDemo1 nevű adatfolyamot.</span><span class="sxs-lookup"><span data-stu-id="aaa10-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="aaa10-112">A parancs az adatfolyamot a fájlon TaxiDemo1.jsadatokon.</span><span class="sxs-lookup"><span data-stu-id="aaa10-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="aaa10-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaa10-113">PARAMETERS</span></span>

### <span data-ttu-id="aaa10-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="aaa10-114">-DataFactoryName</span></span>
<span data-ttu-id="aaa10-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="aaa10-115">The data factory name.</span></span>

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

### <span data-ttu-id="aaa10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa10-116">-DefaultProfile</span></span>
<span data-ttu-id="aaa10-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aaa10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaa10-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="aaa10-118">-DefinitionFile</span></span>
<span data-ttu-id="aaa10-119">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="aaa10-119">The JSON file path.</span></span>

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

### <span data-ttu-id="aaa10-120">-Force</span><span class="sxs-lookup"><span data-stu-id="aaa10-120">-Force</span></span>
<span data-ttu-id="aaa10-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aaa10-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="aaa10-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aaa10-122">-Name</span></span>
<span data-ttu-id="aaa10-123">Az adatfolyam neve.</span><span class="sxs-lookup"><span data-stu-id="aaa10-123">The data flow name.</span></span>

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

### <span data-ttu-id="aaa10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaa10-124">-ResourceGroupName</span></span>
<span data-ttu-id="aaa10-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aaa10-125">The resource group name.</span></span>

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

### <span data-ttu-id="aaa10-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaa10-126">-ResourceId</span></span>
<span data-ttu-id="aaa10-127">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="aaa10-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="aaa10-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaa10-128">-Confirm</span></span>
<span data-ttu-id="aaa10-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aaa10-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaa10-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaa10-130">-WhatIf</span></span>
<span data-ttu-id="aaa10-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aaa10-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaa10-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aaa10-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaa10-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa10-133">CommonParameters</span></span>
<span data-ttu-id="aaa10-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa10-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa10-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aaa10-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa10-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaa10-136">INPUTS</span></span>

### <span data-ttu-id="aaa10-137">System.String</span><span class="sxs-lookup"><span data-stu-id="aaa10-137">System.String</span></span>

## <span data-ttu-id="aaa10-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaa10-138">OUTPUTS</span></span>

### <span data-ttu-id="aaa10-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="aaa10-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="aaa10-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aaa10-140">NOTES</span></span>
<span data-ttu-id="aaa10-141">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="aaa10-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="aaa10-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aaa10-142">RELATED LINKS</span></span>

[<span data-ttu-id="aaa10-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="aaa10-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="aaa10-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="aaa10-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
