---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
ms.openlocfilehash: a655ac87dcc99eca1a8c5a5329d2073d54614ceb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157298"
---
# <span data-ttu-id="c0afe-101">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="c0afe-101">Update-AzDataCollectionRule</span></span>

## <span data-ttu-id="c0afe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0afe-102">SYNOPSIS</span></span>
<span data-ttu-id="c0afe-103">Frissíti az adatgyűjtési szabályok címketulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="c0afe-103">Updates a data collection rule tags property.</span></span>

## <span data-ttu-id="c0afe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0afe-104">SYNTAX</span></span>

### <span data-ttu-id="c0afe-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0afe-105">ByName (Default)</span></span>
```
Update-AzDataCollectionRule 
      -ResourceGroupName <string> 
      -RuleName <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="c0afe-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0afe-106">ByResourceId</span></span>
```
Update-AzDataCollectionRule 
      -RuleId <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="c0afe-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0afe-107">ByInputObject</span></span>
```
Update-AzDataCollectionRule 
      -InputObject <PSDataCollectionRuleResource> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="c0afe-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0afe-108">DESCRIPTION</span></span>
<span data-ttu-id="c0afe-109">Az **Update-AzDataCollectionRule** parancsmag frissíti az adatgyűjtési szabály Címkék tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="c0afe-109">The **Update-AzDataCollectionRule** cmdlet updates a data collection rule Tags property.</span></span>

<span data-ttu-id="c0afe-110">Az adatgyűjtési szabályok (DCR) definiálják az Azure Monitorra érkező adatokat, és meghatározzák, hogy hová kell küldeni vagy tárolni az adatokat.</span><span class="sxs-lookup"><span data-stu-id="c0afe-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="c0afe-111">Az alábbi teljes [áttekintést nyújtjuk a DCR-ről.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="c0afe-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="c0afe-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0afe-112">EXAMPLES</span></span>

### <span data-ttu-id="c0afe-113">1. példa: Adatgyűjtési szabályok címkéinek frissítése</span><span class="sxs-lookup"><span data-stu-id="c0afe-113">Example 1: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleName 'newDcr'
                                   -ResourceGroupName 'testdcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="c0afe-114">Ez a parancs frissíti a megadott adatgyűjtési szabály címketulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="c0afe-114">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="c0afe-115">2. példa: Adatgyűjtési szabályok címkéinek frissítése</span><span class="sxs-lookup"><span data-stu-id="c0afe-115">Example 2: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="c0afe-116">Ez a parancs frissíti a megadott adatgyűjtési szabály címketulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="c0afe-116">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="c0afe-117">3. példa: Adatgyűjtési szabályok címkéinek frissítése</span><span class="sxs-lookup"><span data-stu-id="c0afe-117">Example 3: Update data collection rule tags</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr | Update-AzDataCollectionRule -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : {provState}
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="c0afe-118">Ez a parancs frissíti a megadott adatgyűjtési szabály címketulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="c0afe-118">This command updates the tags property for the given data collection rule.</span></span>

## <span data-ttu-id="c0afe-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0afe-119">PARAMETERS</span></span>

### <span data-ttu-id="c0afe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0afe-120">-DefaultProfile</span></span>
<span data-ttu-id="c0afe-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c0afe-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0afe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0afe-122">-ResourceGroupName</span></span>
<span data-ttu-id="c0afe-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c0afe-123">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0afe-124">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c0afe-124">-RuleName</span></span>
<span data-ttu-id="c0afe-125">Az erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="c0afe-125">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0afe-126">-RuleId</span><span class="sxs-lookup"><span data-stu-id="c0afe-126">-RuleId</span></span>
<span data-ttu-id="c0afe-127">Az adatgyűjtési szabály erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c0afe-127">The resource ID of the data collection rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="c0afe-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0afe-128">-InputObject</span></span>
<span data-ttu-id="c0afe-129">PSDataCollectionRuleResource objektum</span><span class="sxs-lookup"><span data-stu-id="c0afe-129">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="c0afe-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0afe-130">-Tag</span></span>
<span data-ttu-id="c0afe-131">Az adatgyűjtési szabály címketulajdonságában</span><span class="sxs-lookup"><span data-stu-id="c0afe-131">The tags property of the data collection rule</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: Falose
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0afe-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0afe-132">-Confirm</span></span>
<span data-ttu-id="c0afe-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c0afe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0afe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0afe-134">-WhatIf</span></span>
<span data-ttu-id="c0afe-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c0afe-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0afe-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0afe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0afe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0afe-137">CommonParameters</span></span>
<span data-ttu-id="c0afe-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0afe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0afe-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0afe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0afe-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0afe-140">INPUTS</span></span>

### <span data-ttu-id="c0afe-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c0afe-141">System.String</span></span>

## <span data-ttu-id="c0afe-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0afe-142">OUTPUTS</span></span>

### <span data-ttu-id="c0afe-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="c0afe-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="c0afe-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0afe-144">NOTES</span></span>

## <span data-ttu-id="c0afe-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0afe-145">RELATED LINKS</span></span>

<span data-ttu-id="c0afe-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="c0afe-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span></span>