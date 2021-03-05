---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 66f5cf02c4f50c699f790ec2790080fa37ab166d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009189"
---
# <span data-ttu-id="a96aa-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="a96aa-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="a96aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a96aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a96aa-103">Eltávolít egy adatfolyamot a Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="a96aa-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="a96aa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a96aa-104">SYNTAX</span></span>

### <span data-ttu-id="a96aa-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a96aa-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a96aa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a96aa-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96aa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a96aa-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a96aa-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a96aa-108">DESCRIPTION</span></span>
<span data-ttu-id="a96aa-109">A Remove-AzDataFactoryV2DataFlow parancsmag eltávolítja az adatfolyamot az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="a96aa-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="a96aa-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a96aa-110">EXAMPLES</span></span>

### <span data-ttu-id="a96aa-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a96aa-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="a96aa-112">Ez a parancs eltávolítja az Adatfolyam5 nevű adatfolyamot a WikiADF nevű adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="a96aa-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="a96aa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a96aa-113">PARAMETERS</span></span>

### <span data-ttu-id="a96aa-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a96aa-114">-DataFactoryName</span></span>
<span data-ttu-id="a96aa-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="a96aa-115">The data factory name.</span></span>

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

### <span data-ttu-id="a96aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96aa-116">-DefaultProfile</span></span>
<span data-ttu-id="a96aa-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a96aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a96aa-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a96aa-118">-Force</span></span>
<span data-ttu-id="a96aa-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a96aa-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a96aa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a96aa-120">-InputObject</span></span>
<span data-ttu-id="a96aa-121">Az adatfolyam-objektum.</span><span class="sxs-lookup"><span data-stu-id="a96aa-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a96aa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a96aa-122">-Name</span></span>
<span data-ttu-id="a96aa-123">Az adatfolyam neve.</span><span class="sxs-lookup"><span data-stu-id="a96aa-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a96aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="a96aa-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a96aa-125">The resource group name.</span></span>

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

### <span data-ttu-id="a96aa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a96aa-126">-ResourceId</span></span>
<span data-ttu-id="a96aa-127">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="a96aa-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a96aa-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a96aa-128">-PassThru</span></span>
<span data-ttu-id="a96aa-129">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="a96aa-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="a96aa-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a96aa-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="a96aa-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a96aa-131">-Confirm</span></span>
<span data-ttu-id="a96aa-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a96aa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a96aa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a96aa-133">-WhatIf</span></span>
<span data-ttu-id="a96aa-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a96aa-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a96aa-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a96aa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a96aa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96aa-136">CommonParameters</span></span>
<span data-ttu-id="a96aa-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a96aa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96aa-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a96aa-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96aa-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a96aa-139">INPUTS</span></span>

### <span data-ttu-id="a96aa-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="a96aa-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="a96aa-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a96aa-141">System.String</span></span>

## <span data-ttu-id="a96aa-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a96aa-142">OUTPUTS</span></span>

### <span data-ttu-id="a96aa-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="a96aa-143">System.Void</span></span>

### <span data-ttu-id="a96aa-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a96aa-144">System.Boolean</span></span>

## <span data-ttu-id="a96aa-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a96aa-145">NOTES</span></span>
<span data-ttu-id="a96aa-146">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="a96aa-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a96aa-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a96aa-147">RELATED LINKS</span></span>

[<span data-ttu-id="a96aa-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="a96aa-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="a96aa-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="a96aa-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

