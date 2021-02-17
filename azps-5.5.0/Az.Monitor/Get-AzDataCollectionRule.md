---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 8826dfdf8fe0152035319c576210088bcd5521e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147426"
---
# <span data-ttu-id="721de-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="721de-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="721de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="721de-102">SYNOPSIS</span></span>
<span data-ttu-id="721de-103">Adatgyűjtési szabályt(ak) kap.</span><span class="sxs-lookup"><span data-stu-id="721de-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="721de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="721de-104">SYNTAX</span></span>

### <span data-ttu-id="721de-105">BySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="721de-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="721de-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="721de-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="721de-107">ByName</span><span class="sxs-lookup"><span data-stu-id="721de-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="721de-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="721de-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="721de-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="721de-109">DESCRIPTION</span></span>
<span data-ttu-id="721de-110">A **Get-AzDataCollectionRule** parancsmag egy vagy több adatgyűjtési szabályt kap.</span><span class="sxs-lookup"><span data-stu-id="721de-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="721de-111">Az adatgyűjtési szabályok (DCR) definiálják az Azure Monitorra érkező adatokat, és meghatározzák, hogy hová kell küldeni vagy tárolni az adatokat.</span><span class="sxs-lookup"><span data-stu-id="721de-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="721de-112">Az alábbi teljes [áttekintést nyújtjuk a DCR-ről.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="721de-112">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="721de-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="721de-113">EXAMPLES</span></span>

### <span data-ttu-id="721de-114">1. példa: Adatgyűjtési szabályok lekérte előfizetésazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="721de-114">Example 1: Get data collection rules by subscription ID</span></span>
```
PS C:\>Get-AzDataCollectionRule

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="721de-115">Ez a parancs felsorolja az aktuális előfizetés összes adatgyűjtési szabályát.</span><span class="sxs-lookup"><span data-stu-id="721de-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="721de-116">2. példa: Az adott erőforráscsoport adatgyűjtési szabályainak lekérte</span><span class="sxs-lookup"><span data-stu-id="721de-116">Example 2: Get data collection rules for the given resource group</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="721de-117">Ez a parancs felsorolja az adott erőforráscsoport adatgyűjtési szabályait.</span><span class="sxs-lookup"><span data-stu-id="721de-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="721de-118">3. példa: Adatgyűjtési szabály lekérte</span><span class="sxs-lookup"><span data-stu-id="721de-118">Example 3: Get a data collection rule</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup" -RuleName "testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="721de-119">Ez a parancs felsorol egy (egyetlen elemet tartalmazó listát) adatgyűjtési szabályt.</span><span class="sxs-lookup"><span data-stu-id="721de-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="721de-120">4. példa: Adatgyűjtési szabály lekérte szabályazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="721de-120">Example 4: Get a data collection rule by Rule ID</span></span>
```
PS C:\>Get-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="721de-121">Ez a parancs felsorol egy (egyetlen elemet tartalmazó listát) adatgyűjtési szabályt.</span><span class="sxs-lookup"><span data-stu-id="721de-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="721de-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="721de-122">PARAMETERS</span></span>

### <span data-ttu-id="721de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721de-123">-DefaultProfile</span></span>
<span data-ttu-id="721de-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="721de-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="721de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721de-125">-ResourceGroupName</span></span>
<span data-ttu-id="721de-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="721de-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="721de-127">-RuleName</span><span class="sxs-lookup"><span data-stu-id="721de-127">-RuleName</span></span>
<span data-ttu-id="721de-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="721de-128">The name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="721de-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="721de-129">-RuleId</span></span>
<span data-ttu-id="721de-130">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="721de-130">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="721de-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721de-131">CommonParameters</span></span>
<span data-ttu-id="721de-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721de-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721de-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="721de-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721de-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="721de-134">INPUTS</span></span>

### <span data-ttu-id="721de-135">System.String</span><span class="sxs-lookup"><span data-stu-id="721de-135">System.String</span></span>

## <span data-ttu-id="721de-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="721de-136">OUTPUTS</span></span>

### <span data-ttu-id="721de-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="721de-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="721de-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="721de-138">NOTES</span></span>

## <span data-ttu-id="721de-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="721de-139">RELATED LINKS</span></span>

<span data-ttu-id="721de-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="721de-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
