---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184180"
---
# <span data-ttu-id="52888-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="52888-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="52888-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52888-102">SYNOPSIS</span></span>
<span data-ttu-id="52888-103">Információt kap az adatfeldolgozási folyamatokról.</span><span class="sxs-lookup"><span data-stu-id="52888-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="52888-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52888-104">SYNTAX</span></span>

### <span data-ttu-id="52888-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52888-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52888-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="52888-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52888-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="52888-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52888-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="52888-108">DESCRIPTION</span></span>
<span data-ttu-id="52888-109">Az Get-AzDataFactoryV2Pipeline parancsmag információkat kap az Azure Data Factory csővezetékekről.</span><span class="sxs-lookup"><span data-stu-id="52888-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="52888-110">Ha megad egy csővezeték nevét, ez a parancsmag információkat kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="52888-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="52888-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="52888-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="52888-112">Példák</span><span class="sxs-lookup"><span data-stu-id="52888-112">EXAMPLES</span></span>

### <span data-ttu-id="52888-113">1. példa: adatok beolvasása az összes csővezetékről</span><span class="sxs-lookup"><span data-stu-id="52888-113">Example 1: Get information about all pipelines</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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

<span data-ttu-id="52888-114">Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="52888-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="52888-115">Az alábbi parancsok közül választhat.</span><span class="sxs-lookup"><span data-stu-id="52888-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="52888-116">A második egy DataFactory-objektumot használ paraméterként.</span><span class="sxs-lookup"><span data-stu-id="52888-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="52888-117">2. példa: információk kérése egy adott csővezetékről</span><span class="sxs-lookup"><span data-stu-id="52888-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="52888-118">Ez a parancs információt kap a DPWikisample nevű csővezetékről az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="52888-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="52888-119">A parancs a pipeline operátorral továbbítja ezeket az információkat az Format-List parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="52888-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="52888-120">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="52888-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="52888-121">További információt a Get-Help formázása – lista című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="52888-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="52888-122">3. példa: adott csővezeték tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="52888-122">Example 3: Get the properties for a specific pipeline</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

<span data-ttu-id="52888-123">Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított tevékenységek tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="52888-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="52888-124">4. példa: információk beszerzése az első tevékenységhez tartozó bemenetekről</span><span class="sxs-lookup"><span data-stu-id="52888-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="52888-125">Ez a parancs információt kap a DPWikisample nevű pipeline-kapcsolatról az WikiADF nevű adatgyárban, majd normál pont jelöléssel jeleníti meg az adott csővezetékhez társított tevékenységek tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="52888-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="52888-126">A parancs a tevékenységek tömb első elemének bemenet tulajdonságát jeleníti meg a Format-List parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="52888-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="52888-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52888-127">PARAMETERS</span></span>

### <span data-ttu-id="52888-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="52888-128">-DataFactory</span></span>
<span data-ttu-id="52888-129">Egy PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="52888-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="52888-130">Ez a parancsmag azokat a csővezetékeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="52888-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="52888-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="52888-131">-DataFactoryName</span></span>
<span data-ttu-id="52888-132">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52888-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="52888-133">Ez a parancsmag azokat a csővezetékeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="52888-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="52888-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52888-134">-DefaultProfile</span></span>
<span data-ttu-id="52888-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52888-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52888-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="52888-136">-Name</span></span>
<span data-ttu-id="52888-137">Annak a csővezetéknek a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="52888-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52888-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52888-138">-ResourceGroupName</span></span>
<span data-ttu-id="52888-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52888-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="52888-140">Ez a parancsmag olyan csővezetékeket kap, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="52888-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="52888-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52888-141">-ResourceId</span></span>
<span data-ttu-id="52888-142">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="52888-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="52888-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52888-143">CommonParameters</span></span>
<span data-ttu-id="52888-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52888-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52888-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52888-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52888-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52888-146">INPUTS</span></span>

### <span data-ttu-id="52888-147">System. String</span><span class="sxs-lookup"><span data-stu-id="52888-147">System.String</span></span>

### <span data-ttu-id="52888-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="52888-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="52888-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52888-149">OUTPUTS</span></span>

### <span data-ttu-id="52888-150">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="52888-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="52888-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52888-151">NOTES</span></span>
<span data-ttu-id="52888-152">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="52888-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="52888-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52888-153">RELATED LINKS</span></span>

[<span data-ttu-id="52888-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="52888-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="52888-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="52888-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="52888-156">Meghívó-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="52888-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
