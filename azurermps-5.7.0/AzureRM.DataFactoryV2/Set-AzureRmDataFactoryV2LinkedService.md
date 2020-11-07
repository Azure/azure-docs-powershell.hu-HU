---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 2f7cfba7db5d675a73d21d6cd1814c13a1998ab1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672381"
---
# <span data-ttu-id="0355c-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0355c-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="0355c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0355c-102">SYNOPSIS</span></span>
<span data-ttu-id="0355c-103">Az adattárolók vagy a Felhőbeli szolgáltatások összekapcsolása az adatfeldolgozó szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="0355c-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0355c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0355c-104">SYNTAX</span></span>

### <span data-ttu-id="0355c-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0355c-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0355c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0355c-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0355c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0355c-107">DESCRIPTION</span></span>
<span data-ttu-id="0355c-108">Az Set-AzureRmDataFactoryV2LinkedService parancsmag az Azure Data Factory adattárolóhoz vagy egy felhőalapú szolgáltatáshoz csatolja az adattárolót.</span><span class="sxs-lookup"><span data-stu-id="0355c-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="0355c-109">Ha már létezik egy olyan kapcsolt szolgáltatás neve, amely már létezik, ez a parancsmag a kapcsolt szolgáltatás cseréje előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0355c-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="0355c-110">Ha az erő paramétert adja meg, a parancsmag megerősítés nélkül felülírja a meglévő kapcsolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="0355c-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="0355c-111">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="0355c-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="0355c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0355c-112">EXAMPLES</span></span>

### <span data-ttu-id="0355c-113">1. példa: kapcsolt szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="0355c-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="0355c-114">Ez a parancs létrehoz egy LinkedServiceCuratedWikiData nevű hivatkozást a WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="0355c-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="0355c-115">Ez a hivatkozás egy, a fájlban megadott Azure Blob-tárolóhoz csatolja a WikiADF nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="0355c-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="0355c-116">A parancs a csővezeték-kezelő használatával átadja az eredményt az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="0355c-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0355c-117">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="0355c-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="0355c-118">További információt a Get-Help formázása – lista című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="0355c-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="0355c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0355c-119">PARAMETERS</span></span>

### <span data-ttu-id="0355c-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0355c-120">-DataFactoryName</span></span>
<span data-ttu-id="0355c-121">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0355c-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0355c-122">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást az adatgyárhoz, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="0355c-122">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0355c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0355c-123">-DefaultProfile</span></span>
<span data-ttu-id="0355c-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0355c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0355c-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0355c-125">-DefinitionFile</span></span>
<span data-ttu-id="0355c-126">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="0355c-126">The JSON file path.</span></span>

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

### <span data-ttu-id="0355c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="0355c-127">-Force</span></span>
<span data-ttu-id="0355c-128">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0355c-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0355c-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0355c-129">-Name</span></span>
<span data-ttu-id="0355c-130">A létrehozandó kapcsolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0355c-130">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="0355c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0355c-131">-ResourceGroupName</span></span>
<span data-ttu-id="0355c-132">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0355c-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0355c-133">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást a csoporthoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="0355c-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0355c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0355c-134">-ResourceId</span></span>
<span data-ttu-id="0355c-135">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0355c-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0355c-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0355c-136">-Confirm</span></span>
<span data-ttu-id="0355c-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0355c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0355c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0355c-138">-WhatIf</span></span>
<span data-ttu-id="0355c-139">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0355c-139">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0355c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0355c-140">CommonParameters</span></span>
<span data-ttu-id="0355c-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0355c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0355c-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0355c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0355c-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0355c-143">INPUTS</span></span>

### <span data-ttu-id="0355c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0355c-144">System.String</span></span>

## <span data-ttu-id="0355c-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0355c-145">OUTPUTS</span></span>

### <span data-ttu-id="0355c-146">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0355c-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="0355c-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0355c-147">NOTES</span></span>
<span data-ttu-id="0355c-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="0355c-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0355c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0355c-149">RELATED LINKS</span></span>

[<span data-ttu-id="0355c-150">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0355c-150">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="0355c-151">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0355c-151">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
