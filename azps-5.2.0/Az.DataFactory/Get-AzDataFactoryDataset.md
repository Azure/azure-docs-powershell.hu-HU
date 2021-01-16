---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354593"
---
# <span data-ttu-id="9f194-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="9f194-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="9f194-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f194-102">SYNOPSIS</span></span>
<span data-ttu-id="9f194-103">Információkat kap az Azure Data Factoryban található adatkészletekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="9f194-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="9f194-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f194-104">SYNTAX</span></span>

### <span data-ttu-id="9f194-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f194-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f194-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9f194-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f194-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f194-107">DESCRIPTION</span></span>
<span data-ttu-id="9f194-108">A **Get-AzDataFactoryDataset** parancsmag információkat kap az Azure Data Factory adatkészleteiről.</span><span class="sxs-lookup"><span data-stu-id="9f194-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="9f194-109">Ha megadja egy adatkészlet nevét, ez a parancsmag információt kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="9f194-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="9f194-110">Ha nem ad meg nevet, ez a parancsmag információt kap az adatüzemben található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="9f194-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="9f194-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f194-111">EXAMPLES</span></span>

### <span data-ttu-id="9f194-112">1. példa: Információ az összes adatkészletről</span><span class="sxs-lookup"><span data-stu-id="9f194-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="9f194-113">Ez a parancs információkat kap a WikiADF nevű adat factoryban található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="9f194-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="9f194-114">2. példa: Információ lekérte egy adott adatkészletről</span><span class="sxs-lookup"><span data-stu-id="9f194-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="9f194-115">Ez a parancs információkat kap a DAWikipediaClickEvents nevű adatkészletről a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="9f194-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="9f194-116">3. példa: Adott adatkészlet helyének lekérte</span><span class="sxs-lookup"><span data-stu-id="9f194-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="9f194-117">Ez a parancs információkat kap a DAWikipediaClickEvents nevű adatkészletről a WikiADF nevű adatüzemben,  majd a szokásos pontozott adatokat használja az adatkészlethez társított hely megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="9f194-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="9f194-118">Másik lehetőségként rendelje hozzá a **Get-AzDataFactoryDataset** parancsmag kimenetét egy változóhoz, majd a pont notation segítségével tekintse meg a változóban tárolt adatkészlet-objektummal társított Location tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="9f194-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="9f194-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f194-119">PARAMETERS</span></span>

### <span data-ttu-id="9f194-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9f194-120">-DataFactory</span></span>
<span data-ttu-id="9f194-121">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="9f194-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9f194-122">Ez a parancsmag a paraméter által megadott adat factoryhoz tartozó adatkészleteket kap.</span><span class="sxs-lookup"><span data-stu-id="9f194-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f194-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9f194-123">-DataFactoryName</span></span>
<span data-ttu-id="9f194-124">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f194-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9f194-125">Ez a parancsmag a paraméter által megadott adat factoryhoz tartozó adatkészleteket kap.</span><span class="sxs-lookup"><span data-stu-id="9f194-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f194-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f194-126">-DefaultProfile</span></span>
<span data-ttu-id="9f194-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9f194-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f194-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9f194-128">-Name</span></span>
<span data-ttu-id="9f194-129">Annak az adatkészletnek a nevét adja meg, amelyről a parancsmag információt kap.</span><span class="sxs-lookup"><span data-stu-id="9f194-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f194-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f194-130">-ResourceGroupName</span></span>
<span data-ttu-id="9f194-131">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f194-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9f194-132">Ez a parancsmag a paraméter által megadott csoporthoz tartozó adatkészleteket kapja.</span><span class="sxs-lookup"><span data-stu-id="9f194-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f194-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f194-133">CommonParameters</span></span>
<span data-ttu-id="9f194-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f194-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f194-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f194-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f194-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f194-136">INPUTS</span></span>

### <span data-ttu-id="9f194-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9f194-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9f194-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9f194-138">System.String</span></span>

## <span data-ttu-id="9f194-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f194-139">OUTPUTS</span></span>

### <span data-ttu-id="9f194-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="9f194-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="9f194-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f194-141">NOTES</span></span>
* <span data-ttu-id="9f194-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="9f194-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9f194-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f194-143">RELATED LINKS</span></span>

[<span data-ttu-id="9f194-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="9f194-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="9f194-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="9f194-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


