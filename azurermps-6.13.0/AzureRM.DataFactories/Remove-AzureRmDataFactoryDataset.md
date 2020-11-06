---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: d4bb50dcc9e3f04d69131afbb7ac8b4f85e5070c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502975"
---
# <span data-ttu-id="15136-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="15136-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="15136-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15136-102">SYNOPSIS</span></span>
<span data-ttu-id="15136-103">Az Azure Data Factory adatkészletének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="15136-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15136-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15136-104">SYNTAX</span></span>

### <span data-ttu-id="15136-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15136-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15136-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="15136-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15136-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="15136-107">DESCRIPTION</span></span>
<span data-ttu-id="15136-108">A **Remove-AzureRmDataFactoryDataset** parancsmag eltávolítja az adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="15136-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="15136-109">Példák</span><span class="sxs-lookup"><span data-stu-id="15136-109">EXAMPLES</span></span>

### <span data-ttu-id="15136-110">1. példa: adatkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="15136-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="15136-111">Ez a parancs eltávolítja a DAWikiAggregatedData nevű adatkészletet az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="15136-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="15136-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="15136-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="15136-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15136-113">PARAMETERS</span></span>

### <span data-ttu-id="15136-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="15136-114">-DataFactory</span></span>
<span data-ttu-id="15136-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="15136-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="15136-116">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="15136-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="15136-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="15136-117">-DataFactoryName</span></span>
<span data-ttu-id="15136-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15136-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="15136-119">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="15136-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="15136-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15136-120">-DefaultProfile</span></span>
<span data-ttu-id="15136-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="15136-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15136-122">-Force</span><span class="sxs-lookup"><span data-stu-id="15136-122">-Force</span></span>
<span data-ttu-id="15136-123">Jelzi, hogy ez a parancsmag eltávolítja az adatkészletet, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15136-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="15136-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15136-124">-Name</span></span>
<span data-ttu-id="15136-125">Az eltávolítandó adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15136-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="15136-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15136-126">-ResourceGroupName</span></span>
<span data-ttu-id="15136-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15136-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="15136-128">Ez a parancsmag eltávolítja azt az adatkészletet, amely a paraméter által megadott csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="15136-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="15136-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15136-129">-Confirm</span></span>
<span data-ttu-id="15136-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15136-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15136-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15136-131">-WhatIf</span></span>
<span data-ttu-id="15136-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15136-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15136-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15136-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15136-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15136-134">CommonParameters</span></span>
<span data-ttu-id="15136-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15136-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15136-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15136-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15136-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15136-137">INPUTS</span></span>

### <span data-ttu-id="15136-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="15136-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="15136-139">System. String</span><span class="sxs-lookup"><span data-stu-id="15136-139">System.String</span></span>

## <span data-ttu-id="15136-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15136-140">OUTPUTS</span></span>

### <span data-ttu-id="15136-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="15136-141">System.Void</span></span>

## <span data-ttu-id="15136-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15136-142">NOTES</span></span>
* <span data-ttu-id="15136-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="15136-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="15136-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15136-144">RELATED LINKS</span></span>

[<span data-ttu-id="15136-145">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="15136-145">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="15136-146">Új – AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="15136-146">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


