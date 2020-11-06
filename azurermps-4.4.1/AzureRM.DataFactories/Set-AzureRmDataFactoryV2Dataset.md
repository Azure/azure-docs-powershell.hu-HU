---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 4254a243894893e58c1c59ea19a8953ddcc8f101
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493545"
---
# <span data-ttu-id="2597f-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2597f-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="2597f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2597f-102">SYNOPSIS</span></span>
<span data-ttu-id="2597f-103">Adatkészletet hoz létre az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="2597f-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2597f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2597f-104">SYNTAX</span></span>

### <span data-ttu-id="2597f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2597f-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2597f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2597f-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2597f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2597f-107">DESCRIPTION</span></span>
<span data-ttu-id="2597f-108">Az Set-AzureRmDataFactoryV2Dataset parancsmag létrehoz egy adatkészletet az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="2597f-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="2597f-109">Ha olyan adatkészletet ad meg, amely már létezik, ez a parancsmag az adatkészlet visszavonása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2597f-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="2597f-110">Ha az erő paramétert adja meg, a parancsmag a létező adatkészletet megerősítés nélkül cseréli le.</span><span class="sxs-lookup"><span data-stu-id="2597f-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="2597f-111">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="2597f-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="2597f-112">Ha az adatfeldolgozóban már létezik azonos nevű adatkészlet, ez a parancsmag arra kéri, hogy erősítse meg, hogy felülírja-e a meglévő adatkészletet az új adatkészlettel.</span><span class="sxs-lookup"><span data-stu-id="2597f-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="2597f-113">Ha a meglévő adatkészlet felülírásának megerősítését hagyja jóvá, az adatkészlet-definíciót is lecseréli a program.</span><span class="sxs-lookup"><span data-stu-id="2597f-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="2597f-114">Példák</span><span class="sxs-lookup"><span data-stu-id="2597f-114">EXAMPLES</span></span>

### <span data-ttu-id="2597f-115">1. példa: adatkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="2597f-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="2597f-116">A parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet a WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="2597f-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="2597f-117">A parancs az adatkészletet az DAWikipediaClickEvents.jsfájlon lévő adatokra alapozja.</span><span class="sxs-lookup"><span data-stu-id="2597f-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="2597f-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2597f-118">PARAMETERS</span></span>

### <span data-ttu-id="2597f-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2597f-119">-Confirm</span></span>
<span data-ttu-id="2597f-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2597f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2597f-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2597f-121">-DataFactoryName</span></span>
<span data-ttu-id="2597f-122">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2597f-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2597f-123">Ez a parancsmag létrehoz egy adatkészletet az adatgyárban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="2597f-123">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2597f-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="2597f-124">-DefinitionFile</span></span>
<span data-ttu-id="2597f-125">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="2597f-125">The JSON file path.</span></span>

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

### <span data-ttu-id="2597f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2597f-126">-Force</span></span>
<span data-ttu-id="2597f-127">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2597f-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2597f-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2597f-128">-Name</span></span>
<span data-ttu-id="2597f-129">A létrehozandó adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2597f-129">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2597f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2597f-130">-ResourceGroupName</span></span>
<span data-ttu-id="2597f-131">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2597f-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2597f-132">Ez a parancsmag létrehoz egy adatkészletet abban a csoportban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="2597f-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2597f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2597f-133">-ResourceId</span></span>
<span data-ttu-id="2597f-134">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="2597f-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2597f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2597f-135">-WhatIf</span></span>
<span data-ttu-id="2597f-136">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2597f-136">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2597f-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2597f-137">-DefaultProfile</span></span>
<span data-ttu-id="2597f-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2597f-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2597f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2597f-139">CommonParameters</span></span>
<span data-ttu-id="2597f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2597f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2597f-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2597f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2597f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2597f-142">INPUTS</span></span>

### <span data-ttu-id="2597f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2597f-143">System.String</span></span>

## <span data-ttu-id="2597f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2597f-144">OUTPUTS</span></span>

### <span data-ttu-id="2597f-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="2597f-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="2597f-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2597f-146">NOTES</span></span>
<span data-ttu-id="2597f-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="2597f-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2597f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2597f-148">RELATED LINKS</span></span>

[<span data-ttu-id="2597f-149">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2597f-149">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="2597f-150">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2597f-150">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
