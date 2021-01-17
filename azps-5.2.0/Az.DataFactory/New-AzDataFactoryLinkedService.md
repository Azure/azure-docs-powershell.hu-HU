---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324515"
---
# <span data-ttu-id="34536-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="34536-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="34536-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34536-102">SYNOPSIS</span></span>
<span data-ttu-id="34536-103">Egy adattárat vagy felhőszolgáltatást egy Azure Data Factoryhoz kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="34536-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="34536-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="34536-104">SYNTAX</span></span>

### <span data-ttu-id="34536-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="34536-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34536-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="34536-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34536-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="34536-107">DESCRIPTION</span></span>
<span data-ttu-id="34536-108">A **New-AzDataFactoryLinkedService** parancsmag adattárat vagy felhőszolgáltatást csatol az Azure Data Factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="34536-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="34536-109">Ha egy már létező csatolt szolgáltatás nevét adja meg, ez a parancsmag megerősítést kér, mielőtt lecseréli a csatolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="34536-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="34536-110">Ha a Force *paramétert* adja meg, a parancsmag jóváhagyás nélkül lecseréli a meglévő csatolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="34536-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="34536-111">Ezeket a műveleteket a következő sorrendben végezze el:</span><span class="sxs-lookup"><span data-stu-id="34536-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="34536-112">Adatüzem létrehozása</span><span class="sxs-lookup"><span data-stu-id="34536-112">Create a data factory.</span></span> 
- <span data-ttu-id="34536-113">Csatolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="34536-113">Create linked services.</span></span> 
- <span data-ttu-id="34536-114">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="34536-114">Create datasets.</span></span> 
- <span data-ttu-id="34536-115">Folyamat létrehozása</span><span class="sxs-lookup"><span data-stu-id="34536-115">Create a pipeline.</span></span>

## <span data-ttu-id="34536-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="34536-116">EXAMPLES</span></span>

### <span data-ttu-id="34536-117">1. példa: Csatolt szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="34536-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="34536-118">Ez a parancs létrehoz egy LinkedServiceCuratedWikiData nevű csatolt szolgáltatást a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="34536-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="34536-119">Ez a csatolt szolgáltatás a fájlban megadott Azure blobtárat a WikiADF nevű adatszolgáltatóhoz csatolja.</span><span class="sxs-lookup"><span data-stu-id="34536-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="34536-120">A parancs a folyamat műveleti Format-List keresztül átadja az eredményt a Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="34536-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="34536-121">Ez a Windows PowerShell-parancsmag formázta az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="34536-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="34536-122">További információért írja be a `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="34536-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="34536-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34536-123">PARAMETERS</span></span>

### <span data-ttu-id="34536-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="34536-124">-DataFactory</span></span>
<span data-ttu-id="34536-125">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="34536-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="34536-126">Ez a parancsmag csatolt szolgáltatást hoz létre a paraméter által megadott adat factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="34536-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="34536-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="34536-127">-DataFactoryName</span></span>
<span data-ttu-id="34536-128">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34536-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="34536-129">Ez a parancsmag csatolt szolgáltatást hoz létre a paraméter által megadott adat factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="34536-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="34536-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34536-130">-DefaultProfile</span></span>
<span data-ttu-id="34536-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="34536-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34536-132">-File</span><span class="sxs-lookup"><span data-stu-id="34536-132">-File</span></span>
<span data-ttu-id="34536-133">A hivatkozott szolgáltatás leírását tartalmazó JavaScript-objektum-notation (JSON) fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="34536-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="34536-134">-Force</span><span class="sxs-lookup"><span data-stu-id="34536-134">-Force</span></span>
<span data-ttu-id="34536-135">Azt jelzi, hogy ez a parancsmag egy meglévő csatolt szolgáltatás helyére vált, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="34536-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="34536-136">-Name</span><span class="sxs-lookup"><span data-stu-id="34536-136">-Name</span></span>
<span data-ttu-id="34536-137">A létrehozni szükséges csatolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="34536-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="34536-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34536-138">-ResourceGroupName</span></span>
<span data-ttu-id="34536-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34536-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="34536-140">Ez a parancsmag csatolt szolgáltatást hoz létre a paraméter által megadott csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="34536-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="34536-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34536-141">-Confirm</span></span>
<span data-ttu-id="34536-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="34536-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34536-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34536-143">-WhatIf</span></span>
<span data-ttu-id="34536-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="34536-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34536-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34536-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34536-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34536-146">CommonParameters</span></span>
<span data-ttu-id="34536-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34536-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34536-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34536-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34536-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34536-149">INPUTS</span></span>

### <span data-ttu-id="34536-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="34536-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="34536-151">System.String</span><span class="sxs-lookup"><span data-stu-id="34536-151">System.String</span></span>

## <span data-ttu-id="34536-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34536-152">OUTPUTS</span></span>

### <span data-ttu-id="34536-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="34536-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="34536-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="34536-154">NOTES</span></span>
* <span data-ttu-id="34536-155">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="34536-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="34536-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34536-156">RELATED LINKS</span></span>

[<span data-ttu-id="34536-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="34536-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="34536-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="34536-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


