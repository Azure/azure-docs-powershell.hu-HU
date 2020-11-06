---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: ae640ffb0f595419bba57ff92d7789692af55d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493552"
---
# <span data-ttu-id="fcb25-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fcb25-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="fcb25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcb25-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb25-103">Futószalagot hoz létre az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="fcb25-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcb25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcb25-104">SYNTAX</span></span>

### <span data-ttu-id="fcb25-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fcb25-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcb25-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fcb25-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcb25-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcb25-107">DESCRIPTION</span></span>
<span data-ttu-id="fcb25-108">A **New-AzureRmDataFactoryPipeline** parancsmag létrehoz egy csővezetéket az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="fcb25-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="fcb25-109">Ha már létezik egy olyan csővezeték neve, amely már létezik, a parancsmag kéri a megerősítést, mielőtt felülírja a futószalagot.</span><span class="sxs-lookup"><span data-stu-id="fcb25-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="fcb25-110">Ha az *erő* paramétert adja meg, a parancsmag megerősítés nélkül lecseréli a meglévő csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="fcb25-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="fcb25-111">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="fcb25-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="fcb25-112">Adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="fcb25-112">Create a data factory.</span></span> 
- <span data-ttu-id="fcb25-113">Kapcsolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="fcb25-113">Create linked services.</span></span> 
- <span data-ttu-id="fcb25-114">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="fcb25-114">Create datasets.</span></span> 
- <span data-ttu-id="fcb25-115">Csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="fcb25-115">Create a pipeline.</span></span>

<span data-ttu-id="fcb25-116">Ha az adatfeldolgozóban már létezik egy azonos nevű csővezeték, ez a parancsmag arra kéri, hogy erősítse meg, hogy felülírja-e a meglévő csővezetéket az új adatkapcsolattal.</span><span class="sxs-lookup"><span data-stu-id="fcb25-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="fcb25-117">Ha a meglévő csővezeték felülírását erősítse meg, a program a csővezeték-definíciót is lecseréli.</span><span class="sxs-lookup"><span data-stu-id="fcb25-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="fcb25-118">Példák</span><span class="sxs-lookup"><span data-stu-id="fcb25-118">EXAMPLES</span></span>

### <span data-ttu-id="fcb25-119">Példa 1: csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="fcb25-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="fcb25-120">Ez a parancs létrehoz egy DPWikisample nevű csővezetéket az ADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="fcb25-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="fcb25-121">A parancs a munkafolyamatot a fájl DPWikisample.jsban lévő adatokra alapozja.</span><span class="sxs-lookup"><span data-stu-id="fcb25-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="fcb25-122">Ez a fájl olyan tevékenységekre vonatkozó információkat tartalmaz, mint például a folyamat másolása és a HDInsight tevékenység a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="fcb25-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="fcb25-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcb25-123">PARAMETERS</span></span>

### <span data-ttu-id="fcb25-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fcb25-124">-DataFactory</span></span>
<span data-ttu-id="fcb25-125">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fcb25-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fcb25-126">Ez a parancsmag létrehoz egy csővezetéket az adatfeldolgozó számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb25-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fcb25-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fcb25-127">-DataFactoryName</span></span>
<span data-ttu-id="fcb25-128">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb25-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fcb25-129">Ez a parancsmag létrehoz egy csővezetéket az adatfeldolgozó számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb25-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fcb25-130">-Fájl</span><span class="sxs-lookup"><span data-stu-id="fcb25-130">-File</span></span>
<span data-ttu-id="fcb25-131">Annak a JavaScript-objektumnak a teljes elérési útját adja meg, amely a csővezeték leírását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fcb25-131">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="fcb25-132">-Force</span><span class="sxs-lookup"><span data-stu-id="fcb25-132">-Force</span></span>
<span data-ttu-id="fcb25-133">Azt jelzi, hogy ez a parancsmag egy meglévő csővezetéket cserél le, nem kell megerősítést kérnie.</span><span class="sxs-lookup"><span data-stu-id="fcb25-133">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="fcb25-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fcb25-134">-Name</span></span>
<span data-ttu-id="fcb25-135">A létrehozandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb25-135">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="fcb25-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcb25-136">-ResourceGroupName</span></span>
<span data-ttu-id="fcb25-137">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcb25-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fcb25-138">Ez a parancsmag létrehoz egy futószalagot annak a csoportnak, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="fcb25-138">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fcb25-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fcb25-139">-Confirm</span></span>
<span data-ttu-id="fcb25-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fcb25-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb25-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb25-141">-WhatIf</span></span>
<span data-ttu-id="fcb25-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fcb25-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcb25-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fcb25-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb25-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb25-144">-DefaultProfile</span></span>
<span data-ttu-id="fcb25-145">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcb25-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcb25-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb25-146">CommonParameters</span></span>
<span data-ttu-id="fcb25-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcb25-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb25-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb25-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb25-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcb25-149">INPUTS</span></span>

## <span data-ttu-id="fcb25-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcb25-150">OUTPUTS</span></span>

### <span data-ttu-id="fcb25-151">Microsoft. WindowsAzure. Command. Utilities. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="fcb25-151">Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="fcb25-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcb25-152">NOTES</span></span>
* <span data-ttu-id="fcb25-153">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="fcb25-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fcb25-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcb25-154">RELATED LINKS</span></span>

[<span data-ttu-id="fcb25-155">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fcb25-155">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="fcb25-156">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fcb25-156">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="fcb25-157">Önéletrajz – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fcb25-157">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="fcb25-158">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="fcb25-158">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="fcb25-159">Felfüggesztés – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fcb25-159">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


