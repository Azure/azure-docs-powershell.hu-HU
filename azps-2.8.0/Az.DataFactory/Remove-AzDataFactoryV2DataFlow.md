---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 75c155b765a1bcbc565a85fc0f47130a6d2a5cf0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667000"
---
# <span data-ttu-id="ef013-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="ef013-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="ef013-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef013-102">SYNOPSIS</span></span>
<span data-ttu-id="ef013-103">Adatforgalom eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="ef013-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="ef013-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef013-104">SYNTAX</span></span>

### <span data-ttu-id="ef013-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef013-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef013-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef013-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef013-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef013-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef013-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef013-108">DESCRIPTION</span></span>
<span data-ttu-id="ef013-109">A Remove-AzDataFactoryV2DataFlow parancsmag eltávolítja az adatáramlást az Azure Data Factory szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="ef013-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="ef013-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ef013-110">EXAMPLES</span></span>

### <span data-ttu-id="ef013-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ef013-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="ef013-112">Ez a parancs eltávolítja a dataflow5 nevű adatfolyamot az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="ef013-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="ef013-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef013-113">PARAMETERS</span></span>

### <span data-ttu-id="ef013-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ef013-114">-DataFactoryName</span></span>
<span data-ttu-id="ef013-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="ef013-115">The data factory name.</span></span>

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

### <span data-ttu-id="ef013-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef013-116">-DefaultProfile</span></span>
<span data-ttu-id="ef013-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef013-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef013-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ef013-118">-Force</span></span>
<span data-ttu-id="ef013-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef013-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ef013-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef013-120">-InputObject</span></span>
<span data-ttu-id="ef013-121">Az adatfolyam-objektum.</span><span class="sxs-lookup"><span data-stu-id="ef013-121">The data flow object.</span></span>

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

### <span data-ttu-id="ef013-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef013-122">-Name</span></span>
<span data-ttu-id="ef013-123">Az adatforgalom neve.</span><span class="sxs-lookup"><span data-stu-id="ef013-123">The data flow name.</span></span>

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

### <span data-ttu-id="ef013-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef013-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef013-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef013-125">The resource group name.</span></span>

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

### <span data-ttu-id="ef013-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef013-126">-ResourceId</span></span>
<span data-ttu-id="ef013-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ef013-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ef013-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef013-128">-PassThru</span></span>
<span data-ttu-id="ef013-129">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="ef013-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="ef013-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ef013-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="ef013-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef013-131">-Confirm</span></span>
<span data-ttu-id="ef013-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef013-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef013-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef013-133">-WhatIf</span></span>
<span data-ttu-id="ef013-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef013-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef013-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef013-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef013-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef013-136">CommonParameters</span></span>
<span data-ttu-id="ef013-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef013-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef013-138">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef013-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef013-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef013-139">INPUTS</span></span>

### <span data-ttu-id="ef013-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="ef013-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="ef013-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ef013-141">System.String</span></span>

## <span data-ttu-id="ef013-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef013-142">OUTPUTS</span></span>

### <span data-ttu-id="ef013-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="ef013-143">System.Void</span></span>

### <span data-ttu-id="ef013-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef013-144">System.Boolean</span></span>

## <span data-ttu-id="ef013-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef013-145">NOTES</span></span>
<span data-ttu-id="ef013-146">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="ef013-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ef013-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef013-147">RELATED LINKS</span></span>

[<span data-ttu-id="ef013-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="ef013-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="ef013-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="ef013-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

