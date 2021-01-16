---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327315"
---
# <span data-ttu-id="75f52-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="75f52-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="75f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f52-102">SYNOPSIS</span></span>
<span data-ttu-id="75f52-103">Eltávolít egy adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="75f52-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="75f52-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75f52-104">SYNTAX</span></span>

### <span data-ttu-id="75f52-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75f52-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75f52-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="75f52-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75f52-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75f52-107">DESCRIPTION</span></span>
<span data-ttu-id="75f52-108">A **Remove-AzDataFactoryDataset** parancsmag eltávolít egy adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="75f52-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="75f52-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75f52-109">EXAMPLES</span></span>

### <span data-ttu-id="75f52-110">1. példa: Adatkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="75f52-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="75f52-111">Ez a parancs eltávolítja a DAWikiAggregatedData nevű adatkészletet a WikiADF nevű adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="75f52-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="75f52-112">A parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="75f52-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="75f52-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75f52-113">PARAMETERS</span></span>

### <span data-ttu-id="75f52-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="75f52-114">-DataFactory</span></span>
<span data-ttu-id="75f52-115">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="75f52-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="75f52-116">Ez a parancsmag eltávolít egy adatkészletet a paraméter által megadott adatüzemmódból.</span><span class="sxs-lookup"><span data-stu-id="75f52-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="75f52-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="75f52-117">-DataFactoryName</span></span>
<span data-ttu-id="75f52-118">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75f52-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="75f52-119">Ez a parancsmag eltávolít egy adatkészletet a paraméter által megadott adatüzemmódból.</span><span class="sxs-lookup"><span data-stu-id="75f52-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="75f52-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f52-120">-DefaultProfile</span></span>
<span data-ttu-id="75f52-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="75f52-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75f52-122">-Force</span><span class="sxs-lookup"><span data-stu-id="75f52-122">-Force</span></span>
<span data-ttu-id="75f52-123">Azt jelzi, hogy ez a parancsmag a megerősítés kérése nélkül eltávolítja az adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="75f52-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="75f52-124">-Name</span><span class="sxs-lookup"><span data-stu-id="75f52-124">-Name</span></span>
<span data-ttu-id="75f52-125">Az eltávolítható adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75f52-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="75f52-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f52-126">-ResourceGroupName</span></span>
<span data-ttu-id="75f52-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75f52-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="75f52-128">Ez a parancsmag eltávolít egy adatkészletet a paraméter által megadott csoportból.</span><span class="sxs-lookup"><span data-stu-id="75f52-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="75f52-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75f52-129">-Confirm</span></span>
<span data-ttu-id="75f52-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="75f52-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75f52-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75f52-131">-WhatIf</span></span>
<span data-ttu-id="75f52-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="75f52-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75f52-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75f52-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75f52-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f52-134">CommonParameters</span></span>
<span data-ttu-id="75f52-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f52-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f52-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f52-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f52-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75f52-137">INPUTS</span></span>

### <span data-ttu-id="75f52-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="75f52-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="75f52-139">System.String</span><span class="sxs-lookup"><span data-stu-id="75f52-139">System.String</span></span>

## <span data-ttu-id="75f52-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75f52-140">OUTPUTS</span></span>

### <span data-ttu-id="75f52-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="75f52-141">System.Void</span></span>

## <span data-ttu-id="75f52-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75f52-142">NOTES</span></span>
* <span data-ttu-id="75f52-143">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="75f52-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="75f52-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75f52-144">RELATED LINKS</span></span>

[<span data-ttu-id="75f52-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="75f52-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="75f52-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="75f52-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


