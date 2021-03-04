---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
ms.openlocfilehash: e51e43d2555decaa3f37509a89ebe9d55ba2ac96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924777"
---
# <span data-ttu-id="4130c-101">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="4130c-101">Set-AzDataCollectionRule</span></span>

## <span data-ttu-id="4130c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4130c-102">SYNOPSIS</span></span>
<span data-ttu-id="4130c-103">Adatgyűjtési szabály frissítése (teljes cseréje).</span><span class="sxs-lookup"><span data-stu-id="4130c-103">Updates (full replacement) a data collection rule.</span></span>

## <span data-ttu-id="4130c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4130c-104">SYNTAX</span></span>

### <span data-ttu-id="4130c-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4130c-105">ByName (Default)</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -ResourceGroupName <string>
   -RuleName <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="4130c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4130c-106">ByResourceId</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -RuleId <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="4130c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4130c-107">ByInputObject</span></span>
```
Set-AzDataCollectionRule 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="4130c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4130c-108">DESCRIPTION</span></span>
<span data-ttu-id="4130c-109">A **Set-AzDataCollectionRule** parancsmag lecserél egy meglévő adatgyűjtési szabályt.</span><span class="sxs-lookup"><span data-stu-id="4130c-109">The **Set-AzDataCollectionRule** cmdlet replaces an existing data collection rule.</span></span>

<span data-ttu-id="4130c-110">Az adatgyűjtési szabályok (DCR) definiálják az Azure Monitorra érkező adatokat, és meghatározzák, hogy hová kell küldeni vagy tárolni az adatokat.</span><span class="sxs-lookup"><span data-stu-id="4130c-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="4130c-111">Az alábbi teljes [áttekintést nyújtjuk a DCR-ről.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="4130c-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="4130c-112">A -RuleFile paramétert úgy használhatja, hogy egy három tulajdonságot tartalmazó json-fájlt hoz létre: dataSources, destinations, dataFlows (lásd a #1).</span><span class="sxs-lookup"><span data-stu-id="4130c-112">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1).</span></span>

<span data-ttu-id="4130c-113">Itt találja a [séma részleteit.](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="4130c-113">You may find here the [schema detail](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="4130c-114">A parancsmaggal szerkesített DCR kimenete ConvertTo-Json is támogatott (példa #2).</span><span class="sxs-lookup"><span data-stu-id="4130c-114">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (Example #2).</span></span>

## <span data-ttu-id="4130c-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4130c-115">EXAMPLES</span></span>

### <span data-ttu-id="4130c-116">1. példa: Adatgyűjtési szabály frissítése, JSON a Rest API-ból</span><span class="sxs-lookup"><span data-stu-id="4130c-116">Example 1: Update data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -ResourceGroupName 'testdcr' 
                                -RuleName 'newDcr' 
                                -RuleFile 'C:\samples\dcr1.json'
                                -Description 'Updated Description'

Description       : Updated Description
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

# Note: Content of C:\samples\dcr1.json
{
  "properties": {
    "dataSources": {
      "performanceCounters": [
        {
          "streams": [
            "Microsoft-InsightsMetrics"
          ],
          "scheduledTransferPeriod": "PT1M",
          "samplingFrequencyInSeconds": 10,
          "counterSpecifiers": [
            "\\Processor Information(_Total)\\% Processor Time"
          ],
          "name": "perfCounter01"
        }
      ]
    },
    "destinations": {
      "azureMonitorMetrics": {
        "name": "azureMonitorMetrics-default"
      }
    },
    "dataFlows": [
      {
        "streams": [
          "Microsoft-InsightsMetrics"
        ],
        "destinations": [
          "azureMonitorMetrics-default"
        ]
      }
    ]
  }
}
```

<span data-ttu-id="4130c-117">Ez a parancs lecseréli az aktuális előfizetés meglévő adatgyűjtési szabályait.</span><span class="sxs-lookup"><span data-stu-id="4130c-117">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="4130c-118">2. példa: Adatgyűjtési szabály frissítése, JSON a PSDataCollectionRuleResource szolgáltatótól</span><span class="sxs-lookup"><span data-stu-id="4130c-118">Example 2: Update data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr' 
                                -RuleFile 'C:\samples\dcr2.json'
                                -Description 'Updated Description'

Description       : Updated Description
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

# Note: Content of C:\samples\dcr2.json
{
  "DataSources": {
    "PerformanceCounters": [
      {
        "Streams": [
          "Microsoft-InsightsMetrics"
        ],
        "ScheduledTransferPeriod": "PT1M",
        "SamplingFrequencyInSeconds": 10,
        "CounterSpecifiers": [
          "\\Processor Information(_Total)\\% Processor Time"
        ],
        "Name": "perfCounter01"
      }
    ]
  },
  "Destinations": {
    "AzureMonitorMetrics": {
      "Name": "azureMonitorMetrics-default"
    }
  },
  "DataFlows": [
    {
      "Streams": [
        "Microsoft-InsightsMetrics"
      ],
      "Destinations": [
        "azureMonitorMetrics-default"
      ]
    }
  ]
}
```

<span data-ttu-id="4130c-119">Ez a parancs lecseréli az aktuális előfizetés meglévő adatgyűjtési szabályait.</span><span class="sxs-lookup"><span data-stu-id="4130c-119">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="4130c-120">3. példa: Adatgyűjtési szabály frissítése objektumból</span><span class="sxs-lookup"><span data-stu-id="4130c-120">Example 3: Update data collection rule from object</span></span>
```powershell
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr.Description = 'This is a test'
PS C:\>$dcr | Set-AzDataCollectionRule

Description       : This is a test
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

## <span data-ttu-id="4130c-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4130c-121">PARAMETERS</span></span>

### <span data-ttu-id="4130c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4130c-122">-DefaultProfile</span></span>
<span data-ttu-id="4130c-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4130c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4130c-124">-Location</span><span class="sxs-lookup"><span data-stu-id="4130c-124">-Location</span></span>
<span data-ttu-id="4130c-125">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="4130c-125">The resource location</span></span>

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

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4130c-126">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="4130c-126">-RuleFile</span></span>
<span data-ttu-id="4130c-127">A JSON fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="4130c-127">The JSON file path</span></span>

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

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4130c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4130c-128">-ResourceGroupName</span></span>
<span data-ttu-id="4130c-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4130c-129">The resource group name</span></span>

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

### <span data-ttu-id="4130c-130">-RuleName</span><span class="sxs-lookup"><span data-stu-id="4130c-130">-RuleName</span></span>
<span data-ttu-id="4130c-131">Az erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="4130c-131">The resource name</span></span>

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

### <span data-ttu-id="4130c-132">-RuleId</span><span class="sxs-lookup"><span data-stu-id="4130c-132">-RuleId</span></span>
<span data-ttu-id="4130c-133">Az erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="4130c-133">The resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4130c-134">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4130c-134">-Description</span></span>
<span data-ttu-id="4130c-135">Az erőforrás leírása</span><span class="sxs-lookup"><span data-stu-id="4130c-135">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4130c-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="4130c-136">-Tag</span></span>
<span data-ttu-id="4130c-137">Az erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="4130c-137">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4130c-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4130c-138">-InputObject</span></span>
<span data-ttu-id="4130c-139">PSDataCollectionRuleResource objektum</span><span class="sxs-lookup"><span data-stu-id="4130c-139">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="4130c-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4130c-140">-Confirm</span></span>
<span data-ttu-id="4130c-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4130c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4130c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4130c-142">-WhatIf</span></span>
<span data-ttu-id="4130c-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4130c-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4130c-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4130c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4130c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4130c-145">CommonParameters</span></span>
<span data-ttu-id="4130c-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4130c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4130c-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4130c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4130c-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4130c-148">INPUTS</span></span>

### <span data-ttu-id="4130c-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4130c-149">System.String</span></span>

## <span data-ttu-id="4130c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4130c-150">OUTPUTS</span></span>

### <span data-ttu-id="4130c-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="4130c-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="4130c-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4130c-152">NOTES</span></span>

## <span data-ttu-id="4130c-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4130c-153">RELATED LINKS</span></span>

<span data-ttu-id="4130c-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="4130c-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>