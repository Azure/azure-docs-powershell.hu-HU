---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155882"
---
# <span data-ttu-id="6b607-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6b607-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="6b607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b607-102">SYNOPSIS</span></span>
<span data-ttu-id="6b607-103">Információkat kap az Azure Data Factoryban található prognózisról.</span><span class="sxs-lookup"><span data-stu-id="6b607-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="6b607-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b607-104">SYNTAX</span></span>

### <span data-ttu-id="6b607-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b607-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b607-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6b607-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b607-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b607-107">DESCRIPTION</span></span>
<span data-ttu-id="6b607-108">A **Get-AzDataFactoryPipeline** parancsmag információt kap az Azure Data Factoryban található prognózisról.</span><span class="sxs-lookup"><span data-stu-id="6b607-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="6b607-109">Ha megadja egy folyamat nevét, ez a parancsmag információt kap a folyamatról.</span><span class="sxs-lookup"><span data-stu-id="6b607-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="6b607-110">Ha nem ad meg nevet, ez a parancsmag információt kap az adatüzemben található összes folyamatról.</span><span class="sxs-lookup"><span data-stu-id="6b607-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="6b607-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b607-111">EXAMPLES</span></span>

### <span data-ttu-id="6b607-112">1. példa: Információ az összes folyamatról</span><span class="sxs-lookup"><span data-stu-id="6b607-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="6b607-113">Ez a parancs információkat kap a WikiADF nevű adat factoryban található összes folyamatról.</span><span class="sxs-lookup"><span data-stu-id="6b607-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="6b607-114">Az alábbi példaparancsok közül választhat.</span><span class="sxs-lookup"><span data-stu-id="6b607-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="6b607-115">A második paraméterként **a DataFactory** objektumot használja.</span><span class="sxs-lookup"><span data-stu-id="6b607-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="6b607-116">2. példa: Információ lekérte egy adott folyamatról</span><span class="sxs-lookup"><span data-stu-id="6b607-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="6b607-117">Ez a parancs információkat kap a WIKIWikisample nevű folyamatról a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="6b607-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="6b607-118">A parancs a folyamat műveleti Format-List keresztül átadja az adatokat a Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="6b607-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6b607-119">Ez a parancsmag formázja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="6b607-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="6b607-120">További információért írja be a `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="6b607-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="6b607-121">3. példa: Egy adott folyamat tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="6b607-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="6b607-122">Ez a parancs információkat kap a WikiADF nevű adatüzemben lévő DPWikisample nevű folyamatról, majd a szokásos pont-adatokat használja a folyamathoz társított **Tulajdonságok** tulajdonság megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="6b607-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="6b607-123">4. példa: Tevékenységek lekérte egy adott folyamathoz</span><span class="sxs-lookup"><span data-stu-id="6b607-123">Example 4: Get the activities for a specific pipeline</span></span>
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

<span data-ttu-id="6b607-124">Ez a parancs információkat kap a WikiADF nevű adatüzemben lévő DPWikisample nevű folyamatról, majd a szokásos pont-ként használja a folyamathoz társított **Tevékenységek** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="6b607-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="6b607-125">5. példa: A futásidejű adatok lekérte egy adott folyamathoz</span><span class="sxs-lookup"><span data-stu-id="6b607-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="6b607-126">Ez a parancs információkat kap a DpWikisample nevű folyamatról a WikiADF nevű adatüzemben, majd a szokásos pont-adatokat használja a folyamathoz társított **RuntimeInfo** tulajdonság megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="6b607-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="6b607-127">6. példa: Információk az első tevékenység bemeneti adatairól</span><span class="sxs-lookup"><span data-stu-id="6b607-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="6b607-128">Ez a parancs információkat kap a WikiADF nevű adatüzemben lévő DPWikisample nevű folyamatról, majd a szokásos pont-ként használja a folyamathoz társított **Tevékenységek** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="6b607-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="6b607-129">A parancs a Tevékenységek tömb első elemének **Inputs** tulajdonságát jeleníti meg a **Format-List segítségével.** </span><span class="sxs-lookup"><span data-stu-id="6b607-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="6b607-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b607-130">PARAMETERS</span></span>

### <span data-ttu-id="6b607-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6b607-131">-DataFactory</span></span>
<span data-ttu-id="6b607-132">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b607-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6b607-133">Ez a parancsmag a paraméter által megadott adatüzembe tartozó prognózisokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6b607-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b607-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6b607-134">-DataFactoryName</span></span>
<span data-ttu-id="6b607-135">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b607-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6b607-136">Ez a parancsmag a paraméter által megadott adatüzembe tartozó prognózisokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6b607-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b607-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b607-137">-DefaultProfile</span></span>
<span data-ttu-id="6b607-138">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6b607-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b607-139">-Name</span><span class="sxs-lookup"><span data-stu-id="6b607-139">-Name</span></span>
<span data-ttu-id="6b607-140">Annak a folyamatnak a nevét adja meg, amelyről információt kell kapni.</span><span class="sxs-lookup"><span data-stu-id="6b607-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="6b607-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b607-141">-ResourceGroupName</span></span>
<span data-ttu-id="6b607-142">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b607-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6b607-143">Ez a parancsmag a paraméter által megadott csoporthoz tartozó prognózisokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6b607-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b607-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b607-144">CommonParameters</span></span>
<span data-ttu-id="6b607-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b607-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b607-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b607-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b607-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b607-147">INPUTS</span></span>

### <span data-ttu-id="6b607-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6b607-148">System.String</span></span>

### <span data-ttu-id="6b607-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6b607-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="6b607-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b607-150">OUTPUTS</span></span>

### <span data-ttu-id="6b607-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="6b607-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="6b607-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b607-152">NOTES</span></span>
* <span data-ttu-id="6b607-153">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="6b607-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6b607-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b607-154">RELATED LINKS</span></span>

[<span data-ttu-id="6b607-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6b607-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="6b607-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6b607-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="6b607-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6b607-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="6b607-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="6b607-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="6b607-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6b607-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


