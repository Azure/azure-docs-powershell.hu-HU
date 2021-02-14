---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
ms.openlocfilehash: cdde294c3af4684146d265e2024f6948660312bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203443"
---
# <span data-ttu-id="319fd-101">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="319fd-101">New-AzDataCollectionRule</span></span>

## <span data-ttu-id="319fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="319fd-102">SYNOPSIS</span></span>
<span data-ttu-id="319fd-103">Hozzon létre egy adatgyűjtési szabályt.</span><span class="sxs-lookup"><span data-stu-id="319fd-103">Create a data collection rule.</span></span>

## <span data-ttu-id="319fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="319fd-104">SYNTAX</span></span>

### <span data-ttu-id="319fd-105">ByFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="319fd-105">ByFile (Default)</span></span>
```
New-AzDataCollectionRule
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

## <span data-ttu-id="319fd-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="319fd-106">DESCRIPTION</span></span>
<span data-ttu-id="319fd-107">A **New-AzDataCollectionRule** parancsmag létrehoz egy adatgyűjtési szabályt.</span><span class="sxs-lookup"><span data-stu-id="319fd-107">The **New-AzDataCollectionRule** cmdlet creates a data collection rule.</span></span>

<span data-ttu-id="319fd-108">Az adatgyűjtési szabályok (DCR) definiálják az Azure Monitorra érkező adatokat, és meghatározzák, hogy hová kell küldeni vagy tárolni az adatokat.</span><span class="sxs-lookup"><span data-stu-id="319fd-108">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="319fd-109">Az alábbi teljes [áttekintést nyújtjuk a DCR-ről.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="319fd-109">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="319fd-110">A -RuleFile paraméter használatának használhatja a következő három tulajdonságot tartalmazó json-fájlt: dataSources, destinations, dataFlows (lásd a #1)</span><span class="sxs-lookup"><span data-stu-id="319fd-110">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1)</span></span>

<span data-ttu-id="319fd-111">Itt találja a [séma részleteit.](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="319fd-111">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="319fd-112">A parancsmaggal szerkesített DCR kimenete is ConvertTo-Json (lásd a #2).</span><span class="sxs-lookup"><span data-stu-id="319fd-112">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (see Example #2).</span></span>

## <span data-ttu-id="319fd-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="319fd-113">EXAMPLES</span></span>

### <span data-ttu-id="319fd-114">1. példa: Adatgyűjtési szabály (JSON) létrehozása Rest API-ból</span><span class="sxs-lookup"><span data-stu-id="319fd-114">Example 1: Create data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx1' -RuleFile 'C:\samples\dcrEx1.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx1
Name              : newDcrEx1
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx1.json
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

<span data-ttu-id="319fd-115">Ez a parancs adatgyűjtési szabályokat hoz létre az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="319fd-115">This command creates a data collection rules for the current subscription.</span></span>

### <span data-ttu-id="319fd-116">2. példa: Adatgyűjtési szabály létrehozása (JSON a PSDataCollectionRuleResource szolgáltatótól)</span><span class="sxs-lookup"><span data-stu-id="319fd-116">Example 2: Create data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx2' -RuleFile 'C:\samples\dcrEx2.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx2
Name              : newDcrEx2
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx2.json
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

<span data-ttu-id="319fd-117">Ez a parancs adatgyűjtési szabályokat hoz létre az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="319fd-117">This command creates a data collection rules for the current subscription.</span></span>

## <span data-ttu-id="319fd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="319fd-118">PARAMETERS</span></span>

### <span data-ttu-id="319fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319fd-119">-DefaultProfile</span></span>
<span data-ttu-id="319fd-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="319fd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="319fd-121">-Location</span><span class="sxs-lookup"><span data-stu-id="319fd-121">-Location</span></span>
<span data-ttu-id="319fd-122">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="319fd-122">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="319fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="319fd-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="319fd-124">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319fd-125">-RuleName</span><span class="sxs-lookup"><span data-stu-id="319fd-125">-RuleName</span></span>
<span data-ttu-id="319fd-126">Az erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="319fd-126">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319fd-127">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="319fd-127">-RuleFile</span></span>
<span data-ttu-id="319fd-128">A JSON fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="319fd-128">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319fd-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="319fd-129">-Description</span></span>
<span data-ttu-id="319fd-130">Az erőforrás leírása</span><span class="sxs-lookup"><span data-stu-id="319fd-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319fd-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="319fd-131">-Tag</span></span>
<span data-ttu-id="319fd-132">Az erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="319fd-132">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319fd-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="319fd-133">-Confirm</span></span>
<span data-ttu-id="319fd-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="319fd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="319fd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="319fd-135">-WhatIf</span></span>
<span data-ttu-id="319fd-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="319fd-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="319fd-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="319fd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="319fd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319fd-138">CommonParameters</span></span>
<span data-ttu-id="319fd-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="319fd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319fd-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="319fd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319fd-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="319fd-141">INPUTS</span></span>

### <span data-ttu-id="319fd-142">System.String</span><span class="sxs-lookup"><span data-stu-id="319fd-142">System.String</span></span>

## <span data-ttu-id="319fd-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="319fd-143">OUTPUTS</span></span>

### <span data-ttu-id="319fd-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="319fd-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="319fd-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="319fd-145">NOTES</span></span>

## <span data-ttu-id="319fd-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="319fd-146">RELATED LINKS</span></span>

<span data-ttu-id="319fd-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="319fd-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>