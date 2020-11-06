---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 47cbd81fa7e2e8f3877c2e933254cde4e2cee8ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491955"
---
# <span data-ttu-id="5cb5d-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5cb5d-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="5cb5d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5cb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb5d-103">Az adattárolók vagy a Felhőbeli szolgáltatások összekapcsolása az adatfeldolgozó szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cb5d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5cb5d-104">SYNTAX</span></span>

### <span data-ttu-id="5cb5d-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5cb5d-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cb5d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5cb5d-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cb5d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5cb5d-107">DESCRIPTION</span></span>
<span data-ttu-id="5cb5d-108">Az Set-AzureRmDataFactoryV2LinkedService parancsmag az Azure Data Factory adattárolóhoz vagy egy felhőalapú szolgáltatáshoz csatolja az adattárolót.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="5cb5d-109">Ha már létezik egy olyan kapcsolt szolgáltatás neve, amely már létezik, ez a parancsmag a kapcsolt szolgáltatás cseréje előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="5cb5d-110">Ha az erő paramétert adja meg, a parancsmag megerősítés nélkül felülírja a meglévő kapcsolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="5cb5d-111">Végezze el ezeket a műveleteket a következő sorrendben:-------hoz létre egy adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="5cb5d-112">– Kapcsolt szolgáltatások létrehozása.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-112">-- Create linked services.</span></span>
<span data-ttu-id="5cb5d-113">– Adatkészletek létrehozása.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-113">-- Create datasets.</span></span>
<span data-ttu-id="5cb5d-114">– Csővezeték létrehozása.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="5cb5d-115">Példák</span><span class="sxs-lookup"><span data-stu-id="5cb5d-115">EXAMPLES</span></span>

### <span data-ttu-id="5cb5d-116">1. példa: kapcsolt szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="5cb5d-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="5cb5d-117">Ez a parancs létrehoz egy LinkedServiceCuratedWikiData nevű hivatkozást a WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="5cb5d-118">Ez a hivatkozás egy, a fájlban megadott Azure Blob-tárolóhoz csatolja a WikiADF nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="5cb5d-119">A parancs a csővezeték-kezelő használatával átadja az eredményt az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5cb5d-120">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="5cb5d-121">További információt a Get-Help formázása – lista című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="5cb5d-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5cb5d-122">PARAMETERS</span></span>

### <span data-ttu-id="5cb5d-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5cb5d-123">-DataFactoryName</span></span>
<span data-ttu-id="5cb5d-124">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5cb5d-125">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást az adatgyárhoz, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cb5d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb5d-126">-DefaultProfile</span></span>
<span data-ttu-id="5cb5d-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cb5d-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="5cb5d-128">-DefinitionFile</span></span>
<span data-ttu-id="5cb5d-129">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-129">The JSON file path.</span></span>

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

### <span data-ttu-id="5cb5d-130">-Force</span><span class="sxs-lookup"><span data-stu-id="5cb5d-130">-Force</span></span>
<span data-ttu-id="5cb5d-131">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5cb5d-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5cb5d-132">-Name</span></span>
<span data-ttu-id="5cb5d-133">A létrehozandó kapcsolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-133">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb5d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb5d-134">-ResourceGroupName</span></span>
<span data-ttu-id="5cb5d-135">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5cb5d-136">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást a csoporthoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cb5d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cb5d-137">-ResourceId</span></span>
<span data-ttu-id="5cb5d-138">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5cb5d-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5cb5d-139">-Confirm</span></span>
<span data-ttu-id="5cb5d-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cb5d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cb5d-141">-WhatIf</span></span>
<span data-ttu-id="5cb5d-142">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5cb5d-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5cb5d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb5d-143">CommonParameters</span></span>
<span data-ttu-id="5cb5d-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5cb5d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb5d-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb5d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb5d-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cb5d-146">INPUTS</span></span>

### <span data-ttu-id="5cb5d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5cb5d-147">System.String</span></span>

## <span data-ttu-id="5cb5d-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cb5d-148">OUTPUTS</span></span>

### <span data-ttu-id="5cb5d-149">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="5cb5d-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="5cb5d-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5cb5d-150">NOTES</span></span>
<span data-ttu-id="5cb5d-151">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="5cb5d-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5cb5d-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cb5d-152">RELATED LINKS</span></span>

[<span data-ttu-id="5cb5d-153">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5cb5d-153">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="5cb5d-154">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5cb5d-154">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
