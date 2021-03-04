---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: 185f01f31f8cae62e51b7b28909f66fbf37884e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939625"
---
# <span data-ttu-id="981c1-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="981c1-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="981c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="981c1-102">SYNOPSIS</span></span>
<span data-ttu-id="981c1-103">Adja hozzá az adatfolyam-erőforrást és a függőségeit adott adatfolyam-hibakeresési munkamenethez.</span><span class="sxs-lookup"><span data-stu-id="981c1-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="981c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="981c1-104">SYNTAX</span></span>

### <span data-ttu-id="981c1-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="981c1-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="981c1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="981c1-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="981c1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="981c1-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="981c1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="981c1-108">DESCRIPTION</span></span>
<span data-ttu-id="981c1-109">Ez a parancs az adatfolyam-erőforrást és annak függőségeit az adott hibakeresési munkamenethez csatolja. Az adatfolyam-hibakeresési munkafolyamat PowerShell-parancssorának a következőnek kell lennie:</span><span class="sxs-lookup"><span data-stu-id="981c1-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="981c1-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="981c1-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="981c1-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="981c1-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="981c1-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ismételje meg ezt a lépést a különböző parancsok/célok esetén, vagy ismételje meg a 2–3. lépést a csomagfájl módosítása érdekében)</span><span class="sxs-lookup"><span data-stu-id="981c1-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="981c1-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="981c1-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="981c1-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="981c1-114">EXAMPLES</span></span>

### <span data-ttu-id="981c1-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="981c1-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="981c1-116">Adatfolyam-csomag hozzáadása a "WikiADF" data factory "550effe4-93a3-485c-8525-eaf25259efbd" hibakeresési munkamenetéhez.</span><span class="sxs-lookup"><span data-stu-id="981c1-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="981c1-117">A Pakcage-fájl adatfolyam-hibakeresési erőforrást, az adatkészlet hibakeresési resouce listáját, a csatolt szolgáltatás-hibakeresési erőforrás listáját, a hibakeresési beállítást és a munkamenetazonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="981c1-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="981c1-118">Például:</span><span class="sxs-lookup"><span data-stu-id="981c1-118">For instance:</span></span>

<span data-ttu-id="981c1-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName=name; AccountKey=key; EndpointSuffix=core.windows.net" } } }], "debugSettings": { "sourceSettings": [ { "sourceName": "sourceName": "source1"; "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" } }</span><span class="sxs-lookup"><span data-stu-id="981c1-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="981c1-120">A SessionID paraméter a csomagfájl meglévő sessionId tulajdonságának helyére használatos.</span><span class="sxs-lookup"><span data-stu-id="981c1-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="981c1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="981c1-121">PARAMETERS</span></span>

### <span data-ttu-id="981c1-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="981c1-122">-DataFactory</span></span>
<span data-ttu-id="981c1-123">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="981c1-123">The data factory object.</span></span>

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

### <span data-ttu-id="981c1-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="981c1-124">-DataFactoryName</span></span>
<span data-ttu-id="981c1-125">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="981c1-125">The data factory name.</span></span>

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

### <span data-ttu-id="981c1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981c1-126">-DefaultProfile</span></span>
<span data-ttu-id="981c1-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="981c1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="981c1-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="981c1-128">-PackageFile</span></span>
<span data-ttu-id="981c1-129">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="981c1-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="981c1-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="981c1-130">-PassThru</span></span>
<span data-ttu-id="981c1-131">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="981c1-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="981c1-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="981c1-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="981c1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="981c1-133">-ResourceGroupName</span></span>
<span data-ttu-id="981c1-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="981c1-134">The resource group name.</span></span>

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

### <span data-ttu-id="981c1-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="981c1-135">-ResourceId</span></span>
<span data-ttu-id="981c1-136">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="981c1-136">The Azure resource ID.</span></span>

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

### <span data-ttu-id="981c1-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="981c1-137">-Confirm</span></span>
<span data-ttu-id="981c1-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="981c1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="981c1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="981c1-139">-WhatIf</span></span>
<span data-ttu-id="981c1-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="981c1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="981c1-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="981c1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="981c1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981c1-142">CommonParameters</span></span>
<span data-ttu-id="981c1-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="981c1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981c1-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="981c1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981c1-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="981c1-145">INPUTS</span></span>

### <span data-ttu-id="981c1-146">System.String</span><span class="sxs-lookup"><span data-stu-id="981c1-146">System.String</span></span>

### <span data-ttu-id="981c1-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="981c1-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="981c1-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="981c1-148">OUTPUTS</span></span>

### <span data-ttu-id="981c1-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="981c1-149">System.Void</span></span>

### <span data-ttu-id="981c1-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="981c1-150">System.Boolean</span></span>

## <span data-ttu-id="981c1-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="981c1-151">NOTES</span></span>
<span data-ttu-id="981c1-152">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="981c1-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="981c1-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="981c1-153">RELATED LINKS</span></span>

[<span data-ttu-id="981c1-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="981c1-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="981c1-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="981c1-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="981c1-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="981c1-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="981c1-157">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="981c1-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
