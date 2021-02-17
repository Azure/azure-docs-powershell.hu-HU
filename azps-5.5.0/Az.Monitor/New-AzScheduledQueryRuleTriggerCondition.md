---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147354"
---
# <span data-ttu-id="45d4f-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="45d4f-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="45d4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="45d4f-103">Eseményindító feltétel típusú objektumot hoz létre</span><span class="sxs-lookup"><span data-stu-id="45d4f-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="45d4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="45d4f-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45d4f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="45d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="45d4f-106">Eseményindító feltétel típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="45d4f-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="45d4f-107">Ezt az objektumot át kell adni annak a parancsnak, amely a Riasztási művelet objektumot hozza létre</span><span class="sxs-lookup"><span data-stu-id="45d4f-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="45d4f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="45d4f-108">EXAMPLES</span></span>

### <span data-ttu-id="45d4f-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="45d4f-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="45d4f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45d4f-110">PARAMETERS</span></span>

### <span data-ttu-id="45d4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d4f-111">-DefaultProfile</span></span>
<span data-ttu-id="45d4f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45d4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45d4f-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="45d4f-113">-MetricTrigger</span></span>
<span data-ttu-id="45d4f-114">Trigger feltétel a metrikus lekérdezési szabályhoz</span><span class="sxs-lookup"><span data-stu-id="45d4f-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d4f-115">-Threshold</span><span class="sxs-lookup"><span data-stu-id="45d4f-115">-Threshold</span></span>
<span data-ttu-id="45d4f-116">Az a küszöbérték, amely felett riasztást kap</span><span class="sxs-lookup"><span data-stu-id="45d4f-116">The threshold above which alert gets fired</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d4f-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="45d4f-117">-ThresholdOperator</span></span>
<span data-ttu-id="45d4f-118">A küszöbérték operátora: GreaterThan, LessThan vagy Equal</span><span class="sxs-lookup"><span data-stu-id="45d4f-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d4f-119">CommonParameters</span></span>
<span data-ttu-id="45d4f-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d4f-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45d4f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d4f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45d4f-122">INPUTS</span></span>

### <span data-ttu-id="45d4f-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="45d4f-123">None</span></span>

## <span data-ttu-id="45d4f-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45d4f-124">OUTPUTS</span></span>

### <span data-ttu-id="45d4f-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="45d4f-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="45d4f-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="45d4f-126">NOTES</span></span>

## <span data-ttu-id="45d4f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45d4f-127">RELATED LINKS</span></span>
