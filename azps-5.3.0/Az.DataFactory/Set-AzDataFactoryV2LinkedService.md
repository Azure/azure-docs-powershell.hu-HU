---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: d6fd12e96a98d0771a984aa5234013dbe4a548af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480387"
---
# <span data-ttu-id="caf2f-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="caf2f-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="caf2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caf2f-102">SYNOPSIS</span></span>
<span data-ttu-id="caf2f-103">Adattárat vagy felhőszolgáltatást a Data Factoryhoz kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="caf2f-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="caf2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="caf2f-104">SYNTAX</span></span>

### <span data-ttu-id="caf2f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="caf2f-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="caf2f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="caf2f-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caf2f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="caf2f-107">DESCRIPTION</span></span>
<span data-ttu-id="caf2f-108">A Set-AzDataFactoryV2LinkedService parancsmag egy adattárat vagy egy felhőszolgáltatást az Azure Data Factoryhoz kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="caf2f-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="caf2f-109">Ha egy már létező csatolt szolgáltatás nevét adja meg, ez a parancsmag megerősítést kér, mielőtt lecseréli a csatolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="caf2f-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="caf2f-110">Ha a Force paramétert adja meg, a parancsmag jóváhagyás nélkül lecseréli a meglévő csatolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="caf2f-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="caf2f-111">Végezze el ezeket a műveleteket a következő sorrendben: - Adatüzem létrehozása.</span><span class="sxs-lookup"><span data-stu-id="caf2f-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="caf2f-112">– Csatolt szolgáltatások létrehozása.</span><span class="sxs-lookup"><span data-stu-id="caf2f-112">-- Create linked services.</span></span>
<span data-ttu-id="caf2f-113">– Adatkészletek létrehozása.</span><span class="sxs-lookup"><span data-stu-id="caf2f-113">-- Create datasets.</span></span>
<span data-ttu-id="caf2f-114">– Folyamat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="caf2f-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="caf2f-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="caf2f-115">EXAMPLES</span></span>

### <span data-ttu-id="caf2f-116">1. példa: Csatolt szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="caf2f-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="caf2f-117">Ez a parancs létrehoz egy LinkedServiceCuratedWikiData nevű csatolt szolgáltatást a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="caf2f-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="caf2f-118">Ez a csatolt szolgáltatás a fájlban megadott Azure blobtárat a WikiADF nevű adatszolgáltatóhoz csatolja.</span><span class="sxs-lookup"><span data-stu-id="caf2f-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="caf2f-119">A parancs a folyamat műveleti Format-List parancsmagnak továbbküldi az eredményt.</span><span class="sxs-lookup"><span data-stu-id="caf2f-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="caf2f-120">Ez a Windows PowerShell-parancsmag formázta az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="caf2f-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="caf2f-121">További információért írja be a Get-Help formátumlistát.</span><span class="sxs-lookup"><span data-stu-id="caf2f-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="caf2f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="caf2f-122">PARAMETERS</span></span>

### <span data-ttu-id="caf2f-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="caf2f-123">-DataFactoryName</span></span>
<span data-ttu-id="caf2f-124">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="caf2f-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="caf2f-125">Ez a parancsmag csatolt szolgáltatást hoz létre a paraméter által megadott adat factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="caf2f-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="caf2f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf2f-126">-DefaultProfile</span></span>
<span data-ttu-id="caf2f-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="caf2f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caf2f-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="caf2f-128">-DefinitionFile</span></span>
<span data-ttu-id="caf2f-129">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="caf2f-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf2f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="caf2f-130">-Force</span></span>
<span data-ttu-id="caf2f-131">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="caf2f-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="caf2f-132">-Name</span><span class="sxs-lookup"><span data-stu-id="caf2f-132">-Name</span></span>
<span data-ttu-id="caf2f-133">A létrehozni szükséges csatolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="caf2f-133">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf2f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caf2f-134">-ResourceGroupName</span></span>
<span data-ttu-id="caf2f-135">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="caf2f-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="caf2f-136">Ez a parancsmag csatolt szolgáltatást hoz létre a paraméter által megadott csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="caf2f-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="caf2f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caf2f-137">-ResourceId</span></span>
<span data-ttu-id="caf2f-138">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="caf2f-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="caf2f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caf2f-139">-Confirm</span></span>
<span data-ttu-id="caf2f-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="caf2f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caf2f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caf2f-141">-WhatIf</span></span>
<span data-ttu-id="caf2f-142">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="caf2f-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="caf2f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf2f-143">CommonParameters</span></span>
<span data-ttu-id="caf2f-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caf2f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf2f-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf2f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf2f-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="caf2f-146">INPUTS</span></span>

### <span data-ttu-id="caf2f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="caf2f-147">System.String</span></span>

## <span data-ttu-id="caf2f-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="caf2f-148">OUTPUTS</span></span>

### <span data-ttu-id="caf2f-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="caf2f-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="caf2f-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="caf2f-150">NOTES</span></span>
<span data-ttu-id="caf2f-151">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="caf2f-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="caf2f-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="caf2f-152">RELATED LINKS</span></span>

[<span data-ttu-id="caf2f-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="caf2f-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="caf2f-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="caf2f-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
