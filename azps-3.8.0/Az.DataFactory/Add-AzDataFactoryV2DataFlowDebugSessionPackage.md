---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: c319ee7fba1bddff8e93e56601c623658094253d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014424"
---
# <span data-ttu-id="6de36-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="6de36-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="6de36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6de36-102">SYNOPSIS</span></span>
<span data-ttu-id="6de36-103">Adatfolyam-erőforrás és annak függőségeinek hozzáadása adott adatfolyam-hibakeresési munkamenethez.</span><span class="sxs-lookup"><span data-stu-id="6de36-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="6de36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6de36-104">SYNTAX</span></span>

### <span data-ttu-id="6de36-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6de36-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6de36-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6de36-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6de36-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6de36-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6de36-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6de36-108">DESCRIPTION</span></span>
<span data-ttu-id="6de36-109">Ez a parancs az adatáramlás-erőforrást és a függőségeket az adott hibakeresési munkamenethez csatolja a PowerShell-parancssor az adatfolyam-hibakeresési munkafolyamathoz:</span><span class="sxs-lookup"><span data-stu-id="6de36-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="6de36-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="6de36-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="6de36-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="6de36-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="6de36-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ismételje meg ezt a lépést a különböző parancsok/célok esetén, vagy ismételje meg az 2-3-es lépést a csomagfájl módosítása céljából)</span><span class="sxs-lookup"><span data-stu-id="6de36-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="6de36-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="6de36-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="6de36-114">Példák</span><span class="sxs-lookup"><span data-stu-id="6de36-114">EXAMPLES</span></span>

### <span data-ttu-id="6de36-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6de36-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="6de36-116">Adatfolyam-csomag felvétele a Debug-munkamenetbe "550effe4 – 93a3 – 485c-8525-eaf25259efbd" "WikiADF" Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6de36-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="6de36-117">A Pakcage-fájl adatáramlás-debug-erőforrást, az adatkészlet-debug Resouce listáját, a kapcsolt szolgáltatás hibakeresési erőforrását, a hibakeresési beállításokat és a munkamenet-azonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6de36-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="6de36-118">Például:</span><span class="sxs-lookup"><span data-stu-id="6de36-118">For instance:</span></span>

<span data-ttu-id="6de36-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName = név; AccountKey = kulcs; EndpointSuffix = Core. Windows. net "}}}]," debugSettings ": {" sourceSettings ": [{" sourceName ":" source1 ";" rowLimit ": 1000}]}," 4f988caf-e765-47d2-82cd-430334a6b135 "}</span><span class="sxs-lookup"><span data-stu-id="6de36-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="6de36-120">A munkamenet-összekapcsoló paraméter a meglévő munkamenet-tulajdonságnak a csomagfájl helyére való lecserélésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="6de36-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="6de36-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6de36-121">PARAMETERS</span></span>

### <span data-ttu-id="6de36-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6de36-122">-DataFactory</span></span>
<span data-ttu-id="6de36-123">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="6de36-123">The data factory object.</span></span>

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

### <span data-ttu-id="6de36-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6de36-124">-DataFactoryName</span></span>
<span data-ttu-id="6de36-125">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="6de36-125">The data factory name.</span></span>

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

### <span data-ttu-id="6de36-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de36-126">-DefaultProfile</span></span>
<span data-ttu-id="6de36-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6de36-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6de36-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="6de36-128">-PackageFile</span></span>
<span data-ttu-id="6de36-129">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6de36-129">The JSON file path.</span></span>

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

### <span data-ttu-id="6de36-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6de36-130">-PassThru</span></span>
<span data-ttu-id="6de36-131">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="6de36-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="6de36-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6de36-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="6de36-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de36-133">-ResourceGroupName</span></span>
<span data-ttu-id="6de36-134">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6de36-134">The resource group name.</span></span>

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

### <span data-ttu-id="6de36-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6de36-135">-ResourceId</span></span>
<span data-ttu-id="6de36-136">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="6de36-136">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6de36-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6de36-137">-Confirm</span></span>
<span data-ttu-id="6de36-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6de36-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de36-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de36-139">-WhatIf</span></span>
<span data-ttu-id="6de36-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6de36-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6de36-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6de36-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de36-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de36-142">CommonParameters</span></span>
<span data-ttu-id="6de36-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6de36-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de36-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6de36-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de36-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6de36-145">INPUTS</span></span>

### <span data-ttu-id="6de36-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6de36-146">System.String</span></span>

### <span data-ttu-id="6de36-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6de36-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6de36-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6de36-148">OUTPUTS</span></span>

### <span data-ttu-id="6de36-149">System. Void</span><span class="sxs-lookup"><span data-stu-id="6de36-149">System.Void</span></span>

### <span data-ttu-id="6de36-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6de36-150">System.Boolean</span></span>

## <span data-ttu-id="6de36-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6de36-151">NOTES</span></span>
<span data-ttu-id="6de36-152">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="6de36-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6de36-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6de36-153">RELATED LINKS</span></span>

[<span data-ttu-id="6de36-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="6de36-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="6de36-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="6de36-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="6de36-156">Meghívó-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="6de36-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="6de36-157">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="6de36-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
