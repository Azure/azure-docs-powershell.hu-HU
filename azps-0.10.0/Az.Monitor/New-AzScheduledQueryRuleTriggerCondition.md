---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 53331c82a2ea1ac16b67c32f67545fec7d08e3dd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841938"
---
# <span data-ttu-id="c551a-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="c551a-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="c551a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c551a-102">SYNOPSIS</span></span>
<span data-ttu-id="c551a-103">Objektum típusú trigger-feltételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c551a-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="c551a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c551a-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c551a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c551a-105">DESCRIPTION</span></span>
<span data-ttu-id="c551a-106">Létrehoz egy olyan objektumot, amely típusú trigger-feltételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c551a-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="c551a-107">Ezt az objektumot az értesítési művelet objektumát létrehozó parancsnak kell átadnia</span><span class="sxs-lookup"><span data-stu-id="c551a-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="c551a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c551a-108">EXAMPLES</span></span>

### <span data-ttu-id="c551a-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c551a-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="c551a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c551a-110">PARAMETERS</span></span>

### <span data-ttu-id="c551a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c551a-111">-DefaultProfile</span></span>
<span data-ttu-id="c551a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c551a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c551a-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="c551a-113">-MetricTrigger</span></span>
<span data-ttu-id="c551a-114">A metrika-lekérdezési szabály kiváltó feltétele</span><span class="sxs-lookup"><span data-stu-id="c551a-114">Trigger condition for metric query rule</span></span>

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

### <span data-ttu-id="c551a-115">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="c551a-115">-Threshold</span></span>
<span data-ttu-id="c551a-116">Az a küszöb, amelyen a riasztást kilőtték</span><span class="sxs-lookup"><span data-stu-id="c551a-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="c551a-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="c551a-117">-ThresholdOperator</span></span>
<span data-ttu-id="c551a-118">A küszöb operátor: GreaterThan, LessThan vagy egyenlő</span><span class="sxs-lookup"><span data-stu-id="c551a-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="c551a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c551a-119">CommonParameters</span></span>
<span data-ttu-id="c551a-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c551a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c551a-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c551a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c551a-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c551a-122">INPUTS</span></span>

### <span data-ttu-id="c551a-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="c551a-123">None</span></span>

## <span data-ttu-id="c551a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c551a-124">OUTPUTS</span></span>

### <span data-ttu-id="c551a-125">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="c551a-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="c551a-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c551a-126">NOTES</span></span>

## <span data-ttu-id="c551a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c551a-127">RELATED LINKS</span></span>
