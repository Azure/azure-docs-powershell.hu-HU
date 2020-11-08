---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 8b5b9e8cfd1909b0d91627a2c0600620f264da78
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184174"
---
# <span data-ttu-id="784b8-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="784b8-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="784b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="784b8-102">SYNOPSIS</span></span>
<span data-ttu-id="784b8-103">Adatforgalom eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="784b8-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="784b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="784b8-104">SYNTAX</span></span>

### <span data-ttu-id="784b8-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="784b8-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="784b8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="784b8-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="784b8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="784b8-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="784b8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="784b8-108">DESCRIPTION</span></span>
<span data-ttu-id="784b8-109">A Remove-AzDataFactoryV2DataFlow parancsmag eltávolítja az adatáramlást az Azure Data Factory szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="784b8-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="784b8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="784b8-110">EXAMPLES</span></span>

### <span data-ttu-id="784b8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="784b8-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="784b8-112">Ez a parancs eltávolítja a dataflow5 nevű adatfolyamot az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="784b8-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="784b8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="784b8-113">PARAMETERS</span></span>

### <span data-ttu-id="784b8-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="784b8-114">-DataFactoryName</span></span>
<span data-ttu-id="784b8-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="784b8-115">The data factory name.</span></span>

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

### <span data-ttu-id="784b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="784b8-116">-DefaultProfile</span></span>
<span data-ttu-id="784b8-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="784b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="784b8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="784b8-118">-Force</span></span>
<span data-ttu-id="784b8-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="784b8-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="784b8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="784b8-120">-InputObject</span></span>
<span data-ttu-id="784b8-121">Az adatfolyam-objektum.</span><span class="sxs-lookup"><span data-stu-id="784b8-121">The data flow object.</span></span>

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

### <span data-ttu-id="784b8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="784b8-122">-Name</span></span>
<span data-ttu-id="784b8-123">Az adatforgalom neve.</span><span class="sxs-lookup"><span data-stu-id="784b8-123">The data flow name.</span></span>

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

### <span data-ttu-id="784b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="784b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="784b8-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="784b8-125">The resource group name.</span></span>

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

### <span data-ttu-id="784b8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="784b8-126">-ResourceId</span></span>
<span data-ttu-id="784b8-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="784b8-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="784b8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="784b8-128">-PassThru</span></span>
<span data-ttu-id="784b8-129">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="784b8-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="784b8-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="784b8-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="784b8-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="784b8-131">-Confirm</span></span>
<span data-ttu-id="784b8-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="784b8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="784b8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="784b8-133">-WhatIf</span></span>
<span data-ttu-id="784b8-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="784b8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="784b8-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="784b8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="784b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784b8-136">CommonParameters</span></span>
<span data-ttu-id="784b8-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="784b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784b8-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="784b8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784b8-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="784b8-139">INPUTS</span></span>

### <span data-ttu-id="784b8-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="784b8-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="784b8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="784b8-141">System.String</span></span>

## <span data-ttu-id="784b8-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="784b8-142">OUTPUTS</span></span>

### <span data-ttu-id="784b8-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="784b8-143">System.Void</span></span>

### <span data-ttu-id="784b8-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="784b8-144">System.Boolean</span></span>

## <span data-ttu-id="784b8-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="784b8-145">NOTES</span></span>
<span data-ttu-id="784b8-146">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="784b8-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="784b8-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="784b8-147">RELATED LINKS</span></span>

[<span data-ttu-id="784b8-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="784b8-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="784b8-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="784b8-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

