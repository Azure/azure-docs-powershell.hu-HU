---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181150"
---
# <span data-ttu-id="0f945-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="0f945-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="0f945-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f945-102">SYNOPSIS</span></span>
<span data-ttu-id="0f945-103">Adatáramlást hoz létre az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="0f945-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="0f945-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f945-104">SYNTAX</span></span>

### <span data-ttu-id="0f945-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f945-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f945-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f945-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f945-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f945-107">DESCRIPTION</span></span>
<span data-ttu-id="0f945-108">Az Set-AzDataFactoryV2DataFlow parancsmag adatáramlást hoz létre, vagy egy meglévő adatfolyamot frissít az Azure Data Factory alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="0f945-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="0f945-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0f945-109">EXAMPLES</span></span>

### <span data-ttu-id="0f945-110">1. példa: adatfolyam létrehozása</span><span class="sxs-lookup"><span data-stu-id="0f945-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="0f945-111">Ez a parancs létrehoz egy TaxiDemo1 nevű adatáramlást az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="0f945-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="0f945-112">A parancs az adatáramlást az adatokra a fájl TaxiDemo1.js.</span><span class="sxs-lookup"><span data-stu-id="0f945-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="0f945-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f945-113">PARAMETERS</span></span>

### <span data-ttu-id="0f945-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0f945-114">-DataFactoryName</span></span>
<span data-ttu-id="0f945-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="0f945-115">The data factory name.</span></span>

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

### <span data-ttu-id="0f945-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f945-116">-DefaultProfile</span></span>
<span data-ttu-id="0f945-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f945-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f945-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0f945-118">-DefinitionFile</span></span>
<span data-ttu-id="0f945-119">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="0f945-119">The JSON file path.</span></span>

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

### <span data-ttu-id="0f945-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0f945-120">-Force</span></span>
<span data-ttu-id="0f945-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f945-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0f945-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f945-122">-Name</span></span>
<span data-ttu-id="0f945-123">Az adatforgalom neve.</span><span class="sxs-lookup"><span data-stu-id="0f945-123">The data flow name.</span></span>

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

### <span data-ttu-id="0f945-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f945-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f945-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0f945-125">The resource group name.</span></span>

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

### <span data-ttu-id="0f945-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f945-126">-ResourceId</span></span>
<span data-ttu-id="0f945-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0f945-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0f945-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f945-128">-Confirm</span></span>
<span data-ttu-id="0f945-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f945-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f945-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f945-130">-WhatIf</span></span>
<span data-ttu-id="0f945-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f945-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f945-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f945-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f945-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f945-133">CommonParameters</span></span>
<span data-ttu-id="0f945-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f945-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f945-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0f945-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f945-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f945-136">INPUTS</span></span>

### <span data-ttu-id="0f945-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0f945-137">System.String</span></span>

## <span data-ttu-id="0f945-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f945-138">OUTPUTS</span></span>

### <span data-ttu-id="0f945-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="0f945-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="0f945-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f945-140">NOTES</span></span>
<span data-ttu-id="0f945-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="0f945-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0f945-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f945-142">RELATED LINKS</span></span>

[<span data-ttu-id="0f945-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="0f945-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="0f945-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="0f945-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
