---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5b11273e61689c515cc7ed72f013514fcd309dcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928241"
---
# <span data-ttu-id="d18c0-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="d18c0-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="d18c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d18c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d18c0-103">Egy adattárat vagy felhőszolgáltatást egy Azure Data Factoryhoz kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="d18c0-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="d18c0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d18c0-104">SYNTAX</span></span>

### <span data-ttu-id="d18c0-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d18c0-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d18c0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d18c0-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d18c0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d18c0-107">DESCRIPTION</span></span>
<span data-ttu-id="d18c0-108">A **New-AzDataFactoryLinkedService** parancsmag adattárat vagy felhőszolgáltatást csatol az Azure Data Factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="d18c0-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="d18c0-109">Ha egy már létező csatolt szolgáltatás nevét adja meg, ez a parancsmag megerősítést kér, mielőtt lecseréli a csatolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d18c0-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="d18c0-110">Ha a Force *paramétert* adja meg, a parancsmag jóváhagyás nélkül lecseréli a meglévő csatolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d18c0-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="d18c0-111">Ezeket a műveleteket a következő sorrendben végezze el:</span><span class="sxs-lookup"><span data-stu-id="d18c0-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="d18c0-112">Adatüzem létrehozása</span><span class="sxs-lookup"><span data-stu-id="d18c0-112">Create a data factory.</span></span> 
- <span data-ttu-id="d18c0-113">Csatolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="d18c0-113">Create linked services.</span></span> 
- <span data-ttu-id="d18c0-114">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="d18c0-114">Create datasets.</span></span> 
- <span data-ttu-id="d18c0-115">Folyamat létrehozása</span><span class="sxs-lookup"><span data-stu-id="d18c0-115">Create a pipeline.</span></span>

## <span data-ttu-id="d18c0-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d18c0-116">EXAMPLES</span></span>

### <span data-ttu-id="d18c0-117">1. példa: Csatolt szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="d18c0-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="d18c0-118">Ez a parancs létrehoz egy LinkedServiceCuratedWikiData nevű csatolt szolgáltatást a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="d18c0-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="d18c0-119">Ez a csatolt szolgáltatás a fájlban megadott Azure blobtárat a WikiADF nevű adatszolgáltatóhoz csatolja.</span><span class="sxs-lookup"><span data-stu-id="d18c0-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="d18c0-120">A parancs a folyamat műveleti Format-List parancsmagnak továbbküldi az eredményt.</span><span class="sxs-lookup"><span data-stu-id="d18c0-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d18c0-121">Ez a Windows PowerShell-parancsmag formázta az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="d18c0-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="d18c0-122">További információért írja be a `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="d18c0-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="d18c0-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d18c0-123">PARAMETERS</span></span>

### <span data-ttu-id="d18c0-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d18c0-124">-DataFactory</span></span>
<span data-ttu-id="d18c0-125">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="d18c0-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d18c0-126">Ez a parancsmag csatolt szolgáltatást hoz létre a paraméter által megadott adat factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="d18c0-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d18c0-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d18c0-127">-DataFactoryName</span></span>
<span data-ttu-id="d18c0-128">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d18c0-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d18c0-129">Ez a parancsmag csatolt szolgáltatást hoz létre a paraméter által megadott adat factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="d18c0-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d18c0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18c0-130">-DefaultProfile</span></span>
<span data-ttu-id="d18c0-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d18c0-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d18c0-132">-File</span><span class="sxs-lookup"><span data-stu-id="d18c0-132">-File</span></span>
<span data-ttu-id="d18c0-133">A hivatkozott szolgáltatás leírását tartalmazó JavaScript-objektum-notation (JSON) fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d18c0-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="d18c0-134">-Force</span><span class="sxs-lookup"><span data-stu-id="d18c0-134">-Force</span></span>
<span data-ttu-id="d18c0-135">Azt jelzi, hogy ez a parancsmag egy meglévő csatolt szolgáltatás helyére vált, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d18c0-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d18c0-136">-Name</span><span class="sxs-lookup"><span data-stu-id="d18c0-136">-Name</span></span>
<span data-ttu-id="d18c0-137">A létrehozni szükséges csatolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="d18c0-137">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d18c0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d18c0-138">-ResourceGroupName</span></span>
<span data-ttu-id="d18c0-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d18c0-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d18c0-140">Ez a parancsmag csatolt szolgáltatást hoz létre a paraméter által megadott csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="d18c0-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d18c0-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d18c0-141">-Confirm</span></span>
<span data-ttu-id="d18c0-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d18c0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d18c0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18c0-143">-WhatIf</span></span>
<span data-ttu-id="d18c0-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d18c0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d18c0-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d18c0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d18c0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18c0-146">CommonParameters</span></span>
<span data-ttu-id="d18c0-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18c0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18c0-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d18c0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18c0-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d18c0-149">INPUTS</span></span>

### <span data-ttu-id="d18c0-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d18c0-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d18c0-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d18c0-151">System.String</span></span>

## <span data-ttu-id="d18c0-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d18c0-152">OUTPUTS</span></span>

### <span data-ttu-id="d18c0-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="d18c0-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="d18c0-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d18c0-154">NOTES</span></span>
* <span data-ttu-id="d18c0-155">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="d18c0-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d18c0-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d18c0-156">RELATED LINKS</span></span>

[<span data-ttu-id="d18c0-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="d18c0-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="d18c0-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="d18c0-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


