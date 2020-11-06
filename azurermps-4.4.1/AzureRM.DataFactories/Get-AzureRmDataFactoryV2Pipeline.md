---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e0abd64298d74c52f2081e6d36f42b1ad2dee913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493559"
---
# <span data-ttu-id="48529-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="48529-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="48529-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48529-102">SYNOPSIS</span></span>
<span data-ttu-id="48529-103">Információt kap az adatfeldolgozási folyamatokról.</span><span class="sxs-lookup"><span data-stu-id="48529-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48529-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48529-104">SYNTAX</span></span>

### <span data-ttu-id="48529-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48529-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48529-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="48529-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48529-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="48529-107">DESCRIPTION</span></span>
<span data-ttu-id="48529-108">Az Get-AzureRmDataFactoryV2Pipeline parancsmag információkat kap az Azure Data Factory csővezetékekről.</span><span class="sxs-lookup"><span data-stu-id="48529-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="48529-109">Ha megad egy csővezeték nevét, ez a parancsmag információkat kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="48529-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="48529-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="48529-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="48529-111">Példák</span><span class="sxs-lookup"><span data-stu-id="48529-111">EXAMPLES</span></span>

### <span data-ttu-id="48529-112">1. példa: adatok beolvasása az összes csővezetékről</span><span class="sxs-lookup"><span data-stu-id="48529-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="48529-113">Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="48529-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="48529-114">Az alábbi parancsok közül választhat.</span><span class="sxs-lookup"><span data-stu-id="48529-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="48529-115">A második egy DataFactory-objektumot használ paraméterként.</span><span class="sxs-lookup"><span data-stu-id="48529-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="48529-116">2. példa: információk kérése egy adott csővezetékről</span><span class="sxs-lookup"><span data-stu-id="48529-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="48529-117">Ez a parancs információt kap a DPWikisample nevű csővezetékről az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="48529-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="48529-118">A parancs a pipeline operátorral továbbítja ezeket az információkat az Format-List parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="48529-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="48529-119">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="48529-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="48529-120">További információt a Get-Help formázása – lista című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="48529-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="48529-121">3. példa: adott csővezeték tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="48529-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}
```

<span data-ttu-id="48529-122">Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított tevékenységek tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="48529-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="48529-123">Példa 6: információk beszerzése az első tevékenységhez tartozó bemenetekről</span><span class="sxs-lookup"><span data-stu-id="48529-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="48529-124">Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított tevékenységek tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="48529-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="48529-125">A parancs a tevékenységek tömb első elemének bemenet tulajdonságát jeleníti meg a Format-List parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="48529-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="48529-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48529-126">PARAMETERS</span></span>

### <span data-ttu-id="48529-127">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="48529-127">-DataFactory</span></span>
<span data-ttu-id="48529-128">Egy PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="48529-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="48529-129">Ez a parancsmag azokat a csővezetékeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="48529-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="48529-130">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="48529-130">-DataFactoryName</span></span>
<span data-ttu-id="48529-131">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48529-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="48529-132">Ez a parancsmag azokat a csővezetékeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="48529-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="48529-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48529-133">-Name</span></span>
<span data-ttu-id="48529-134">Annak a csővezetéknek a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="48529-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48529-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48529-135">-ResourceGroupName</span></span>
<span data-ttu-id="48529-136">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48529-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="48529-137">Ez a parancsmag olyan csővezetékeket kap, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="48529-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="48529-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48529-138">-DefaultProfile</span></span>
<span data-ttu-id="48529-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48529-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48529-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48529-140">CommonParameters</span></span>
<span data-ttu-id="48529-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48529-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48529-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48529-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48529-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48529-143">INPUTS</span></span>

### <span data-ttu-id="48529-144">System. String</span><span class="sxs-lookup"><span data-stu-id="48529-144">System.String</span></span>
<span data-ttu-id="48529-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="48529-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="48529-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48529-146">OUTPUTS</span></span>

### <span data-ttu-id="48529-147">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="48529-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="48529-148">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="48529-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="48529-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48529-149">NOTES</span></span>
<span data-ttu-id="48529-150">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="48529-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="48529-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48529-151">RELATED LINKS</span></span>

[<span data-ttu-id="48529-152">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="48529-152">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="48529-153">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="48529-153">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="48529-154">Meghívó-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="48529-154">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
