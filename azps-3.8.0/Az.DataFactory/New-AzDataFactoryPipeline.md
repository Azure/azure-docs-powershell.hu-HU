---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847225"
---
# <span data-ttu-id="4c74b-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4c74b-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="4c74b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c74b-102">SYNOPSIS</span></span>
<span data-ttu-id="4c74b-103">Futószalagot hoz létre az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="4c74b-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="4c74b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c74b-104">SYNTAX</span></span>

### <span data-ttu-id="4c74b-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c74b-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c74b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4c74b-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c74b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c74b-107">DESCRIPTION</span></span>
<span data-ttu-id="4c74b-108">A **New-AzDataFactoryPipeline** parancsmag létrehoz egy csővezetéket az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="4c74b-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="4c74b-109">Ha már létezik egy olyan csővezeték neve, amely már létezik, a parancsmag kéri a megerősítést, mielőtt felülírja a futószalagot.</span><span class="sxs-lookup"><span data-stu-id="4c74b-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="4c74b-110">Ha az *erő* paramétert adja meg, a parancsmag megerősítés nélkül lecseréli a meglévő csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="4c74b-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="4c74b-111">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="4c74b-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="4c74b-112">Adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="4c74b-112">Create a data factory.</span></span> 
- <span data-ttu-id="4c74b-113">Kapcsolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="4c74b-113">Create linked services.</span></span> 
- <span data-ttu-id="4c74b-114">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="4c74b-114">Create datasets.</span></span> 
- <span data-ttu-id="4c74b-115">Csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="4c74b-115">Create a pipeline.</span></span>
<span data-ttu-id="4c74b-116">Ha az adatfeldolgozóban már létezik egy azonos nevű csővezeték, ez a parancsmag arra kéri, hogy erősítse meg, hogy felülírja-e a meglévő csővezetéket az új adatkapcsolattal.</span><span class="sxs-lookup"><span data-stu-id="4c74b-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="4c74b-117">Ha a meglévő csővezeték felülírását erősítse meg, a program a csővezeték-definíciót is lecseréli.</span><span class="sxs-lookup"><span data-stu-id="4c74b-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="4c74b-118">Példák</span><span class="sxs-lookup"><span data-stu-id="4c74b-118">EXAMPLES</span></span>

### <span data-ttu-id="4c74b-119">Példa 1: csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="4c74b-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="4c74b-120">Ez a parancs létrehoz egy DPWikisample nevű csővezetéket az ADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="4c74b-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="4c74b-121">A parancs a munkafolyamatot a fájl DPWikisample.jsban lévő adatokra alapozja.</span><span class="sxs-lookup"><span data-stu-id="4c74b-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="4c74b-122">Ez a fájl olyan tevékenységekre vonatkozó információkat tartalmaz, mint például a folyamat másolása és a HDInsight tevékenység a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="4c74b-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="4c74b-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c74b-123">PARAMETERS</span></span>

### <span data-ttu-id="4c74b-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4c74b-124">-DataFactory</span></span>
<span data-ttu-id="4c74b-125">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4c74b-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4c74b-126">Ez a parancsmag létrehoz egy csővezetéket az adatfeldolgozó számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c74b-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c74b-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4c74b-127">-DataFactoryName</span></span>
<span data-ttu-id="4c74b-128">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c74b-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4c74b-129">Ez a parancsmag létrehoz egy csővezetéket az adatfeldolgozó számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c74b-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c74b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c74b-130">-DefaultProfile</span></span>
<span data-ttu-id="4c74b-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4c74b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c74b-132">-Fájl</span><span class="sxs-lookup"><span data-stu-id="4c74b-132">-File</span></span>
<span data-ttu-id="4c74b-133">Annak a JavaScript-objektumnak a teljes elérési útját adja meg, amely a csővezeték leírását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4c74b-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c74b-134">-Force</span><span class="sxs-lookup"><span data-stu-id="4c74b-134">-Force</span></span>
<span data-ttu-id="4c74b-135">Azt jelzi, hogy ez a parancsmag egy meglévő csővezetéket cserél le, nem kell megerősítést kérnie.</span><span class="sxs-lookup"><span data-stu-id="4c74b-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4c74b-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c74b-136">-Name</span></span>
<span data-ttu-id="4c74b-137">A létrehozandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c74b-137">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="4c74b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c74b-138">-ResourceGroupName</span></span>
<span data-ttu-id="4c74b-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c74b-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4c74b-140">Ez a parancsmag létrehoz egy futószalagot annak a csoportnak, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="4c74b-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c74b-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4c74b-141">-Confirm</span></span>
<span data-ttu-id="4c74b-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4c74b-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c74b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c74b-143">-WhatIf</span></span>
<span data-ttu-id="4c74b-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4c74b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c74b-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c74b-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c74b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c74b-146">CommonParameters</span></span>
<span data-ttu-id="4c74b-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c74b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c74b-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c74b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c74b-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c74b-149">INPUTS</span></span>

### <span data-ttu-id="4c74b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4c74b-150">System.String</span></span>

### <span data-ttu-id="4c74b-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4c74b-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="4c74b-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c74b-152">OUTPUTS</span></span>

### <span data-ttu-id="4c74b-153">Microsoft. Azure. Command. DataFactories. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="4c74b-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="4c74b-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c74b-154">NOTES</span></span>
* <span data-ttu-id="4c74b-155">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="4c74b-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4c74b-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c74b-156">RELATED LINKS</span></span>

[<span data-ttu-id="4c74b-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4c74b-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="4c74b-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4c74b-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="4c74b-159">Önéletrajz – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4c74b-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="4c74b-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="4c74b-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="4c74b-161">Felfüggesztés – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4c74b-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


