---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 85e9e96db366adcb30494ac22e7d1b73bbff9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493553"
---
# <span data-ttu-id="67465-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="67465-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="67465-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67465-102">SYNOPSIS</span></span>
<span data-ttu-id="67465-103">Az Azure Data Factory adatkészletének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="67465-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67465-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67465-104">SYNTAX</span></span>

### <span data-ttu-id="67465-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67465-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67465-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="67465-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67465-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="67465-107">DESCRIPTION</span></span>
<span data-ttu-id="67465-108">A **Remove-AzureRmDataFactoryDataset** parancsmag eltávolítja az adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="67465-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="67465-109">Példák</span><span class="sxs-lookup"><span data-stu-id="67465-109">EXAMPLES</span></span>

### <span data-ttu-id="67465-110">1. példa: adatkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="67465-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="67465-111">Ez a parancs eltávolítja a DAWikiAggregatedData nevű adatkészletet az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="67465-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="67465-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="67465-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="67465-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67465-113">PARAMETERS</span></span>

### <span data-ttu-id="67465-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="67465-114">-DataFactory</span></span>
<span data-ttu-id="67465-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="67465-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="67465-116">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="67465-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="67465-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="67465-117">-DataFactoryName</span></span>
<span data-ttu-id="67465-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67465-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="67465-119">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="67465-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="67465-120">-Force</span><span class="sxs-lookup"><span data-stu-id="67465-120">-Force</span></span>
<span data-ttu-id="67465-121">Jelzi, hogy ez a parancsmag eltávolítja az adatkészletet, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67465-121">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="67465-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="67465-122">-Name</span></span>
<span data-ttu-id="67465-123">Az eltávolítandó adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67465-123">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="67465-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67465-124">-ResourceGroupName</span></span>
<span data-ttu-id="67465-125">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67465-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="67465-126">Ez a parancsmag eltávolítja azt az adatkészletet, amely a paraméter által megadott csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="67465-126">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="67465-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="67465-127">-Confirm</span></span>
<span data-ttu-id="67465-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67465-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67465-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67465-129">-WhatIf</span></span>
<span data-ttu-id="67465-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="67465-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67465-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67465-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67465-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67465-132">-DefaultProfile</span></span>
<span data-ttu-id="67465-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67465-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67465-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67465-134">CommonParameters</span></span>
<span data-ttu-id="67465-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67465-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67465-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67465-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67465-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67465-137">INPUTS</span></span>

## <span data-ttu-id="67465-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67465-138">OUTPUTS</span></span>

### <span data-ttu-id="67465-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67465-139">System.Boolean</span></span>

## <span data-ttu-id="67465-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67465-140">NOTES</span></span>
* <span data-ttu-id="67465-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="67465-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="67465-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67465-142">RELATED LINKS</span></span>

[<span data-ttu-id="67465-143">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="67465-143">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="67465-144">Új – AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="67465-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


