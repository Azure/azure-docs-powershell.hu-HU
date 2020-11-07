---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: f977344f2beabe8352a7417130063c3e9d4d3e1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680898"
---
# <span data-ttu-id="07061-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="07061-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="07061-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07061-102">SYNOPSIS</span></span>
<span data-ttu-id="07061-103">Az adattárolók vagy a Felhőbeli szolgáltatások összekapcsolása az adatfeldolgozó szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="07061-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07061-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07061-104">SYNTAX</span></span>

### <span data-ttu-id="07061-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07061-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="07061-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="07061-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="07061-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="07061-107">DESCRIPTION</span></span>
<span data-ttu-id="07061-108">Az Set-AzureRmDataFactoryV2LinkedService parancsmag az Azure Data Factory adattárolóhoz vagy egy felhőalapú szolgáltatáshoz csatolja az adattárolót.</span><span class="sxs-lookup"><span data-stu-id="07061-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="07061-109">Ha már létezik egy olyan kapcsolt szolgáltatás neve, amely már létezik, ez a parancsmag a kapcsolt szolgáltatás cseréje előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07061-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="07061-110">Ha az erő paramétert adja meg, a parancsmag megerősítés nélkül felülírja a meglévő kapcsolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="07061-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="07061-111">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="07061-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="07061-112">Példák</span><span class="sxs-lookup"><span data-stu-id="07061-112">EXAMPLES</span></span>

### <span data-ttu-id="07061-113">1. példa: kapcsolt szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="07061-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

```

<span data-ttu-id="07061-114">Ez a parancs létrehoz egy LinkedServiceCuratedWikiData nevű hivatkozást a WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="07061-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="07061-115">Ez a hivatkozás egy, a fájlban megadott Azure Blob-tárolóhoz csatolja a WikiADF nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="07061-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="07061-116">A parancs a csővezeték-kezelő használatával átadja az eredményt az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="07061-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="07061-117">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="07061-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="07061-118">További információt a Get-Help formázása – lista című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="07061-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="07061-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07061-119">PARAMETERS</span></span>

### <span data-ttu-id="07061-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07061-120">-Confirm</span></span>
<span data-ttu-id="07061-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07061-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07061-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="07061-122">-DataFactoryName</span></span>
<span data-ttu-id="07061-123">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07061-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="07061-124">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást az adatgyárhoz, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="07061-124">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07061-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="07061-125">-DefinitionFile</span></span>
<span data-ttu-id="07061-126">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="07061-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07061-127">-Force</span><span class="sxs-lookup"><span data-stu-id="07061-127">-Force</span></span>
<span data-ttu-id="07061-128">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="07061-128">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07061-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="07061-129">-Name</span></span>
<span data-ttu-id="07061-130">A létrehozandó kapcsolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07061-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07061-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07061-131">-ResourceGroupName</span></span>
<span data-ttu-id="07061-132">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07061-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="07061-133">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást a csoporthoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="07061-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07061-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07061-134">-ResourceId</span></span>
<span data-ttu-id="07061-135">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="07061-135">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07061-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07061-136">-WhatIf</span></span>
<span data-ttu-id="07061-137">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="07061-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="07061-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07061-138">INPUTS</span></span>

### <span data-ttu-id="07061-139">System. String</span><span class="sxs-lookup"><span data-stu-id="07061-139">System.String</span></span>


## <span data-ttu-id="07061-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07061-140">OUTPUTS</span></span>

### <span data-ttu-id="07061-141">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="07061-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>


## <span data-ttu-id="07061-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07061-142">NOTES</span></span>
<span data-ttu-id="07061-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="07061-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="07061-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07061-144">RELATED LINKS</span></span>
[<span data-ttu-id="07061-145">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="07061-145">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="07061-146">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="07061-146">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
