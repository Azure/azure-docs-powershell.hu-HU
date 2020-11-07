---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: ac17206073ff9992c8569da884d1d53c385bccbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671134"
---
# <span data-ttu-id="5c13e-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="5c13e-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="5c13e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c13e-102">SYNOPSIS</span></span>
<span data-ttu-id="5c13e-103">Az Azure Data Factory adatkészletének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="5c13e-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="5c13e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c13e-104">SYNTAX</span></span>

### <span data-ttu-id="5c13e-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c13e-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c13e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5c13e-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c13e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c13e-107">DESCRIPTION</span></span>
<span data-ttu-id="5c13e-108">A **Remove-AzDataFactoryDataset** parancsmag eltávolítja az adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="5c13e-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="5c13e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5c13e-109">EXAMPLES</span></span>

### <span data-ttu-id="5c13e-110">1. példa: adatkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5c13e-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5c13e-111">Ez a parancs eltávolítja a DAWikiAggregatedData nevű adatkészletet az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="5c13e-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="5c13e-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="5c13e-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="5c13e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c13e-113">PARAMETERS</span></span>

### <span data-ttu-id="5c13e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13e-114">-DataFactory</span></span>
<span data-ttu-id="5c13e-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5c13e-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5c13e-116">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c13e-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c13e-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5c13e-117">-DataFactoryName</span></span>
<span data-ttu-id="5c13e-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c13e-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5c13e-119">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c13e-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5c13e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c13e-120">-DefaultProfile</span></span>
<span data-ttu-id="5c13e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5c13e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c13e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5c13e-122">-Force</span></span>
<span data-ttu-id="5c13e-123">Jelzi, hogy ez a parancsmag eltávolítja az adatkészletet, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5c13e-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="5c13e-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5c13e-124">-Name</span></span>
<span data-ttu-id="5c13e-125">Az eltávolítandó adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c13e-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c13e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c13e-126">-ResourceGroupName</span></span>
<span data-ttu-id="5c13e-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c13e-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5c13e-128">Ez a parancsmag eltávolítja azt az adatkészletet, amely a paraméter által megadott csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="5c13e-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5c13e-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5c13e-129">-Confirm</span></span>
<span data-ttu-id="5c13e-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5c13e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c13e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c13e-131">-WhatIf</span></span>
<span data-ttu-id="5c13e-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5c13e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c13e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5c13e-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c13e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c13e-134">CommonParameters</span></span>
<span data-ttu-id="5c13e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c13e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c13e-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c13e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c13e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c13e-137">INPUTS</span></span>

### <span data-ttu-id="5c13e-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13e-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="5c13e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5c13e-139">System.String</span></span>

## <span data-ttu-id="5c13e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c13e-140">OUTPUTS</span></span>

### <span data-ttu-id="5c13e-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="5c13e-141">System.Void</span></span>

## <span data-ttu-id="5c13e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c13e-142">NOTES</span></span>
* <span data-ttu-id="5c13e-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="5c13e-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5c13e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c13e-144">RELATED LINKS</span></span>

[<span data-ttu-id="5c13e-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="5c13e-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="5c13e-146">Új – AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="5c13e-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


