---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: d6fd12e96a98d0771a984aa5234013dbe4a548af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847138"
---
# <span data-ttu-id="09df4-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="09df4-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="09df4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09df4-102">SYNOPSIS</span></span>
<span data-ttu-id="09df4-103">Az adattárolók vagy a Felhőbeli szolgáltatások összekapcsolása az adatfeldolgozó szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="09df4-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="09df4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09df4-104">SYNTAX</span></span>

### <span data-ttu-id="09df4-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09df4-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09df4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="09df4-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09df4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="09df4-107">DESCRIPTION</span></span>
<span data-ttu-id="09df4-108">Az Set-AzDataFactoryV2LinkedService parancsmag az Azure Data Factory adattárolóhoz vagy egy felhőalapú szolgáltatáshoz csatolja az adattárolót.</span><span class="sxs-lookup"><span data-stu-id="09df4-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="09df4-109">Ha már létezik egy olyan kapcsolt szolgáltatás neve, amely már létezik, ez a parancsmag a kapcsolt szolgáltatás cseréje előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09df4-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="09df4-110">Ha az erő paramétert adja meg, a parancsmag megerősítés nélkül felülírja a meglévő kapcsolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="09df4-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="09df4-111">Végezze el ezeket a műveleteket a következő sorrendben:-------hoz létre egy adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="09df4-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="09df4-112">– Kapcsolt szolgáltatások létrehozása.</span><span class="sxs-lookup"><span data-stu-id="09df4-112">-- Create linked services.</span></span>
<span data-ttu-id="09df4-113">– Adatkészletek létrehozása.</span><span class="sxs-lookup"><span data-stu-id="09df4-113">-- Create datasets.</span></span>
<span data-ttu-id="09df4-114">– Csővezeték létrehozása.</span><span class="sxs-lookup"><span data-stu-id="09df4-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="09df4-115">Példák</span><span class="sxs-lookup"><span data-stu-id="09df4-115">EXAMPLES</span></span>

### <span data-ttu-id="09df4-116">1. példa: kapcsolt szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="09df4-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="09df4-117">Ez a parancs létrehoz egy LinkedServiceCuratedWikiData nevű hivatkozást a WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="09df4-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="09df4-118">Ez a hivatkozás egy, a fájlban megadott Azure Blob-tárolóhoz csatolja a WikiADF nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="09df4-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="09df4-119">A parancs a csővezeték-kezelő használatával átadja az eredményt az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="09df4-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="09df4-120">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="09df4-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="09df4-121">További információt a Get-Help formázása – lista című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="09df4-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="09df4-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09df4-122">PARAMETERS</span></span>

### <span data-ttu-id="09df4-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="09df4-123">-DataFactoryName</span></span>
<span data-ttu-id="09df4-124">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09df4-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="09df4-125">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást az adatgyárhoz, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="09df4-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="09df4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09df4-126">-DefaultProfile</span></span>
<span data-ttu-id="09df4-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09df4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09df4-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="09df4-128">-DefinitionFile</span></span>
<span data-ttu-id="09df4-129">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="09df4-129">The JSON file path.</span></span>

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

### <span data-ttu-id="09df4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="09df4-130">-Force</span></span>
<span data-ttu-id="09df4-131">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="09df4-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="09df4-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09df4-132">-Name</span></span>
<span data-ttu-id="09df4-133">A létrehozandó kapcsolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09df4-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="09df4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09df4-134">-ResourceGroupName</span></span>
<span data-ttu-id="09df4-135">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09df4-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="09df4-136">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást a csoporthoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="09df4-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="09df4-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09df4-137">-ResourceId</span></span>
<span data-ttu-id="09df4-138">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="09df4-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="09df4-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09df4-139">-Confirm</span></span>
<span data-ttu-id="09df4-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09df4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09df4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09df4-141">-WhatIf</span></span>
<span data-ttu-id="09df4-142">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="09df4-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="09df4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09df4-143">CommonParameters</span></span>
<span data-ttu-id="09df4-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09df4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09df4-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09df4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09df4-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09df4-146">INPUTS</span></span>

### <span data-ttu-id="09df4-147">System. String</span><span class="sxs-lookup"><span data-stu-id="09df4-147">System.String</span></span>

## <span data-ttu-id="09df4-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09df4-148">OUTPUTS</span></span>

### <span data-ttu-id="09df4-149">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="09df4-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="09df4-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09df4-150">NOTES</span></span>
<span data-ttu-id="09df4-151">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="09df4-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="09df4-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09df4-152">RELATED LINKS</span></span>

[<span data-ttu-id="09df4-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="09df4-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="09df4-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="09df4-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
