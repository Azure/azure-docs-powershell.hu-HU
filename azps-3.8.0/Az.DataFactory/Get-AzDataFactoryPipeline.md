---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013844"
---
# <span data-ttu-id="86764-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="86764-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="86764-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86764-102">SYNOPSIS</span></span>
<span data-ttu-id="86764-103">Információt kap a csővezetékekről az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="86764-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="86764-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86764-104">SYNTAX</span></span>

### <span data-ttu-id="86764-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86764-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86764-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="86764-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86764-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="86764-107">DESCRIPTION</span></span>
<span data-ttu-id="86764-108">A **Get-AzDataFactoryPipeline** parancsmag információkat kap az Azure Data Factory csővezetékekről.</span><span class="sxs-lookup"><span data-stu-id="86764-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="86764-109">Ha megad egy csővezeték nevét, ez a parancsmag információkat kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="86764-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="86764-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="86764-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="86764-111">Példák</span><span class="sxs-lookup"><span data-stu-id="86764-111">EXAMPLES</span></span>

### <span data-ttu-id="86764-112">1. példa: adatok beolvasása az összes csővezetékről</span><span class="sxs-lookup"><span data-stu-id="86764-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="86764-113">Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="86764-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="86764-114">Az alábbi parancsok közül választhat.</span><span class="sxs-lookup"><span data-stu-id="86764-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="86764-115">A második egy **DataFactory** -objektumot használ paraméterként.</span><span class="sxs-lookup"><span data-stu-id="86764-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="86764-116">2. példa: információk kérése egy adott csővezetékről</span><span class="sxs-lookup"><span data-stu-id="86764-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="86764-117">Ez a parancs információt kap a DPWikisample nevű csővezetékről az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="86764-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="86764-118">A parancs a pipeline operátorral továbbítja ezeket az információkat az Format-List parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="86764-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="86764-119">Az adott parancsmag formázza az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="86764-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="86764-120">További információért írja be a következőt: `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="86764-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="86764-121">3. példa: adott csővezeték tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="86764-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="86764-122">Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **Tulajdonságok** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="86764-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="86764-123">Példa 4: adott csővezeték tevékenységének beszerzése</span><span class="sxs-lookup"><span data-stu-id="86764-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
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

<span data-ttu-id="86764-124">Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **tevékenységek** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="86764-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="86764-125">Példa 5: a futásidejű adatok beszerzése egy adott csővezetékhez</span><span class="sxs-lookup"><span data-stu-id="86764-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="86764-126">Ez a parancs információt kap az WikiADF nevű adatDPWikisamplei nevű csővezetékről, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **RuntimeInfo** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="86764-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="86764-127">Példa 6: információk beszerzése az első tevékenységhez tartozó bemenetekről</span><span class="sxs-lookup"><span data-stu-id="86764-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="86764-128">Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított **tevékenységek** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="86764-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="86764-129">A parancs a **tevékenységek** tömb első elemének **bemenet** tulajdonságát jeleníti meg a **Format listával**.</span><span class="sxs-lookup"><span data-stu-id="86764-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="86764-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86764-130">PARAMETERS</span></span>

### <span data-ttu-id="86764-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="86764-131">-DataFactory</span></span>
<span data-ttu-id="86764-132">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="86764-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="86764-133">Ez a parancsmag azokat a csővezetékeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="86764-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="86764-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="86764-134">-DataFactoryName</span></span>
<span data-ttu-id="86764-135">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86764-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="86764-136">Ez a parancsmag azokat a csővezetékeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="86764-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="86764-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86764-137">-DefaultProfile</span></span>
<span data-ttu-id="86764-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="86764-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86764-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86764-139">-Name</span></span>
<span data-ttu-id="86764-140">Annak a csővezetéknek a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="86764-140">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86764-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86764-141">-ResourceGroupName</span></span>
<span data-ttu-id="86764-142">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86764-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="86764-143">Ez a parancsmag olyan csővezetékeket kap, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="86764-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="86764-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86764-144">CommonParameters</span></span>
<span data-ttu-id="86764-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86764-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86764-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86764-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86764-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86764-147">INPUTS</span></span>

### <span data-ttu-id="86764-148">System. String</span><span class="sxs-lookup"><span data-stu-id="86764-148">System.String</span></span>

### <span data-ttu-id="86764-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="86764-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="86764-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86764-150">OUTPUTS</span></span>

### <span data-ttu-id="86764-151">Microsoft. Azure. Command. DataFactories. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="86764-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="86764-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86764-152">NOTES</span></span>
* <span data-ttu-id="86764-153">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="86764-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="86764-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86764-154">RELATED LINKS</span></span>

[<span data-ttu-id="86764-155">Új – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="86764-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="86764-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="86764-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="86764-157">Önéletrajz – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="86764-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="86764-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="86764-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="86764-159">Felfüggesztés – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="86764-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


