---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298376"
---
# <span data-ttu-id="b4218-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="b4218-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="b4218-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4218-102">SYNOPSIS</span></span>
<span data-ttu-id="b4218-103">Az Azure Data Factory adatkészletének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b4218-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="b4218-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4218-104">SYNTAX</span></span>

### <span data-ttu-id="b4218-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4218-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4218-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b4218-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4218-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4218-107">DESCRIPTION</span></span>
<span data-ttu-id="b4218-108">A **Remove-AzDataFactoryDataset** parancsmag eltávolítja az adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="b4218-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="b4218-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b4218-109">EXAMPLES</span></span>

### <span data-ttu-id="b4218-110">1. példa: adatkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b4218-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="b4218-111">Ez a parancs eltávolítja a DAWikiAggregatedData nevű adatkészletet az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="b4218-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="b4218-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b4218-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="b4218-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4218-113">PARAMETERS</span></span>

### <span data-ttu-id="b4218-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4218-114">-DataFactory</span></span>
<span data-ttu-id="b4218-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b4218-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b4218-116">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4218-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4218-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b4218-117">-DataFactoryName</span></span>
<span data-ttu-id="b4218-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4218-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b4218-119">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4218-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4218-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4218-120">-DefaultProfile</span></span>
<span data-ttu-id="b4218-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b4218-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4218-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b4218-122">-Force</span></span>
<span data-ttu-id="b4218-123">Jelzi, hogy ez a parancsmag eltávolítja az adatkészletet, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4218-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b4218-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4218-124">-Name</span></span>
<span data-ttu-id="b4218-125">Az eltávolítandó adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4218-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="b4218-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4218-126">-ResourceGroupName</span></span>
<span data-ttu-id="b4218-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4218-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b4218-128">Ez a parancsmag eltávolítja azt az adatkészletet, amely a paraméter által megadott csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="b4218-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4218-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4218-129">-Confirm</span></span>
<span data-ttu-id="b4218-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4218-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4218-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4218-131">-WhatIf</span></span>
<span data-ttu-id="b4218-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4218-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4218-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4218-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4218-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4218-134">CommonParameters</span></span>
<span data-ttu-id="b4218-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4218-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4218-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4218-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4218-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4218-137">INPUTS</span></span>

### <span data-ttu-id="b4218-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b4218-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b4218-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4218-139">System.String</span></span>

## <span data-ttu-id="b4218-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4218-140">OUTPUTS</span></span>

### <span data-ttu-id="b4218-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="b4218-141">System.Void</span></span>

## <span data-ttu-id="b4218-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4218-142">NOTES</span></span>
* <span data-ttu-id="b4218-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="b4218-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b4218-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4218-144">RELATED LINKS</span></span>

[<span data-ttu-id="b4218-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="b4218-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="b4218-146">Új – AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="b4218-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


