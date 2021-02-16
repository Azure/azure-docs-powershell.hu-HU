---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5af8053f3d504cfc3eb28a2f8ad71f83492f0e3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204462"
---
# <span data-ttu-id="8d8b1-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8d8b1-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="8d8b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8b1-103">Információkat kap a Data Factoryban található adatkészletekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="8d8b1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d8b1-104">SYNTAX</span></span>

### <span data-ttu-id="8d8b1-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d8b1-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8b1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8d8b1-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8b1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d8b1-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d8b1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d8b1-108">DESCRIPTION</span></span>
<span data-ttu-id="8d8b1-109">A Get-AzDataFactoryV2Dataset parancsmag információkat kap az Azure Data Factory adatkészleteiről.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="8d8b1-110">Ha megadja egy adatkészlet nevét, ez a parancsmag információt kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="8d8b1-111">Ha nem ad meg nevet, ez a parancsmag információt kap az adatüzemben található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="8d8b1-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d8b1-112">EXAMPLES</span></span>

### <span data-ttu-id="8d8b1-113">1. példa: Információ az összes adatkészletről</span><span class="sxs-lookup"><span data-stu-id="8d8b1-113">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="8d8b1-114">Ez a parancs információkat kap a WikiADF nevű adat factoryban található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="8d8b1-115">2. példa: Információ lekérte egy adott adatkészletről</span><span class="sxs-lookup"><span data-stu-id="8d8b1-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="8d8b1-116">Ez a parancs információkat kap a DAWikipediaClickEvents nevű adatkészletről a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="8d8b1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d8b1-117">PARAMETERS</span></span>

### <span data-ttu-id="8d8b1-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d8b1-118">-DataFactory</span></span>
<span data-ttu-id="8d8b1-119">EGY PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="8d8b1-120">Ez a parancsmag a paraméter által megadott adat factoryhoz tartozó adatkészleteket kap.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d8b1-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8d8b1-121">-DataFactoryName</span></span>
<span data-ttu-id="8d8b1-122">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8d8b1-123">Ez a parancsmag a paraméter által megadott adat factoryhoz tartozó adatkészleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d8b1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8b1-124">-DefaultProfile</span></span>
<span data-ttu-id="8d8b1-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d8b1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8d8b1-126">-Name</span></span>
<span data-ttu-id="8d8b1-127">Annak az adatkészletnek a nevét adja meg, amelyről információt kell kapni.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d8b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d8b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="8d8b1-129">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8d8b1-130">Ez a parancsmag a paraméter által megadott csoporthoz tartozó adatkészleteket kapja.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d8b1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d8b1-131">-ResourceId</span></span>
<span data-ttu-id="8d8b1-132">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8d8b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8b1-133">CommonParameters</span></span>
<span data-ttu-id="8d8b1-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8b1-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d8b1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8b1-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d8b1-136">INPUTS</span></span>

### <span data-ttu-id="8d8b1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8d8b1-137">System.String</span></span>

### <span data-ttu-id="8d8b1-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8d8b1-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8d8b1-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d8b1-139">OUTPUTS</span></span>

### <span data-ttu-id="8d8b1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="8d8b1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="8d8b1-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d8b1-141">NOTES</span></span>
<span data-ttu-id="8d8b1-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="8d8b1-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8d8b1-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d8b1-143">RELATED LINKS</span></span>

[<span data-ttu-id="8d8b1-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8d8b1-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="8d8b1-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8d8b1-145">Remove-AzDataFactoryV2Dataset</span></span>]()
