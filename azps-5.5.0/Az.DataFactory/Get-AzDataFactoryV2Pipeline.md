---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155858"
---
# <span data-ttu-id="f9081-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f9081-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="f9081-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9081-102">SYNOPSIS</span></span>
<span data-ttu-id="f9081-103">Információkat kap a Data Factoryban található prognózisról.</span><span class="sxs-lookup"><span data-stu-id="f9081-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="f9081-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9081-104">SYNTAX</span></span>

### <span data-ttu-id="f9081-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9081-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9081-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f9081-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9081-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9081-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9081-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9081-108">DESCRIPTION</span></span>
<span data-ttu-id="f9081-109">A Get-AzDataFactoryV2Pipeline parancsmag információkat kap az Azure Data Factoryban található prognózisról.</span><span class="sxs-lookup"><span data-stu-id="f9081-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="f9081-110">Ha megadja egy folyamat nevét, ez a parancsmag információt kap a folyamatról.</span><span class="sxs-lookup"><span data-stu-id="f9081-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="f9081-111">Ha nem ad meg nevet, ez a parancsmag információt kap az adatüzemben található összes folyamatról.</span><span class="sxs-lookup"><span data-stu-id="f9081-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="f9081-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9081-112">EXAMPLES</span></span>

### <span data-ttu-id="f9081-113">1. példa: Információ az összes folyamatról</span><span class="sxs-lookup"><span data-stu-id="f9081-113">Example 1: Get information about all pipelines</span></span>
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

<span data-ttu-id="f9081-114">Ez a parancs információkat kap a WikiADF nevű adat factoryban található összes folyamatról.</span><span class="sxs-lookup"><span data-stu-id="f9081-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="f9081-115">Az alábbi példaparancsok bármelyikét használhatja.</span><span class="sxs-lookup"><span data-stu-id="f9081-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="f9081-116">A második paraméterként a DataFactory objektumot használja.</span><span class="sxs-lookup"><span data-stu-id="f9081-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="f9081-117">2. példa: Információ lekérte egy adott folyamatról</span><span class="sxs-lookup"><span data-stu-id="f9081-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="f9081-118">Ez a parancs információkat kap a WIKIWikisample nevű folyamatról a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="f9081-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="f9081-119">A parancs a folyamat műveleti Format-List keresztül átadja az adatokat a Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="f9081-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f9081-120">Ez a Windows PowerShell-parancsmag formázta az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="f9081-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="f9081-121">További információért írja be a Get-Help formátumlistát.</span><span class="sxs-lookup"><span data-stu-id="f9081-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="f9081-122">3. példa: Egy adott folyamat tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="f9081-122">Example 3: Get the properties for a specific pipeline</span></span>
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

<span data-ttu-id="f9081-123">Ez a parancs információkat kap a WikiADF nevű adatüzemben lévő DPWikisample nevű folyamatról, majd a szokásos pont-ként használja a folyamathoz társított Tevékenységek tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="f9081-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="f9081-124">4. példa: Információk az első tevékenység bemeneti adatairól</span><span class="sxs-lookup"><span data-stu-id="f9081-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="f9081-125">Ez a parancs információkat kap a WikiADF nevű adatüzemben lévő DPWikisample nevű folyamatról, majd a szokásos pont-ként használja a folyamathoz társított Tevékenységek tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="f9081-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="f9081-126">A parancs a Tevékenységek tömb első elemének Inputs tulajdonságát jeleníti meg a Format-List parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f9081-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="f9081-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9081-127">PARAMETERS</span></span>

### <span data-ttu-id="f9081-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9081-128">-DataFactory</span></span>
<span data-ttu-id="f9081-129">EGY PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f9081-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="f9081-130">Ez a parancsmag a paraméter által megadott adatüzembe tartozó prognózisokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f9081-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f9081-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f9081-131">-DataFactoryName</span></span>
<span data-ttu-id="f9081-132">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9081-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f9081-133">Ez a parancsmag a paraméter által megadott adatüzembe tartozó prognózisokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f9081-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f9081-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9081-134">-DefaultProfile</span></span>
<span data-ttu-id="f9081-135">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9081-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9081-136">-Name</span><span class="sxs-lookup"><span data-stu-id="f9081-136">-Name</span></span>
<span data-ttu-id="f9081-137">Annak a folyamatnak a nevét adja meg, amelyről információt kell kapni.</span><span class="sxs-lookup"><span data-stu-id="f9081-137">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="f9081-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9081-138">-ResourceGroupName</span></span>
<span data-ttu-id="f9081-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9081-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f9081-140">Ez a parancsmag a paraméter által megadott csoporthoz tartozó prognózisokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f9081-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f9081-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9081-141">-ResourceId</span></span>
<span data-ttu-id="f9081-142">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="f9081-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f9081-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9081-143">CommonParameters</span></span>
<span data-ttu-id="f9081-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9081-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9081-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9081-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9081-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9081-146">INPUTS</span></span>

### <span data-ttu-id="f9081-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f9081-147">System.String</span></span>

### <span data-ttu-id="f9081-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f9081-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f9081-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9081-149">OUTPUTS</span></span>

### <span data-ttu-id="f9081-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f9081-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="f9081-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9081-151">NOTES</span></span>
<span data-ttu-id="f9081-152">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="f9081-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f9081-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9081-153">RELATED LINKS</span></span>

[<span data-ttu-id="f9081-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f9081-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f9081-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f9081-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f9081-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f9081-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
