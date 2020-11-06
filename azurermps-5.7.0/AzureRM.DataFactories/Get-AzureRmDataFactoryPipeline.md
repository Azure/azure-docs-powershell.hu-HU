---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 17a6be37e62693f3e6d6e7c9089f72771fc0a9f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492322"
---
# <span data-ttu-id="5cb87-101">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cb87-101">Get-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="5cb87-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5cb87-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb87-103">Információt kap a csővezetékekről az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="5cb87-103">Gets information about pipelines in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cb87-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5cb87-104">SYNTAX</span></span>

### <span data-ttu-id="5cb87-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5cb87-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cb87-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5cb87-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cb87-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5cb87-107">DESCRIPTION</span></span>
<span data-ttu-id="5cb87-108">A **Get-AzureRmDataFactoryPipeline** parancsmag információkat kap az Azure Data Factory csővezetékekről.</span><span class="sxs-lookup"><span data-stu-id="5cb87-108">The **Get-AzureRmDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="5cb87-109">Ha megad egy csővezeték nevét, ez a parancsmag információkat kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="5cb87-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="5cb87-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="5cb87-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="5cb87-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5cb87-111">EXAMPLES</span></span>

### <span data-ttu-id="5cb87-112">1. példa: adatok beolvasása az összes csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5cb87-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="5cb87-113">Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="5cb87-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="5cb87-114">Az alábbi parancsok közül választhat.</span><span class="sxs-lookup"><span data-stu-id="5cb87-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="5cb87-115">A második egy **DataFactory** -objektumot használ paraméterként.</span><span class="sxs-lookup"><span data-stu-id="5cb87-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="5cb87-116">2. példa: információk kérése egy adott csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5cb87-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="5cb87-117">Ez a parancs információt kap a DPWikisample nevű csővezetékről az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="5cb87-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="5cb87-118">A parancs a pipeline operátorral továbbítja ezeket az információkat az Format-List parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="5cb87-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5cb87-119">Az adott parancsmag formázza az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="5cb87-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="5cb87-120">További információért írja be a következőt: `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="5cb87-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="5cb87-121">3. példa: adott csővezeték tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="5cb87-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="5cb87-122">Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **Tulajdonságok** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5cb87-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="5cb87-123">Példa 4: adott csővezeték tevékenységének beszerzése</span><span class="sxs-lookup"><span data-stu-id="5cb87-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="5cb87-124">Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **tevékenységek** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5cb87-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="5cb87-125">Példa 5: a futásidejű adatok beszerzése egy adott csővezetékhez</span><span class="sxs-lookup"><span data-stu-id="5cb87-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="5cb87-126">Ez a parancs információt kap az WikiADF nevű adatDPWikisamplei nevű csővezetékről, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **RuntimeInfo** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5cb87-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="5cb87-127">Példa 6: információk beszerzése az első tevékenységhez tartozó bemenetekről</span><span class="sxs-lookup"><span data-stu-id="5cb87-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="5cb87-128">Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **tevékenységek** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5cb87-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="5cb87-129">A parancs a **tevékenységek** tömb első elemének **bemenet** tulajdonságát jeleníti meg a **Format listával**.</span><span class="sxs-lookup"><span data-stu-id="5cb87-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="5cb87-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5cb87-130">PARAMETERS</span></span>

### <span data-ttu-id="5cb87-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5cb87-131">-DataFactory</span></span>
<span data-ttu-id="5cb87-132">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5cb87-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5cb87-133">Ez a parancsmag azokat a csővezetékeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5cb87-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb87-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5cb87-134">-DataFactoryName</span></span>
<span data-ttu-id="5cb87-135">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cb87-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5cb87-136">Ez a parancsmag azokat a csővezetékeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5cb87-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cb87-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb87-137">-DefaultProfile</span></span>
<span data-ttu-id="5cb87-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5cb87-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cb87-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5cb87-139">-Name</span></span>
<span data-ttu-id="5cb87-140">Annak a csővezetéknek a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="5cb87-140">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb87-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb87-141">-ResourceGroupName</span></span>
<span data-ttu-id="5cb87-142">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cb87-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5cb87-143">Ez a parancsmag olyan csővezetékeket kap, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="5cb87-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cb87-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb87-144">CommonParameters</span></span>
<span data-ttu-id="5cb87-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5cb87-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb87-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb87-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb87-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cb87-147">INPUTS</span></span>

### <span data-ttu-id="5cb87-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="5cb87-148">None</span></span>
<span data-ttu-id="5cb87-149">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5cb87-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5cb87-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cb87-150">OUTPUTS</span></span>

### <span data-ttu-id="5cb87-151">System. Collections. Generic. list ' 1 [[Microsoft. WindowsAzure. Command. Utilities. PSPipeline, Microsoft. WindowsAzure. commands. Utilities, Version = 0.8.2.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]] Microsoft. WindowsAzure. commands. Utilities. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="5cb87-151">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSPipeline, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="5cb87-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5cb87-152">NOTES</span></span>
* <span data-ttu-id="5cb87-153">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="5cb87-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5cb87-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cb87-154">RELATED LINKS</span></span>

[<span data-ttu-id="5cb87-155">Új – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cb87-155">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="5cb87-156">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cb87-156">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="5cb87-157">Önéletrajz – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cb87-157">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="5cb87-158">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="5cb87-158">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="5cb87-159">Felfüggesztés – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cb87-159">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


